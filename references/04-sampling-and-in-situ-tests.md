# Sampling and in-situ tests

Contents
1. Sample types, codes and quality
2. Recovery
3. Standard Penetration Test (SPT): procedure
4. SPT notation, refusal and odd results
5. SPT corrections (N60, (N1)60)
6. Pocket penetrometer
7. Torvane and field vane
8. Dynamic cone (DCPT / DCP)
9. CPT / CPTu, dilatometer, pressuremeter
10. Hydraulic tests (packer, falling/rising head)
11. A generic field-test record

## 1. Sample types, codes and quality

| Common code(s) | Sample | Quality | Notes |
| --- | --- | --- | --- |
| SS, SB | Split spoon / split barrel (SPT sampler) | Representative but disturbed (area ratio ~110%) | 35 mm ID × 50 mm OD standard; 450 or 610 mm long; 2" and 3" variants |
| ST, U, U(50), U(75), TW | Thin-walled (Shelby) tube, pushed | Undisturbed (best when area ratio < 10% and recovery ratio ≥ 96%) | Clays and silts; not possible in clean sand |
| PS | Piston sampler | High quality in soft soils | |
| D | Disturbed | Low | Auger or wash returns; strata identification only |
| B, BK | Bulk | Low | Large mass for compaction and CBR tests |
| A, AG | Auger grab / auger cuttings | Low; depth uncertain | |
| W, WS | Wash sample | Low; fines washed out | |
| C, R, HQ… | Rock core run | | See `03` |
| MC | Modified California / ring sampler | Driven; semi-undisturbed | Western US practice |
| SC | Sonic core | Continuous, disturbed by vibration | |
| BLK | Block sample | Highest quality | From test pits |
| W (environmental) | Water sample | | |

Codes vary by firm. Always keep the code as written and map it to a canonical
type through the firm's legend.

Containers: bag (B), glass jar (G), tube (T), environmental vials with
preservative. Container affects whether moisture content is meaningful later.

## 2. Recovery

- Recovery is the length of sample in the sampler relative to the length driven
  or pushed; written as a length (often inches) or a percentage.
- Recovery larger than the drive length is a red flag (heave, misread, or the
  sample included fall-in).
- "NR" or 0 means no recovery: describe from cuttings or leave the interval
  undescribed, and say which.
- Low recovery in granular soil, gravel or cobbles is normal; low recovery in
  stiff clay is a question.

## 3. SPT procedure

- 63.5 kg (140 lb) hammer falling 760 mm (30 in) drives the split spoon.
- Blows are counted for three successive 150 mm (6 in) increments. The first is
  the seating drive. N = blows for the 2nd + 3rd increments (300 mm / 12 in).
- A 610 mm (24 in) spoon gives four increments; N is still increments 2 + 3.
- Usually at 0.75–1.5 m intervals and at strata changes.
- The hole base must be clean and, below water, the water or mud level in the
  hole kept at or above the groundwater level; otherwise base heave loosens the
  soil and N comes out falsely low.
- Compare increments: "1, 7, 23" suggests a layer change within the drive or
  loose fall-in in the first increment.
- A solid 60° cone is sometimes used instead of the spoon in gravel or weak rock.
- SPT is not very repeatable: two crews side by side can differ noticeably.

## 4. SPT notation, refusal and odd results

| Written | Meaning |
| --- | --- |
| 3-4-6 or 3/4/6 | Blows per 150 mm increment; N = 10 |
| 3-4-6-8 | Four increments (610 mm spoon); N = 4 + 6 = 10 |
| 50/100 mm, 50/4", 50/5" | 50 blows achieved only that penetration in the increment shown: refusal |
| 12-30/75 mm | Second increment refused after 75 mm |
| 50+ , ">50" | Refusal; penetration not recorded |
| WOH | Spoon advanced under weight of hammer alone (N effectively 0) |
| WOR | Advanced under weight of rods alone |
| HB | Hammer bouncing: refusal on rock or boulder |
| N* or N (inferred) | A value extrapolated from a partial drive; must be labelled as inferred |
| bpf | Blows per foot; some older logs record a single number per 12 in |
| N > 60 | Look: total blows exceeding 60; for soils (N1)60 > 60 usually means cemented sand, coarse gravel, cobbles, boulders or rock |

Refusal criteria differ by standard: ASTM D1586 allows stopping at 50 blows in
any 150 mm increment, 100 blows total, or 10 successive blows with no advance;
the Australian standard ends the test at 30 blows in 100 mm of seating drive;
in rock, more blows are often allowed and both seating and test drives are
recorded. A refusal shorter than the nominal drive is an expected outcome, not
a data error.

Reporting practice for refusals varies: some firms print "50/100 mm", some
print an inferred N, some print both. Whether an inferred N belongs on a
factual log is a long-standing debate; if shown, mark it.

## 5. SPT corrections

- Energy: N60 = N × ER / 60, where ER is the hammer's measured energy ratio in %.
  Automatic hammers often deliver 70–95%; safety hammers about 60%; donut
  hammers less. Many correlations assume 60%.
