# Contributing

Thanks for improving Social Skills.

## Add or update a skill

1. Create `skills/<kebab-case-name>/SKILL.md` with YAML frontmatter `name` and `description`.
2. Document trigger conditions, input/output behavior, safe defaults and success/failure cases.
3. Add examples under `examples/` and regression tests under `tests/`.
4. Keep shared rules universal; project-specific preferences belong in optional profiles.
5. Prefer references and short paraphrases over copied articles or third-party images.
6. Avoid hardcoding paid APIs, tokens or model-only features as mandatory.
7. Explain what was actually tested. Do not mark image-generation tests passed when only prompts were reviewed.
8. Submit a PR explaining the intended behavior, files changed and sample inputs/outputs.

## Style

Write in clear Markdown; use portable prompts. We welcome English/Vietnamese examples. Keep explicit author attribution and link to external sources when relevant.

## Licensing

By contributing, you agree that your contribution is offered under this repository's MIT license and that you have rights to contribute the content.
