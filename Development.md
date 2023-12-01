# AGC (Automatic Gain Control) of BK4819

## Registers used by AGC

[BK4819 Registers_V1.1.pdf](https://github.com/egzumer/uv-k5-firmware-custom/files/13532694/BK4819.Registers_V1.1.pdf)

| Register | Default | Description |
|---|---|---|
| REG_7E<15> | 0 | AGC fix mode:<br>1: Fix<br>0: Auto |
| REG_7E<14:12> | 0b011 | AGC fix index:<br>011: Max.<br>…<br>100: Min. |
| REG_7E<11:6> |  | Signal strength indicator<br>(not in the docs, my interpretation) |
| REG_10<15:0> | 0x0038 | RX AGC Gain Table[0] (Index for max. to min.: 3, 2, 1, 0, -1)<br><9:8>: LNA Gain Short<br>11: 0 dB; 10: -11 dB; 01: -16 dB; 00: -19 dB<br><7:5>: LNA Gain<br>111: 0 dB; 110: -2 dB; 101: -4 dB; 100: -6 dB;<br>011: -9 dB; 010: -14 dB; 001: -19 dB; 000: -24 dB<br><4:3>: MIXER Gain<br>11: 0 dB; 10: -3 dB; 01: -6 dB; 00: -8 dB<br><2:0>: PGA Gain<br>111: 0 dB; 110: -3 dB; 101: -6 dB; 100: -9 dB;<br>011: -15 dB; 010: -21 dB; 001: -27 dB; 000: -33 dB |
| REG_11<15:0> | 0x025a | RX AGC Gain Table[1]<br>The description is the same as REG_10. |
| REG_12<15:0> | 0x037b | RX AGC Gain Table[2]<br>The description is the same as REG_10. |
| REG_13<15:0> | 0x03de | RX AGC Gain Table[3]<br>The description is the same as REG_10. |
| REG_14<15:0> | 0x0000 | RX AGC Gain Table[-1]<br>The description is the same as REG_10. |
| REG_49<13:7> | 0x50 | RF AGC high threshold, 1 dB/LSB |
| REG_49<6:0> | 0x30 | RF AGC low threshold, 1 dB/LSB |
| REG_7B<15:0> | 0xae34 | RSSI table |
| REG_7C<15:0> | 0x8000 | RSSI table |

## How it works

`AGC fix index` (3-bits signed integer, 0b111/0x7 is -1, values from 3 to -1) is an index in the `RX AGC Gain Table`. The LNA short, LNA, MIXER, PGA gains are setup according to the current value from the table item pointed by the index.

In `fix mode` the index is user configurable and doesn't change on its own.

In `auto mode` the RF chip compares the signal strength (`REG_7E<11:6>`) to the high and low thresholds (`REG_49<13:7>`, `REG_49<6:0>`). If signal is higher than "high threshold" it decreases the `AGC fix index`, if it is lower than "low threshold" then it increases it. This way it tries to keep the signal strength between given threshold levels, thus preventing distortion and clipping.

This is in theory. In practice there are some issues. At least in AM mode it doesn't work as it should. Lets assume we have a very strong signal. When AGC is in fix mode, index is set to 3, and value at index 3 is set to 0 the RSSI (read from other register) is around 170. When auto mode is activated (default values in gains table) the index goes to -1, gains at index -1 are 0, so we should get 170 as before. Instead we get RSSI over 300. All of this can be simulated using another radio, even if it only transmits in FM.

Register `REG_7B<15:0>` also plays some role. When it is set to 0x8420 the RSSI will go down to 170 in the fix mode. But if 0x318C value is used it won't.

Another thing, the index sometimes goes to -2 !!??

## 1o11 AM fix issue with strong signals

There is an issue with original implementation. AGC is turned on so it regulates the index. If strong signal is received the AGC will change the index to -1 before AM-fix can react. The AM-fix always modifies gain table at index 3, AGC is locked at -1, so the AM-fix will have no effect on actual gains settings, and the signal will be clipped. One person noticed that when it happens toggling monitor function instantly fixes the issue. This is because toggling monitor resets the AGC and it momentarily switches to index 3 which applies AM-fix gain settings, that brings down the signal strength and the AGC will stay on index 3.