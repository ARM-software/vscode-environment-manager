# Arm Environment Manager

## Overview

This VS Code extension allows you to manage environment artifacts using the [vcpkg-artifacts](https://github.com/microsoft/vcpkg-tool) tool.

## Example

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

When the file is created, modified or the workspace is opened, these artifacts are activated and available to other VS Code extensions and the terminal.

## Submit feedback

To submit feedback, please [create an issue](https://github.com/Arm-Software/vscode-environment-manager/issues/new/choose).
