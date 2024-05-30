# Arm Environment Manager

## Overview

The complete [documentation](https://developer.arm.com/documentation/108029/latest/Extension-pack-and-extensions) for Arm® Environment Manager and the other Keil® Studio extensions is available on Arm Developer.

The Arm Environment Manager extension allows you to manage environment artifacts using the [Microsoft vcpkg-artifacts](https://github.com/microsoft/vcpkg-tool) tool. The extension uses a vcpkg manifest file to acquire and activate the artifacts that you need to set up your development environment. It also manages the license for Arm tools on your system. You can install the extension individually or as part of the Arm Keil Studio Pack extension in Visual Studio Code Desktop.

We recommend installing the [Keil Studio Pack](https://marketplace.visualstudio.com/items?itemName=Arm.keil-studio-pack) for Visual Studio Code Desktop to quickly set up your environment. You can then [import a solution example from keil.arm.com](https://developer.arm.com/documentation/108029/latest/Get-started-with-an-example-project/Import-a-solution-example), [download a μVision project from keil.arm.com](https://developer.arm.com/documentation/108029/latest/Get-started-with-an-example-project/Download-a-Keil--Vision-example), [create a solution from scratch](https://developer.arm.com/documentation/108029/latest/Arm-CMSIS-Solution-extension/Create-a-solution), or [convert an existing μVision project](https://developer.arm.com/documentation/108029/latest/Arm-CMSIS-Solution-extension/Convert-a-Keil--Vision-project-to-a-solution).

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
