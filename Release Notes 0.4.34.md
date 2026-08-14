# Kardex Support Suite 0.4.34

Release date: 2026-08-14 10:09

## Summary
- Publishes a small transition update so older installed copies can receive the updater timeout fix without downloading the full suite package inside the old 45-second limit.
- Replaces the suite updater files only; existing bundled modules and assets remain in place.
- After this transition update is installed, future full suite updates use the longer streamed package downloader.

## Verification
- Published suite-only binaries at version 0.4.34.
- Created a small transition update package.
- Verified package hash and manifest generation.
