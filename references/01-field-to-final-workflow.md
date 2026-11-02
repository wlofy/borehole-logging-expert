# From field log to final log

Contents
1. People and roles
2. The lifecycle of one borehole
3. What the logger does at the rig
4. Why the field log and the final log look different
5. The field-to-final transformations, rule by rule
6. Review and sign-off
7. What each person needs from software

## 1. People and roles

| Role | What they do | What they care about |
| --- | --- | --- |
| Driller | Advances the hole, runs the SPT, pulls core, keeps a driller's log (depths, methods, water, difficulties, a rough strata note from cuttings) | Production metres, equipment safety, getting paid for what was drilled |
| Field logger (technician, geologist or engineer; "inspector", "supervisor", "originated by") | Records every sample and observation as it happens and writes the visual-manual description | Speed, not missing anything, legible sheets |
| Compiler / drafter | Turns field sheets, lab data and photos into the final log, often in gINT, HoleBASE, OpenGround or a house tool | Consistency with the firm's style and with other holes |
| Reviewer (senior engineer, "checked by", "approved by") | Checks the final against the field record, lab data and the other holes; signs off | Errors that change design: wrong strength, wrong water level, missed soft layer, wrong refusal story |
| Designer / client | Reads the log, usually right to left (key numbers first, description second) | Trustworthy N values, strengths, water, boundaries, rock level |

The driller's log usually does not appear in the report; the engineer's log
supersedes it. A logger may be a junior technician, so the reviewer often
rewrites descriptions.

## 2. The lifecycle of one borehole

1. Planning: hole location, target depth, sampling interval (commonly every
   0.75 to 1.5 m and at every change of strata), tests, whether to core rock,
   whether to install a well. Services are located and cleared first (locate
   ticket; hydrovac or daylighting of the top 1.5 to 3 m is common in urban sites).
2. Drilling and field logging: one or more field sheets per hole, soil sheet and
   separate core and fracture sheets in rock.
3. Samples to the lab: moisture content on most samples, then grain size,
   Atterberg limits, and others on selected samples.
4. Water level readings: during drilling, on completion, and later (24 h,
   stabilised, monitoring rounds).
5. Compilation: draft final log, cross-checks against lab and other holes.
6. Review: marked-up draft, corrections, possibly reclassification from lab data.
7. Issue: DRAFT watermark removed, final log in the report appendix, data
   exported (often AGS or a gINT database).

## 3. What the logger does at the rig

Per sample, in roughly this order:
- Depth from and to of the drive or push.
- Sample type and number (SS-3, S3, ST-2, R1 for a core run).
- Blow counts per 150 mm (6 in) increment, or the push length for a tube.
- Recovery length (often in inches on North American sheets).
- Visual-manual description in the firm's order (`02`).
- Quick field tests on cohesive samples: pocket penetrometer, torvane; on
  environmental jobs a PID headspace reading.
- Container (bag, jar, tube) and any preservation.

Continuously, in a notes column or margin:
- Method changes ("switched to HQ coring at 3.05 m", "moved to casing").
- Rig behaviour: chatter, grinding, rods dropping, easier or harder drilling,
  loss of drilling fluid or water return, heave or running sand.
- Obstructions: cobbles, boulders, refusal and what kind (auger, casing, spoon).
- Water: when first noticed, level through casing, level and cave-in on
  completion, with times.
- End of hole: depth and reason, backfill, well details.

Rock is logged more slowly, and many loggers box the core and log it later in a
shed or the office, which lets RQD be judged over a whole rock unit rather than
run by run.

Electronic logging at the rig is used, but published guidance notes that on
fast soil drilling (around 20 m a day) paper is still often faster and is trusted
as a hard copy; tablets suit slow rock coring, core sheds and exposures. Coded
pick-lists help speed.

## 4. Why the field log and the final log look different

- The field log serves the logger: landscape layout, wide columns for notes,
  space for administrative items (times, payment quantities). It is filled left
  to right.
- The final log serves the designer: portrait layout, key numbers in columns on
  the right, plots of N, strength and water content, a graphic strata column.
- Strength tests, lab results and some interpretations do not exist yet when the
  field sheet is written.
- Many firms still prefer the two to look similar, so do not assume one layout.

## 5. Field-to-final transformations, rule by rule

These are the changes reviewers expect a compiler (or software) to make. Each
change should remain traceable to the field record.

