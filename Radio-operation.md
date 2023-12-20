# Basic operation & configuration
Radio display is split into upper VFO and lower VFO. You can change upper/lower selection by pressing `F` + `2 A/B` (or by long press `2 A/B`).

Each VFO can operate independently of each other function in either frequency or channel mode. To switch modes select the desired VFO and press `F` + `3 VFO/MR` (or long press `3 VFO/MR`).

In the `frequency mode` you manually type in the frequency with the keypad. You can also switch different options for that VFO in the menu (first 13 menu entries). If you setup the VFO, the settings can be saved to a memory channel by going into the menu `ChSave` and choosing the memory channel the VFO should be saved into.

In the `channel mode` you can switch between saved memory channels. Memory channels can be added manually as mentioned before or with a computer with [`CHIRP`](https://github.com/egzumer/uvk5-chirp-driver)

> [!WARNING]
Do not use Quansheng CPS it overwrites custom settings.

# Frequency/Memory scanning

## Frequency scanning

To start a frequency scan switch a VFO in frequency mode. Set a start frequency. Set a frequency step (menu `Step`). Start scanning with [custom button scan function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) or by long pressing the `* Scan` button.

### Scan frequency range function
* switch to frequency mode
* set upper and lower VFO frequencies to scan range boundaries
* long-press `5 NOAA`, `ScnRng` label should show up
* start scan with long-press `* Scan`
* it will scan between given boundaries
* long-press `5 NOAA` or `EXIT`, or switch VFOs to exit `ScnRng` mode

`ScnRng` function is also supported by spectrum analyzer. If you activated the function just start [spectrum analyzer](./Spectrum-analyzer).

## Memory-channels scanning

To scan channels saved in the radio memory switch the VFO to Memory mode.

The radio has 2 scanning lists. Each memory-channel can belong to 0, 1 or 2 lists. To add/delete a channel to/from a list switch current VFO to desired channel and go to a menu `ScAdd1` or `ScAdd2`, alternatively you can long press `5 NOAA` button, you will see icons `I` and `II` toggling on and off on the right side of the channel label.

If you set up the scanning lists you can start scanning by using [custom button scan function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) or by long pressing `* Scan` button. If you press the function button or long press `* Scan` while scanning, the scanning list will be switched, you will see corresponding icon on the top left of the screen: 1, 2 or * (star means: All memory channels). Active scanning list can also be changed with menu `SList`. You can view scan lists and its channels by going to menu: `SList1` or `SList2`.

## Common frequency/channel scanning features

You can change the scan direction while scanning with `UP/DOWN` buttons.

The scan can be stopped with the `EXIT` button, the search result will be ignored and frequency/channel will return to the one that was set before scan begun. Alternatively you can stop the scan with `PTT` or `MENU` button in which case the frequency/channel will be set to the last channel where transmission was found.

# Single frequency scanning (frequency copy), DCS/CTCSS scanning

This function will allow you to find out and copy frequency and coding settings. The frequency search will only work for strong signals. The transmitting radio has to be close. To start a frequency copy (FC) function use `4 FC` function button. Scanner screen will open. Push and hold a PTT button on the other radio. Wait couple of seconds until frequency and code (if used) appears on the screen. The settings can be saved with the `MENU` button. The settings will be save either to a channel or the main VFO, depending in which mode you started the scan.

You can also search only the DCS/CTCSS code for a frequency set on the main VFO. Choose desired frequency or channel and press `F` + `* SCAN`. The same screen will appear, but the frequency search will be omitted, instead the frequency of the main VFO will be used. Wait for a signal to appear or press the PTT on the other radio. It takes 1-2sec for the code to be found. The save procedure is the same as above.

There is another option of DCS/CTCSS code scanning. Choose desired frequency or a channel. Go to the menu `RxDCS` or `RxCTCS`. Enter the menu option and press `* SCAN` button. A SCAN label will appear. Wait for a radio signal or press the PTT button on the other radio. When code is found the SCAN label will disappear, to save confirm the option with the `MENU` button. It doesn't matter on which of the two menu items you start the scan. Both DCS and CTCSS will always be found, and the menu entry will be changed to the correct one.

# 1750 Hz toneburst for repeater access

When the `PTT` is pressed, the 1750 Hz can be activated by pressing [`Function-button-II`](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#function-button-ii) (_side key 2, bottom_)


# DTMF calling (decoding)

[DTMF](https://en.wikipedia.org/wiki/Dual-tone_multi-frequency_signaling) calling can be turned on in the menu `D Decd` (DTMF Decoding). You need a computer and programming cable to setup the whole system (use [Chirp](https://github.com/egzumer/uvk5-chirp-driver/releases)). You need to change `ANI ID` (programmable from the computer) of each radio to be unique in your network. It is also a good idea to program the list of contacts, their IDs and names.

The basic idea is to be able to dial a one particular person (or a group) among many on the same frequency. If you turn on the DTMF calling on a given channel your radio will be silent on that channel until an incoming call arrives with the destination ID matching `ANI ID` of your radio. If you receive the call a time window opens up in which the speaker activates and a person on the other side can talk to you. The time window expires after a delay set in `D Hold` menu entry from the time when incoming signal disappears.

The call pattern is `recipient*sender` where recipient is the `ANI ID` of a radio to which the call is being sent to, and sender is `ANI ID` of a radio that transmits the call (e.g. 102*103). In QS radio you only need to enter the recipient ID, the rest is appended automatically. You can send the call in two ways. One is, you go to the menu `D list` and choose a contact from the list and hit MENU button, its ID will be copied to the DTMF input box. You can transmit the call with PTT button. You can also open the DTMF input box by short press `* SCAN` button, and enter 3 digit recipient ID and hit PTT to send.

You can use `#` wildcard in place of any of the ID digits to make a group calls where every radio matching the pattern will activate. In particular you can call `###` to call everyone.

Menu items for DTMF calling:
* `ANI ID` - ID of your radio.
* `D ST` - DTMF site tone, whether you want to hear the tones in your speaker while they are being sent
* `D Resp`
  * `DO NOTHING` - does nothing
  * `RING` - radio beeps while the receiving time window is active
  * `REPLAY` - sends a DTMF call back to the caller
  * `BOTH` - both REPLAY and RING
* `D Hold` - length of a receiving time window
* `D Prel` - DTMF call preload, time from the RF path activation to when the DTMF codes start being sent, higher value gives the receiving radio time to detect the signal and open squelch on time so it will not loose the codes
* `D Decd` - turns on the DTMF decoding
* `D List` - list of DTMF contacts

# TX on all bands

## Warning

**This modification is UNTESTED and is for RESEARCH PURPOSES ONLY, to explore the capabilities of the device and its chipset. DO NOT transmit on illegal frequencies. DO use a dummy load. The author(s) and contributor(s) of this repository are NOT liable for any damages, litigation, or other consequences of the misuse of this research firmware and do not accept any culpability. By installing any firmware from this repository, you accept full responsibility for any consequences that may arise and waive the right to pursue legal action against the author(s).**

This option won't give you ability to transmit in any other modulation than FM, this is a hardware limitation. Switching to AM or SSB only switches AF audio output mode of a RF IC. It doesn't switch the whole IC into AM/SSB mode. This is for listening only. This firmware is also built with additional lock that blocks TX when AM or SSB is on.

As an example against using this for actual communications, consider the following chart for transmission power for a transmission at 27.254MHz:

![txspectrum](https://github.com/egzumer/uv-k5-firmware-custom/assets/14902414/65cdcb90-01b3-4344-a06b-ac7b8c408899)

- 27.254MHz -> **228 microwatts**
- 54 Mhz -> 2.4 milliwatts
- 81 Mhz -> 230 milliwatts
- 109 Mhz -> 558 milliwatts
- 136 Mhz -> 412 milliwatts
- 163 Mhz -> 122 milliwatts
- 190 Mhz -> 14.8 milliwatts
- 218 Mhz -> 2 milliwatts
- And finally, on 245 Mhz -> 2.6 milliwatts.

CREDITS: https://github.com/Tunas1337/UV-K5-Modded-Firmwares#even-bigger-warning

## How to unlock TX on all bands

1. Go to [hidden menu](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Menu#hidden-menu)
1. Enter menu `F-Lock`
1. Choose option `UNLOCK ALL`
1. Repeat steps 2-3 10 times. Do it carefully, if you confirm any other option in the process counter will get zeroed and you will have to repeat that 10 times more.
