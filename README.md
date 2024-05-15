# pico-template
This repository provides a simple template project for developing with the RPi Pico (RP2040) in Visual Studio Code on MacOS.

The project configures VS Code to program and debug the target device via its SWD pins by using another Pico as a USB/SWD bridge (see [Picoprobe](https://github.com/raspberrypi/picoprobe)).

## VSCode setup
Note that for this to work VS Code needs a couple of external tools and plug-ins (e.g. see instructions [here](https://www.digikey.be/en/maker/projects/raspberry-pi-pico-and-rp2040-cc-part-2-debugging-with-vs-code/470abc7efb07432b82c95f6f67f184c0)).

> **Important** Both VSCode and CMake need to know where to find the Pico SDK in your setup. You can configure this as follows:
- in VSCode open the command pallette and select `CMake: Open CMake tools extension settings`
- under 'Cmake: Build Environment' add the item `PICO_SDK_PATH` with the value of the path to the Pico SDK on your machine (e.g. `~/pico/pico-sdk`)
- add the same item further down under 'Cmake: Configure Environment'
- finally, add and export `PICO_SDK_PATH` to your login shell environment (e.g. in `~/.zprofile`)
- quit and relaunch VSCode