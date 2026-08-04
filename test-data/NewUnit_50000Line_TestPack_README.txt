Kardex Support Suite - Synthetic New Unit Test Pack
===================================================

Generated: 2026-08-04 09:46:14
Purpose: test Warehouse Advanced Strategy New Units imports, reports, opportunity analysis, route animation and high-volume ERP processing.

This is synthetic data only. It is not customer data.

Recommended import order inside Warehouse Advanced Strategy > New Units:
1. Start a New Units project.
2. Import folder and select this full folder, or import the CSV files individually.
3. Use New_Unit_Machine_Plan.csv for proposed machine setup.
4. Use New_Unit_Bin_Rules.csv and New_Unit_Tray_Plan.csv for tray/bin planning.
5. Use ERP_OrderLines_50000.csv as the main ERP/order history file.
6. Use ERP_Current_Stock_And_Static_Locations.csv and Warehouse_Aisle_And_Route_Map.csv for before/after route analysis.
7. Use Strategy_Do_Not_Move_List.csv to test excluded materials in reports and change lists.

Files:
- ERP_OrderLines_50000.csv: 50,000 data rows plus header. Main ERP order history.
- ERP_Material_Master_3000.csv: 3,000 SKU/material rows with dimensions, weight, lot/serial/expiry/barcode signals.
- ERP_Current_Stock_And_Static_Locations.csv: current static rack location and suggested Kardex allocation data.
- New_Unit_Machine_Plan.csv: five proposed machines, including Shuttle XP and Megamat RS Carousel examples.
- New_Unit_Bin_Rules.csv: bin dimensions, classes, planned location counts and weight limits.
- New_Unit_Tray_Plan.csv: tray-level planning rows for each proposed unit.
- ERP_Picked_Together_Sample.csv: associated material pairs for grouping/replenishment testing.
- Warehouse_Aisle_And_Route_Map.csv: aisle geometry for before/after picking route visualisation.
- Strategy_Do_Not_Move_List.csv: test material exclusions for reports and change recommendations.
- Module_Opportunity_Input.csv: input signals for lot, serial, expiry, barcode, ERP and aisle/zone module opportunity reporting.

Column guidance:
- MaterialCode links ERP orders, material master, stock, exclusions and picked-together rows.
- SuggestedMachine links proposed stock allocation to New_Unit_Machine_Plan.csv.
- SuggestedBin links proposed stock allocation to New_Unit_Bin_Rules.csv.
- Aisle, Side, Bay and Level give the static-racking route evidence.
- LotNumber, SerialNumber, ExpiryDate and Barcode are deliberately populated on some rows to test Power Pick module opportunity reports.

Expected scale:
- 50,000 ERP lines.
- 10,000 orders at 5 lines/order.
- 3,000 materials.
- 5 proposed Kardex units.
- 392 tray rows.
