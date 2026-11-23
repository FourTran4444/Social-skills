---
name: anti-slop-image
description: Pre-generation image prompt architect. Transform a simple idea into a complete, physically plausible, generator-ready image prompt before creating an image. Supports ChatGPT Images, Gemini, Claude as a prompt-writing assistant, and generic image generators.
---

# Anti-Slop Image — Pre-Generation Prompt Architect

## Mission (strict scope)

This skill runs **BEFORE image generation**, not after. Its output is a complete, copy-ready prompt that has already been enriched, reconciled, and checked for realistic photography. The skill is neither a rendered-image detector nor an image-quality scoring or post-hoc repair workflow.

**Input:** a user's basic visual idea, brief, or planned image-edit instruction.
**Output:** one polished, usable image-generation or image-edit *prompt* for the selected generator.
**Default:** prompt only. Do not generate or edit an image, review a previously rendered output, publish or upload anything as part of this skill. If the host later generates an image at the user's explicit request, this skill's role ends when the final prompt is handed off.

## Triggers

Use when the user asks for an image concept to be converted, enhanced, fulfilled, expanded, realism-checked or adapted **before generation**; or when they need a realistic image-edit prompt *before applying an edit*.

Do not invoke this skill as a post-generation audit or image-forensics tool. If a user asks to fix a previously generated image, treat their feedback and references as **constraints for a new pre-generation prompt**, without operating a post-hoc inspection/scoring workflow.

## Input

Only the idea is required. Optional information: intended subject/action, genre, geography and time period, mood, reference scene, destination generator (ChatGPT Images / Gemini / generic), aspect ratio, exact on-image text, constraints, exclusion list, project profile, or authorized edit boundaries. Never force the user to know aperture, lens, exposure, focus or light details.

When unspecified, choose coherent defaults without inventing hard factual location details or restricting who may appear. User intent outranks generic styling defaults. A Vietnamese-only, no-face, male-only or square-Facebook requirement is **not universal**; see [project profiles](references/project-profiles.md) only if specifically relevant.

## Workflow — all before generation

1. **Interpret the idea.** Extract required subjects, actions, story, location, context, output ratio, essential objects, exact text, restrictions and reference-preservation needs.
2. **Fulfill missing scene details.** Choose a scene with tangible geometry, real object relationships and purposeful composition. Make modest creative assumptions that strengthen the user's idea without replacing it with stock motifs.
3. **Build a private [Photo Shot Plan](references/photo-shot-plan.md).** Define viewpoint/height/distance, framing, field of view, focal subject, depth of field, motion, source-driven lighting, surface materials, environmental context and genre. Camera numbers are optional supporting examples, not magic realism keywords.
4. **Apply photography/scene constraints.** Read [photography physics](references/photography-physics.md) and applicable [scene guides](references/scene-guides.md): exposure and dynamic range, 3D depth/focus, shadow geometry, background object structure, surface contact, wear patterns and candid arrangement. Use only rules relevant to this particular scene.
5. **Resolve contradictions *before writing the prompt*.** Reconcile viewpoint and perspective; focus distance, focal length and DoF; exposure and motion; light vector, shadows and reflections; materials and physical use. Preserve deliberate artistic exceptions and do not enforce falsely rigid camera rules.
6. **Preflight the draft prompt.** Run the **pre-generation safeguards** in [quality-audit.md](references/quality-audit.md). Revise wording until the prompt protects required content, avoids likely AI clichés and describes physically possible relationships. Do not grade an image that does not exist.
7. **Adapt for the target generator.** Use [generator adapters](references/generator-adapters.md). Prefer portable natural language, and never invent vendor-specific prompt flags.
8. **Deliver the result.** Output the **final copy-ready prompt first**. If it helps, add a brief avoidance line and no more than three assumptions. Do not show the internal shot plan, checklist, score, or chain of thought unless specifically requested.

For an image-edit request, use [image-editing.md](references/image-editing.md) to draft strict **MUST KEEP / CHANGE ONLY / BLEND NATURALLY** instructions *before* the edit.

## Pre-generation contract

A valid final prompt must:
- Contain the user's requested primary subject and relevant secondary objects without unauthorized substitutions.
- Establish scene place, composition and meaningful action; neither over-stage everything nor inject dirt or clutter mechanically.
- Describe a credible camera/viewpoint, focus relationships and exposure/lighting behavior where relevant.
- Preserve sensor dynamic-range realism: avoid automatically lifting deep unlit rooms to daytime brightness.
- Keep shadows consistent with primary light in world space and responsive to receiving surfaces.
- Keep foreground, middle-distance and background props structurally plausible (wheels, gates, poles, railings, leaves, tools).
- Describe surface-specific texture, wear, reflections and grounding rather than uniform procedural noise.
- Avoid blanket cinematic buzzwords, unnecessary HDR, unrealistic bokeh, forced symmetry, random neon/rain/fog and repeated coffee props unless requested.
- Respect intentional photography techniques (symmetry, grain, HDR, composites, bloom) when motivated or explicitly requested.
- Preserve requested on-image text/brand constraints, aspect ratio and edit boundaries.

## Output

**Default — generation prompt:**

```text
[A single cohesive image prompt, usually about 120–250 words; positive scene instructions first, concrete constraints, and relevant anti-slop safeguards. Copy/paste directly into the chosen image generator.]
```

**Optional avoidance note:** brief and model-compatible; do not assume the generator has a separate negative-prompt control.

**Edit prompt:** `MUST KEEP`, `CHANGE ONLY`, `BLEND NATURALLY`, and relevant `DO NOT ALTER`.

**No post-generation result:** Never attach QA scores or claim an image has passed inspection. The preflight confirms **prompt coherence**, not guaranteed image realism.

## References

- [Internal pre-generation shot plan](references/photo-shot-plan.md)
- [Photography and optical physics](references/photography-physics.md)
- [Landscape, street, fine art and other scene guides](references/scene-guides.md)
- [Pre-generation prompt safeguards](references/quality-audit.md)
- [Generator adapters](references/generator-adapters.md)
- [Pre-edit prompt preservation](references/image-editing.md)
- [Optional project profiles](references/project-profiles.md)
- [Prompt examples](examples/README.md)
- [Prompt regression cases](tests/regression-cases.md)
- [Sources and acknowledgments](references/sources.md)
