# Change Log

## Unreleased

## 1.1.13

- Fix license detection for AVH package.

## 1.1.12

- Disable telemetry by default for SSK and HSK licenses.

## 1.1.11

- Added detection of missing long pathname support on Windows.
- Extension API: Expose v2 version, which includes licensing information.
- Don't show the option to configure the tools while the environment is activating.

## 1.1.10

- Clarify that the MDK 6 Community license is for non-commercial free of charge use.
- Support for handling multiple activated licenses.
- Add diagnostics for unlicensed packages.

## 1.1.9

- Add command to open armlm.
- Support for handling license expiry.

## 1.1.8

- Status bar does not disappear when workspace is not configured, allowing easier initialization.
- Make primary quick-pick action opening the visual configuration editor.
- Show list of entries added to VS Code PATH on hover.

## 1.1.7

- Remove option from settings to silence license notifications.
- armlm binary bumped to version 1.2.6 .
- Fixed license detection on Windows.

## 1.1.6

- Rename status bar and icon.
- Use title case across messages.
- Make primary quick-pick action opening the visual configuration editor.
- Require license activation only when project uses tools requiring a license.

## 1.1.5

- Improve visual look of the license information in the status bar.

## 1.1.4

- Add command to activate any Arm license.

## 1.1.3

- Add license information in the status bar.

## 1.1.2

- Add logic for MDK license check.

## 1.1.1

- Preserve focus when showing environment manager output channel.

## 1.1.0

- Add custom editor for managing tool configurations.

## 1.0.6

- Prevent concurrently activating the same environment.

## 1.0.5

- Fix activating vcpkg-configuration files not at the workspace root.

## 1.0.4

- Warn about conflicts with the Microsoft Embedded Tools extension. Offer to disable the vcpkg support provided by that extension.
- Fix activateOnWorkspaceOpen, reactivateOnConfigChange and activateOnConfigCreation settings.

## 1.0.3

- De-duplicate log messages in output channel.

## 1.0.1

- Initial Release
