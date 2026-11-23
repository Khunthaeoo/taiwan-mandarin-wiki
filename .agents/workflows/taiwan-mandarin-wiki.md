# Taiwan Mandarin Wiki Graph Workflow

## Rules

- Discuss first; generate later. The user must approve the teaching outline before full Wiki drafting or slide creation.
- Save each stage's inputs and outputs separately so stages can be inspected and rerun.
- Each correction loop allows at most **three correction rounds**. If issues remain, report them and stop that branch; never silently pass it.
- Do not invent sources, evidence, findings, or run records. Do not equate A1–C1 with TOCFL levels without reliable evidence.

## Graph

```text
G0 Scope and level map
  → G1 Source collection
  → G2 Evidence cards
  → G3 Coverage gate ── fail → G1 (coverage loop, max 3 returns)
  → G4 Teaching outline
  → G5 User approval ── changes requested → G4
  → G6 Wiki drafting
  → G7 Content checks
  → G8 Independent source review
  → G9 Corrections and re-review (max 3 rounds)
  → G10 Slide generation
  → G11 HTML rendering checks
  → G12 Ready for handoff
```

Any loop that still fails after round three ends with an unresolved-issues report; affected work is not marked ready. Scope changes or proposed exceptions to a failed coverage gate require user approval.

## Nodes and artifacts

| Node | Purpose | Separate output |
|---|---|---|
| G0 | Define five project levels, six sections, scope, and requirements. | `project/scope-and-levels.md` |
| G1 | Find and register at least five reliable sources; prioritize Taiwan government and university sources. | `sources/source-register.csv` |
| G2 | Record each source, original location, key information, relevant section and level, limitations, and conflicts. | `sources/evidence-cards/EC-####.md` |
| G3 | Check evidence coverage for every section at every level before lesson drafting. | `sources/coverage-matrix.csv` and gate result |
| G4 | Create goals and a lesson sequence linked to evidence. | `outline/teaching-outline.md` |
| G5 | Pause for explicit user approval; record the decision and requested changes. | `outline/approval-record.md` |
| G6 | Draft lessons only after approval; cite evidence and include required learning activities and answer keys. | `wiki/<level>/<section>/` |
| G7 | Run language/script, citation, factual-traceability, and exercise checks. | `qa/reports/` |
| G8 | A reviewer independent of the content creator checks the draft against original sources and evidence cards. | `reviews/independent-source-review.md` |
| G9 | Correct findings and repeat independent review. Keep a per-loop round count. | `reviews/correction-log.md` and updated review |
| G10 | Build teaching slides only from reviewed Wiki content; preserve lesson/source traceability. | `slides/content-map.md` and `slides/html/` |
| G11 | Render and inspect the HTML slides; fix rendering issues within the bounded loop. | `qa/reports/html-rendering.md` and `qa/artifacts/` |
| G12 | Hand off only outputs whose required checks pass; list any unresolved or blocked work. | Handoff summary; no automatic publication |

## Gates and return paths

- **Coverage gate:** Use a 30-cell matrix (six sections × five levels). Proposed pass condition: every cell has at least one relevant evidence card, and the source register contains at least five distinct reliable sources. If incomplete, return to G1 for up to three coverage correction rounds. Then report uncovered cells and stop before G4.
- **Outline approval:** G5 is mandatory before G6 or G10. If the user requests changes, return to G4 and seek approval again.
- **Content/review loop:** G7 failures return to G6. Independent-review findings return to G6, then G7 and G8 are repeated. Maximum three correction rounds; then report unresolved findings and block affected content.
- **Slide loop:** G11 failures return to G10. Maximum three correction rounds; then report remaining rendering issues and block affected slides.
- Keep original-source disagreements visible with source context; do not silently harmonize conflicting explanations.
