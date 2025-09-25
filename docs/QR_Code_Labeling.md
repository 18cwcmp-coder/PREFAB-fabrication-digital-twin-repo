
# QR Code Labeling

- Each piece gets a unique `ENTIRE_Piece_ID` + `ENTIRE_Spool_ID`.
- Dynamo graph `QR_Generator.dyn` exports PNGs named by Piece_ID and writes the file path back to the element.
- Create a Revit schedule or tag that displays the QR image next to the Piece_ID.
- Shop operators scan QR to auto‑populate station logs (Start/End) with minimal typing.
