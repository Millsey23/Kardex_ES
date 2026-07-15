# Kardex Support Suite 0.4.7

## Summary
- Fixes the PowerShell update installer so extracted `.kdxupd` files are actually copied into the installed application folder.
- Adds stronger update logging for extraction, copy source, install folder and installed executable version after update.
- Waits for the running suite process to close before replacing files, and reports a clear failure if it cannot close in time.
- Verifies that the update package contains `KardexSupportSuite.exe` before applying it.

## Important
- PCs already running a build with the previous updater may need the 0.4.7 installer once, because that older build generates the old update script before it can install this fix.
- After 0.4.7 is installed, future GitHub `.kdxupd` updates should apply through the normal update channel.

# Kardex Support Suite 0.4.6

## Summary
- Adds a developer diagnostic bundle export under Help / About.
- Captures licence status, installed module file checks, runtime paths, session summary and local Support Suite / Log Reader diagnostic files.
- Adds a Log Reader diagnostic summary including loaded source count, analysis state, environment node/link counts and environment-view notes.
- Intended for cases where an installed PC behaves differently from the development PC, such as a blank Log Reader environment view.

# Kardex Support Suite 0.4.5

## Summary
- Improves the manual update check confirmation popup.
- Successful manual checks now say the update channel is connected.
- The popup shows current version, latest version, release date and whether the suite is on the correct version or a new version is available.
- Startup checks remain quiet unless an update needs to be installed.

# Kardex Support Suite 0.4.4

## Summary
- Handles missing GitHub update manifests gracefully.
- A 404 for `kardex-support-suite-update.json` is now shown as an unpublished update channel rather than a failed update.
- Startup update checks continue silently with the installed version when the update channel has not yet been published.
- Manual update checks now explain that the update channel has not been published yet.

# Kardex Support Suite 0.4.3

## Summary
- Adds automatic update checking every time the suite opens.
- If a newer GitHub manifest version is available, the suite downloads, verifies and applies the `.kdxupd` update package automatically.
- If the startup update check fails, the suite continues running the installed version and records the failure in the session status.
- The manual Updates button remains available for a manual check.

# Kardex Support Suite 0.4.2

## Summary
- Switches the suite updater to a passive Kardex update package file instead of a setup executable.
- Uses the GitHub manifest at `https://raw.githubusercontent.com/Millsey23/Kardex_ES/main/kardex-support-suite-update.json`.
- Adds `.kdxupd` update packages. These are ZIP-compatible internally but are treated as Kardex update data files by the installed suite.
- The suite now refuses to apply downloaded EXE/installers through the update path.
- The release builder now creates `Kardex Support Suite Update <version>.kdxupd`.
- The GitHub upload script now uploads the `.kdxupd` package and writes `updateFileUrl` / `updateFileSha256` to the manifest.
- Updates are still SHA-256 verified before being applied.

## Update Flow
- Support Suite checks the GitHub JSON manifest.
- If the manifest version is newer, the suite downloads the `.kdxupd` update file.
- The suite verifies the SHA-256 hash from the manifest.
- The suite closes, applies the update package into the installed folder, and restarts.

# Kardex Support Suite 0.4.1

## Summary
- Adds the Power Pick Port Checker to Support Tools.
- Adds standalone Port Checker export for customer PCs.
- Adds a 5-day first-run expiry window to the standalone Port Checker.
- Updates the suite manual with Port Checker workflow, direction rules and expiry behaviour.

## Port Checker
- Starts with an empty test plan so engineers add only the checks required for the case.
- Add Row now offers standard templates for SQL Server, SQL Browser, Rule Engine, MCS, machine/controller, light pointer, diagnostics, Cross Enterprise Unit, web/API and custom checks.
- Each check records source, destination, port and flow direction.
- Checks only prove connectivity from the PC running the checker. Remote-source checks are marked Review and instruct the engineer to run the standalone checker from that source PC.
- The integrated Support Suite module does not expire.
- Exported standalone Port Checker packages run for 5 days from first run on the customer Windows profile.

# Kardex Support Suite 0.4.0

## Summary
- Expands the suite into a fuller all-in-one support workspace.
- Adds SQL / Backup Tools as a separate licensable module.
- Updates the dashboard so every licensed module is shown as a card.
- Adds an in-page Back button and improved navigation history for support sub-pages.
- Updates the suite manual into a combined master manual covering every module.

## Modules
- Power Pick Log Reader is included as a licensed module.
- Warehouse Advanced Strategy is included as a licensed module.
- SQL / Backup Tools is included as a licensed module.
- Support Tools is included as a licensed module.
- Environment Health Check is included as a licensed module.

## SQL / Backup Tools
- Adds SQL instance discovery and connection testing.
- Adds restore and scan workflows for customer SQL backups/databases.
- Adds SQL Backup Inspector with quick preflight checks:
  - SQL connection test
  - RESTORE HEADERONLY
  - media family/sequence validation
  - RESTORE FILELISTONLY
  - RESTORE VERIFYONLY
- Adds PDF export for SQL workspace and backup inspector reports.

## Support And Health
- Adds individual service status cards for Kardex, Power Pick, SQL, MCS and Rule-related services.
- Adds Environment Health Check pass/review/fail cards and PDF export.
- Adds Support Bundle creation based on session evidence, reports and customer PDFs.
- Adds Known Error Knowledge Base, Customer Data Wizard, Version Audit and Redaction Tool.

## Help And Customer Documents
- Replaces the short suite manual with a combined master manual covering:
  - Licensing
  - Dashboard/navigation
  - SQL / Backup Tools
  - Power Pick Log Reader
  - Warehouse Advanced Strategy
  - Support Tools
  - Environment Health Check
  - Reports/exports
  - Customer data request PDFs
  - Troubleshooting notes
- Keeps links to the detailed Log Reader manual and Advanced Strategy PDF.

## Updates
- Uses suite-level update checking through the shared update channel.
