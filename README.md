# Social Skills

Open-source, reusable AI skills for social content creation and publishing.

## Skills

| Skill | Purpose |
| --- | --- |
| [Anti-Slop Image](skills/anti-slop-image/SKILL.md) | Convert plain-language visual ideas into photography-grounded, generator-ready prompts for ChatGPT, Gemini, and other image models. |

## Quick start

1. Open [`skills/anti-slop-image/SKILL.md`](skills/anti-slop-image/SKILL.md) and its referenced files.
2. Load the skill into any AI assistant that supports Markdown skill instructions (or paste the skill instructions into your assistant's context).
3. Ask: **"Use anti-slop-image. Create a realistic photo prompt of an old Vietnamese courtyard in late afternoon, for Gemini."**
4. Copy the generated prompt into the image generator. Generation is optional and must be expressly requested.

This is **prompt engineering and visual quality guidance**, not a promise of indistinguishable realism, a detector of AI-generated images, or a particular vendor's API.

## Philosophy

- A physically plausible photograph can be beautiful without looking synthetic.
- Use camera position, optics, exposure, light, material and context coherently.
- Honor the user's subject, mood, constraints and reference images.
- Avoid repeating clichés, gratuitous HDR, generic cinematic buzzwords and fabricated details.
- Output practical prompts, with limited generator-specific adjustments.
- Distinguish facts, user preferences, and creative proposals.

## Repository layout

```text
skills/
  anti-slop-image/
    SKILL.md
    references/
    examples/
    tests/
```

## Contributing

Issues and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). Add new reusable skills under `skills/<skill-name>/SKILL.md`, with clear inputs, outputs, examples, evaluation criteria, and no secret credentials.

## License

MIT — see [LICENSE](LICENSE). External articles are referenced by link; their text and images are not republished here.
