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
you can run the github action and download the hex firmware using the modified yml file. 

while the manual shows the last firmware as being v2.09 the code  provided by OD makes v2.10. As far as i can tell there is no mention of the difference between v2.09 and v2.10 you can see this in the 
# testing | release | debug
PROFILE ?= release
ARCH = avr32
FIRMWARE_VERSION = 2.10
