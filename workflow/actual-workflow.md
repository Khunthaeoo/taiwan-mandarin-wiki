# Actual Project Workflow

This document records what is visible in the project files. It distinguishes completed work from the required workflow stages that are incomplete or not recorded. It does not treat an unrecorded check or correction as completed.

## Stage record

| Graph stage | What the stage requires | Actual inputs and outputs | Status |
|---|---|---|---|
| **G0 — Scope and level map** | Define the project scope, five levels, and six sections. | `README.md` and the project instructions define A1–C1, six sections, Taiwan Mandarin, and the language and lesson requirements. A1–C1 are project levels, not asserted equivalents of another scale. | **Recorded.** |
| **G1 — Source collection** | Find and register reliable sources, prioritising Taiwan government and university materials. | `sources/source-register.md` records 21 material entries from seven identifiable source families. The collection includes the ACCC books, MOE and NTU materials, NAER and Taiwan Mandarin resources, and other items. Some audio attribution is provisional, one video is unverified, and some material is commercial or supplementary. | **Collection recorded; not every item is verified or suitable as evidence.** |
| **G2 — Evidence cards** | Record source locations, support, relevance, limitations, and differences. | `sources/evidence-cards/ACCC-01.md` through `ACCC-21.md` provide source-specific notes. The cards distinguish direct support from related examples, describe source limits, and record uncertainty and rights notes where available. | **Recorded for the collected entries.** |
| **G3 — Coverage gate** | Check all 30 section-and-level cells before lesson drafting. The proposed pass condition requires relevant evidence in every cell and at least five distinct reliable sources. | `sources/level-coverage-matrix.md` marks **0 Strong, 30 Partial, 0 Missing**. The analysis says cross-level materials do not establish adequate project-level coverage. `sources/coverage-analysis.md` explicitly records the gate as **NOT PASSED**. | **NOT PASSED.** This remains the overall G3 result. An exception was approved for one pilot lesson only; it did not change the gate result. |
| **G4 — Teaching outline** | Prepare a lesson sequence linked to evidence. | `outline/teaching-outline.md` defines one A1 Pronunciation pilot, including goals, source plan, examples, practice, quiz, and known limits. No separate outline for the Vocabulary pilot was found. | **Recorded for Pronunciation only.** |
| **G5 — User approval** | Obtain approval before full lesson drafting or slide creation; return to G4 if changes are requested. | `outline/approval-record.md` records user approval on 2026-11-20 for the Pronunciation outline and an exception for that single pilot. It states there was no approval for other lessons, levels, sections, or HTML slides. No later approval record was found. | **Recorded for the Pronunciation pilot only. Approval for the Vocabulary pilot and HTML slides is not documented in the inspected files.** |
| **G6 — Wiki drafting** | Draft lessons only after the required approval, with evidence links and learning activities. | Two files exist: `wiki/A1/Pronunciation/taiwan-mandarin-basics.md` and `wiki/A1/Vocabulary/greetings-and-self-introduction.md`. Both are labelled as internal A1 pilot content and include learning material and source notes. They do not establish complete A1 coverage, much less complete A1–C1 coverage. | **Two pilot lessons exist. The Vocabulary approval path is not documented.** |
| **G7 — Content checks** | Check language and scripts, citations, factual traceability, exercises, and answer keys; save actual results. | `workflow/quality-checklists.md` lists planned checks. The source register, evidence cards, and coverage matrix preserve some source and coverage checking. No general content-check report was found in `qa/reports/`; no saved result was found for language/script, exercise-key, or full lesson checks. | **Only the source/coverage records are saved. The wider G7 checks are not evidenced as completed or passed.** |
| **G8 — Independent source review** | Have a reviewer check the lesson against original sources and evidence cards. | `reviews/independent-source-review.md` records pass 1 for the A1 Vocabulary pilot. The reviewer reported “No significant issues found in the reviewed changes.” The record limits the review scope and says Burmese translations were not separately verified. | **Recorded for Vocabulary only. No Pronunciation review record was found.** |
| **G9 — Corrections and re-review** | Correct review findings, repeat checks and review, and stop after at most three correction rounds. | The Vocabulary review has no itemized findings. No correction log or per-round record was found. | **No G6→G7→G8 correction-and-re-review round is documented.** |
| **G10 — Slide generation** | Create slides from reviewed Wiki content and preserve lesson/source traceability. | `slides/html/taiwan-mandarin-basics.html` contains 14 slides based on the two A1 pilot lessons. The HTML has slide/source notes and labels some items as original or source-supported. The approval record covers the Pronunciation pilot only and explicitly excludes HTML slides; no later slide approval was found. | **HTML exists, but prior approval for slide generation is undocumented.** |
| **G11 — HTML rendering checks** | Render in a browser and check navigation, layout, assets, console errors, and language display; save evidence where useful. | The user reports manually checking the HTML in a browser and confirming it works correctly. No screenshot or HTML rendering report was found in the QA folders. | **A manual check is reported, but there is no saved evidence of its scope or result.** |
| **G12 — Ready for handoff** | Hand off only outputs whose required checks pass and list unresolved work. | The gate remains failed; review and QA coverage is partial; Burmese review remains outstanding; slide-approval evidence is missing. | **Overall project is not ready to claim all gates passed.** |

