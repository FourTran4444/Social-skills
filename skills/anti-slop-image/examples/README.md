# Copy-ready examples

These examples show the expected **input → final prompt** behavior. Realism is not a synonym for underexposure, handheld blur, film grain or iPhone photography.

## 1. Landscape — generic

**Input:** "A peaceful rice terrace in northern Vietnam at sunrise. Real photo."

**Prompt:**
```text
Create a believable landscape photograph of terraced rice fields in a mountainous northern Vietnamese valley shortly after sunrise. Place the camera on a stable path above the fields, about eye level, looking diagonally across irregular terraces descending into the valley. The nearest terrace edges show uneven soil, water and young rice plants; farther terraces become softer and less contrasty with atmospheric distance. The ridgeline, plants and water follow natural terrain; no duplicated mountain shapes or perfectly repeated terraces. Side light from the low morning sun creates coherent shadows and restrained warm highlights; shaded slopes remain cooler, without exaggerated orange gradients. Use a moderately wide, natural photographic field of view with enough depth of field to resolve the foreground path and much of the valley. Organic surface texture, subtle imperfections and restrained postprocessing. A quiet, spacious frame with one clear visual path through the terraces. No added text, fabricated landmark, enormous sun, extreme HDR or fantasy scenery. Landscape orientation, 3:2.
```

## 2. Street — Gemini

**Input:** "Vietnam street market, candid, no faces."

**Prompt:**
```text
Generate a candid documentary-style photograph of a Vietnamese neighborhood street market in the early morning. Position the camera at standing height, slightly to the side of a narrow produce stall, observing rather than staging. Woven baskets, leafy greens, a parked motorbike and ordinary shopfronts occupy plausible positions with room for people to pass. People appear only as partial figures or from behind, no front-facing recognizable faces; their gestures differ naturally and their hands interact believably with produce and baskets. Soft daylight from the open street creates consistent shadows beneath the stall awning. A normal-to-moderately-wide photographic perspective, clear focus on the central stall, natural distance falloff rather than aggressive artificial bokeh. Maintain believable Vietnamese signage only if the text can be rendered correctly; otherwise avoid readable signage. Preserve slightly uneven everyday details without adding theatrical grime or cinematic neon. Single photograph, not a montage. Vertical orientation, 4:5.
```

## 3. Still life — ChatGPT Images

**Input:** "An old chair in an empty room, lonely, beautiful but not AI."

**Prompt:**
```text
Create a quiet fine-art photograph of a single worn wooden chair beside an open window in an otherwise ordinary, sparsely furnished room. Camera at seated eye level from the doorway, framing the chair off-center with generous negative space in the muted plaster wall. A real late-afternoon window is the primary light source; its direction matches the chair's contact shadow and the soft falloff across the floor. Let the varnish show age, small scratches and varied wood grain without hyperdetail or artificial dirt. Keep the chair, floorboards, wall intersection and window geometry structurally sound. The emotion comes from absence and ordinary stillness, not props, rain, fog, coffee cups or dramatic film effects. Natural color, restrained contrast, coherent focus, subtle documentary-art direction. No text or collage. Square composition, 1:1.
```

## 4. Existing-image edit

**Input:** "Add a small lamp to the desk, don't change anything else."

**Edit instruction:**
```text
Edit the supplied image instead of recreating it. MUST KEEP the original camera position, framing, walls, windows, furniture, visible text and all objects outside the target area. CHANGE ONLY by adding a small, physically plausible desk lamp on the right rear corner of the desk, scaled correctly and not blocking any existing controls. BLEND NATURALLY with the original perspective, white balance, light direction, material grain and contact shadow; if switched on, use a restrained local pool of light consistent with the scene. DO NOT move or replace the desk, crop the image, redraw labels or modify surrounding architecture.
```
