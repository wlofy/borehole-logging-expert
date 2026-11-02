# Soil description

Contents
1. Description order by system
2. Particle sizes by system
3. Proportion words (secondary constituents)
4. USCS group symbols and group names
5. Consistency of fine-grained soils
6. Relative density of coarse-grained soils
7. Moisture condition
8. Plasticity and field identification tests
9. Colour
10. Structure and fabric
11. Origin and geological unit
12. Inclusions, organics, fill and contamination indicators
13. Field vs laboratory classification
14. Worked examples

Values marked "verify" are from general practice or differ between editions;
confirm against the governing standard before turning them into product rules.

## 1. Description order by system

The point of a fixed order is that nothing gets skipped and every log reads the
same. The order differs by system and by firm.

| System | Typical order |
| --- | --- |
| ASTM D2488 / USCS (US practice) | Group name in capitals (e.g. "Lean CLAY with sand") and group symbol (CL); then colour, moisture, consistency or density, plasticity, structure, cementation, particle angularity and shape, maximum particle size, odour, HCl reaction, additional comments; origin often prefixed (FILL, ALLUVIUM) |
| Canadian practice (CFEM-style, Ontario MTO-style, many Canadian consultancies) | Main constituent in capitals with proportion words ("SAND, some silt, trace gravel"), then density/consistency, colour, moisture; USCS symbol added in brackets on many finals ("CLAY (CH)"); origin prefixed ("SILTY CLAY TILL", "FILL") |
| One Canadian firm's printed field checklist | Plastic soil: colour, moisture, consistency, plasticity, misc (organics, coarse material, oxidation, structures). Granular soil: colour, moisture, density, gradation, grain size, misc (fines, oxidation, depositional structures) |
| AS 1726 (Australia), as summarised in Look's handbook | Soil type, USC symbol, colour, plasticity/particle description, structure, consistency, moisture, origin; water level alongside |
| BS 5930 / ISO 14688 (UK, international) | Consistency or density, bedding/structure, colour, composite soil type with secondary constituents as adjectives ("Firm thinly laminated grey slightly sandy CLAY"), then additional information, then geological unit in brackets or capitals (verify exact 2015 wording) |

GroundScribe practice notes:
- The app's description arranger currently orders: material and modifiers,
  colour, consistency/density, moisture. That matches common Canadian finals.
- Engineers expect the main soil name in capitals and modifiers in ordinary case.
- Do not infer missing properties when re-ordering; re-ordering must preserve
  wording and meaning.

## 2. Particle sizes by system

| Fraction | USCS / ASTM | Canadian legend seen on field sheets | AS 1726 / BS / ISO |
| --- | --- | --- | --- |
| Boulders | > 300 mm | > 200 mm | > 200 mm (ISO: large boulders > 630 mm) |
| Cobbles | 75–300 mm | 75–200 mm | 60/63–200 mm |
| Coarse gravel | 19–75 mm | 19–75 mm | 20–60/63 mm |
| Medium gravel | — | — | 6–20 mm |
| Fine gravel | 4.75–19 mm (No. 4 sieve) | 4.75–19 mm | 2–6 mm |
| Coarse sand | 2–4.75 mm | 2–4.75 mm | 0.6–2 mm |
| Medium sand | 0.425–2 mm | 0.425–2 mm | 0.2–0.6 mm |
| Fine sand | 0.075–0.425 mm | 0.075–0.425 mm | 0.06/0.075–0.2 mm |
| Fines (silt + clay) | < 0.075 mm (No. 200) | < 0.075 mm | < 0.06 or 0.075 mm |
| Silt / clay split | by plasticity, not size, in USCS | — | 0.002 mm by size (BS/ISO) |

Consequence: "coarse sand" in one system is not the same size range as in another,
so never compare a description to a lab curve without knowing the system.

## 3. Proportion words for secondary constituents

