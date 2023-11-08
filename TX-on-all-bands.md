# Warning

**This modification is UNTESTED and is for RESEARCH PURPOSES ONLY, to explore the capabilities of the device and its chipset. DO NOT transmit on illegal frequencies. DO use a dummy load. The author(s) and contributor(s) of this repository are NOT liable for any damages, litigation, or other consequences of the misuse of this research firmware and do not accept any culpability. By installing any firmware from this repository, you accept full responsibility for any consequences that may arise and waive the right to pursue legal action against the author(s).**

This option won't give you ability to transmit in any other modulation that FM, this is hardware limitation. Switching to AM or SSB only switches AF audio output mode of a RF IC. It doesn't switch the whole IC into AM/SSB mode. This is for listening only. This firmware is also built with additional lock that blocks TX when AM or SSB is on.

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

# How to unlock TX on all bands

1. Go to [hidden menu](https://github.com/egzumer/uv-k5-firmware-custom/wiki/Menu#hidden-menu)
1. Enter menu `F-Lock`
1. Choose option `UNLOCK ALL`
1. Repeat steps 2-3 10 times. Do it carefully, if you confirm any other option in the process counter will get zeroed and you will have to repeat that 10 time more.