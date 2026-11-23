# Generator adapters

All adapters share the same **scene specification**. Never promise identical results across models. Model capabilities change; follow the user's current interface/API documentation.

## Universal scene contract

Describe, in natural language: subject and action; setting and concrete objects; camera placement and framing; focal priority and depth cues; light and exposure character; texture/material; mood/story; aspect ratio; exact text or preservation boundaries; artifact avoidance.

## ChatGPT Images

Prefer a coherent paragraph with clear visual intent and explicit image-edit preservation where needed. Specify requested aspect ratio and exact on-image text. When the user asks the assistant to **generate** (rather than only write a prompt), invoke the available image-generation capability instead of presenting only a prompt.

## Gemini image generation

Use the same scene contract, direct spatial constraints and natural-language style. Put specific typography, composition, reference image and aspect requirements where the connected Gemini product supports them. Avoid inventing control flags or claiming a given Gemini model supports a particular negative-prompt parameter.

## Generic generator / uncertain model

Return a portable positive prompt plus a compact "avoid" sentence. Include a separate negative-prompt field **only if the destination interface supports it**. Avoid vendor-specific weighted tokens, special syntax, unsupported seeds, model version guesses or camera metadata hallucinations.

## Prompt design rules

- Concrete sensory and spatial information beats "masterpiece, 16K, award winning, trending".
- Prefer positive composition requirements before exclusions.
- Limit competing directions. If the user says candid street photo, don't also force flawless editorial studio lighting.
- Use camera numbers sparingly and consistently; explain what they accomplish.
- For text in images, quote exact characters and include typography hierarchy. Some generators still fail at spelling; advise post-generation verification.
- For reference images, explicitly say what to preserve versus what to alter.
- If the result looks synthetic, revise the *scene/physics* rather than adding more superlative adjectives.

## Optional answer modes

- **prompt-only**: only the copy-ready prompt.
- **prompt + options**: main prompt plus one alternative framing or light decision.
- **audit + rewrite**: defect list and corrected prompt for an uploaded image.
- **generate**: prompt architecture followed by generation when a tool exists and the user requested it.
