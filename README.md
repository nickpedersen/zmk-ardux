# ZMK ARDUX Implementation

This repo contains the [ZMK](https://zmkfirmware.dev/) ARDUX implementation and pre-built firmware for boards that have been setup to use ARDUX by the core ARDUX development team.

## Prebuilt Firmware

The `Releases` area of this repository contains the latest builds of the ZMK ARDUX implementation. You can click on the most recent release and download the appropriate artifact for your MCU + board combination. Inside the zip file will be the necessary file for flashing your MCU.

### Firmware Files

Inside the firmware zip file will be 4 files

- `ardux.dtsi`: The ARDUX definition that was used for the build
- A file with `.dts.pre.tmp` at the end that is the generated DTS file used for the build (this is for any required troubleshooting)
- A file with `-zmk-ardux.hex` at the end that is the hex firmware image that can be used to flash your MCU
- A file with `-zmk-ardux.uf2` at the end that is the uf2 firmware image that can be used to flash your MCU

Please Note: the `hex` and `uf2` files may or may not be present depending on your MCU + board combo. **PLEASE** use the proper file for flashing your board.

**We are NOT responsible for any failed firmware flashes!**

## Adding ARDUX Support

If you'd like to add ARDUX support to a board that supports ZMK but is not built by this repo. Please follow the standard ZMK docs on how to add a new shield but using this repo as your `zmk-config` and open a Pull Request.

Also, update the `.github/workflows/build.yml` file for the new board being submitted.

Note: This repo is setup with github actions so you _can_ work directly via GitHub Actions similar to how the ZMK documentation outlines.

## Licensing

Unless otherwise stated all source code is licensed under the [Apache 2 License](LICENSE-APACHE-2.0.txt).

Unless otherwise stated the non source code contents of this repository are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](LICENSE-CC-Attribution-NonCommercial-ShareAlike-4.0-International.txt)
