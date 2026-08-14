# Kardex Support Suite 0.4.33

Release date: 2026-08-14 09:49

## Summary
- Fixes update package downloads timing out after 45 seconds on slower or inspected network connections.
- Keeps the GitHub manifest check quick while allowing the larger `.kdxupd` update package to stream for up to 30 minutes.
- Downloads update packages through a temporary `.download` file first, preventing failed downloads from leaving corrupt update packages behind.
- Improves the timeout message so support can distinguish a manifest/channel problem from a slow package download.

## Verification
- Built Kardex Support Suite.
- Built Advanced Strategy module.
- Created suite update package and manifest.
- Verified the GitHub manifest points to version 0.4.33.
