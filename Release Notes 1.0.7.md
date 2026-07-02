# Kardex WMS 1.0.7

Release date: 2026-07-02 16:30

## Summary
- Adds the external live console and encrypted support log viewer for colleague/customer testing.

## Changes
- Adds a separate Kardex WMS Live Console executable for dev/support log monitoring.
- Adds a separate Kardex WMS Support Log Viewer executable for encrypted .kwmslog packages.
- Adds structured diagnostic logging alongside the readable log file.
- Adds Help > Create support package to generate encrypted support bundles.
- Improves import/dashboard logging so SQL restore and dashboard cache failures are easier to diagnose.
- Makes dashboard cache generation retryable after a successful SQL restore instead of failing the whole import.

## Verification
- Built Kardex WMS application, installer, live console, and support log viewer.

## Installer
- Kardex WMS Setup 1.0.7.exe

