# Arm Environment Manager

## Overview

The complete [documentation](https://developer.arm.com/documentation/108029/latest/Extension-pack-and-extensions) for the Keil® Studio extensions is available on Arm® Developer.

The Arm Environment Manager extension allows you to manage environment artifacts using the [Microsoft vcpkg-artifacts](https://github.com/microsoft/vcpkg-tool) tool. The extension uses a vcpkg manifest file to acquire and activate the artifacts that you need to set up your development environment. You can install the extension individually or as part of the Arm Keil Studio Pack extension in Visual Studio Code Desktop.

We recommend installing the Keil Studio Pack for Visual Studio Code Desktop to quickly set up your environment. When you have installed the pack, read the documentation available on Arm Developer to get started. You can [import a csolution example from keil.arm.com](https://developer.arm.com/documentation/108029/latest/Get-started-with-an-example-project/Import-a-csolution-example), [download and convert a μVision project from keil.arm.com](https://developer.arm.com/documentation/108029/latest/Get-started-with-an-example-project/Download-and-convert-a-Keil--Vision-example), [create a csolution project from scratch](https://developer.arm.com/documentation/108029/latest/Arm-CMSIS-csolution-extension/Create-a-csolution-project), or [convert an existing μVision project](https://developer.arm.com/documentation/108029/latest/Arm-CMSIS-csolution-extension/Convert-a-Keil--Vision-project-to-a-csolution-project).

## Intended use cases for the extensions

- **Embedded and IoT software development using CMSIS-Packs and csolution projects**: The Common Microcontroller Software Interface Standard (CMSIS) provides driver, peripheral, and middleware support for thousands of MCUs and hundreds of development boards. Using the csolution project format, you can incorporate any CMSIS-Pack based device, board, and software component into your application. For more information about supported hardware for CMSIS projects, go to the [Boards](https://www.keil.arm.com/boards/) and [Devices](https://www.keil.arm.com/devices/) pages on keil.arm.com. For information about CMSIS-Packs, go to [open-cmsis-pack.org](https://www.open-cmsis-pack.org/index.html).

- **Enhancement of a pre-existing Visual Studio Code embedded software development workflow**: You can adapt USB device management and embedded debug to other project formats (for example, CMake) and toolchains without additional overhead. This use case requires familiarity with Visual Studio Code to configure tasks. See the individual extensions for more details.

## Example vcpkg manifest file 

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

When you create or modify the file, or when you open the workspace, these artifacts are activated and available to other Visual Studio Code extensions and the terminal.

## Submit feedback

To submit feedback, please [see our support page](https://www.keil.arm.com/support/#:~:text=Installing%20the%20Tools).
