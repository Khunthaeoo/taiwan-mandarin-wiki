# HTML Presentation Manual Test Report

## Test information

- **Test and recheck date:** 2026-11-22. The screenshot files are dated November 22, 2026; no separate log records exact times.
- **Browser:** Microsoft Edge, as reported by the user and visible in screenshots `page5.png`, `page6.png`, and `page7.png`.
- **Test type:** Manual browser test and focused manual recheck. The user reports that the presentation worked correctly.
- **Tested file:** `slides/html/taiwan-mandarin-basics.html`
- **Homework context:** `sources/Homework 10 - 用 LLM Wiki 做一份教學 HTML.txt` asks for a usable teaching HTML presentation and an execution or check record.

## Tests and observed results

The user did not provide a step-by-step test log. The screenshots provide evidence of the following rendered states, but do not by themselves prove that buttons or other controls were activated.

| Test / observation | Actual result | Screenshot evidence |
|---|---|---|
| Open the presentation and view the first slide. | The opening slide rendered. The progress display showed 01 / 14, and the 14-slide count was visible. | `qa/artifacts/page1.png` |
| View the learning objectives slide. | Slide 02 / 14 rendered with its learning-goal cards and bilingual text visible. | `qa/artifacts/page2.png` |
| View the tones slide. | Slide 04 / 14 rendered with tone examples and Traditional Chinese, Burmese, Zhuyin, and Pinyin content visible. | `qa/artifacts/page4.png` |
| View a vocabulary slide in Edge. | Slide 07 / 14 rendered in an Edge window. Traditional Chinese, Burmese, Zhuyin, Pinyin, and navigation controls are visible. | `qa/artifacts/page5.png` |
| View the quiz slide in Edge. | Slide 13 / 14 rendered with quiz questions and answer controls visible. The screenshot does not show answers being selected or checked. | `qa/artifacts/page6.png` |
| View the final self-check slide in Edge. | Slide 14 / 14 rendered with self-check boxes and content visible. The screenshot does not show checkboxes being used. | `qa/artifacts/page7.png` |
| Focused manual recheck of slides represented by `page6.png` and `page7.png`. | The user reports that the navigation bar and slide content worked correctly. No confirmed content-blocking overlap was found. The exact actions and any additional check steps were not recorded. | User report; no separate screenshot or step-by-step log for this recheck. |
| Overall manual test. | The user reports that the presentation worked correctly in Microsoft Edge. The exact scope of the full test was not recorded. | User report; no separate test log. |

## Problems and limits

- The first review of `page6.png` and `page7.png` noted that the sticky bottom navigation appeared to overlap lower slide content in the captured views. This was an observation from screenshots, not a confirmed failure. In the later manual recheck, the user reported that the navigation bar and slide content worked correctly and no content-blocking overlap was found. The exact recheck steps were not recorded.
- The screenshots show controls, but do not establish that answer checking, quiz feedback, or self-check boxes were operated successfully. The user's recheck covered the navigation bar and slide content represented by `page6.png` and `page7.png`; it does not establish that every interactive control was tested.
- No screenshot or saved result records browser console checks, responsive-size checks, or missing-asset checks. These are **not verified by the available evidence**.
- No confirmed content-blocking problem was found in the screenshot review or reported recheck. The user's overall report that the presentation worked correctly is recorded, but detailed test steps were not supplied.

## Screenshot files reviewed

- `qa/artifacts/page1.png`
- `qa/artifacts/page2.png`
- `qa/artifacts/page4.png`
- `qa/artifacts/page5.png`
- `qa/artifacts/page6.png`
- `qa/artifacts/page7.png`
