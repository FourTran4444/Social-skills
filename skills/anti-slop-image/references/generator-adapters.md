# Generator adapters — pre-generation prompt output

The skill prepares the prompt **before** generation. All adapters share the same photographic scene specification; capabilities vary and identical results are not guaranteed.

## Universal scene contract

Describe subject/action, environment, spatial relationships, camera placement/framing, focus and depth cues, light and exposure, surfaces/materials, story, aspect ratio, necessary text or preservation instructions, and specific potential artifact prevention. Complete the prompt so the image generator need not know the skill itself.

## ChatGPT Images

Return a natural-language **ready-to-paste prompt** for ChatGPT's image generator. Specify composition, ratio and exact requested text clearly; avoid extraneous pseudo-control parameters. This skill's job ends with prompt preparation. The caller may invoke the image generator separately when explicitly requested.

## Gemini

Return the same physically coherent scene with clear positive instructions, requested aspect ratio and exact text when needed. Avoid unverified negative-prompt fields, weight syntax or undocumented feature promises.

## Claude

Claude may be used to **run this skill and write the final prompt**, which the user then supplies to a supported image generator. Do not imply that prompt-writing in Claude itself always generates the photographic image.

## Generic model

Favor portable natural language and a compact contextual avoidance statement; provide a separate negative-prompt block only if the chosen interface supports it. Do not invent model versions, settings or APIs.

## Pre-generation modes

- **prompt-only (default):** final, copy-ready image prompt.
- **prompt + alternative:** final prompt with one optional framing/lighting alternative.
- **edit-prompt:** complete instructions to be applied *before* editing an existing supplied image.
- **rewrite-before-generation:** correct a draft prompt or use user feedback/reference imagery to create a new, fully preflighted prompt.

The adapter does not run post-generation quality scoring, generated-image forensics or claim a rendered image passed an audit.
