# How firms differ, and how to onboard a new one

Contents
1. Why this matters
2. The dimensions on which firms differ
3. Patterns already seen on customer logs
4. The convention profile (what to capture per organisation)
5. Onboarding procedure for a new firm
6. Question bank for the firm's engineer
7. Rules for keeping this company-agnostic

## 1. Why this matters

New customers will keep bringing conventions nobody has seen yet. The product
stays ready by treating every convention as data in a per-organisation profile,
backed by a standard-agnostic measurement model, and by having a repeatable way
to learn a new firm's conventions from their own field and final logs.

## 2. Dimensions on which firms differ

| Dimension | Examples of variation |
| --- | --- |
| Classification system | USCS (ASTM D2487/D2488), Canadian CFEM/MTO-style wording, AS 1726, BS 5930/ISO 14688, AASHTO for roads |
| Description order | Name first vs consistency first; colour before or after density |
| Proportion words | trace/few/little/some/mostly; trace/some/-y/and; trace/some/with/and; slightly/very |
| Consistency and density terms | firm vs medium; compact vs medium dense; different kPa limits |
| Particle-size limits | Cobbles 75–200 vs 75–300 mm; sand/gravel split at 2 or 4.75 mm |
| Units | Feet field sheets with metre finals; inches for recovery; kg/cm² or tsf instruments |
| Sample codes | SS/SB/ST/A/C/W; S1 vs SS-1; split portions 3A/3B |
| SPT reporting | N only; increments; refusal as "50/100 mm", "50+", or inferred N; four-increment spoons |
| Field strength tests | Pocket penetrometer, torvane, field vane, none; units and conversion |
| Rock logging | Weathering scheme, strength scheme, separate fracture sheets, codes for joints, RQD per run or per unit |
| Groundwater | Table of stages vs free text; cave-in recorded or not |
| Within-layer changes | Indented "below x m" sub-lines vs separate depth notes vs new layers |
| Lab data on the log | Plotted only; sub-lines; columns; not shown |
| Installations | Drawn column; text; separate installation log |
| Layout and template | Columns, plots, legends, logo and title block (template data, not code) |
| Workflow | Who reviews, how drafts are marked, what "final" means |
| Hole types | Vertical soil holes only; inclined rock holes; test pits; CPT |
| Environmental add-ons | PID, odour, staining, containers |

## 3. Patterns already seen on customer logs

Kept here without company names; the evidence lives in the team's own files.

- Handwritten field sheets in feet with metre finals; inches and feet mixed on
  one sheet ("0–3\"").
- "S.A.A." and "same as above" for repeated layers and core runs.
- Within-layer changes written as new lines and shown on the final as indented
  "- … below x m" sub-lines.
- USCS symbol added in brackets on the final ("CLAY (CH)"); origin and matrix
  added ("SILTY CLAY TILL").
- Torvane and pocket penetrometer recorded in a MISC TESTS column and converted
  to kPa on the final; unit conventions had to be inferred from field/final
  pairs.
- Lab results inserted as sub-lines ("LL=…, PL=…, PI=… at x m", "PSA: …").
- Method per depth range in the final header (auger, then HQ triple tube).
- Rock: core sheets with run lengths and RQD as lengths ("1.14/1.50"),
  separate fracture sheets with one row per break, letters written in tick
  boxes, mineral shorthand (FeS2, Qtz, chalco), "BCZ", "MB", "EOR".
- Inclined holes with bearing and angle written in the header margin.
- Compiled PDFs with several holes, re-used and mislabelled sheets, the same
  hole ID written three ways.
- A field sheet with an "engineer review comment" column and PID column, in
  feet, with USCS group names ("Lean CLAY w/ sand").
- A printed proportion key with a gap (some 10–20%, with 25–35%).
- Refusal written as "50+" with recovery, and "spoon bouncing" in the notes.
- Real issued finals still contain slips (inverted depth ranges).

## 4. The convention profile

Capture these per organisation (neutral names, stored as configuration):

