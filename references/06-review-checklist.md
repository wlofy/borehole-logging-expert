# What a reviewer checks

Contents
1. How reviewers think about findings
2. Depth and geometry checks
3. Sample and SPT checks
4. Description consistency checks
5. Strength and lab checks
6. Groundwater checks
7. Rock checks
8. Header, completion and presentation checks
9. Things that are NOT errors
10. Turning a check into a product QA rule

## 1. How reviewers think about findings

Rank by what could change a design decision or embarrass the firm:
1. **Critical**: wrong or missing water level, a soft or loose layer described as
   strong (or the reverse), wrong depth or termination, rock level claimed
   without proof, a sample or result attached to the wrong depth or hole.
2. **Major**: contradictions between description and tests; missing required
   fields; refusal or N presented misleadingly; field and lab classification
   disagreeing without comment.
3. **Minor**: wording, order, casing, abbreviations, legend gaps.

Reviewers want few, specific, actionable findings. Ten cosmetic warnings bury the
one that matters; group repeats ("3 refusals shorter than drive length:
expected") and lead with critical items.

## 2. Depth and geometry

| Check | Flag when |
| --- | --- |
| Continuity | Gaps or overlaps between layers; the first layer does not start at 0 (unless hydrovac/daylighted or pre-drilled, which should be stated) |
| Range direction | A from–to with from ≥ to (e.g. "band from 4.35 m to 4.20 m"; this kind of slip appears on real issued finals) |
| Bottom | Last layer bottom ≠ end-of-hole depth; samples or tests below EOH |
| Units | Feet and metres mixed; inches read as feet or metres; a depth with a foot mark treated as metres |
| Decimal slips | A layer or run that swallows the next one ("0–94" for 0–0.94); an implausible hole depth |
| Inclined holes | Elevations computed as vertical when the hole is inclined |
| Elevation | Elevation column inconsistent with ground elevation minus depth |

## 3. Samples and SPT

| Check | Flag when |
| --- | --- |
| Sample in a described layer | A sample depth falls in an undescribed interval or gap |
| Recovery | Recovery > drive or push length; recovery missing on a driven sample; high recovery claimed in material that rarely recovers (clean gravel) worth a second look |
| SPT arithmetic | N ≠ 2nd + 3rd increments; N recorded with fewer than three increments and no refusal |
| SPT increment pattern | Strongly increasing first increment vs rest (fall-in or boundary) without a remark |
| Refusal labelling | A refusal presented as a plain N; an inferred N not marked as inferred |
| SPT on a non-SPT sample | Blows on a Shelby tube or core sample type |
| Duplicates | Duplicate sample IDs in a hole; same depth with two different IDs |
| Below water | Very low N in sand below water with wash boring and no note on base heave |
| Sampling interval | Long unsampled intervals without explanation |

## 4. Description consistency

| Check | Flag when |
| --- | --- |
| Density vs N (coarse soils) | Term outside its N band by a clear margin, e.g. "dense" with N < 20, "loose" with N > 15 (use the firm's system; allow for gravel inflating N) |
| Consistency vs N (fine soils) | "soft" with N > 10, "hard" with N < 10; weaker check than strength tests |
| Consistency vs measured strength | Term contradicts PP, torvane or vane Cu band (`02` §5) |
| Moisture vs water | "dry" well below a measured stabilised water level in granular soil; "wet" with no water and no drilling fluid; drilling-water effects not noted |
| Name vs symbol | "CLAY" with symbol SM; "lean" with LL ≥ 50; dual symbol without 5–12% fines |
| Missing order items | Required items for the firm's system absent (colour, moisture, density/consistency, plasticity for fines) |
| Fill identification | Man-made inclusions described but layer not called FILL, or FILL with no basis |
| S.A.A. unresolved | "S.A.A." left in a final, or pointing at nothing |
| Within-layer changes | Changes present on the field sheet but dropped from the final |
| Origin claims | TILL, ALLUVIUM etc. with nothing supporting it |
| Cross-hole | The same unit named differently in adjacent holes |

## 5. Strength and lab

| Check | Flag when |
| --- | --- |
| PP on SPT samples | Pocket penetrometer values on split-spoon samples (Look: meaningless on driven samples) |
| PP in granular soil | PP readings on sand or gravel |
| Unit conversion | PP or torvane plotted without a stated unit or with an impossible magnitude |
| Field vs lab class | Field USCS disagrees with lab-derived class and no comment or revision |
| Atterberg sanity | PL > LL; PI ≠ LL − PL; non-plastic with LL/PL values; PI recorded on a "rock" sample with very little passing 0.425 mm |
| Grain size sanity | Percentages not summing to ~100; "clay" description with 80% sand |
| Moisture content | Natural w far above LL in a "stiff" clay; w outside plausible range (warn, not error: peats and organics can exceed 100%) |
| Lab-to-sample match | Lab result depth outside the sample interval; sample ID conflict |

## 6. Groundwater

| Check | Flag when |
| --- | --- |
| Stage stated | Water depth without date, time or stage |
| Drilling fluid | A "groundwater level" taken with mud or wash water in the hole presented as stabilised |
| Status conflict | "Dry" with a depth; "not observed" alongside a measured level at the same stage |
| Cave-in vs water | Cave-in above the water level without comment |
| Well screen | Well reading reported without screen interval |
| Plausibility | Water level contradicted by moisture descriptions and neighbouring holes |

## 7. Rock

| Check | Flag when |
| --- | --- |
| Recovery order | RQD > TCR, SCR > TCR, TCR > 100% |
| Run geometry | Runs overlap, leave gaps, or exceed typical length without note |
| RQD basis | RQD computed with mechanical breaks counted; denominator not the run (or unit) length |
| Top of rock | Rock called from refusal alone; no proving core length |
| Weathering vs strength | "Fresh, extremely weak" or "completely weathered, very strong" without explanation |
| Fracture codes | Unknown codes; natural vs mechanical not distinguished |
| Orientation | Angles stated without saying "to core axis" or "dip" |

## 8. Header, completion, presentation

- Hole ID, project, location, coordinates and datum, ground elevation, dates,
  drilling contractor and method(s), hammer type, logger, reviewer.
- Termination depth and reason; backfill; installation details.
- Legend for symbols and abbreviations used.
- Disclaimer on approximate boundaries.
- DRAFT status shown until sign-off; reviewer identity recorded.
- Sheet numbering ("1 of 2") complete; no missing page.

## 9. Things that are NOT errors

Do not flag these as problems (at most, an informational note):
- A refusal penetration shorter than the nominal drive length.
- "Compact" (Canadian) instead of "medium dense".
- No groundwater recorded in a hole that was explicitly dry or not observed.
- Low recovery in gravel, cobbles or fill.
- Moisture content > 100% in peat or organic soil.
- Different descriptions in adjacent holes where geology plausibly changes.
- A gap at the top of the hole cleared by hydrovac, when stated.
- High N in gravel or till with a "compact" description, when gravel inflation
  is noted.

## 10. Turning a check into a product QA rule

For each rule decide and write down:
- Which system's thresholds it uses, and that thresholds are configurable per
  organisation.
- Severity (blocks finalisation vs warns vs informs) using §1.
- Its message in plain engineering language with a next action (AGENTS.md §3,
  `geotech-error-copy` skill): what conflicts, at what depth, and what to check.
- How it groups repeats so one cause produces one card.
- Who confirmed the threshold (a practising engineer) and when.
