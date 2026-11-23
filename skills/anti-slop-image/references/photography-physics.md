# Photography Physics — practical decisions

Use these as **plausibility checks**, not a camera-parameter incantation.

## Scene geometry and optics
- Camera placement (position, height, distance, angle) determines perspective. Focal length changes field of view at a fixed position; changing distance to reframe changes apparent near/far size relationships.
- Specify sensor format or state "full-frame equivalent" only if numerical focal length is needed. Normal, wide, and telephoto perspectives have different framing implications.
- Depth of field depends on aperture, focal length, subject distance, sensor format and display criterion. Do not impose fake background blur arbitrarily. Subjects at similar focus distances generally should render with similar sharpness unless another effect explains the difference.
- Wide landscape scenes may benefit from deeper focus; portraits or details may warrant shallower focus. Neither is mandatory.
- Natural atmosphere often reduces distant contrast/clarity; this depends on weather, distance and visibility, not on a compulsory haze filter.

## Exposure and motion
- Exposure results from the scene light, aperture, shutter speed and gain/ISO; settings must be mutually plausible.
- A fast shutter can freeze motion. A slow shutter can blur moving subjects or the camera. Stationary objects and moving subjects should not blur identically without a physical reason.
- Night scenes require plausible motivated light sources, sufficiently long exposure, high sensitivity, or other explained techniques. Do not light every dark surface uniformly.
- Grain/noise and dynamic range are choices or environmental consequences, not mandatory markers of "real".
- HDR, long exposures and multi-exposure composites can be legitimate, but must be declared when a single-exposure documentary aesthetic is requested.

## Light, color and material
- Identify dominant sources, directions, approximate sizes and relative brightness. Hard light makes defined shadows; larger diffuse sources make softer shadows.
- Reflections must follow camera position, surface geometry, roughness and light source; rough surfaces scatter differently from polished ones.
- White balance can be creative and mixed-source color temperatures are plausible. Do not force all lights into a single hue.
- Histograms do not need to be centered. Silhouettes and high/low-key exposures can be intentional.
- Avoid global clarity, artificial hyperdetail, excessive local contrast, repeated texture and unrealistically flawless materials.

## Camera settings: examples, not hard rules
- Quiet courtyard, bright afternoon: moderate wide field of view; f/5.6–f/11, low ISO, shutter compatible with handholding.
- Candid evening market: 28–50mm equivalent, shutter matched to movement, ISO/light matched to conditions.
- Detailed still life: choose a focus plane that preserves the intended texture; shallow depth only if the composition benefits.
- Moon: angular size follows geometry; telephoto framing can make it dominant, but an oversized moon behind a wide landscape may imply a composite. Never mislabel a composite as an untouched single photo.

**Final decision:** Would a real camera placed in this location, seeing these materials and lights, plausibly record the described result?

## Optical realism extensions (v1.1)

These are conditional photographic relationships, **not universal fixed-number requirements**.

### Focus surface, depth of field and hyperfocal strategy
- Focus is defined by subject distance and a lens-dependent best-focus surface; practical focus surfaces may exhibit curvature/field aberrations. Do not treat blur as a pasted 2D mask or demand one globally flat focus plane.
- Defocus generally increases away from best focus, but perceived blur depends on optical design, aberrations, depth, sensor format and final viewing size; do not require strictly monotonic blur at every pixel.
- A wide aperture such as f/1.2–f/2 can yield shallow depth at close portrait distances but **does not guarantee** razor-thin focus at every subject distance. f/2.8–f/5.6 can balance subject and context. f/8–f/16 may provide deeper focus, depending on subject distance and equipment, while diffraction can reduce fine-detail sharpness.
- For landscapes, consider a deliberately selected focal distance / hyperfocal-style strategy where appropriate; don't blindly prescribe hyperfocal focusing or a fixed 1/3–2/3 DoF rule.

### Bokeh and optical artifacts
- Out-of-focus highlights depend on aperture geometry, lens design, focal length, focus distance and background distance. Shapes may be rounded, polygonal, cat-eye or ringed for **some** real optical designs; these are not inherently artificial. Reject repeated/stamped, inconsistent or unjustified patterns rather than all ring bokeh.
- Vignetting may appear naturally, often more conspicuously wide-open, but is not compulsory and should not look like an added black border.
- Halation/bloom can appear around sufficiently bright highlights with optical/film/diffusion causes; don't paint uniform glow over dark objects.
- Chromatic aberration occurs on certain high-contrast edges depending on optical behavior; keep it plausible, not a random RGB outline.
- Lens flare/veiling glare needs a luminous source at a relevant angle or plausible off-frame illumination; flare form should be consistent rather than decorative.