| System | Terms |
| --- | --- |
| ASTM D2488 (by estimated %) | trace < 5%, few 5–10%, little 15–25%, some 30–45%, mostly 50–100% |
| Burmister (older US practice) | trace 0–10%, little 10–20%, some 20–35%, and 35–50% |
| Canadian (CFEM-style) | trace 1–10%, some 10–20%, adjective form ("silty", "sandy") 20–35%, "and" 35–50% |
| One Canadian firm's printed key | trace 0–10%, some 10–20%, with 25–35%, and 35–50% (note the 20–25% gap on the printed key) |
| ASTM group names (USCS) | "with sand" / "with gravel" when 15–29% (fine soils) or ≥ 15% (coarse soils); "sandy"/"gravelly" when ≥ 30% (verify against D2487 flowcharts) |
| BS 5930 / ISO 14688 | "slightly", unqualified adjective, "very" for secondary fractions; thresholds differ for fine vs coarse principal soils (verify) |

Common shorthand: "w/" = with, "tr" = trace, "sm" or "so" = some, "&" = and.

These are the biggest source of firm-to-firm difference. Treat them as a
per-organisation setting, never a constant.

## 4. USCS group symbols and group names

| Symbol | Meaning |
| --- | --- |
| GW, GP | Well / poorly graded gravel (< 5% fines) |
| GM, GC | Silty / clayey gravel (> 12% fines) |
| SW, SP | Well / poorly graded sand (< 5% fines) |
| SM, SC | Silty / clayey sand (> 12% fines) |
| GW-GM, SP-SM etc. | Dual symbols for 5–12% fines |
| ML, CL | Silt / lean clay (LL < 50) |
| MH, CH | Elastic silt / fat clay (LL ≥ 50) |
| CL-ML | Silty clay (PI 4–7, above the A-line) |
| OL, OH | Organic silt or clay |
| PT | Peat (highly organic) |

Grading: well graded needs Cu ≥ 4 (gravel) or ≥ 6 (sand) and 1 ≤ Cc ≤ 3 (ASTM).
Look's handbook gives a simpler AS-style rule: uniform if U < 5; well graded if
U > 5 and C between 1 and 3. Cu = D60/D10, Cc = D30²/(D60·D10).

Some systems use CI / MI for intermediate plasticity (LL 35–50) instead of L/H.

ASTM group names are formal: "Lean CLAY with sand", "Sandy lean CLAY", "Poorly
graded SAND with silt". Canadian finals more often write "CLAY (CL), some sand".

Without lab confirmation, a field classification is an opinion. Borderline cases
(silty sand vs sandy silt, CL vs CH) need lab tests.

## 5. Consistency of fine-grained soils

Field feel and approximate undrained shear strength:

| Term | Field feel (AS 1726 style, from Look) | Su, AS 1726 and CFEM-style (kPa) | Su, BS 5930:2015 terms (kPa, verify) | SPT N (rough, see note) |
| --- | --- | --- | --- | --- |
| Very soft | Exudes between fingers when squeezed | < 12 | < 10 extremely low/very soft | ≤ 2 |
| Soft | Moulded by light finger pressure | 12–25 | 10–20 | 2–4 or 2–5 |
| Firm | Moulded by strong finger pressure | 25–50 | 20–40 | 4–8 or 5–10 |
| Stiff | Cannot be moulded by fingers; indented by thumb | 50–100 | 40–75 | 8–15 or 10–20 |
| Very stiff | Indented by thumbnail | 100–200 | 75–150 | 15–30 or 20–40 |
| Hard | Difficult to indent by thumbnail | > 200 | > 150 | > 30 or > 40 |

Notes:
- The N column is a crude correlation (Terzaghi–Peck style ranges, and Look's
  Table 5.3 ranges in the second figure). Cu/N ratios in the literature run from
  about 2 to 8 kPa per blow, and up to 15 for low-plasticity clays. Never use N
  alone to overrule a measured strength; use it to flag a contradiction.
