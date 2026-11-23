# Historical feedback regression cases

Use this list to evaluate prompt rewriting and, when an output image exists, visual QA. These cases are condensed from prior user feedback; identifiers are examples, not downloadable test assets.

| Case | Input intent | Failure to prevent | Expected skill behavior |
| --- | --- | --- | --- |
| CDL-0021/0027 | One photographic scene | Multi-panel labeled collage | Explicit single-frame scene; reject collage |
| CDL-0026 | Room, moving boxes | Generic coffee, flowers, notebook | Preserve room/boxes as main subject |
| CDL-0027 | Vietnamese bread | Missing requested bread | Repeat must-have object in prompt and QA |
| CDL-0032 | Photographic scene | Dashboard infographic | Require photographic composition, not graphics |
| CDL-0033 | Exact square | Near-square noncompliance | Specify 1:1 and verify actual output size |
| TT100-010 | Door, suitcase, keys | Coffee props substituted | Main subject fidelity over style clichés |
| TT100-013 | One apartment/porch scene | Two scenes mixed; wrong text | One scene; exact text verification |
| TT100-059 | Adult male from behind | Wrong cast or frontal face | Conditional project profile enforces casting |
| TT100-074 | Documentary image | Oversized poster typography | No unsolicited large lettering |
| TT100-078 | Natural focus | Uniform sharpness / fake bokeh | Plan focus plane, realistic distance falloff |
| TT100-081 | Quiet photographic story | Motivational poster styling | Exclude decorative motivational text |
| Landscape | Natural mountains | Giant moon, identical peaks, fog filter | Physical sky scale, varied terrain and weather |
| Street | Local market | Generic neon rain, all posed | Candid spatially credible activity |
| Edit | One lamp added | Entire room changes | Preserve protected geometry and content |
| Vendor portability | User chooses Gemini | Fake negative_prompt API syntax | Natural text and qualified capabilities |

## Suggested manual acceptance

For each case inspect the **written prompt** before attempting generation:
1. Does it retain all essential nouns and constraints?
2. Does camera/light/focus have a coherent physical story?
3. Are avoidance clauses specific rather than word salad?
4. Are project-specific assumptions loaded only when relevant?
5. Is the text directly usable in ChatGPT Images, Gemini or a generic generator?

Visual checks require real generated outputs; prompt-only success is not a claim that the image was rendered or passed QA.
