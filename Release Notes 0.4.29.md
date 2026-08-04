# Kardex Support Suite 0.4.29

Release date: 2026-08-04

## Summary
- Refines the Warehouse Advanced Strategy New Units workflow.
- Simplifies New Units report options into a smaller customer-facing set.
- Adds a slide-style Placement Presentation PDF for New Units proposals.
- Updates LR35 / VBM handling so it is treated as the fastest Kardex machine class.

## Warehouse Advanced Strategy - New Units
- New Units project setup now starts cleanly and uses button-driven Add machine / Add bin type dialogs.
- Machine setup now uses dropdowns for machine type, capacity unit and access opening.
- Capacity terminology now adapts by machine type:
  - Shuttle: trays
  - Carousel / RS: carriers or shelves
  - LR35 / VBM: boxes or totes
- LR35 / VBM placement is prioritised for high runners where fit and capacity allow.
- LR35 / VBM reporting now explains bin/tote pre-staging while the operator picks from the current bin.
- Preload HTML is now a step-through guide with Previous / Next navigation by machine.
- New Units Reports page now focuses on:
  - Animated picking comparison
  - Placement presentation PDF
  - Part placement HTML
  - Preload HTML

## Verification
- Built Kardex Support Suite in Release mode.
- Built and packaged the bundled Advanced Strategy module.
- Created the 0.4.29 .kdxupd update package and manifest.
