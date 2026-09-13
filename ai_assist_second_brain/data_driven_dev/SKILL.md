---
name: data-driven-skill-methodology
description: Build high-accuracy skills grounded in real operational data. Use when creating a new skill that involves pricing, estimation, quoting, forecasting, resource allocation, or any process where the user has historical data (CSVs, billing records, CRM exports, project logs) that should inform the skill's rules and validation. Also use when the user says 'build a skill from my data,' 'turn this into a process,' 'create a system from our records,' 'make this repeatable,' or wants to formalize any data-backed workflow into a reliable, self-improving skill.
---

# Data-Driven Skill Methodology

Build skills where every rule has provenance, every default comes from frequency analysis, and every validation check exists because an error actually happened.

## The 7 Phases

Execute in order. Each phase produces a specific deliverable that the next phase depends on.

### Phase 1: Export Real Data

Extract granular records from the system of record. Get individual line items, not summaries. Aim for 100+ records minimum. Export two views when possible:
- **Structural** — what each record is made of (line items, components)
- **Temporal** — when records occurred (for trends, seasonality)

Document exports: row count, columns, date range, source system. Store as CSVs in `data/` with a parsing guide.

**Deliverable:** Raw data exports + `data/data-guide.md`

### Phase 2: Reverse-Engineer the Source of Truth

Analyze the data to derive real rules. Do not copy existing documentation — validate it against reality.

1. **Frequency analysis** — count every value. Most common = default. Sort by occurrence.
2. **Gap detection** — compare data against existing docs. Find undocumented-but-real values and documented-but-unused values.
3. **Tier discovery** — name natural clusters in the data. If prices cluster at 4 points, those are 4 tiers.
4. **Default identification** — the most frequent value per category is the default. Document why.

**Deliverable:** `source-of-truth.md` — authoritative reference with version history. Explicitly states it overrides all other sources.

### Phase 3: Cluster Into Archetypes

Group records by composition into named categories. For each archetype:
- Count and % of total
- Value range (min, median, max)
- Typical composition (which components, what quantities)
- 2-3 named real examples

Every record must map to exactly one archetype. If records fall between categories, refine.

**Deliverable:** `archetypes.md` — benchmarks, co-occurrence patterns, size distribution

### Phase 4: Build and Break

Use the skill on real past inputs. When errors occur:

1. Document: date, wrong output, root cause, prevention rule
2. Add prevention rule to the relevant validation section
3. Tag with `[ADDED <date>]`
4. Optionally add a few-shot example showing the catch

The error log is append-only. It is the skill's immune system.

**Deliverable:** `validation-rules.md` with error log table

### Phase 5: Design Multi-Gate Validation

Three gates positioned at different points in the workflow:

**Gate 1 — Pre-Processing (before any calculations):**
- [ ] All inputs complete and unambiguous
- [ ] Every input maps to a required resource
- [ ] No orphaned components
- [ ] Quantities are exact, not ranges

**Gate 2 — Post-Processing (after output, before presenting):**
- [ ] All math verified row by row
- [ ] Totals reconcile
- [ ] Required components present
- [ ] Forbidden components absent

**Gate 3 — Historical (after Gates 1-2 pass):**
- [ ] Archetype identified
- [ ] Total within historical range
- [ ] Proportions within norms
- [ ] 2-3 comparable past records identified
- [ ] Deviations >30% flagged with reasoning

Write gates as checkbox lists. Checkboxes prevent skipping.

**Deliverable:** Three gate checklists integrated into the skill's process steps

### Phase 6: Write Few-Shot Examples

Four minimum example types:

| Type | Demonstrates |
|---|---|
| **Happy path** | Correct end-to-end execution with reasoning |
| **Ambiguous input** | When to stop and ask, what NOT to assume |
| **Complex case** | Scale, edge conditions, compounding decisions |
| **Validation catch** | Skill REFUSING to proceed — the most important example |

Include reasoning (not just input/output). Use real data. The validation catch example should show a realistic, subtle error and the exact pushback language.

**Deliverable:** `examples.md` with 4+ calibration examples

### Phase 7: Design for Evolution

Ensure the skill improves with every use:

- **Error log** — append-only, dated entries
- **`[ADDED <date>]` tags** — traceable rule additions
- **Version history** — on the source of truth document
- **Raw data preserved** — alongside processed references, enabling re-analysis
- **Separation of concerns** — five distinct files, each changing for different reasons

The flywheel: Use skill -> catch error -> add rule -> update examples -> skill gets smarter

**Deliverable:** Complete file architecture per `references/file-architecture.md`

## File Architecture

```
skill-name/
├── SKILL.md                 # Process + workflow (you are here)
├── source-of-truth.md       # Rates, prices, rules (single authority)
├── archetypes.md            # Historical benchmarks + record types
├── examples.md              # 4+ calibration examples
├── validation-rules.md      # Living doc with error log
├── references/              # Supplementary material
└── data/                    # Raw exports + parsing guide
```

For complete architecture guidance: read `references/file-architecture.md`
For detailed phase instructions: read `references/methodology.md`

## Non-Negotiable Principles

1. **Every rule has provenance.** No rule exists because it "seems right." Every rule traces to data or a caught error.
2. **Frequency determines defaults.** The most common value wins, not the value someone wrote in a doc years ago.
3. **Errors become antibodies.** Every caught mistake is logged, tagged, and converted to a prevention check.
4. **Checkboxes, not prose.** Validation gates use checkbox lists. You cannot skim past a checklist.
5. **The source of truth wins.** If any file conflicts with the source of truth document, defer to the source of truth.
6. **Stop when uncertain.** If an input is ambiguous, stop and ask. Never guess quantities, durations, or scope.
7. **Validate against history.** Every output gets compared against real past records before presentation.
