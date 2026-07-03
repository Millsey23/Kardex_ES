# Kardex WMS 1.0.9

Release date: 2026-07-03

## Summary
- Adds a lightweight in-app update package alongside the full setup installer.
- Keeps the full installer available as a fallback for clean installs and repair installs.
- Adds release-build signing hooks so Kardex WMS can be code-signed once a certificate is available.

## Changes
- The online update manifest now supports both a full installer URL and a lightweight update package URL.
- The app now prefers the update package for normal in-app updates.
- Downloaded update packages are verified with SHA-256 before they are applied.
- The app now closes, applies the ZIP package into the installed folder, then reopens automatically.
- If no update package is present in the manifest, the updater falls back to the full installer flow.
- The release builder now creates:
  - `Kardex WMS Setup <version>.exe`
  - `Kardex WMS Update <version>.zip`
  - `kardex-wms-update.json`
  - `Release Notes <version>.md`
- The release builder can sign the app, support tools, and setup executable when a certificate thumbprint or certificate file is supplied.

## Security
- Update packages are hash-checked before installation.
- Code signing is prepared but not active in this release because no signing certificate has been supplied yet.
- Windows SmartScreen warnings can still appear until the executable files are signed with a trusted code-signing certificate and build reputation.

## Verification
- Built Kardex WMS application in Release mode.
- Published Kardex WMS application, support tools, full installer, and update package.
- Verified the generated manifest hash entries against the package files.

## Installer
- Kardex WMS Setup 1.0.9.exe

## Lightweight update package
- Kardex WMS Update 1.0.9.zip
