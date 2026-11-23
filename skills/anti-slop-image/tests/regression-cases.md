# Historical feedback regression cases

Use this list to evaluate **pre-generation prompt transformation only**, not generated-image review. These cases are condensed from prior user feedback; identifiers are examples, not downloadable test assets.

| Case | Input intent | Failure to prevent | Expected skill behavior |
| --- | --- | --- | --- |
| CDL-0021/0027 | One photographic scene | Multi-panel labeled collage | Explicit single-frame scene; reject collage |
| CDL-0026 | Room, moving boxes | Generic coffee, flowers, notebook | Preserve room/boxes as main subject |
| CDL-0027 | Vietnamese bread | Missing requested bread | Repeat must-have object clearly in prompt |
| CDL-0032 | Photographic scene | Dashboard infographic | Require photographic composition, not graphics |
| CDL-0033 | Exact square | Near-square noncompliance | Specify 1:1 and request exact output ratio |
| TT100-010 | Door, suitcase, keys | Coffee props substituted | Main subject fidelity over style clichés |
| TT100-013 | One apartment/porch scene | Two scenes mixed; wrong text | One scene; specify exact requested text before generation |
| TT100-059 | Adult male from behind | Wrong cast or frontal face | Conditional project profile enforces casting |
| TT100-074 | Documentary image | Oversized poster typography | No unsolicited large lettering |
| TT100-078 | Natural focus | Uniform sharpness / fake bokeh | Plan focus plane, realistic distance falloff |
| TT100-081 | Quiet photographic story | Motivational poster styling | Exclude decorative motivational text |
| Landscape | Natural mountains | Giant moon, identical peaks, fog filter | Physical sky scale, varied terrain and weather |
| Street | Local market | Generic neon rain, all posed | Candid spatially credible activity |
| Edit | One lamp added | Entire room changes | Preserve protected geometry and content |
| Vendor portability | User chooses Gemini | Fake negative_prompt API syntax | Natural text and qualified capabilities |

## Suggested manual acceptance

For each case inspect the **written prompt** before attempting generation:
1. Does it retain all essential nouns and constraints?
2. Does camera/light/focus have a coherent physical story?
3. Are avoidance clauses specific rather than word salad?
4. Are project-specific assumptions loaded only when relevant?
5. Is the text directly usable in ChatGPT Images, Gemini or a generic generator?

These tests check the completeness and internal consistency of the *written prompt before generation*. Do not run rendered-image QA as part of this skill.

## Optical realism pack — v1.1 regression scenarios

| Case | Scene and purpose | Pre-generation risk to prevent | Prompt pass condition |
| --- | --- | --- | --- |
| Shallow focus | Close portrait at f/1.2–f/1.4 with background lights, stated subject distance | Sharp far background, arbitrary blur on same-distance features | Camera distance and intended focal subject identified; defocus follows plausible optical geometry rather than a pasted mask |
| Grounded object | Cup/box/shoe on a table/floor in diffuse or directional light | Floating object, missing occlusion, shadow direction inconsistent | Plausible supporting surface, contact grounding and lighting response, without mandatory harsh black border |
| 85mm vs 24mm | Same subject across portrait and environmental framing at explicitly different camera distances | Treating focal length as the *cause* of changing perspective; distorted faces with wrong camera position | Physically coherent field of view, camera placement, scale relationships and convergence |
| Skin and materials | Portrait or product packaging in daylight/window or studio lighting | Waxy skin, duplicated pores, plastic paper/metal/wood, pasted labels | Skin/micro-texture at plausible resolution; distinct material responses, folds and edges |
| Camera movement | Panning cyclist with a slow shutter | Sharp background demanded as universal rule; anatomy warped to show blur | Tracked subject can stay relatively crisp while stationary background streaks in motion direction |
| Aperture-distance | f/1.4 used for distant landscape subject | Universal claim that *all* f/1.4 scenes have razor-thin focus | DoF reasoning includes distance/sensor/focal length, without fabricated impossible blur |
| Diffraction | Landscape f/16–f/22 | Unconditional "maximum detail everywhere" claim | Account for increased DoF and potential diffraction softness rather than promising absolute sharpness |
| Mixed lighting | Evening shopfront and blue ambient sky | Every light rendered same temperature; shadow directions disagree | Plausible practical + ambient light with coherent color and shadow behavior |
| Intentional optical look | Film portrait with ring bokeh, subtle bloom, grain | Reject legitimate optical character as AI slop by default | Allow optically justified ring bokeh, bloom and grain; reject unjustified patterned overlays |
| Editing preservation | Add a lamp to an existing photograph | Scene, camera, unrelated objects drift | Authorized edit alone plus physically required local effects; protected geometry preserved |

### Testing scope
These are **manual pre-generation prompt specifications**. Test the produced prompt, not a rendered image. A pass means the prompt contains appropriate realism constraints without contradiction; it does not guarantee the generator obeys them.

### 5.5 Long Cast Shadows & Secondary Background Props Test

- **Scenario:** Low-angle sunlit street, alley or courtyard featuring long cast shadows, foliage shadows, a parked bicycle or gate/railings in the background, and small fallen leaves or twigs on textured paving.
- **Failure Mode to Catch:** Incompatible world-space shadow vectors or lengths (after accounting for perspective and surface slopes); shadow forms melted into ambiguous blobs despite adequate visibility; distorted distant wheels, spokes, rails or bars fused into walls; leaves floating or looking flat and pasted on.
- **Pass Criteria:** Shadows remain physically consistent with the dominant light and receiving surfaces; object silhouettes and long-shadow contours are believable at the rendered scale; distant props retain coherent mechanical geometry; small debris makes credible contact with uneven ground.
- **Prompt-level acceptance:** The generated prompt explicitly preserves motivated light direction, shadow-ground interaction, secondary prop structure and debris contact where relevant.
- **Scope boundary:** Evaluate the prompt's preventive instructions only; no post-generation visual acceptance occurs in this skill.

## Anti-Perfection pre-generation regression cases

| Prompt scenario | Failure to prevent before generation | Expected revised prompt |
| --- | --- | --- |
| Quiet Vietnamese alley with two walking shadows | Every object has dramatic highlights, perfect peeling paint, cinematic foliage frame, and all details equally emphasized | Two shadows carry the story; wall has plain sections; subdued unremarkable background; selective light and only plausible localized wear |
| Ordinary clean kitchen | Skill injects grime, film grain and random clutter as proof of realism | Preserve naturally clean environment; avoid synthetic polish without manufacturing damage |
| Weathered wall | Entire surface uniformly filled with picturesque moss, cracks and peeling paint | Physically caused, localized deterioration with large untouched/plain sections |
| Street documentary | Background props all neatly positioned and independently eye-catching | Off-axis, incidental background arrangement and unobtrusive secondary objects |
| Formal symmetric architecture explicitly requested | Skill forces arbitrary cropping and disorder | Preserve deliberate architectural symmetry and accurate geometry |

Only evaluate **pre-generation prompt wording**. These are not image-level visual assertions.
