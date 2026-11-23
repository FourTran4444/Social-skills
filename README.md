# Social Skills

Open-source, reusable AI skills for creating better social and visual content. Each skill is a collection of **Markdown instructions, references, examples and tests**—not an image model, plugin, or paid API.

## Available skills

| Skill | What it does | Start here |
| --- | --- | --- |
| **Anti-Slop Image** | Turns a simple idea into a realistic, photography-grounded prompt for ChatGPT Images, Gemini and other image generators. Also supports image-edit instructions and visual-quality reviews. | [Read the skill](skills/anti-slop-image/SKILL.md) · [Examples](skills/anti-slop-image/examples/README.md) |

## Anti-Slop Image — How to use

### 1. Get the skill

**Option A — use the GitHub files directly**

Open [`skills/anti-slop-image/SKILL.md`](skills/anti-slop-image/SKILL.md) and the files it links to in [`references/`](skills/anti-slop-image/references/). Supply them to an assistant using that product's file, project, knowledge or skill-loading feature, **if available**.

**Option B — download the repository**

```bash
git clone https://github.com/FourTran4444/Social-skills.git
cd Social-skills
```

Or use GitHub's **Code → Download ZIP**.

The skill lives at:

```text
skills/anti-slop-image/
├── SKILL.md                    # Entry point and expected behavior
├── references/
│   ├── photo-shot-plan.md      # Internal photographer-first scene planning
│   ├── photography-physics.md  # Optics, lighting, motion, materials
│   ├── scene-guides.md         # Landscape, street, portrait, interiors, etc.
│   ├── generator-adapters.md   # ChatGPT, Gemini, generic model guidance
│   ├── image-editing.md        # Keep/change/blend constraints
│   ├── quality-audit.md        # Before/after checks
│   └── project-profiles.md     # Optional project-specific preferences
├── examples/README.md
└── tests/regression-cases.md
```

**Important:** Merely sharing the GitHub URL in a prompt does not guarantee your assistant has read all referenced files. Provide the actual files, or use a compatible skill loader that makes the entire skill directory accessible.

### 2. Load it into your AI assistant

There is no universal one-click installer. The method depends on your product:

| Environment | How to load it |
| --- | --- |
| **ChatGPT chat or Project** | Attach the `SKILL.md` text/file and the relevant reference files, or place them in available Project/knowledge files. Ask ChatGPT to follow `anti-slop-image` when writing the prompt. |
| **Custom GPT (if supported by your account)** | Add the skill and its references as knowledge; in its instructions, tell it to consult `SKILL.md` and select references based on the task. |
| **Gemini chat** | Provide the skill text and relevant reference documents through supported file upload or paste them into the conversation. Ask Gemini to follow the skill. |
| **Coding agent with skills support** | Put the **whole** `skills/anti-slop-image/` directory in the tool's documented skill location. The specific install path and discovery behavior are agent-dependent. |
| **Other AI assistant** | Paste `SKILL.md` and the applicable references, then give your image idea. Long context may require selecting only the relevant references. |

These are **manual/compatible loading approaches**, not verified automatic GitHub integrations. If your assistant cannot read local files or URLs, paste the contents explicitly.

### 3. Give it a simple image idea

You do **not** need to understand camera settings. The assistant should use the skill to decide plausible framing, lens behavior, light, texture and exclusions.

**Copy/paste — ChatGPT**

```text
Follow the attached anti-slop-image skill and its relevant references.
Turn this idea into a copy-ready prompt for ChatGPT Images:
"An old wooden chair inside a quiet Vietnamese house in late afternoon."
Make it feel like a believable photograph, not a glossy AI render.
Return the final image prompt first. Do not generate the image yet.
```

**Copy/paste — Gemini**

```text
Use the anti-slop-image skill in the attached files.
Write a ready-to-use Gemini image-generation prompt for:
"A bicycle leaning against an old yellow wall on a quiet street in Hội An, Vietnam."
Keep the optics, light, material textures and perspective physically plausible.
Output the prompt only. Do not generate the image yet.
```

**Copy/paste — any other model**

```text
Use anti-slop-image to convert this image idea into a portable photographic prompt:
"A misty mountain valley with small rice terraces at sunrise."
Target generator: generic. Aspect ratio: 3:2.
Preserve a realistic landscape; no fantasy elements or exaggerated HDR.
Write a natural-language prompt without vendor-specific flags.
```

### 4. Copy the result into your image generator

