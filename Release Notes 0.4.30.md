# Kardex Support Suite 0.4.30

Release date: 2026-08-04

## Summary
- Adds the consolidated New Units Strategy Report as the main customer-facing New Units output.
- Expands the report beyond placement-only content into capacity, movement tiers, static rack rationale, module opportunities, risks and sign-off.
- Keeps Preload HTML and Part Placement HTML as visual operational outputs.

## Warehouse Advanced Strategy - New Units
- Renames the main report action to New Units Strategy Report.
- Adds report sections for:
  - executive summary
  - machine allocation
  - picking impact
  - fast, medium and slow mover counts
  - Kardex allocation versus static rack allocation
  - size exceptions and capacity overflow
  - Power Pick module opportunities
  - static rack future optimisation data requirements
  - customer sign-off risks
  - recommended customer deliverables
- Keeps LR35 / VBM prioritised as the fastest machine class where fit and capacity allow.
- Keeps the current manually configured New Units machine setup as the source of truth for generation.

## Verification
- Built Kardex Support Suite in Debug mode.
- Built Kardex Support Suite in Release mode.
- Built and packaged the bundled Advanced Strategy module.
- Created the 0.4.30 .kdxupd update package and manifest.
