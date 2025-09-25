
# Fabrication Workflow Guide

**Pipeline**: Revit/CADmep → Spool → Plasma → Groove → FitUp → Weld → QA → Sync back → ACC/Power BI

1. **Load Database**: Use the drop‑in DB (pipes, elbows, reducers, flanges with weights & icons).
2. **Route & Spool**: Generate spools with ENTIRE_Piece_ID and ENTIRE_Spool_ID.
3. **QR Labels**: Run `QR_Generator.dyn` to create QR codes & a tag schedule.
4. **Shop Stations**: Scan QR at each station (Plasma, Groove, FitUp, Weld). Logs follow `Station_Log_Schema.csv`.
5. **Sync to Revit**: Run `StationLog_Sync.dyn` to write timestamps back to Shared Parameters and set `Fabrication_Status`.
6. **Visualize**: Use View Filters to color code status (grey/blue/orange/yellow/green/bright‑green).
7. **Analytics**: Power BI template reads station & delivery logs — shows cycle time, throughput, bottlenecks.
8. **Delivery**: Use `Delivery_Log_Schema.csv` for planned/confirmed deliveries, crane booking, site access.

See also:
- `QR_Code_Labeling.md`
- `ACC_PowerBI_Embedding.md`
