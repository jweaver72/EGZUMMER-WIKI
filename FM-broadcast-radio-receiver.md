# BROADCAST FM

The radio is capable of receiving broadcast FM from 76 to 108 MHz. For this it uses a separate chip (BK1080). RDS is not implemented.

_During broadcast reception the active VFO still has priority. This means that any reception on the active VFO will temporarily disable broadcast reception and the radio switches to VFO reception. At the end of VFO reception the radio switches back to broadcast._

# BASIC OPERATION

* `F` + `0 FM` or long press `0 FM` or [custom button function](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Button-functions#custom-button-functions) starts broadcast reception
* `Exit` or using above start command, when radio is in FM radio mode, ends broadcast reception
* `F` + `VFO/MR` or long press `VFO/MR` changes between VFO or memory channels (VFO-/MR-mode)

## Set a frequency in FM-VFO mode

Simply typing a frequency sets it to receive. Resolution is 100 kHz so entering 929 would tune to 92.9 MHz. Use arrow keys to change in 100 kHz steps.
## Store in memory from FM-VFO mode

Pressing `M` in VFO mode allows to store the current  frequency in a memory channel. Use arrow keys to select memory, confirm with `M`. There are 20 memories available.

## Select a memory

In MR-mode entering `01-20` selects a memory channel. Use `UP/DOWN` to step a memory channel up or down.

## Delete a stored memory

In MR-mode pressing `M` allows to delete that memory channel.

# SCANNING FOR STATIONS FROM FM-VFO

## Auto scan 

Start with `F` + `* Scan` or long press `* Scan`
The radio scans for stations and stores the first 20 stations in memory. Scanning starts at the low side of the band. Initiating auto-scan will delete previously stored channels. `Exit` ends autoscan.
## Manual scan 

Short press `* Scan` starts manual scan. The radio scans from the current frequency up until a station is received. You can continue scanning in any direction using arrow keys. `Exit` stops scanmode.