# My Notes
- Export layout from https://config.qmk.fm/#/meletrix/zoom65_lite/LAYOUT_all
- Install Dev env. https://docs.qmk.fm/#/newbs_getting_started
- Run QMK MSYS 
- Set config manually or update ini file: `C:\Users\...\AppData\Local\QMK.EXE\qmk.exe\qmk.exe.ini`:
    + `qmk config user.qmk_home = C:/Projects/_Playground/qmk_firmware`
    + `qmk config user.keyboard=meletrix/zoom65_lite`
    + `qmk config user.keymap = cloudsinmycoffee`
- Update config under keyboard's folder or 
- Update exported keymap via `qmk json2c {path_to_json_keymap}`
- Compile using `qmk compile` or `util/docker_build.sh <keyboard>:<keymap>`
- Check generated file `...\qmk_firmware\meletrix_zoom65_lite_cloudsinmycoffee.hex` and set keyboard in DFU state by unpluging keyboard, hold down Esc and plug in your keyboard (it will stop working)
- Run `qmk flash` or `util/docker_build.sh <keyboard>:<keymap>:flash`
- Enjoy

## Other Notes:
- git clone with recursive sub-modules: `git clone --recurse-submodules https://github.com/alekseylesnoy/qmk_firmware.git`
- How to flash a board without taking out the PCB: https://docs.google.com/document/d/1WNpflqKHjuuKW0LrzAFXgna1ZIhd8ayAJEjm9g_49DU/edit (https://discord.com/channels/709692387160752189/924280469330231318/931286439310811167)






# Quantum Mechanical Keyboard Firmware

[![Current Version](https://img.shields.io/github/tag/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/tags)
[![Discord](https://img.shields.io/discord/440868230475677696.svg)](https://discord.gg/Uq7gcHh)
[![Docs Status](https://img.shields.io/badge/docs-ready-orange.svg)](https://docs.qmk.fm)
[![GitHub contributors](https://img.shields.io/github/contributors/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/pulse/monthly)
[![GitHub forks](https://img.shields.io/github/forks/qmk/qmk_firmware.svg?style=social&label=Fork)](https://github.com/qmk/qmk_firmware/)

This is a keyboard firmware based on the [tmk\_keyboard firmware](https://github.com/tmk/tmk_keyboard) with some useful features for Atmel AVR and ARM controllers, and more specifically, the [OLKB product line](https://olkb.com), the [ErgoDox EZ](https://ergodox-ez.com) keyboard, and the [Clueboard product line](https://clueboard.co).

## Documentation

* [See the official documentation on docs.qmk.fm](https://docs.qmk.fm)

The docs are powered by [Docsify](https://docsify.js.org/) and hosted on [GitHub](/docs/). They are also viewable offline; see [Previewing the Documentation](https://docs.qmk.fm/#/contributing?id=previewing-the-documentation) for more details.

You can request changes by making a fork and opening a [pull request](https://github.com/qmk/qmk_firmware/pulls), or by clicking the "Edit this page" link at the bottom of any page.

## Supported Keyboards

* [Planck](/keyboards/planck/)
* [Preonic](/keyboards/preonic/)
* [ErgoDox EZ](/keyboards/ergodox_ez/)
* [Clueboard](/keyboards/clueboard/)
* [Cluepad](/keyboards/clueboard/17/)
* [Atreus](/keyboards/atreus/)

The project also includes community support for [lots of other keyboards](/keyboards/).

## Maintainers

QMK is developed and maintained by Jack Humbert of OLKB with contributions from the community, and of course, [Hasu](https://github.com/tmk). The OLKB product firmwares are maintained by [Jack Humbert](https://github.com/jackhumbert), the Ergodox EZ by [ZSA Technology Labs](https://github.com/zsa), the Clueboard by [Zach White](https://github.com/skullydazed), and the Atreus by [Phil Hagelberg](https://github.com/technomancy).

## Official Website

[qmk.fm](https://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.