### Field of view, perspective and proportions
- A 14–35mm **full-frame-equivalent** lens offers a relatively wide field of view; at a close camera position, near objects can dominate. The perspective difference comes from *camera position*, not focal length alone.
- A 35–50mm equivalent field of view often supports environmental documentary compositions, but does not replicate human vision in every respect.
- A 70–135mm or longer telephoto equivalent provides tighter framing at a given position; the familiar compressed appearance typically results from moving farther away to maintain subject framing, not intrinsic lens-induced compression.
- Camera tilt can make parallel verticals converge in perspective. Corrected/shift lenses and post-processing can change this; don't insist all verticals must be plumb.

### Shutter, moving parts and camera motion
- Freeze or blur subject components according to *relative movement* and exposure time: fingers, wheels, water, hair, fabrics and moving vehicles may differ.
- Fast shutters (~1/500–1/4000s, conditions permitting) often freeze action; slower shutter choices (~1/60 to multi-second) can reveal directionally credible blur. These are examples, not thresholds guaranteed to work in every scene.
- Stationary architecture may still blur when the **camera** moves or shakes; with panning, tracked moving objects may be sharper than the stationary background.
- Do not warp anatomy or rigid geometry merely to indicate movement.

### Exposure, dynamic range and noise
- Respect highlight roll-off, plausible clipping and shadow separation for scene brightness and capture medium; pure white/black pixels are not automatically wrong.
- Mixed temperature sources may produce warm practical light alongside cooler sky/window light, but Kelvin values are approximate, not requirements.
- Noise/grain depends on sensor signal, processing, exposure and film choice; do not require high-ISO noise or place a texture overlay that contradicts the scene.

### Motivated lighting, grounding and tactile materials
- Shadow sharpness depends largely on the light's *apparent angular size* at the subject. Direct sun and small lamps often produce harder shadows; cloud cover, large windows and diffusion make softer transitions.
- Surfaces touching usually exhibit plausible ambient occlusion/contact shading, but diffuse light may make dark contact shadows subtle or nearly invisible. Verify physically credible grounding, not mandatory black halos.
- Bounce light contributes fill and sometimes neighboring surface color; avoid assuming every bounce is strongly tinted.
- Skin can show believable pores, fine hairs, subtle irregularity, and natural specular areas without artificially adding exaggerated blemishes. Fabric folds respond to gravity, body motion and construction.
- Paper/cardboard have edge thickness, fibers, folds and print behavior; glass has thickness/refraction/reflection; metals vary in roughness/specularity; wood shows coherent grain and end grain. Material appearance should fit image scale and camera distance, not expose every microscopic detail.

## Sensor Dynamic Range & Anti-HDR Rules

- **No Synthetic HDR Tone-Mapping:** Respect believable camera sensor dynamic-range limits. In a single exposure balanced for bright outdoor sunlight, a deep, unlit interior (open doorway or shaded room) should usually retain substantially darker tones with limited visible detail—not appear artificially lifted and evenly illuminated like a 3D render. Exception: motivated interior lighting, bounced sunlight, a deliberate exposure choice, or a disclosed multi-exposure/composite technique can reasonably preserve more interior detail.
- **True Z-Depth Plane Consistency:** Focus and depth-of-field blur must respond continuously to actual three-dimensional subject distance and the lens's focus surface. Avoid arbitrary 2D masks, sudden patches of blur on connected objects at comparable focal distances, or sharp foreground objects with inexplicably blurred sections at the same distance. Allow genuine lens field curvature, occlusion, motion, and differing fine-detail contrast.
- **Organic Micro-Imperfections over Procedural Texture:** Wear, moss, peeling paint and wood grain should arise from plausible mechanisms—water runoff, exposure to sun and moisture, repeated handling, contact, or foot traffic—rather than evenly distributed procedural speckles or repeated noise. Do not add aging or dirt where a new or clean surface was requested.
