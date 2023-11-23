# Arm Environment Manager

## Overview

The complete [documentation](https://developer.arm.com/documentation/108029/latest/Extension-pack-and-extensions) for the Keil Studio extensions is available on Arm Developer.

The **Arm Environment Manager** extension allows you to manage environment artifacts using the [Microsoft vcpkg-artifacts](https://github.com/microsoft/vcpkg-tool) tool. The extension uses a vcpkg manifest file to acquire and activate the artifacts you need to set up your development environment. It can be installed individually or together with other extensions contained in the pack available for Visual Studio Code Desktop.

We recommend installing the **Keil Studio Pack** for Visual Studio Code Desktop to quickly set up your environment and start working with an example.

## Intended use cases for the extensions

- **Embedded and IoT software development using CMSIS-Packs and csolution projects**: The "Common Microcontroller Software Interface Standard" (CMSIS) provides driver, peripheral and middleware support for thousands of MCUs and hundreds of development boards. Using the csolution project format, you can incorporate any CMSIS-Pack based device, board, and software component into your application. For more information about supported hardware for CMSIS projects, go to the [Boards](https://www.keil.arm.com/boards/) and [Devices](https://www.keil.arm.com/devices/) pages on keil.arm.com. For information about CMSIS-Packs, go to [open-cmsis-pack.org](https://www.open-cmsis-pack.org/index.html).

- **Enhancement of a pre-existing Visual Studio Code embedded software development workflow**: USB device management and embedded debug can be adapted to other project formats (for example CMake) and toolchains without additional overhead. This use case requires familiarity with Visual Studio Code to configure tasks. See the individual extensions for more details.

## Vcpkg manifest file example

Create a file named `vcpkg-configuration.json` in your workspace with the following contents:

```json
{
  "registries": [
    {
      "name": "microsoft",
      "location": "https://aka.ms/vcpkg-ce-default",
      "kind": "artifact"
    },
    {
      "name": "arm",
      "location": "https://aka.ms/vcpkg-artifacts-arm",
      "kind": "artifact"
    }
  ],
  "requires": {
    "microsoft:tools/kitware/cmake": "^3.25.2",
    "arm:compilers/arm/arm-none-eabi-gcc": "^12.2.1-0"
  }
}
```

When you create the file, modify it, or when you open the workspace, these artifacts are activated and available to other Visual Studio Code extensions and the terminal.

## Submit feedback

To submit feedback, please [see our support page](https://www.keil.arm.com/support/#:~:text=Installing%20the%20Tools).
