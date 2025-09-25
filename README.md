
# PREFAB ENGINEERING — Fabrication Digital Twin

A connected workflow for Pipework fabrication across Revit/CADmep ⇄ Shop Robots ⇄ ACC ⇄ Power BI.

## What’s here
- `database/` — Drop‑in Fabrication MEP DB (CS Sch40, SS Sch10) with icons, connectors, flanges (Table E, EN1092 PN16, DIN PN10/16)
- `integration/` — Revit Shared Parameters, CSV schemas, and ACC/Power BI docs
- `dynamo/` — Dynamo graphs: QR generation, Station Log sync, STEP export auto‑naming
- `powerbi/` — KPI template for cycle times, throughput, bottlenecks, delivery readiness
- `docs/` — Setup & training guides (Markdown) with screenshots

## Quick start
1. Download the latest **Drop‑In DB** from `database/` and unzip into your Fabrication DB folder.
2. Load `integration/ENTIRE_SharedParameters.txt` into Revit.
3. Run Dynamo graphs from `dynamo/`:
   - `QR_Generator.dyn` — creates QR images & Piece_IDs
   - `StationLog_Sync.dyn` — writes timestamps & status back to Revit; applies colors
   - `STEP_Export_AutoName.dyn` — exports STEP/DXF with Piece_ID filenames
4. Publish the **Power BI** template in `powerbi/` and embed in ACC.

> For full guidance, see `docs/Fabrication_Workflow_Guide.md`.
