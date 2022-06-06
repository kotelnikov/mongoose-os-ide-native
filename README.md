# Mongoose OS IDE with native build ESP32 applications on MacOS

This is a modification of [Mongoose OS](https://mongoose-os.com) extension provides support Mongoose OS in Visual Studio Code. The difference between the original extension is using [mos-native](https://github.com/v-kiniv/mos-native) script for building applications for ESP32 on MacOS in a fraction of the time (without using a Docker). Also in the modified extension was hidden option of the menu for remote build, because of false clicking sometimes.

![](https://mongoose-os.com/docs/quickstart/images/ide.png)

## Features

- Building applications for ESP32 on MacOS in a fraction of time without using a Docker
- Run any mos command: `Ctrl+.`
- Open device serial log console: toggle "Output" panel
  (`Shift+Ctrl+U` / `Shift+Cmd+U`)
  and select "Mongoose OS" output in a dropdown
- To build firmware, open app directory in VSCode, select board and run `build`.
  Note: `mos` tool executes in the first workspace's directory, so only that
  directory can be built, and it must be a Mongoose firmware directory with
  the `mos.yml` file
- To flash firmware, select port and run `flash`
- To configure wifi, run `wifi NETWORK PASSWORD`
- Edit files on a device: select port and click on a file to edit and save
- Edit device config as a file: select port and click on "Device configuration"
- C/C++ and JS API autocompletions:

![](https://mongoose-os.com/docs/quickstart/images/ide_autocomplete.gif)

## Installation

Download compiled extension file [mongoose-os-ide-0.6.0.vsix](https://github.com/kotelnikov/mongoose-os-ide-native/blob/master/mongoose-os-ide-native-0.6.0.vsix) and install it manually to Visual Studio Code, details here: [Install extensions from a VSIX](https://code.visualstudio.com/docs/editor/extension-marketplace#_install-from-a-vsix).

## Requirements

* [mos command-line tool](https://mongoose-os.com/docs/) installed
* [mos-native](https://github.com/v-kiniv/mos-native) script installed
* Added environment variable "MOS_NATIVE" as a path to mos_build_local.sh script
