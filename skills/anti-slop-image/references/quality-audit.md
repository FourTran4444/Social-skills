# Anti-Slop Visual Audit

A **heuristic human-facing review aid**, not a calibrated AI-image detector or proof of authenticity. Only judge visual facts that can actually be inspected. Report "not assessable" if no image was supplied.

## Hard failures (reject regardless of score)
- Incorrect main subject, missing required object, incorrect specified text, wrong aspect ratio when essential.
- Impossible architecture or geometry, duplicated body parts, severe anatomy or object deformation.
- Impossible primary shadows/reflections/light source relationships without intentional surrealism/composite.
- Edited regions replacing or materially changing protected image areas.
- Unrequested collage, poster, logo or prominent typography violating constraints.
- Misrepresenting a synthetic/composited image as unedited journalistic evidence.

## Heuristic rubric, 100 points
| Dimension | Max |
| --- | ---: |
| Camera, focus and photographic coherence | 20 |
| Light, color and exposure plausibility | 20 |
| Geometry, anatomy and object integrity | 20 |
| Materials and environmental detail | 15 |
| Composition and storytelling | 10 |
| Subject/context instruction fidelity | 10 |
| Overall naturalness | 5 |

Suggested triage: **85–100** candidate pass; **75–84** revise/review; **0–74** reject. A hard failure overrides totals. These numbers are an editorial rubric, NOT a probability or authenticity score.

## Repair procedure

For each issue:
1. Quote/describe the specific visible defect (not generic "too AI").
2. Link it to an applicable category above and identify severity.
3. Supply a targeted instruction that corrects the physical cause.
4. Preserve successful parts of the image and user requirements.
5. After a new image is supplied, compare the new result against original defects.
6. Stop pretending a revision succeeded if no generated image or visual readback exists.

## Regression tests

Use [regression-cases.md](../tests/regression-cases.md), especially prompt leakage, accidental collage, stereotyped café props, fake shallow depth, oversized typography, mismatched silhouettes and edit drift.
