# ER-101 Indexed Quad Sequencer

This repo contains the source code for the ER-101 firmware.

## Toolchain Installation (64-bit linux host)

`scripts/install-toolchain.sh` will install the toolchain to `~/microchip`. 

If you decide to install the toolchain in another location then you will need to edit `scripts/avr32.mk` to reflect your chosen location.

## Compilation

```bash
cd {project-root}
make firmware
```

The flash-able HEX file will be written to `release/avr32/er-101-firmware-{version}.hex`.

## Helpful AVR32 References

* https://hofmeyr.de/avr32%20hello%20world/
* 

# testing | release | debug
PROFILE ?= release
ARCH = avr32
FIRMWARE_VERSION = 2.10

you can run the github action and download the hex firmware using the modified yml file. The file will be linked in artefacts. 

while the manual shows the last firmware as being v2.09 the code  provided by OD makes v2.10. As far as i can tell there is no mention of the difference between v2.09 and v2.10. You can see this v2.10 designation specified in the scripts/env.mk. 


to place into dfu mode place switch into dev mode, hold down reset button, plug in usb to computer, switch to usb mode, release reset and run 
sudo dfu-util -a 0 -s 0x8000000:leave -D /home/vt/microchip/er-101/release/avr32/er-101-firmware-v210.hex https://github.com/machinehistories/er-101/blob/main/er-101-firmware-v210.hex

the previous programmers for mac and windows are shared above and have all previous firmware files upto v2.07 if they are ever needed. 

additional information sources 
https://groups.google.com/g/odevices
https://llllllll.co/t/orthogonal-devices-er-101-102/68830
https://discord.gg/tCWz8vDJy
https://modwiggler.com/forum/viewtopic.php?t=90269&start=1250
