# Menu operation

The menu can be accessed with the `M` button _(short press)_.

Once in the main menu, the menu items will be displayed on the left-hand side of the screen. The currently selected menu item will be highlighted and current value for that menu item will be shown on the right. Also, at the bottom left side a number of the menu item will be shown, ranging from 01 to the highest number. 

To find the menu item to access, the `UP/DOWN` arrow keys may be used, or the **_menu item number_** (see lists below) may be entered on the numeric keypad. For instance, to access the VOX settings a number 57 can be entered on the keypad.

Once the desired menu item is highlighted, pressing the `M`enu key will enter into that menu item.

Once the menu item is selected, pressing the up and down arrow keys will adjust the setting for that menu item. To confirm the selection, press the `M`enu key. To cancel the selection, press the `EXIT` key.

# Main menu

The number in front of the menu-item-description is a **_menu item number_** that can be used for quick selection
1. `Step` - step of the frequency (in kHz), up/down buttons change frequency by this value, also you can only set a frequency that is multiple of half of this value.
1. `TxPwr` - radio output power (LOW/MID/HIGH)
1. `RxDCS` - receiver Digital-Coded Squelch, if you enable this, squelch will only unlock if this code is being received. You can start a DCS/CTCSS scan while you are in this menu option by pressing `* SCAN` button
1. `RxCTCS` - receiver Continuous Tone-Coded Squelch System, squelch will only unlock if this code is being received. You can start a DCS/CTCSS scan while you are in this menu option by pressing `* SCAN` button
1. `TxDCS` - transmitter Digital-Coded Squelch, radio will send given code while transmitting
1. `TxCTCS` - transmitter Continuous Tone-Coded Squelch System, radio will send given code while transmitting
1. `TxODir` - transmitter frequency offset direction
1. `TxOffs` - transmitter frequency offset value
1. `W/N` - bandwidth used by transceiver
   * WIDE - 25kHz
   * NARROW - 12.5kHz
1. `Scramb` - scrambler, distorts the audio so it would be harder to understand for other listeners, if two radios use the same setting they can communicate
1. `BusyCL` - busy channel lockout, blocks radio from transmitting when signal is being received
1. `Compnd` - compander (compressor/expander), allows signals with a large dynamic range to be transmitted over facilities that have a smaller dynamic range capability, improves audio quality, both radios should use this option
1. `Demodu` - demodulator mode, default is FM, AM/USB can be used for listening only
1. `ScAdd1` - add channel to scan list 1
1. `ScAdd2` - add channel to scan list 2
1. `ChSave` - save current setting to a memory channel
1. `ChDele` - delete memory channel
1. `ChName` - modify memory channel name
   * Use up/down keys to select a channel to edit
   * Press the Menu button again to enter edit name mode
   * Use up/down keys or digits (0 ~ 9) to cycle the letters etc.
   * Press the Menu button to move to the next character position
   * Repeat above two steps till you reach the end
   * When "Sure?" pops up, press Menu to save, or Exit to cancel
   * Press Exit at any time to cancel the edit and return to main menu.
1. `SList` - selects which channel is used by memory channel scanner
1. `SList1` - channels assigned to scan list 1
1. `SList2` - channels assigned to scan list 2
1. `ScnRev` - scan resume mode
   * CARRIER - resume scan after signal disappears
   * TIMEOUT - resume scan after 5 seconds pause
   * STOP - after receiving a signal, stop the scan
1. `F1Shrt` - side button 1 short press function
1. `F1Long` - side button 1 long press function
1. `F2Shrt` - side button 2 short press function
1. `F2Long` - side button 2 long press function
1. `M Long` - menu button long press function
1. `KeyLck` - auto keypad lock option
1. `TxTOut` - max transmission time limit
1. `BatSav` - battery save option, a rate between active time and sleep time
1. `Mic` - microphone sensitivity
1. `MicBar` - microphone bar that appears while transmitting
1. `ChDisp` - channel display style
1. `POnMsg` - power on message
1. `BatTxt` - additional battery value on the status bar in % or volts
1. `BackLt` - backlight duration
1. `BLMin` - minimal backlight brightness, when the screen backlight turns OFF it will go dim to this value
2. `BLMax` - maximal backlight brightness, when the screen backlight turns ON it will turn bright to this value
1. `BltTRX` - backlight activation on TX or RX
1. `Beep` - keypad press beep sound
1. `Roger` - roger beep at the end of transmission
1. `STE` - squelch tail eliminator, eliminates noise at the end of a transmission
1. `RP STE` - repeater squelch tail eliminator
1. `1 Call` - one key call channel, lets you quickly switch to the channel with `9 Call` button
1. `ANI ID` - DTMF communication radio ID
1. `UPCode` - DTMF code that is sent at the beginning of transmission
1. `DWCode` - DTMF code that is sent at the end of a transmission
1. `PTT ID` - sets if `UPCode` and/or `DWCode` should be transmitted
1. `D ST` - DTMF side tone switch, lets you hear transmitted tones in the radio speaker
1. `D Resp` - DTMF decoding response 
   * DO NOTHING: do nothing
   * RING - Local ringing
   * REPLY - reply response
   * BOTH - local ringing + reply response
1. `D Hold` - DTMF auto reset time
1. `D Prel` - DTMF pre-load time
1. `D Decd` - enables [DTMF decoder](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Radio-operation#dtmf-calling-decoding) 
1. `D List` - list of DTMF contacts
1. `D Live` - displays DTMF codes received by radio in the middle of the screen
1. `AM Fix` - activates autogain AM fix function
1. `VOX` - voice TX activation sensitivity level VOX Setting
1. `BatVol` - battery voltage and percentage
1. `RxMode` - sets how the upper and lower frequency is used
   * MAIN ONLY - always transmits and listens on the main frequency
   * DUAL RX RESPOND - listens to both frequencies, if signal is received on the secondary frequency it locks to it for a couple of seconds so you can respond to the call (`DWR`)
   * CROSS BAND - always transmits on the primary and listens on the secondary frequency (`XB`)
   * MAIN TX DUAL RX - always transmits on the primary, listens to both (`DW`)
60. `Sql` - squelch sensitivity level

# Hidden menu

Hidden menu is activated by holding `PTT` + `SIDE BUTTON 1` while turning on the radio and than Release All Keys.

61. `F Lock` - sets the TX frequency band plan. 
    * DEFAULT+ (137-174, 400-470) - allows TX on default bands, plus options `Tx 200`, `Tx 350`, `Tx 500`
    * FCC HAM (144-148, 420-450)
    * CE HAM (144-146, 430-440)
    * GB HAM (144-148, 430-440)
    * (137-174, 400-430)
    * (137-174, 400-438)
    * DISABLE ALL - disables TX on all frequencies
    * UNLOCK ALL - enables TX on all bands (it has additional lock, read a wiki on [how to turn that on](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Radio-operation#tx-on-all-bands))
1. `Tx 200` - enables TX on 200MHz
1. `Tx 350` - enables TX on 350MHz
1. `Tx 500` - enables TX on 500MHz
1. `350 En` - enables RX on 350MHz
1. `ScraEn` - enables scrambler function
1. `BatCal` - battery calibration, measure the voltage on the back of the radio, and adjust the value in the menu accordingly
1. `BatTyp` - battery type, 1600mAh and 2200mAh battery has very different discharge curve, this is used to calculate battery level percentage
1. `Reset` - resets radio configuration settings
   * VFO - removes only channel settings
   * ALL - resets all radio settings