| Field sheet | Final log | Notes |
| --- | --- | --- |
| "S.A.A.", "same as above", "see above", a down-arrow | The previous layer's description, or the layers merged into one | Merge only when the material really is the same; keep differing details as sub-lines |
| Depths in feet and inches ("1'–14", "0–4\"") | Metres, often with a feet scale beside | Inches written with a double prime are a frequent misread |
| A new line inside a layer ("moist below 9'", "no rootlets below 5'") | An indented sub-line under the layer worded "- moist below 2.7 m" | Not a new layer and not a free-floating note |
| Soil name only ("CLAY") | Name plus symbol: "CLAY (CH)"; group name per ASTM ("Lean CLAY with sand") | Symbol from field judgement unless lab data confirm or overturn it |
| "TILL - tan, moist…" | "SILTY CLAY TILL - tan, moist, compact…" | Origin named with its matrix; density or consistency added from N or tests (interpretation) |
| "FILL - mix of clay, silt, organics" | "CLAY FILL - mottled…, some organics" | Fill is always called out; man-made inclusions listed (brick, asphalt, glass, wood) |
| Blows "5, 7, 9" | N = 16 in the N column, plotted | N is the sum of the 2nd and 3rd 150 mm increments |
| "50/4\"", "50+" | Refusal notation kept ("50/100 mm"), sometimes an inferred N* clearly marked | Never present a refusal as an ordinary N without saying so |
| Pocket penetrometer "1.75, 2.0, 2.0" (kg/cm²) | Cu or qu in kPa, plotted | qu ≈ reading × 98.1 kPa; Cu ≈ qu/2. State which one the column shows |
| Torvane "T = 0.6" | Cu in kPa, plotted | Unit depends on the vane head; confirm the firm's convention |
| Notes in the margin | Numbered notes under the log ("1. No seepage or sloughing on completion") | Drilling notes at depth may also be kept as depth remarks |
| Water: "through casing 2.6 m 09:15", "on completion 2.8 m, cave 3.1 m" | Water level table with date, time, depth, cave-in, and the stage (during drilling, on completion, stabilised) | Water through casing or with drilling fluid is not a stabilised level |
| Lab moisture, Atterberg, grain size | Plotted, and often a sub-line: "LL=48, PL=20, PI=28 at 2.3 m"; "PSA: 3% gravel, 14% sand…" | Field classification is reconsidered against lab data |
| End of hole written in the description | "END OF BOREHOLE at 6.4 m. Probable refusal on bedrock; spoon bouncing at 6.3 m" or "AUGER REFUSAL AT 5.94 m ON SUSPECTED BOULDER" | The termination reason matters to the designer |
| Method per depth in the header or notes | Method per depth range in the header ("0.00–3.05 m 200 mm HSA; 3.05–7.60 m HQ triple tube") | |
| Logger's initials | "Originated by / Inspector", "Compiled by", "Checked / Approved by", dates | Sign-off fields |
| — | Disclaimer: stratification lines are approximate; transitions may be gradual | Standard on most finals |

**The classic mistake** is overwriting the field description with the lab
classification. Good practice keeps the field observation and adds the lab
evidence, so a reviewer can see where they disagree and judge reliability at each
depth.

## 6. Review and sign-off

A reviewer typically:
1. Reads the final against the field sheet line by line (depths, samples, blows,
   water, termination).
2. Checks internal consistency (description vs N, vs strength tests, vs lab
   results, vs water level) using a checklist like `06`.
3. Compares with neighbouring holes and the expected geology.
4. Marks up the draft (historically in red so changes stay visible), sends it
   back, and re-checks the revision.
5. Signs or initials "checked/approved"; the log moves from DRAFT to final. A
   professional seal, where used, applies to the report, not to each log.

Revisions are tracked: the draft history matters when a dispute or claim later
asks "what was known when".

## 7. What each person needs from software

| Person | Needs |
| --- | --- |
| Logger | Speed, offline use, pick-lists in the firm's vocabulary, prompts for missing items while the sample is still in hand, photos tied to samples, nothing that slows a 20 m/day rig |
| Compiler | Faithful reading of handwriting, S.A.A. handling, unit conversion, merge/split of layers that keeps the original wording, lab results matched to samples, the firm's output template |
| Reviewer | Side-by-side source and final, every value traceable to its source, a short list of real contradictions, depth-pinned comments, a clear record of who changed what and who approved |
| Designer | Correct N, strength, water and rock level, consistent terms across holes, data export (AGS, gINT, CSV) |
