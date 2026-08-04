# Kardex Support Suite 0.4.31

Release date: 2026-08-04

## Summary
- Cleans up the main suite navigation by moving top-bar actions into dropdown menus.
- Adds a collapsible module rail so the left-hand module list can be hidden and restored.
- Replaces the Advanced Strategy button strip with a workflow dropdown.
- Updates the synthetic Amazon-style ERP test pack with realistic bin sizes and material/bin rules.

## User Interface
- Top bar now uses Project, Admin and Tools dropdown menus.
- Module navigation can be collapsed to a slim rail and expanded again.
- Advanced Strategy pages such as Implementation Type, Import, Dashboard, Bins, Reports and Settings are now selected from one Workflow menu.

## Warehouse Advanced Strategy
- Bin catalogue imports now accept BinClass-based files and explicit width/depth/height columns.
- Bin fit now uses an 85% usable-space factor to allow roughly 15% handling clearance/air gaps.
- Placement evidence now includes an estimated max quantity per selected bin where dimensions and max weight are available.

## Test Data
- Updated AmazonStyle_ERP_100000Orders_20000Parts.zip.
- Contains 20,000 unique materials and 100,000 ERP orders.
- Uses realistic bins: 15 x 15 cm, 30 x 30 cm, 35 x 35 cm, 40 x 60 cm, 60 x 80 cm and static-only.
- Includes per-material max units per bin class using the 85% usable-space rule.

## Verification
- Built Kardex Support Suite in Debug mode.
- Built Kardex Support Suite in Release mode.
- Built and packaged the bundled Advanced Strategy module.
- Created the 0.4.31 .kdxupd update package and manifest.
