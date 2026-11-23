# Pre-generation image-edit prompt — preservation-first

Use this **before** any edit when the user supplies an existing image and asks for edit *instructions*. Return the preservation-focused editing prompt; do not apply the edit or audit its result.

## Edit constraints
1. **MUST KEEP:** original camera viewpoint, crop, room/scene geometry, perspective, aspect ratio, identities and unaffected objects; retain typography/measurements that were not targeted.
2. **CHANGE ONLY:** exact object or area specified by the user, with its intended shape, placement, size, material and color.
3. **BLEND NATURALLY:** scale and occlusion consistent with camera, lighting direction and softness, contact shadows, reflections, grain, white balance, texture and sharpness.
4. **SPECIFY IN ADVANCE:** state that doors, windows, walls, furniture, symbols, labels and all objects outside the authorized area must stay unchanged and integrated naturally.
5. **EXCEPTIONS:** if physical consistency requires a necessary knock-on change (e.g. a new object's shadow), include it narrowly and explicitly.

## Copy-ready output template

```text
Edit the supplied image, not a recreated scene.
MUST KEEP: [all preserved objects, geometry, camera position, image framing, lettering].
CHANGE ONLY: [specific authorized modification].
BLEND NATURALLY: [placement, scale, reflections, shadows, perspective, lighting, texture, color and sharpness].
DO NOT ALTER: [list of protected elements].
```

This is a preventive instruction, not proof of pixel-level preservation. The skill does not perform a post-edit visual review.
