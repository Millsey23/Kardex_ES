# Kardex Support Suite 0.4.28

Release date: 2026-08-04

## Summary
- Adds a New Units Placement Presentation PDF inside Warehouse Advanced Strategy.
- The new report gives a customer-facing, slide-style summary rather than a long text export.
- It highlights parts assessed, parts allocated to Kardex units, parts retained on rack, fast movers, size-check exceptions, machine allocation, and expected picking impact.
- The report links the high-level customer story to the detailed preload HTML and placement exports already available in the suite.

## Warehouse Advanced Strategy
- New report action: Placement presentation PDF.
- Uses the New Units placement plan and future-state simulation.
- Summarises how many parts go into each machine and how much represented pick demand is moved away from static aisle picking.
- Uses entered current/projected picks per hour where available.
- Falls back to aisle walking assumptions when picks per hour has not been entered.
- Includes concise sign-off notes showing what data still needs customer confirmation.

## Verification
- Built Kardex Support Suite in Release mode.
- Built and packaged the bundled Advanced Strategy module.
- Created the 0.4.28 .kdxupd update package and manifest.