## Designed loops, documented execution, and missing loop records

The workflow defines these return paths:

```text
G3 coverage failure → G1 source collection → G2 evidence cards → G3
G5 outline changes → G4 revised outline → G5 approval
G7 content-check failure → G6 lesson correction → G7
G8 review findings → G6 correction → G7 checks → G8 re-review
G11 rendering failure → G10 slide correction → G11
```

Each correction loop is limited to three rounds. If issues remain after round three, the affected branch must be reported as unresolved and must not be marked ready.

**Actually documented:** Source collection and evidence-card work are recorded, and the matrix records the failed G3 assessment. G8 has one saved Vocabulary review pass. The user also reports a manual browser check. These activities are not, by themselves, correction loops. The recorded exception for the Pronunciation pilot changed the scope after G3 failed; it was not a G3 pass or a return to G1.

**No executed correction loop is documented:** The inspected files do not show a G3→G1 return and repeat assessment, a G5→G4 outline-change loop, a G7→G6 content-correction loop, a G8 finding followed by correction and re-review, or a G11→G10 slide-correction loop. The G5 approval record shows the Pronunciation outline was approved, but it does not document a Vocabulary approval or slide approval. The Vocabulary pilot is therefore unapproved in the available records, and approval before creating the HTML slides is undocumented.

**Not run or not recorded:** No source-coverage round count, content correction log, re-review record, slide correction log, or completed QA report was found. A missing record does not prove that an activity never happened; it means this report cannot claim that it happened. The user-reported browser check is not supported by a saved screenshot or written test record.

## Planned quality checks and saved evidence

`workflow/quality-checklists.md` is a plan for checks, not a results report. The saved evidence is limited:

| Check area | Planned check | Evidence found |
|---|---|---|
| Sources and coverage | Source details, evidence cards, source differences, and all 30 level/section cells. | Source register, cards, and coverage matrix/analysis exist. G3 is **NOT PASSED**; all 30 cells are Partial. |
| Lesson language and traceability | Traditional Chinese/Taiwan usage, Burmese, Zhuyin, Pinyin, citations, and lesson content. | Lesson files and citations exist, but no general G7 report was found. Burmese explanations still need qualified review. |
| Exercises and answer keys | Check fixed-answer keys and open-answer rubrics or samples. | Lesson files contain activities and keys, but no saved QA record shows that these were checked. |
| Independent review | Check claims against source material and evidence cards. | One Vocabulary review is saved. It did not separately verify Burmese translations; no Pronunciation review is recorded. |
| HTML slides | Check lesson traceability, browser rendering, navigation, layout, assets, console, and language display. | The user reports a successful manual browser check. No screenshot or rendering report is saved, so the full planned check is not evidenced. |

This distinction is important: a checklist shows what should be checked; only a completed, saved result shows which checks were performed and what they found.

## Main unresolved issues

- **G3 remains NOT PASSED:** all 30 cells are Partial; evidence is not sufficiently assigned to the five project levels.
- The two A1 lessons are pilots and do not demonstrate complete coverage of A1–C1 or all six sections.
- Some Burmese explanations still need review by a qualified Burmese-speaking Mandarin educator.
- The independent source review covers the Vocabulary pilot only; that pilot has no approval recorded. The approval record covers only the Pronunciation pilot and explicitly excludes slide approval.
- No general QA report, correction log, re-review record, or saved browser screenshot was found in the inspected QA and review folders.
- `README.md` still says that no lesson or slide content has been generated, which conflicts with the files now present.
