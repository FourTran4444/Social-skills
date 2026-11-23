# Social Skills

Open-source, reusable AI skills for creating better social and visual content. Each skill is a collection of **Markdown instructions, references, examples and tests**—not an image model, plugin, or paid API.

## Available skills

| Skill | What it does | Start here |
| --- | --- | --- |
| **Anti-Slop Image** | Turns a simple idea into a realistic, photography-grounded prompt for ChatGPT Images, Gemini and other image generators. Also prepares preservation-aware image-edit prompts **before edits are executed**. | [Read the skill](skills/anti-slop-image/SKILL.md) · [Examples](skills/anti-slop-image/examples/README.md) |

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
│   ├── quality-audit.md        # Before-generation prompt checks
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
| **Claude chat / Projects** | Upload the skill instructions and relevant references to a chat, or add them to Claude Project knowledge with project instructions telling Claude to use `SKILL.md`. See [Claude setup](#claude-chat-and-claude-code). |
| **Claude Code** | Install the whole skill folder in `~/.claude/skills/anti-slop-image/` for personal use or `.claude/skills/anti-slop-image/` for one project; run `/anti-slop-image`. See [Claude setup](#claude-chat-and-claude-code). |
| **Coding agent with skills support** | Put the **whole** `skills/anti-slop-image/` directory in the tool's documented skill location. The specific install path and discovery behavior are agent-dependent. |
| **Other AI assistant** | Paste `SKILL.md` and the applicable references, then give your image idea. Long context may require selecting only the relevant references. |

These are **manual/compatible loading approaches**, not verified automatic GitHub integrations. If your assistant cannot read local files or URLs, paste the contents explicitly.

### Claude chat and Claude Code

#### Claude chat / Projects (no terminal required)

1. Download this repository or open the Markdown files on GitHub.
2. In [Claude](https://claude.ai/), use the file attachment control to provide `skills/anti-slop-image/SKILL.md` **plus the relevant files in `references/`**. If your file-upload interface does not accept a `.md` file, paste its content or provide it as plain text.
3. For repeated use, create a **Project**, add the skill documents to Project knowledge, and set project instructions such as: `For image prompt creation or pre-generation prompt realism checks, follow the attached anti-slop-image SKILL.md and consult the appropriate references. Return a copy-ready prompt by default.`
4. Ask for a prompt and take it to your chosen image generator; Claude chat should not be assumed to offer a native photographic image-generation tool.

**Example — Claude chat:**

```text
Use the attached anti-slop-image skill.
Write a copy-ready image prompt for an authentic Vietnamese street scene
at 5 PM with a bicycle leaning against an old yellow wall.
Keep the camera position, light direction, materials and focus physically plausible.
Target image generator: generic. Return only the prompt, not an image.
```

Claude Project knowledge and instructions can be reused across chats inside that Project; a single chat attachment is not a universal skill installation.

#### Claude Code — install as a real slash-invokable skill

Claude Code discovers skills from supported skill directories. After cloning or downloading the repo, run the following commands **from the repository root**:

**Personal installation** — available in your local Claude Code projects:

```bash
mkdir -p ~/.claude/skills
cp -R skills/anti-slop-image ~/.claude/skills/anti-slop-image
```

**Project-only installation** — run from the target project's root (adjust the source path to your downloaded repository):

```bash
mkdir -p .claude/skills
cp -R /path/to/Social-skills/skills/anti-slop-image .claude/skills/anti-slop-image
```

The **entire folder** must be copied, not just `SKILL.md`, because its Markdown instructions refer to adjacent `references/`, `examples/` and `tests/` files.

Then start Claude Code in the relevant project:

```bash
claude
```

Invoke the skill explicitly:

```text
/anti-slop-image Create a documentary photography prompt for
an old bicycle on a quiet Vietnamese street at sunset.
Target: ChatGPT Images. Prompt only.
```

Claude Code may also select the skill automatically for matching requests based on the `SKILL.md` description. Use `/skills` to inspect discovered skills if available in your Claude Code version. If the skill is not discovered, check the directory layout and restart the session. This repository stores source skills in `skills/` for portability; **that folder is not itself an automatic Claude Code install location**.

Official docs: [Claude Code skills](https://code.claude.com/docs/en/skills) · [Claude Projects](https://support.claude.com/en/articles/9519177-how-can-i-create-and-manage-projects) · [Claude file uploads](https://support.claude.com/en/articles/8241126-upload-files-to-claude).

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

### 5. Improve your prompt before generation (optional)

Before running the image generator, you can ask the skill to check and expand your **draft prompt**, not a rendered result:

```text
Use anti-slop-image to strengthen this draft prompt BEFORE creating the image.
Check that the scene, camera, depth of field, exposure, shadows, reflections,
background objects, textures and ground contact are described coherently.
Resolve contradictions and return one complete prompt for Gemini.
Do not generate, inspect or score an image.
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
Use the prompt in the chosen image generator (outside this skill)
```

The **only skill workflow** is **idea → preflighted prompt**. All optical, exposure, material and anti-slop checks happen before handing the prompt to an image generator. Image generation, editing, publishing and uploads are **not automatic**. The skill does **not** claim to detect AI images with certainty or to force any model to obey exact camera metadata.

## Common questions

**Can Claude Code use this as a real skill?** Yes—install the entire skill directory under a supported `.claude/skills/` path and invoke `/anti-slop-image`. Claude chat instead uses attached documents or Project knowledge.

**Can I just send a link to this repository?** Sometimes, if an assistant can access the link and follow its referenced files. Reliable usage requires making the skill contents available to the assistant.

**Do I have to specify 35mm, f/5.6, ISO, etc.?** No. State what you want to see. Camera numbers are optional, physically coherent planning aids—not magic realism tokens.

**Does it work only with Vietnam, coffee images or Facebook?** No. It is general-purpose. The Vietnamese Facebook profile is **optional** and is not loaded as a universal restriction.

**Will ChatGPT and Gemini produce exactly the same image?** No. Prompts are adapted for portability, but output and supported controls differ by model and interface.

**How can I get more realistic images?** Ask the skill to enrich and reconcile your idea **before generation**. It builds a physically coherent prompt with safeguards for lighting, optics, shadow geometry, materials and composition. A good prompt improves direction but cannot guarantee the image model's output.

## Documentation

- [Skill entry point](skills/anti-slop-image/SKILL.md)
- [Photographer-first shot planning](skills/anti-slop-image/references/photo-shot-plan.md)
- [Photography physics](skills/anti-slop-image/references/photography-physics.md)
- [Landscape, street and other genres](skills/anti-slop-image/references/scene-guides.md)
- [Generator adapters](skills/anti-slop-image/references/generator-adapters.md)
- [Pre-generation prompt safeguards](skills/anti-slop-image/references/quality-audit.md)
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