- US practice sometimes uses "medium" instead of "firm".
- Above about 500 kPa the material may be a very weak claystone or mudstone.
- Fissured clay can have about two-thirds of the design strength of intact clay,
  which is why structure matters.

## 6. Relative density of coarse-grained soils

| Term (Canada) | Term (US / AS) | SPT N (uncorrected, first approximation) | Density index Dr (%) | Field feel (from Look) |
| --- | --- | --- | --- | --- |
| Very loose | Very loose | < 4 | < 15 | 50 mm peg driven easily |
| Loose | Loose | 4–10 | 15–35 | 12 mm bar pushed by hand |
| Compact | Medium dense | 10–30 | 35–65 | 12 mm bar needs a hammer for > 200 mm |
| Dense | Dense | 30–50 | 65–85 | 12 mm bar hammered < 200 mm |
| Very dense | Very dense | > 50 | > 85 | 12 mm bar hammered < 60 mm |
| (Cemented) | (Cemented) | > 50 | n/a | Look adds this as an extension |

Notes:
- The table assumes medium sand; finer or coarser materials and overburden
  change the relationship. Design uses corrected values (`04`).
- Gravel, cobbles and boulders inflate N; a high N in gravelly soil is not
  automatically "very dense".
- "Compact" is the Canadian word for medium dense; a description saying
  "compact" is not a typo.

## 7. Moisture condition

| Term | Fine-grained | Coarse-grained |
| --- | --- | --- |
| Dry | Hard, friable or powdery | Runs freely through the hands |
| Moist (damp) | Feels cool, darker colour, can be moulded | Tends to cohere |
| Wet | Free water forms on the hands when handled | Tends to cohere; free water visible |
| Saturated / very wet | Used by some firms for coarse soils below water | |

Some firms express moisture relative to the plastic limit (w < PL, w ≈ PL,
w > PL). Look warns this introduces two error sources in one judgement.

Moisture is separate from the water level. A soil can be logged wet above the
water table (perched water, drilling water) and dry below it (low-permeability
clay). The logger must distinguish natural moisture from moisture added by wash
boring or drilling fluid.

## 8. Plasticity and field identification tests

| Term | Field behaviour |
| --- | --- |
| Non-plastic | Falls apart; cannot roll a thread |
| Low plasticity | Cannot be rolled into a 3 mm thread when moist (AS style) or thread barely formed |
| Medium | Rolls into threads; some shrinkage on drying |
| High | Rolls easily; considerable shrinkage, cracks when dry, greasy feel |

ASTM D2488 field tests for fines: dry strength (none to very high), dilatancy
(none, slow, rapid), toughness (low to high), plasticity (non-plastic to high).
Silt: rapid dilatancy, low dry strength. Clay: no dilatancy, medium to high dry
strength and toughness.

A quick sedimentation (jar) test separates coarse sand (settles in about a
second), fine sand (about 10 s), silt (minutes) and clay (hours).

Atterberg limits are run on the fraction passing 0.425 mm; report the percentage
passing, because a "high PI" on a rock-like material where 90% was discarded is
misleading.

## 9. Colour

Order of words: tone (light, dark, mottled), shade (reddish, greyish…), hue
(brown, grey…), and distribution (uniform, mottled, streaked, banded).
Examples: "dark greyish brown", "mottled brown and grey". Some clients require
Munsell codes. Describe moist colour where possible; note oxidation (orange,
rust) because it marks the zone of water-table fluctuation. Colour changes with
drying, so a colour seen on site may differ from the lab.

## 10. Structure and fabric