- Overburden (granular soils): (N1)60 = CN × N60. A common CN = (100 / σ'v in kPa)^0.5,
  capped (often at 1.7 to 2). Not applied to clays.
- Rod length: short rods deliver less energy (factor about 0.75 below 4 m,
  1.0 above 10 m).
- Borehole diameter: 1.0 for 65–115 mm, about 1.05 at 150 mm, 1.15 at 200 mm.
- Sampler: a US sampler without liners about 1.2.
- Fine or silty sand below water with N' > 15: N = 15 + 0.5 (N' − 15).
- Liquefaction work uses clean-sand-equivalent (N1)60cs.

The field log records raw N. Corrected values belong in design calculations or
a clearly labelled column, never in place of the raw blows. Without the hammer
type and energy ratio on record, N60 cannot be computed.

## 6. Pocket penetrometer (PP)

- Spring-loaded 6.35 mm piston pushed into a clay surface; reads unconfined
  compressive strength qu, usually in kg/cm² or tsf (≈ equal numerically).
- Convert: qu (kPa) ≈ reading × 98.1; Cu ≈ qu / 2. So 2.0 kg/cm² ≈ 196 kPa qu ≈
  98 kPa Cu.
- Usually three readings; report the readings or their average and say which.
- Look recommends reporting the PP reading on the log rather than a converted
  Cu, and gives qu ≈ 0.8 PP in general, 1.15 PP in fills, 0.6 PP in fissured
  clays (his correlation).
- Do not use on SPT samples: driving disturbs them (soft clays read stiff, hard
  clays shatter and read stiff). Use on tube samples (ends) or intact lumps.
- Not meaningful in granular or gravelly soils.
- Maximum reading on most instruments is 4.5 kg/cm²; a reading at the limit
  means "≥".

## 7. Torvane and field vane

Torvane (hand vane on a sample face):
- Reads shear strength directly; units depend on the vane head (standard head
  commonly kg/cm²; sensitive and large heads use multipliers; some read t/m² or
  kPa). Confirm the firm's convention before converting: one firm's field
  values matched the final only if read as t/m² (× 9.81 kPa).

Field vane test (FVT, in the borehole or pushed):
- Gives peak Su and remoulded Su (after about 10 revolutions);
  sensitivity St = peak / remoulded.
- Vane strength for a standard H/D = 2 vane: Su = 6 T / (7 π D³).
- Bjerrum's correction reduces vane strength for plastic clays (μ about 1.0 at
  PI < 20%, 0.85 at 40%, 0.75 at 50%, 0.65 at PI ≥ 80%).
- Lab vane may also be reported.

## 8. Dynamic cone (DCPT / DCP)

- A cone driven by a dropped hammer; blows counted per 100 mm or per 300 mm/ft,
  or penetration per blow (mm/blow).
- Many variants (hammer mass, drop, cone size, rods): the Canadian DCPT with a
  standard SPT hammer differs from the light pavement DCP. Record the variant.
- Mainly a profiling tool; correlations to CBR or strength are rough.
- Plotted as a continuous profile beside the SPT column on many finals.

## 9. CPT / CPTu, dilatometer, pressuremeter

| Test | Measurements | Notes |
| --- | --- | --- |
| CPT | qc cone resistance (MPa), fs sleeve friction (kPa), Rf = fs/qc (%) | Electric and mechanical cones interpreted differently; ~100 m/day |
| CPTu (piezocone) | Adds pore pressure u2 (kPa); qt = qc + (1 − a) u2 | a = net area ratio (≈ 0.75–0.82 for 10 cm² cones) |
| SCPTu | Adds shear-wave velocity Vs (m/s) | Seismic site class |
| Dissipation test | u vs time, t50 | Water level and consolidation coefficient |
| DMT (flat dilatometer) | p0, p1 → ID, KD, ED | Best alongside CPT |
| PMT (pressuremeter) | Lift-off, limit pressure pL, modulus EPMT | In-situ deformation |

CPT data arrive as files with readings every 1–5 cm and soil behaviour type
(Robertson SBT); they are not logged by hand and have no samples.

## 10. Hydraulic tests

- Packer (Lugeon) test in rock: water pressed into a sealed interval at several
  pressure stages; result in Lugeon units and hydraulic conductivity K (m/s).
- Rising/falling head (slug) tests in wells or the open hole: K (m/s).
- Pumping tests on wells: drawdown vs time, transmissivity.

## 11. A generic field-test record

Most of the tests above fit one record shape, which makes adding a new test a new
type rather than a new table:

| Field | Example |
| --- | --- |
| Test type | pocket_penetrometer, torvane, field_vane, dcpt, pid_headspace… |
| Depth or depth range | 2.13 m, or 4.5–5.0 m |
| Sample link (optional) | ST-2 |
| Readings as written | "2.5, 2.25, 2.0" |
| Unit as written | kg/cm² |
| Instrument variant | standard head / sensitive head; DCPT variant |
| Derived value and unit | Cu = 110 kPa |
| Derivation rule and its source | qu = reading × 98.1; Cu = qu/2 (firm setting) |
| Raw text | "PP=2.5,2.25,2.0@7'" |