The assistant should return **a single, ready-to-copy prompt**, usually followed by a short optional "avoid" section—not a wall of keywords or an internal YAML specification.

Example (shortened):

> Create a single documentary-style photograph of a weathered bicycle resting against an aged yellow-plaster wall on a quiet street in Hội An. Frame from eye height on the other side of the lane. Keep the bicycle and wall in coherent focus and allow the distant street to soften naturally. Use restrained late-afternoon light from camera-left, physically consistent contact grounding and shadows, worn plaster and authentic metal/rubber textures. Natural color and contrast, no oversized sun, extreme HDR, artificial blur, unsolicited text or collage. Landscape 3:2.

Paste that into ChatGPT Images, Gemini's image-generation interface or another compatible generator. If your AI assistant also has image-generation capability, **explicitly ask it to generate** after reviewing the prompt; writing a prompt does not automatically create an image.

### 5. Review and improve the result (optional)

After an image is generated, provide that **actual image** to an assistant using the skill:

```text
Use anti-slop-image to review this generated image for artificial-looking details.
Check camera perspective, depth of field, reflections, contact shadows,
materials, anatomy, text and fidelity to my original request.
List specific visible defects and give me a corrected image-generation prompt.
Do not claim it passes image QA until you have inspected the image.
```

For an **existing photo edit**:

```text
Use anti-slop-image to write an image-editing prompt for the attached photo.
Add a small desk lamp to the right side of the desk.
Keep the original camera position, room geometry, furniture, and any existing text.
Change only the lamp and its physically necessary local light/shadow effects.
Return the edit prompt; do not edit the photo yet.
```

## What the skill actually does

```text
Your idea
   ↓
Interpret subject, story and constraints
   ↓
Build an internal photographer-first shot plan
   ↓
Check camera position, optics, light, materials, composition
   ↓
Remove conflicting instructions and familiar AI clichés
   ↓
Adapt natural-language prompt to ChatGPT / Gemini / generic generator
   ↓
Your copy-ready prompt
   ↓
(Optional) Generate image, inspect actual output, revise prompt
```

The default workflow is **idea → prompt**. Image generation, editing, publishing and uploads are **not automatic**. The skill does **not** claim to detect AI images with certainty or to force any model to obey exact camera metadata.

## Common questions

**Can I just send a link to this repository?** Sometimes, if an assistant can access the link and follow its referenced files. Reliable usage requires making the skill contents available to the assistant.

**Do I have to specify 35mm, f/5.6, ISO, etc.?** No. State what you want to see. Camera numbers are optional, physically coherent planning aids—not magic realism tokens.

**Does it work only with Vietnam, coffee images or Facebook?** No. It is general-purpose. The Vietnamese Facebook profile is **optional** and is not loaded as a universal restriction.

**Will ChatGPT and Gemini produce exactly the same image?** No. Prompts are adapted for portability, but output and supported controls differ by model and interface.

**How can I get more realistic images?** Generate, inspect the image, identify specific physical/artifact failures, and ask for a targeted revision. A good prompt improves direction but cannot guarantee a perfect result.

## Documentation

- [Skill entry point](skills/anti-slop-image/SKILL.md)
- [Photographer-first shot planning](skills/anti-slop-image/references/photo-shot-plan.md)
- [Photography physics](skills/anti-slop-image/references/photography-physics.md)
- [Landscape, street and other genres](skills/anti-slop-image/references/scene-guides.md)
- [Generator adapters](skills/anti-slop-image/references/generator-adapters.md)
- [Quality audit](skills/anti-slop-image/references/quality-audit.md)
- [Working examples](skills/anti-slop-image/examples/README.md)
- [Regression cases](skills/anti-slop-image/tests/regression-cases.md)

## Philosophy

- Physical plausibility before empty buzzwords like "8K" and "ultra-realistic".
- Art direction can be beautiful and intentional without looking synthetically perfect.
- Respect exact subject, place, identity, edit boundaries and requested text.
- No forced coffee/rain/neon/fog, stock-photo tropes or identical compositions.
- Preserve the user's creative intent; distinguish project preferences from universal photography principles.
- Make source and test limitations explicit.

## Contributing

Issues and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). Add reusable skills under `skills/<skill-name>/SKILL.md`, with clear inputs, outputs, examples and tests. Do not include secret credentials or copied third-party imagery.

## License

MIT — see [LICENSE](LICENSE). External photography resources are linked for attribution; their article bodies and images are not republished here.
