## Using the Menu
The radio includes a menu system that uses a short term to describe a function that can be somewhat unclear to users, especially users for whom this is their first radio. This explanation of the menu items should help all users understand each menu item.

### Entering the Menu
The large key labeled `M` on the radio serves to enter the menu of the radio. A short press will open the menu to the first item.

### Exiting the Menu
The large key labeled `EXIT` on the radio serves to exit the menu of the radio. A short press will exit the menu. A long press registers as a short press and exits the menu.

### Selecting a Menu Item
Once in the main menu, the menu items will be displayed on the left-hand side of the screen. The currently selected menu item will be highlighted. The currently selected value for that menu item will be shown on the right. Also, at the bottom of the left-hand side is shown the number of the menu item, ranging from 01 to highest number (was 51 and now upto 60 and with Hidden-menu up to 70). 

To find the menu item to access, the up and down arrow keys may be used, or the **menu item number** (see list below) may be entered on the keypad. For instance, to access the VOX settings, the down arrow can be pressed 57 times, or the number 57 can be entered on the keypad.

### Accessing a Menu Item
Once the desired menu item is highlighted, pressing the `M`enu key will enter into that menu item.


### Adjusting a Menu Item
Once the menu item is selected, pressing the up and down arrow keys will adjust the setting for that menu item. To confirm the selection, press the `M`enu key. To cancel the selection, press the `EXIT` key.

# Main menu

1. `Step` - step of the frequency, up/down buttons change frequency by this value, also you can only set a frequency that is multiple of this value
1. `TxPwr` - radio output power
1. `RxDCS` - receiver Digital-Coded Squelch, if you enable this, squelch will only unlock if this code is being received
1. `RxCTCS` - receiver Continuous Tone-Coded Squelch System, squelch will only unlock if this code is being received
1. `TxDCS` - transmitter Digital-Coded Squelch, radio will send given code while transmitting
1. `TxCTCS` - transmitter Continuous Tone-Coded Squelch System, radio will send given code while transmitting
1. `TxODir` - transmitter frequency offset direction
1. `TxOffs` - transmitter frequency offset value
1. `W/N` - bandwidth used by transceiver
   * WIDE - 25kHz
   * NARROW - 12.5kHz
1. `Scramb` - scrambler, distorts the audio so it would be harder to understand for other listeners, if two radios use the same setting they can communicate
1. `BusyCL` - busy channel lockout, blocks radio from transmitting while signal is being received
1. `Compnd` - compander (compressor/expander), allows signals with a large dynamic range to be transmitted over facilities that have a smaller dynamic range capability, improves audio quality, both radios should use this option
1. `Demodu` - demodulator mode, default is FM, AM can be used for listening only
1. `ScAdd1` - add channel to scan list 1
1. `ScAdd2` - add channel to scan list 2
1. `ChSave` - save current setting to a memory channel
1. `ChDele` - delete memory channel
1. `ChName` - modify memory channel name
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
1. `BatSav` - battery save option, the rate between active time and sleep time
1. `Mic` - microphone sensitivity
1. `MicBar` - microphone bar that appears while transmitting
1. `ChDisp` - channel display style (Name + Freq or Number)
1. `POnMsg` - power on message
1. `BatTxt` - additional battery value on the status bar in % or V
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
1. `D Decd` - enables DTMF decoder
1. `D List` - list of DTMF constacts
1. `D Live` - displays DTMF codes received by radio in the middle of the screen
1. `AM Fix` - activates autogain AM fix function
1. `VOX` - voice TX activation sensitivity level
1. `BatVol` - battery voltage and percentage
1. `RxMode` - sets how how the upper and lower frequency is used
   * MAIN ONLY - always transmits and listens on the main frequency 
   * DUAL RX RESPOND - listens to both frequencies, if signal is received on the secondary frequency it locks to it for a couple of seconds so you can respond to the call
   * CROSS BAND - always transmits on the primary and listens on the secondary frequency
   * MAIN TX DUAL RX - always transmits on the primary, listens to both
1. `Sql` - squelch sensitivity level

# Hidden menu

Hidden menu is activated by holding `PTT` + `SIDE BUTTON 1` while turning on the radio and than Release All Keys.

61. `F Lock` - sets the frequency band plan for certain area
1. `Tx 200` - enables TX on 200MHz
1. `Tx 350` - enables TX on 350MHz
1. `Tx 500` - enables TX on 500MHz
1. `350 En` - enables RX on 350MHz
1. `ScraEn` - enables scrambler function
1. `TxEnab` - disables TX on all frequencies
1. `BatCal` - battery calibration, measure the voltage on the back of the radio, and adjust the value in the menu accordingly
1. `BatTyp` - battery type, 1600mAh and 2200mAh battery has very different discharge curve, this is used to calculate battery level percentage
1. `Reset` - resets radio configuration settings
   * VFO - removes only channel settings
   * ALL - resets all radio settings