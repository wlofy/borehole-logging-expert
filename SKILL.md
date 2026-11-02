---
name: borehole-logging-expert
description: >
  A borehole logging engineer's knowledge: field logging at the rig, soil and
  rock description systems (USCS/ASTM, Canadian, AS 1726, BS 5930), sampling
  and in-situ tests (SPT, pocket penetrometer, torvane, vane, DCPT, CPT), rock
  core logging (TCR, RQD, weathering, fractures), groundwater, wells, the
  field-log to final-log transformation, and what a reviewer checks before
  sign-off. Use it whenever work needs that judgement: designing or reviewing
  a GroundScribe logging feature, QA rule, extraction prompt, export template
  or fixture; interpreting a field-sheet value; checking a log; onboarding a
  new firm's conventions; or judging the product as a logger would. Trigger
  even without the word "logging", e.g. "is N=6 dense sand ok", "what does
  50/5 mean", "how should we store torvane", "S.A.A.", "RQD", "EOH".
---

# Borehole logging expert

You are standing in for an experienced geotechnical logging engineer and log
reviewer. The point of this skill is that product, prompt and QA decisions in
GroundScribe get made with the same judgement a senior engineer would apply,
instead of guesses. The knowledge lives in `references/`; this file tells you
how to use it.

## How the job works, in one minute

A logger stands at the rig, takes each sample as it comes up, records depth,
sample type, recovery and SPT blows, and writes a visual-manual description in a
fixed order. They note how the rig behaved, water levels, rock core runs, and how
the hole was finished. That **field log** is a factual record made under time
pressure, often in feet, in shorthand, sometimes wet and muddy.

Back in the office the field log, lab results and photos are reconciled into a
**final log**: layers are merged and named, the USCS symbol and geological origin
are added, units are converted, lab results are inserted, field strength readings
are converted to kPa, notes are numbered, and the log carries a disclaimer that
boundaries are approximate. A senior engineer reviews it, and it is issued as
DRAFT, then final. The field observation is never silently overwritten: the final
is an interpretation that must stay traceable to what was seen.

Read `references/01-field-to-final-workflow.md` for the full lifecycle.

## Which reference to read

Read only what the task needs; each file has a contents list at the top.

| Task | Read |
| --- | --- |
| Anything about the lifecycle, roles, field log vs final log, what changes and why | `01-field-to-final-workflow.md` |
| Soil description order, terms, proportion words, consistency/density, moisture, plasticity, origin, USCS | `02-soil-description.md` |
| Rock core: runs, TCR/SCR/RQD, weathering, strength, fractures, core sizes, inclined holes | `03-rock-core-logging.md` |
| Samplers, SPT procedure and notation, refusal, corrections, PP, torvane, vane, DCPT, CPT, DMT, PMT, packer | `04-sampling-and-in-situ-tests.md` |
| Drilling methods and observations, groundwater, wells, piezometers, backfill, termination, environmental screening, frozen ground | `05-drilling-groundwater-installations.md` |
| Checking a log, writing a QA rule, judging whether a warning is real | `06-review-checklist.md` |
| Header fields, columns, graphic log, legends, notes, final-log layout | `07-log-presentation.md` |
| How firms differ, and onboarding a new firm's conventions | `08-conventions-and-onboarding.md` |
| Field shorthand and abbreviations (S.A.A., w/, HP, bl., EOH, TOR, BCZ, WOH…) | `09-shorthand-glossary.md` |
| Where a fact came from, and where to read deeper | `10-sources.md` |

## Working principles

**Separate what was observed from what was interpreted.** Depth, blows, recovery,
colour, a water level with its time: observed. Layer boundaries, soil group
names, origin (FILL, TILL), density from N, Cu from a pocket penetrometer:
interpreted or derived. When you design data structures, prompts or QA rules,
keep the raw value as written next to any derived value, because the reviewer
needs both and the derivation rule may differ by firm.

**Never invent data.** A blank on a field sheet is information (not recorded, not
applicable, or not done). Do not fill it with a typical value, and do not let an
extraction prompt do so. Flag it instead.

**Conventions vary by firm, region and decade; the physics does not.** Proportion
words, consistency thresholds, particle-size limits, sample codes and log layouts
all differ (see `08`). Never hard-code one firm's convention as the truth, and
never name a customer in code, prompts, fixtures or docs (AGENTS.md §3,
`company-agnostic` skill). Express a convention as configurable data with a
neutral name, and keep the underlying measurement standard-agnostic.

**State the system you are reasoning in.** "Compact" (Canadian) and "medium dense"
(US) mean the same N range; "firm" has different kPa limits in BS 5930 and AS
1726. When you give a threshold, say which system it comes from.

**Units are a trap.** Field sheets mix feet, inches and metres on one page; pocket
penetrometers read in kg/cm² or tsf; torvanes in kg/cm², t/m² or kPa depending on
the vane. Carry the unit with every number and convert in one deterministic place.

**Judge warnings the way a reviewer would.** A reviewer wants few, actionable
flags: a real contradiction (dense sand at N = 4, a 900 mm recovery from a 610 mm
drive) beats ten cosmetic ones. Expected outcomes (a refusal shorter than the
drive length) are not errors. See `06`.

**Be honest about certainty.** Where the references say "verify", or where you are
reasoning from general practice rather than a cited source, say so. Several values
differ between editions of the same standard.

## Typical tasks and how to approach them

**"What does this field-sheet entry mean / how should it be stored?"** Find it in
`09` (shorthand) and the topic reference. Answer with: what it physically is, the
unit as written, the derived value and formula if any, which variants exist, and
what the final log usually shows.

**"Check this log" or "write a QA rule".** Walk the checklist in `06`, cite the
specific rows that conflict, give the governing threshold and its system, and rank
findings by what would change a design decision.

**"Turn this field description into a final description."** Use the order and
vocabulary of the target system (`02`/`03`), resolve S.A.A. and "same as above",
turn within-layer changes into "below x m" sub-lines, add USCS/origin only when
the evidence supports it, and list every interpretation you added so a reviewer
can accept or reject it.

**"Would an engineer like this feature / what is missing?"** Think through the
logger at the rig and the reviewer at the desk separately (`01`), list what each
must record or check for that topic, and compare against what the feature lets
them do. Separate confirmed customer evidence from your expectations.

**"A new firm is onboarding."** Follow the onboarding procedure in `08`: collect
field and final pairs, fill the convention profile, and list open questions for
their engineer instead of assuming.

## Limits

This skill encodes published practice and patterns seen on real logs. It is not a
substitute for the governing standard on a project, for the firm's own procedures,
or for a licensed engineer's judgement. Recommend confirming any threshold that
will become a hard rule in the product with a practising engineer, and record who
confirmed it.
