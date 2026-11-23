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

## Two-stage realism verification (v1.1)

### Pre-generation prompt audit (always applicable)
- [ ] Exact subject, setting, objects, action, exclusions and image format are retained.
- [ ] Camera position and framing are defined where useful; focal length is not confused with perspective caused by camera distance.
- [ ] Requested depth of field is physically compatible with aperture **and** subject distance, focal length, sensor/framing assumptions.
- [ ] Motion blur fits shutter/camera/subject motion, including panning where specified.
- [ ] Light direction, source size, shadow softness, bounce light, color temperature and reflections do not contradict one another.
- [ ] Material descriptions reflect visible scale: no arbitrary pores, maximum texture on every surface or compulsory artificial grain.
- [ ] No meaningless buzzword stacks, generic props, surprise typography or unsupported generator control syntax.
- [ ] For edits: `MUST KEEP`, `CHANGE ONLY`, and `BLEND NATURALLY` boundaries remain explicit.

### Post-generation visual audit (only if an image can actually be inspected)
- [ ] **Focus/DoF:** credible focus surface and depth-dependent defocus, without random 2D blur masks or inconsistent sharpness.
- [ ] **Perspective:** object proportions, near/far scale, tilted verticals and reflections align with camera position.
- [ ] **Lighting:** cast shadows, subtle contact grounding, indirect fill and mixed temperatures agree with the scene.
- [ ] **Materials:** distinct realistic skin, fabric, paper, glass, metal and wood behavior at the visible image scale; not waxy/plastic or oversharpened.
- [ ] **People:** hands, joints, poses, eye lines and grips are coherent; no duplicated or deformed anatomy.
- [ ] **Text/logos:** exact requested spelling and typography, with no unsolicited words or marks.
- [ ] **Composition:** focal anchor and relevant space for gaze/movement, unless intentional tight framing; avoid stray edge clipping.
- [ ] **Instructions:** aspect ratio, scene location, core objects and protected edit regions are correct.

### Evidence boundary
- Prompt-only review can **pass the prompt audit** but cannot pass image realism review.
- Aesthetic options (grain, bloom, shallow DOF, symmetry, soft light) cannot be hard failures merely because they are present; inspect whether they are *physically coherent and appropriate to user intent*.
- The scoring rubric above remains editorial guidance; never claim it is a measured probability of being photographic.
