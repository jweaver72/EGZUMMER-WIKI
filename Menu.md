# Main menu
* `Step` - step of the frequency, up/down buttons change frequency by this value, also you can only set a frequency that is multiple of this value
* `TxPwr` - radio output power
* `RxDCS` - receiver Digital-Coded Squelch, if you enable this, squelch will only unlock if this code is being received
* `RxCTCS` - receiver Continuous Tone-Coded Squelch System, squelch will only unlock if this code is being received
* `TxDCS` - transmitter Digital-Coded Squelch, radio will send given code while transmitting
* `TxCTCS` - transmitter Continuous Tone-Coded Squelch System, radio will send given code while transmitting
* `TxODir` - transmitter frequency offset direction
* `TxOffs` - transmitter frequency offset value
* `W/N` - bandwidth used by transceiver
  * WIDE - 25kHz
  * NARROW - 12.5kHz
* `Scramb` - scrambler, distorts the audio so it would be harder to understand for other listeners, if two radios use the same setting they can communicate
* `BusyCL` - busy channel lockout, blocks radio from transmitting while signal is being received
* `Compnd` - compander (compressor/expander), allows signals with a large dynamic range to be transmitted over facilities that have a smaller dynamic range capability, improves audio quality, both radios should use this option
* `Demodu` - demodulator mode, default is FM, AM can be used for listening only
* `ScAdd1` - add channel to scan list 1
* `ScAdd2` - add channel to scan list 2
* `ChSave` - save current setting to a memory channel
* `ChDele` - delete memory channel
* `ChName` - modify memory channel name
* `SList` - selects which channel is used by memory channel scanner
* `SList1` - channels assigned to scan list 1
* `SList2` - channels assigned to scan list 2
* `ScnRev` - scan resume mode
  * CARRIER - resume scan after signal disappears
  * TIMEOUT - resume scan after 5 seconds pause
  * STOP - after receiving a signal, stop the scan
* `F1Shrt` - side button 1 short press function
* `F1Long` - side button 1 long press function
* `F2Shrt` - side button 2 short press function
* `F2Long` - side button 2 long press function
* `KeyLck` - auto keypad lock option
* `TxTOut` - max transmission time limit
* `BatSav` - battery save option, the rate between active time and sleep time
* `Mic` - microphone sensitivity
* `MicBar` - microphone bar that appears while transmitting
* `ChDisp` - channel display style
* `POnMsg` - power on message
* `BatTxt` - additional battery value on the status bar in % or V
* `BackLt` - backlight duration
* `BltTRX` - backlight activation on TX or RX
* `Beep` - keypad press beep sound
* `Roger` - roger beep at the end of transmission
* `STE` - squelch tail eliminator, eliminates noise at the end of a transmission
* `RP STE` - repeater squelch tail eliminator
* `1 Call` - one key call channel, lets you quickly switch to the channel with `9 Call` button
* `ANI ID` - DTMF communication radio ID
* `UPCode` - DTMF code that is sent at the beginning of transmission
* `DWCode` - DTMF code that is sent at the end of a transmission
* `PTT ID` - sets if `UPCode` and/or `DWCode` should be transmitted
* `D ST` - DTMF side tone switch, lets you hear transmitted tones in the radio speaker
* `D Resp` - DTMF decoding response 
  * DO NOTHING: do nothing
  * RING - Local ringing
  * REPLY - reply response
  * BOTH - local ringing + reply response
* `D Hold` - DTMF auto reset time
* `D Prel` - DTMF pre-load time
* `D Decd` - enables DTMF decoder
* `D List` - list of DTMF constacts
* `D Live` - displays DTMF codes received by radio in the middle of the screen
* `AM Fix` - activates autogain AM fix function
* `VOX` - voice TX activation sensitivity level
* `BatVol` - battery voltage and percentage
* `RxMode` - sets how how the upper and lower frequency is used
  * MAIN ONLY - always transmits and listens on the main frequency 
  * DUAL RX RESPOND - listens to both frequencies, if signal is received on the secondary frequency it locks to it for a couple of seconds so you can respond to a call
  * CROSS BAND - always transmits on the primary and listens on the secondary frequency
  * MAIN TX DUAL RX - always transmits on the primary, listens to both
* `Sql` - squelch sensitivity level

# Hidden menu

Hidden menu is accessed by holding `PTT` + `SIDE BUTTON 1` while turning on the radio

* `F Lock` - sets the frequency band plan for certain area
* `Tx 200` - enables TX on 200MHz
* `Tx 350` - enables TX on 350MHz
* `Tx 500` - enables TX on 500MHz
* `350 En` - enables RX on 350MHz
* `ScraEn` - enables scrambler function
* `TxEnab` - disables TX on all frequencies
* `BatCal` - battery calibration, measure the voltage on the back of the radio, and adjust the value in the menu accordingly
* `Reset` - resets radio configuration settings
  * VFO - removes only channel settings
  * ALL - resets all radio settings