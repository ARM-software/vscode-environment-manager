# Change Log

## [Unreleased]

## 1.12.0

- Fixed issue with new configuration file not saving in the workspace root

## 1.10.0

- List all packages and warn for those which won't work on the current system
- Update to use vcpkg binary in the vcpkg root folder when set

## 1.8.0

- Improved README.

## 1.6.0

- Improvements to command names throughout the UI
- The status bar now reflects the "disabled" state

## 1.4.1

- Updated the default Arm tools registry URL to be https://artifacts.tools.arm.com/vcpkg-registry

## 1.4.0

- Add `acquirePackages` to the packages API. This downloads a list of packages to the cache, without requiring a vcpkg-configuration.json.
- Prevent multiple environment activations occurring at the same time, for example, when repeatedly
  changing a vcpkg-configuration.json. This could cause activations to fail, extra data to be downloaded
  or cache corruption.
- Improve documentation for extension API.

## 1.2.0

- Fix tools download for Arm64 Linux machines by including a vcpkg built for the architecture.
- Enable the extension for Arm64 Windows machines.
- Add names to status bar entries so they can be distinguished.

## 1.1.17

- Fix API types.
- armlm binary bumped to version 1.3.1 .

## 1.1.16

- Add getActiveTools to extension API.

## 1.1.15

- Improve handling of license expiry.

## 1.1.14

- Add inline intellisense for manifest files.

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
