# Internal Photo Shot Plan (v1.1)

A **private intermediate specification** used to translate a plain-language concept into a coherent, generator-ready photographic prompt. It is **not required output** and it is **not a guarantee** an image model respects camera metadata. For a straightforward idea, fill only meaningful fields; keep the user's interaction simple.

## Plan schema (illustrative YAML)

```yaml
intent:
  scene: "Old Vietnamese street with a bicycle against an aged yellow wall"
  genre: "Street / fine-art documentary"
  story: "Quiet late-afternoon nostalgia"
  must_have: ["bicycle", "old yellow wall"]
  avoid: ["extra people", "posters", "neon rain"]
  location: "Hoi An, Vietnam (when requested or verified)"
  aspect_ratio: "3:2"
scene:
  subject_action: "Bicycle leaning stably against plaster wall"
  spatial_relationships: "Wheels contact uneven pavement; wall and street recede naturally"
  contextual_details: "Plausible local architecture and weathering"
camera:
  position: "Across the narrow lane"
  height: "Eye-level"
  distance_to_subject: "Medium-wide"
  framing: "Single frame with breathing room around the bicycle"
  focal_length: "35mm full-frame equivalent (optional)"
  aperture: "f/5.6 illustrative only"
  focus_target: "Bicycle and adjacent textured plaster"
  depth_of_field: "Bicycle and surrounding wall legible; distant street gradually softer"
  motion: "Static scene, handheld or stabilized exposure"
lighting:
  primary: "Late-afternoon directional daylight from frame left"
  secondary: "Soft bounce from nearby facades"
  shadow_quality: "Coherent soft-to-defined transitions and plausible grounding"
  color: "Neutral shade plus restrained warm light on sun-facing surfaces"
materials:
  plaster: "Uneven aged paint, convincing granular wall texture"
  bicycle: "Real metal, rubber, contact and proportion"
  ground: "Real surface texture without repeated stamping"
editing:
  must_keep: []
  change_only: []
  blend_naturally: []
validation:
  physics: "Perspective, focus, light, motion and material response consistent"
  user_fidelity: "Required bicycle and wall remain primary"
  artifact_avoidance: "No fake HDR, decorative bokeh, giant sun or unsolicited text"
generator:
  target: "generic"
  syntax: "natural-language prompt"
```

## Translation rules

1. **User-first:** preserve the named objects, action, style, location, constraints and provided references before adding stylistic elaboration.
2. **Separate actual constraints from creative defaults:** never hard-code a Vietnamese scene, gender, landscape, camera type or 1:1 ratio globally.
3. **Start from geometry:** camera position and object distances determine perspective; focal length governs field of view at a fixed position.
4. **Cross-check exposure and focus:** aperture, focal length, distance, sensor and viewing size influence DoF; shutter and relative motion influence blur; light sources and bounce determine shadows/reflections.
5. **Set tangible material cues:** choose only the surfaces visible at output scale, rather than filling the prompt with microscopic-detail demands.
6. **Select composition intentionally:** rule of thirds, symmetry, leading lines, negative space and gaze room are optional tools, not enforced defaults.
7. **Discard contradictions before output:** if a proposed camera setting conflicts with focus or lighting, adjust the setting or remove unnecessary numeric parameters.
8. **Translate—not expose:** express the important scene choices in an approximately 120–250 word prompt unless the user requests otherwise. The user need not see the YAML.
9. **Audit in two stages:** prompt readiness is checkable before generation; image quality is checkable only after inspecting an actual rendered result.
10. **Remain generator-independent:** output natural language and avoid pretending vendor-specific flags or precise lens effects are universally supported.

## Worked transformation

**Input:** "An old street in Hoi An, bicycle, 5 PM, realistic and nostalgic. For Gemini."

**Output prompt (copy-ready):**

```text
Create a single believable documentary-style photograph of a quiet old street in Hội An, Vietnam, around 5 PM. A weathered bicycle rests naturally against an aged yellow-plaster wall, with both wheels grounded on slightly uneven pavement. View the scene from standing eye level on the opposite side of the narrow lane, using a moderately wide, natural field of view; keep the bicycle and adjacent wall in clear focus while allowing distant street details to soften gradually with distance. Natural late-afternoon light enters from the left and casts coherent shadows across the pavement, with subtle reflected light from nearby façades. Preserve varied plaster aging, restrained bicycle paint wear, realistically weighted metal and rubber surfaces, and plausible old-town architecture without duplicating identical decorations. Leave quiet negative space around the subject, framing the bicycle as part of an ordinary lived-in street rather than a styled advertisement. Natural colors and measured contrast; no excessive HDR, pasted-looking bokeh, neon haze, impossible reflections, additional people or overdone cinematic processing. No text, no watermark, no collage. Landscape 3:2 composition.
```

The exact site architecture should be verified with reference material if accuracy to a specific building is required.

## Acceptance checklist

- The final prompt names all essential user objects and exclusions.
- Spatial and camera relationships could physically exist.
- Any numeric optics/exposure are coherent and optional, never treated as magic controls.
- Light, shadows, reflections and surface texture align.
- The narrative and aesthetic intent survive without repeated cliché props.
- No image-level visual success is claimed when only prompt text exists.
