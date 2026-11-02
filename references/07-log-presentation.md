# Log presentation

Contents
1. Header fields
2. Columns on a final soil log
3. Columns on a final rock log
4. Graphic log and legends
5. Notes, remarks and disclaimers
6. Field-sheet layouts seen in practice
7. Units and scales
8. Status, versions and sign-off
9. Data exchange formats

## 1. Header fields

| Group | Fields |
| --- | --- |
| Identity | Hole ID, sheet x of y, project name and number, client, site/location description |
| Position | Easting/northing or lat/long, coordinate system and zone, ground elevation, datum, how surveyed, inclination and bearing |
| Drilling | Contractor, driller, rig model, method(s) per depth range, hole and casing diameters, core size, hammer type and energy ratio |
| Dates | Start and finish dates (often a range), times |
| People | Logged/originated by, compiled by, checked/approved by, with dates |
| Water | Summary of water levels (or a table) |
| Status | DRAFT / FINAL, revision |

## 2. Columns on a final soil log (typical, left to right)

Elevation · Depth (m, sometimes ft beside) · Graphic strata column ·
Description and classification · Sample type, number, recovery · SPT N (and
plot) · DCPT plot · Strength plot (PP, torvane, vane, lab UCS/triaxial) ·
Water content plot with PL and LL bars · Grain size % (GR SA SI CL) · Unit
weight · Groundwater symbol · Installation column · Remarks.

Look notes designers read logs right to left: key numbers first, description
second, so test columns sit on the right.

## 3. Columns on a final rock log

Depth · Elevation · Graphic · Rock description · Weathering · Strength
(estimated and tested: point load axial/diametral, UCS) · Run number · TCR /
SCR / RQD (often as bars) · Fracture spacing or frequency · Defect descriptions
(depth, type, angle, roughness, infill, thickness) · Water/flush return ·
Remarks.

## 4. Graphic log and legends

- Each soil or rock type has a hatch pattern; patterns vary by firm and are
  driven by the USCS symbol or rock name, with overrides.
- Fill, topsoil and organic soils have their own hatches.
- Rock logs may show fracture ticks at depth: natural joint, mechanical break,
  broken zone.
- A legend sheet or key explains symbols, sample codes, proportion terms and
  abbreviations.

## 5. Notes, remarks and disclaimers

- Depth remarks sit beside the description (casing advanced, cobble, fluid loss).
- Within-layer changes as indented "- … below x m" sub-lines.
- Lab results as sub-lines or in columns.
- Completion notes numbered under the log (termination, water on completion,
  backfill, installation).
- Standard disclaimer: boundaries are approximate and transitions may be gradual;
  water levels may vary with season.

## 6. Field-sheet layouts seen in practice

Field sheets differ widely; a reader (or extraction prompt) must not assume one:
- Header boxes with equipment tick boxes (rig size, hand/portable, SSA/HSA/wash
  bore, diameter) and a water level table with "through casing / on completion"
  and cave columns.
- Depth columns in both m and ft, or ft only.
- Separate VANE (in-situ, remoulded) columns, or a MISC TESTS column with codes
  (H headspace, SPT, T torvane, PP).
- PID (ppm), recovery as "Dr./Rec." pairs, blow counts, an "N value / RQD"
  shared column, and an "engineer review comment" column on the field sheet.
- A printed soil description key (proportion words, grain sizes) and sample
  type key in the footer, plus well details and a printed standpipe sketch.
- Separate core sheets (one row per run) and fracture sheets (one row per break,
  tick-box grids for condition and infill).
- Compiled PDFs holding several holes, with mislabelled or reused sheets.

## 7. Units and scales

- Canada reports in metres; many field sheets are in feet. US work is often in
  feet throughout. Some finals show both scales.
- Recovery in inches or % ; core lengths in m, ft or inches.
- Strength in kPa (final) vs kg/cm², tsf, t/m² (field instruments).
- Every stored number carries its unit; conversions happen once, consistently.

## 8. Status, versions and sign-off

- DRAFT watermark until review is complete; "unsealed" or "not for
  construction" wording on some drafts.
- Revision history: what changed between drafts and who approved.
- A professional seal, where applicable, is on the report, not usually on each
  log.

## 9. Data exchange formats

- AGS 4 (UK/international, with regional variants): groups such as LOCA
  (location), GEOL (strata), SAMP (samples), ISPT (SPT), CORE (core runs), DETL
  (depth-related remarks), FRAC/DISC (discontinuities), WSTG/WSTD (water strikes),
  HDPH (hole depth/method), plus lab groups. Check the group list against the
  current AGS data dictionary before implementing.
- gINT / OpenGround / HoleBASE project databases; many North American firms
  produce finals from gINT.
- CSV or Excel exports; CPT data in vendor or standard formats.
- A log is increasingly seen as a view of a database; exporting the data matters
  as much as the PDF.
