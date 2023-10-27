# Basic operation
Radio display is split into upper VFO and lower VFO. You can change upper/lower selection by pressing `F` + `2 A/B` (or by long press `2 A/B`).

Each VFO can independently of each other function in either frequency or channel mode. To switch modes select the desired VFO and press `F` + `3 VFO/MR` (or long press `3 VFO/MR`).

In the `frequency mode` you manually type in the frequency with the keypad. You can also switch different options for that VFO in the menu (first 13 menu entries). If all settings are set the VFO settings can be saved to a memory channel by going into the menu `ChSave` and choosing the memory channel the VFO should be saved into.

In the `channel mode` you can switch between saved memory channels. Memory channels can be added manually as mentioned before or with a computer software. You can use either Quansheng `Portable Radio CPS` or open source software called `CHIRP` (recommended)

# Channel/frequency scanning

## Memory channels scanning

To scan channels saved in the radio memory switch VFO to memory mode using `3 VFO/MR` function button.

Radio have 2 scanning lists. Each channel can belong to 0, 1 or 2 lists. To add/delete a channel to/from a list switch current VFO to desired channel and go to a menu `ScAdd1` or `ScAdd2`, alternatively you can long press `5 NOAA` button, you will see icons `I` and `II` toggling on and off on the right side of the channel label.

If you set up the scanning lists you can start scanning by using [custom button scan function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) or by long pressing `* Scan` button. If you press the function button or long press `* Scan` while scanning, the scanning list will be switched, you will see corresponding icon on the top left of the screen: 1, 2 or * (star means all memory channels). Active scanning list can also be changed with menu `SList`.

## Memory channels scanning

To start a frequency scan switch VFO to frequency mode using `3 VFO/MR` function button. Set the start frequency. Set the frequency step (menu `Step`). Start scanning with [custom button scan function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) or by long pressing `* Scan` button. You can view scan lists and its channels by going to menu: `SList1` or `SList2`

## Common frequency/channel scanning features

You can change the scan direction while scanning with UP/DOWN buttons.

The scan can be stopped with the `EXIT` button, the search result will be ignored and channel/frequency will return to the one that was set before scan begun. Alternatively you can stop the scan with `PTT` or `MENU` button in which case the channel/frequency will be set to the last channel where transmission was found.