```
profile:
  classification_system: USCS | CFEM_style | AS1726 | BS5930 | other
  description_order: [material, proportion_modifiers, colour, density_consistency, moisture, plasticity, structure, inclusions, origin]
  material_name_case: UPPER | Title | as_written
  symbol_display: "NAME (SYMBOL)" | separate column | none
  proportion_terms: [{word: trace, min: 0, max: 10}, {word: some, min: 10, max: 20}, ...]
  particle_size_limits: {boulder_min_mm: 200, cobble_min_mm: 75, gravel_min_mm: 4.75, sand_min_mm: 0.075}
  density_terms: [{word: compact, n_min: 10, n_max: 30}, ...]
  consistency_terms: [{word: firm, su_min_kpa: 25, su_max_kpa: 50}, ...]
  moisture_terms: [dry, moist, wet]
  field_units: {depth: ft, recovery: in}
  report_units: {depth: m}
  sample_codes: {SS: split_spoon, ST: shelby_tube, A: auger_grab, C: core, W: wash}
  spt: {increments: 3 | 4, refusal_display: "50/100 mm" | inferred_N | both, hammer_type: auto, energy_ratio_pct: null}
  field_tests:
    pocket_penetrometer: {unit: kg/cm2, report_as: Cu_kPa, conversion: "x98.1/2", readings: 3, report: average}
    torvane: {unit: t/m2, report_as: Cu_kPa, conversion: "x9.81"}
  within_layer_changes: sub_lines | depth_notes
  lab_on_log: sub_lines | columns | plots_only
  rock: {weathering_scheme: ISRM, strength_scheme: ISRM, rqd_basis: run | unit, fracture_log: true}
  groundwater_stages: [during_drilling, on_completion, stabilised]
  installation_display: column | notes
  template_id: <export template>
  confirmed_by: <engineer name/role>, confirmed_on: <date>
```

## 5. Onboarding procedure for a new firm

1. Collect at least two or three **field and final pairs** for the same holes,
   ideally including one soil hole, one rock hole if they core, and one with a
   well. Also collect their legend sheet, blank field forms, and any internal
   logging guide.
2. Read the blank forms first: header fields, columns, printed keys (proportion
   words, sample types, grain sizes), footer boxes.
3. Walk each pair line by line and record every transformation (`01` §5): units,
   merges, sub-lines, symbols, origin, conversions, notes, refusal display.
   Infer unit conventions from pairs where the final shows a converted value.
4. Fill the convention profile (§4). Mark every value as "seen", "inferred" or
   "assumed".
5. List everything they record that the product cannot yet store, with how often
   it appears and its design importance.
6. List handwriting and layout hazards (compiled PDFs, codes written in tick
   boxes, units missing on a column).
7. Turn uncertainties into questions for their engineer (§6). Do not guess
   where a wrong guess would change a number on the final.
8. After answers, record who confirmed each convention and when.
9. Add an invented, anonymised fixture that exercises the new conventions; never
   copy their data into fixtures.

## 6. Question bank for the firm's engineer

- Which classification and description standard do you follow? Any house
  variations?
- What proportion words and percentage ranges do you use?
- Do you report density as compact or medium dense? Consistency thresholds?
- Units on the field sheet vs the final; do you show both scales?
- Pocket penetrometer and torvane: instrument units, conversion, report Cu or
  qu, average or each reading?
- SPT refusal: how do you print it (50/x, inferred N, both)? Hammer type and
  energy ratio?
- Within-layer changes: sub-lines, notes, or new layers?
- Lab results: plotted only, or also as sub-lines?
- Rock: weathering and strength schemes; RQD per run or per unit; denominator
  when runs are split; meaning of any letter codes on fracture sheets.
- Inclined holes: show along-hole depth, vertical depth, or both?
- Groundwater: which stages do you report? Cave-in?
- Installations: drawn column or notes?
- What makes you reject a draft log? What do juniors most often get wrong?
- Who signs off, and what does "final" mean in your workflow?

## 7. Rules for keeping this company-agnostic

- Never put a firm's name, logo, address or job numbers into code, prompts,
  tests, fixtures or docs (AGENTS.md §3). Profiles carry neutral identifiers
  and are attached to an organisation at runtime.
- Never encode "if this firm then…" branches; encode the convention as data.
- Never copy customer field data into fixtures; write invented data that
  follows the same patterns.
- A convention seen at one firm is a candidate option, not a default for
  everyone.
