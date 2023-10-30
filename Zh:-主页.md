欢迎访问 uv-k5-firmware-custom wiki!

[电台操作](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Radio-operation)

[菜单说明](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Menu)

# 按键功能
按钮分配了不同的功能,这些功能可以通过先按下 `F/#` 按钮，再按下功能按钮 ( 下文称作`F+`)来激活。另一种方法是单独长按功能按钮而不使用 `F/#`。大多数按钮长按时功能和`F+`一样，但有些按钮长按和`F+`分配了不同的功能。

# 主键盘

## `M` 
* 短按 - 进入菜单
* 信道/频率扫描时短按 - 最后扫描发现的频道显示在屏幕上
* 长按 - 用户在`M Long`菜单中设置的功能
## `EXIT`
* 短按 - 退出当前菜单/功能，删除文版输入界面的 1 个字符
* 长按 - 删除所有输入信息，退出 DTMF 输入框
## `1 BAND`
* `F+`
  * 在 `频率模式` - 切换 1-7 频段, 还有一个支持 >1GHz 频率的 7+ 频段
  * 在 `信道模式` - 信道模式设置复制至频率模式
* 长按 - 相同
## `2 A/B`
* `F+` - 切换A/B主信道
* 长按 - 相同
## `3 VFO/MR`
* `F+` - 频率模式/信道模式切换
* 长按 - 相同
## `4 FC`
* `F+` - 打开频率和 CTCSS 复制模式，打开扫描并开始使用其他电发射来检测频率和 CTCSS，可以使用 M 按钮保存这些设置。
* 长按 - 相同
## `5 NOAA`
* `F+` - 打开频谱分析仪
* 长按 - 在信道模式下切换所选信道分配到的扫描列表。可以在频道标签的右侧看到 `I`、 `II`  变化
## `6 H/M/L`
* `F+` - 切换当前信道发射功率
* 长按 - 相同
## `7 VOX`
* `F+` - 打开/关闭声控发射
* 长按 - 相同
## `8 R`
* `F+` - turns on reverse mode for channel that have frequency offset set. It will replace TX frequency with RX frequency.
* long press - same
## `9 Call`
* `F+` - switches current channel to the `1-Call` channel set in the radio.
* long press - same
## `0 FM`
* `F+` - turns on FM radio
* long press - same
## `* SCAN`
* short press - enters DTMF input mode
* `F+` - turns on CTCSS scanner for current frequency
* long press - in channel mode turns on channel scanner, in frequency mode turns on frequency scanner. When pressed while channel scan is in progress toggles scan lists 1/2/ALL
## `F # 🗝`
* short press - toggles function option
* long press - turns on/off key lock

# Side buttons

## `PTT` 
* Push To Talk button.
* when this button is used to stop channel/frequency scanning, last found channel is preserved on the screen
* held together with `Function button II` transmits tone 1750Hz
* held together with any of the front keypad buttons transmits DTMF codes

## `Function button I` 
* short press - user programmable in the menu: `F1Shrt`
* long press - user programmable in the menu: `F1Long`

## `Function button II` 
* short press - user programmable in the menu: `F2Shrt`
* long press - user programmable in the menu: `F2Long`
* this button can also be used to send tone 1750Hz by holding it together with `PTT` button

# Custom button functions
3 buttons can have its function changed. To change the function go to menu:
* `F1Shrt` - side button 1, short press
* `F1Long` - side button 2, long press
* `F2Shrt` - side button 1, short press
* `F2Long` - side button 2, long press
* `M Long` - menu button, long press

Available functions:
* NONE - no action
* FLASH LIGHT - switch to the next flashlight function: on / flash / SOS / off
* POWER - switch radio output power: L (low) / M (medium) / H (high)
* MONITOR - switch monitor mode on/off
* SCAN - start channels/frequency scanning
* VOX - turn voice activation function on/off
* FM RADIO - turn FM radio on/off
* LOCK KEYPAD - lock/unlock the keypad
* SWITCH VFO - change main VFO to upper/lower
* VFO/MR - change current VFO mode, frequency mode or channel mode

[频谱分析仪](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Spectrum-analyzer)