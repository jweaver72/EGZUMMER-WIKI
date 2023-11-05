# Basic operation & configuration
Radio display is split into upper VFO and lower VFO. You can change upper/lower selection by pressing `F` + `2 A/B` (or by long press `2 A/B`).

Each VFO can independently of each other function in either frequency or channel mode. To switch modes select the desired VFO and press `F` + `3 VFO/MR` (or long press `3 VFO/MR`).

In the `frequency mode` you manually type in the frequency with the keypad. You can also switch different options for that VFO in the menu (first 13 menu entries). If you setup the VFO, the settings can be saved to a memory channel by going into the menu `ChSave` and choosing the memory channel the VFO should be saved into.

In the `channel mode` you can switch between saved memory channels. Memory channels can be added manually as mentioned before or with a computer software. You can use either Quansheng `Portable Radio CPS` or the recommended open source software called [`Chirp`](https://chirp.danplanet.com/projects/chirp/wiki/Download).

## How2 use Chirp with this radio.

Press the programming cable firmly into the radio and check that a _**blue LED**_ lights up near the antenna.

Initially, Chirp comes with popup. Configure that something like this.

> ![Chirp-setup-USB-interface-for-UV-K5](https://github.com/egzumer/uv-k5-firmware-custom/assets/148579604/ade103ca-a367-4531-b699-523f68fe8aee)

In addition to memory channels, you can also adjust various Settings, such as the power-on screen and more...

> ![Logo strings can be Set with Chirp](https://github.com/egzumer/uv-k5-firmware-custom/assets/148579604/c95325d2-50af-47dd-882c-8f49d9f878f5)

Just keep in mind that this firmware's options are expanded in many cases. Some functions or settings may not be available in the computer software, e.g. backlight timeout will have different settings, backlight brightness or MENU button long press function won't be available at all, etc. Those can be changed only in the radio menu.

# Frequency/Memory scanning

## Frequency scanning

To start a frequency scan switch the VFO to frequency mode. Set the start frequency. Set the frequency step (menu `Step`). Start scanning with [custom button scan function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) or by long pressing `* Scan` button.

## Memory-channels scanning

To scan channels saved in the radio memory switch the VFO to Memory mode.

The radio has 2 scanning lists. Each memory-channel can belong to 0, 1 or 2 lists. To add/delete a channel to/from a list switch current VFO to desired channel and go to a menu `ScAdd1` or `ScAdd2`, alternatively you can long press `5 NOAA` button, you will see icons `I` and `II` toggling on and off on the right side of the channel label.

If you set up the scanning lists you can start scanning by using [custom button scan function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) or by long pressing `* Scan` button. If you press the function button or long press `* Scan` while scanning, the scanning list will be switched, you will see corresponding icon on the top left of the screen: 1, 2 or * (star means: All memory channels). Active scanning list can also be changed with menu `SList`. You can view scan lists and its channels by going to menu: `SList1` or `SList2`.

Editing of memory- and scan-list is much easier on an PC with [`Chirp`](https://chirp.danplanet.com/projects/chirp/wiki/Download).

## Common frequency/channel scanning features

You can change the scan direction while scanning with `UP/DOWN` buttons.

The scan can be stopped with the `EXIT` button, the search result will be ignored and frequency/channel will return to the one that was set before scan begun. Alternatively you can stop the scan with `PTT` or `MENU` button in which case the frequency/channel will be set to the last channel where transmission was found.

# 1750 Hz toneburst for repeater access

When the `PTT` is pressed, the 1750 Hz can be activated by pressing [`Function-button-II`](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#function-button-ii) (_side key 2, bottom_)


# DTMF calling (decoding)

[DTMF](https://en.wikipedia.org/wiki/Dual-tone_multi-frequency_signaling) calling can be turned on in the menu `D Decd` (DTMF Decoding). You need a computer and programming cable to setup the whole system. You need to change `ANI ID` (programmable from the computer) of each radio to be unique in your network. It is also a good idea to program the list of contacts, their IDs and names.

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


