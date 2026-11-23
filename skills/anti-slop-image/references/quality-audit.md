# Pre-Generation Realism Safeguards

**Purpose:** prevent predictable AI-image artifacts in the prompt **before** an image is generated. This is a prompt-preparation checklist, **not** an image inspection system, a score, a detector, or a post-generation QA workflow.

Use the relevant checks silently while drafting. If a requirement is missing or contradictory, **rewrite the prompt**. Do not present checkboxes or a numeric score to the user by default. The checklist cannot guarantee what a model will render.

## 1. Subject and instruction fidelity

- [ ] Preserve the exact subject, activity, essential supporting objects, specified geography, mood, aspect ratio, and user exclusions.
- [ ] Keep a single coherent scene rather than introducing unrequested collage/panels, infographic styling or multiple unrelated scenes.
- [ ] Include exact required text only; avoid unsolicited typography, logos and watermarks.
- [ ] Do not insert stock motifs (coffee cups, flowers, notebooks, rain, cinematic neon) unless meaningful or specifically requested.
- [ ] Keep optional project-specific rules separate from universal ones.

## 2. Camera, optical coherence and motion

- [ ] Specify a meaningful camera position/height/distance and framing when it influences the image.
- [ ] Distinguish camera-position perspective from focal-length field of view. Do not attribute perspective changes to lens focal length alone.
- [ ] Reconcile sensor/framing assumptions, focus distance, aperture and intended depth of field. Focus follows plausible 3D distance and lens characteristics, not a patchy blur mask.
- [ ] If subjects are moving, specify believable shutter/motion relationships; panning can make the tracked subject sharper than stationary backgrounds.
- [ ] Do not force a single aperture, perfect sharpness everywhere, grain, flare, optical distortion or extreme bokeh in every scene.

## 3. Exposure, light and shadow geometry

- [ ] Identify primary light direction, size/softness and relative intensity; include other practical or bounce sources only when credible.
- [ ] Match shadow world-space direction and plausible lengths to source elevation, object heights, perspective and receiving-surface slopes.
- [ ] Describe long shadows interacting with uneven paving, terrain and objects rather than uniform merged dark shapes.
- [ ] Preserve realistic sensor dynamic range. In daylight-exposed scenes, unlit interiors may remain deep in shadow; avoid synthetic HDR-style uniformly lifted darkness unless lighting, exposure strategy or composite technique justifies it.
- [ ] Keep reflections/refractions, light temperature and contact/ambient occlusion plausible. Diffuse light need not produce a black outline around every object.

## 4. Objects, organic materials and lived-in composition

- [ ] Require credible geometry of foreground *and* small distant secondary objects, particularly bicycles, gates, railings, furniture, hands and tools.
- [ ] Ensure small leaves, twigs and debris rest naturally on the ground and are not floating/pasted-on shapes.
- [ ] Describe material-specific behavior: fabric weave/folds, skin texture at relevant scale, wood grain, glass thickness, metal finish, botanical fibers, bamboo tension, realistic food texture.
- [ ] Let peeling paint, moss, stains and wear follow physical processes such as water runoff, handling, traffic, sunlight and moisture; avoid uniform procedural noise.
- [ ] Use candid off-axis framing and traces of real use **where the scene calls for documentary realism**. Do not forbid genuine symmetry, orderly spaces, fine-art compositions or legitimately glossy materials.
- [ ] Avoid decorative foliage in every corner or showroom-perfect staging unless requested.

## 5. Edit-request safeguards (when applicable)

- [ ] State the original elements to preserve: viewpoint, perspective, scene geometry, text, identities, crop and unchanged objects.
- [ ] Delimit the exact authorized change and physically required local consequences (e.g. a new object's shadow).
- [ ] Explicitly forbid unrelated edits, scene recreation and accidental text alterations.

## 6. Cross-generator portability

- [ ] Make the prompt complete without requiring the generator to read this skill's reference files.
- [ ] Write observable scene constraints, not “8K, masterpiece, hyperrealistic” stacks.
- [ ] Include model-specific flags only when documented for the user's actual interface.
- [ ] Produce a polished prompt the user can copy directly; do not output internal YAML or scored audits unless requested.

## Preflight decision

**READY TO GENERATE** means the prompt is complete and internally coherent, **not** that an image has been generated or visually verified. When a conflict exists, rewrite the prompt before delivery. Do not perform a post-render score or repair cycle as part of this skill.

## High-priority pre-generation gate — Anti-Perfection

Before returning the final prompt, resolve these upstream problems. This is **prompt design**, not an inspection of an image:

- [ ] **Uneven visual attention:** Have we avoided making every background object, corner, wall and leaf equally sharp, visually prominent and attractive?
- [ ] **No texture saturation:** Are detailed aging, fibers and microtexture selective and physically motivated instead of uniformly covering each surface?
- [ ] **No ubiquitous ideal lighting:** Are there ordinary, subdued or shadowed areas, rather than carefully placed flattering light on every object?
- [ ] **Natural scene placement:** Is the scene free of unnecessary showroom symmetry, four-corner foliage framing, and perfectly arranged props when the brief is candid?
- [ ] **Room for the mundane:** Does the prompt allow some uninteresting areas, partial occlusions, ordinary pavement and quiet visual space?
- [ ] **No fake realism shortcuts:** Are grain, dirt, low exposure, distortion and blur absent unless actually motivated or specifically requested?
- [ ] **Preserve the story:** Does simplifying the scene maintain the core emotional subject instead of removing the meaning?
- [ ] **Respect exceptions:** If the user explicitly asks for a polished advertising shot, formal symmetry, or ornate fine-art direction, do not force an unplanned snapshot aesthetic.

**Priority:** If a technically coherent scene has become excessively curated, rewrite the photographic prompt to reduce global visual polish **before generation**. Do not attach a numerical score.
