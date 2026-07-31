# Kardex Support Suite 0.4.19

## Summary
- Fixes Advanced Strategy module packaging so the bundled module folder contains the standalone engine DLLs and machine image assets.
- Ensures installed PCs receive the Warehouse Advanced Strategy engine under Modules\AdvancedStrategy instead of relying on development-machine paths.
- Makes the suite prefer the bundled Advanced Strategy engine before falling back to local development builds.
- Passes SQL/database and import-state details into the Advanced Strategy engine before strategy generation and report export.
- Routes existing-unit Advanced Strategy reports to the original standalone report services where available: Overall Improvement, Picking Behaviour, Empty Locations and Historical Day Savings.
- Keeps suite fallback PDF generation if a standalone report export fails, while recording the underlying error for diagnostics.
- Restores packaged access to XP and RS machine images for dashboard and machine visualisation cards.

## Verification
- Built Kardex Support Suite in Release mode with zero warnings and zero errors.
- Added packaging validation for KardexBinInsight.WinUI.dll, Assets\XP.png and Assets\RS.png so future releases fail fast if the Advanced Strategy module is incomplete.