| Term | Meaning |
| --- | --- |
| Homogeneous | Essentially one material |
| Heterogeneous | Mixture of types |
| Interbedded / interlaminated / layered / varved | Alternating layers; varved = annual glaciolacustrine couplets |
| Laminated | Layers < 6 mm (thin) or < 20 mm depending on system |
| Lensed / pockets | Inclusions of another soil ("pockets of grey clay", "sand lenses") |
| Fissured | Breaks along definite planes; reduces mass strength |
| Slickensided | Polished, striated fissure surfaces from movement |
| Blocky | Breaks into hard lumps |
| Fibrous / amorphous | Peat: plant remains visible / not visible |
| Cemented | Particles bonded |
| Relict structure | Residual soil keeping parent-rock structure |

## 11. Origin and geological unit

| Origin | What to expect |
| --- | --- |
| Fill (made ground) | Placed by people; heterogeneous; may contain brick, concrete, asphalt, glass, wood, metal, ash, plastic. Always named as FILL |
| Topsoil | Organic surface layer, rootlets |
| Alluvial | Water-laid; stratified; rounded gravel |
| Lacustrine / glaciolacustrine | Lake deposits; laminated or varved silts and clays |
| Glacial till | Ice-deposited; broad grading from clay to boulders; angular to subrounded clasts; often dense or hard; cobbles and boulders cause refusals. Final logs name the matrix: "SILTY CLAY TILL", "SANDY SILT TILL" |
| Outwash | Glaciofluvial sands and gravels |
| Colluvial | Gravity-moved slope debris; heterogeneous |
| Aeolian | Wind-blown; very uniform silt or fine sand (loess) |
| Residual / saprolite | Rock weathered in place; may keep relict structure; grades into extremely weathered rock |
| Organic / peat | Grown in place; dark; very compressible |
| Marine | Possibly sensitive clays (e.g. Champlain Sea clay in eastern Canada) |
| Volcanic | Ash, pumice; can weather to expansive clay |
| Evaporite | Hard crusts in arid regions; gypsum |

Origin is an interpretation. It comes from texture, structure, position and
geological maps, and is usually added or confirmed on the final.

## 12. Inclusions, organics, fill and contamination indicators

Record: rootlets, organics, shells, wood, gypsum nodules or crystals,
oxidation, mottling, calcareous reaction (HCl), cobbles and boulders (estimated
by volume), man-made debris. On environmental or brownfield jobs also record
odour (hydrocarbon, sulphur), staining, sheen, and PID or headspace readings
(ppm). Odour and staining are observations; contamination is an interpretation.

## 13. Field vs laboratory classification

- Field classification is visual-manual (ASTM D2488 or equivalent). Lab
  classification (ASTM D2487) uses grain size and Atterberg limits.
- Where they disagree, a reviewer looks for the reason: wrong sample, sample
  disturbance or drying, fines washed out, field misjudgement, or a layer
  boundary inside the sample.
- The final usually adopts the lab classification for that sample and may
  re-describe the layer, but keeps the field observation traceable.
- A single lab result represents a sample, not a whole layer.

## 14. Worked examples

(Invented examples that follow patterns seen on real logs.)

Field sheet: `CLAY - DK BROWN, MOIST, FIRM TO STIFF, HP, TRACE SILT, TRACE ORGANICS`
Canadian-style final: `CLAY (CH) - Dark brown, moist, firm to stiff, high plasticity, trace silt, trace organics.`
Changes: symbol added from plasticity and later lab data; "DK" and "HP" expanded;
casing normalised.

Field sheet: `Sandy gravel, some silt, grey, moist` at 0–1.2 m, `S.A.A.` below,
"cobble, moved to casing" noted at 0.9 m.
Final: `FILL - Sandy gravel, some silt, grey, moist` with a remark at 0.90 m
"Cobble encountered; advanced casing". The FILL label is an interpretation the
reviewer must agree with.

ASTM style: `Lean CLAY with sand (CL): olive grey, moist, stiff, medium plasticity, no dilatancy, ~20% fine sand.`
BS style (verify wording): `Firm grey slightly sandy CLAY with rare fine gravel. (GLACIAL TILL)`
