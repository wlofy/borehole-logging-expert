# borehole-logging-expert

A Claude skill that gives Claude a geotechnical borehole logging engineer's
knowledge. It covers field logging at the rig, soil and rock description, sampling
and in-situ tests, rock core logging, groundwater and wells, how a field log
becomes a final log, and what a reviewer checks before sign-off.

## Install

Claude Code, for one person:

```bash
git clone https://github.com/wlofy/borehole-logging-expert ~/.claude/skills/borehole-logging-expert
```

Claude Code, in a project: copy this folder into the project's `.claude/skills/`
(or `.agents/skills/`) folder and commit it.

claude.ai: an organisation admin zips this folder and uploads it as a skill.

## Contents

- `SKILL.md`: when to use the skill and how
- `references/`: ten topic files that Claude reads when needed
- `evals/evals.json`: test prompts with pass/fail checks

## Limits

The skill paraphrases published practice and cites the original sources in
`references/10-sources.md`. It contains no client data. Have a practising engineer
confirm any threshold before it becomes a hard rule in a product.
