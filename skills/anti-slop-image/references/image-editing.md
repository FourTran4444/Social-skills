# Realistic image editing — preservation-first

Use this when user supplies an existing image and asks for an edit. Do not silently regenerate unrelated regions.

## Edit constraints
1. **MUST KEEP:** original camera viewpoint, crop, room/scene geometry, perspective, aspect ratio, identities and unaffected objects; retain typography/measurements that were not targeted.
2. **CHANGE ONLY:** exact object or area specified by the user, with its intended shape, placement, size, material and color.
3. **BLEND NATURALLY:** scale and occlusion consistent with camera, lighting direction and softness, contact shadows, reflections, grain, white balance, texture and sharpness.
4. **VERIFY:** no changes to doors, windows, walls, furniture, symbols, labels or other scene content outside the authorized region; no pasted-on appearance.
5. **EXCEPTIONS:** if physical consistency requires a necessary knock-on change (e.g. a new object's shadow), include it narrowly and explicitly.

## Copy-ready output template

```text
Edit the supplied image, not a recreated scene.
MUST KEEP: [all preserved objects, geometry, camera position, image framing, lettering].
CHANGE ONLY: [specific authorized modification].
BLEND NATURALLY: [placement, scale, reflections, shadows, perspective, lighting, texture, color and sharpness].
DO NOT ALTER: [list of protected elements].
```

Do not claim perfect pixel-level preservation; image-generation edits can drift. Recommend visual comparison.
