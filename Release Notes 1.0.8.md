# Kardex WMS 1.0.8

Release date: 2026-07-03 09:13

## Summary
- Adds software-calculated bin quantities for new-unit planning.
- Keeps fixed bin quantities available where a customer has a known bin stock.
- Improves new-unit material placement so large material quantities can be split across multiple approved bins.

## Changes
- New-unit bin setup now supports fixed or software-calculated bin quantities per bin type.
- The layout planner can calculate required bin counts from ERP/order demand, material storage rules, allowed bin types, and safe quantity estimates.
- Material placement now records the planned quantity for each individual bin, rather than treating one material as a single-location placement.
- New-unit PowerPick initial stock exports now use the per-bin planned quantity.
- New-unit customer filling plan reports now show the planned quantity for each bin location.
- Planner cache version increased so older saved projects are recalculated with the new logic.

## Verification
- Published Kardex WMS application for Windows x64.
- Published external live console and support log viewer tools.
- Published the single-file Kardex WMS installer.
- Verified the WinUI project builds cleanly before packaging.

## Installer
- Kardex WMS Setup 1.0.8.exe
