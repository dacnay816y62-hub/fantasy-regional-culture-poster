# Production Reference

## Contents

- Output contract
- Prompt construction
- Rendered poster workflow
- Quality control

## Output contract

For each direction, deliver the completed analysis card before the image prompt. Then provide:

1. final generation prompt
2. readable character deformation logic
3. type/image interaction
4. render-mode plan: direct generation or deterministic post-typesetting
5. variants when requested

## Prompt construction

Build the prompt from the selected direction rather than copying a generic template unchanged. Include:

- region and cultural theme
- primary structure and supporting cue
- dominant character, but state that exact text will be typeset later if the generator is unreliable
- structural transformation source
- composition and whitespace
- material, weather, and light
- restrained palette
- editorial or exhibition context
- exclusions: tourism poster, collage, crowded symbolism, flashy national-trend decoration, full landmark view
- aspect ratio

Compact English scaffold:

```text
Create a refined minimalist cultural poster for [REGION], themed [THEME].
Build the composition around the readable Chinese character [CHARACTER], structurally informed by [PRIMARY STRUCTURE].
Integrate [SUPPORTING CUE] through cropping, masking, negative space, layering, and material transitions.
Use cropped cultural structures rather than full landmarks. Strong hierarchy, generous whitespace, quiet contemporary editorial and exhibition sensibility.
Palette: [PALETTE]. Atmosphere: [TEMPERAMENT].
Reserve clean areas for exact post-typeset Chinese subtitle, keywords, and epigraph.
No tourism advertising, no icon collage, no crowded traditional symbolism, no flashy red-and-gold national-trend styling, no postcard panorama.
Aspect ratio [RATIO].
```

Add model-specific syntax only when the active image tool requires it.

## Select the render mode

Prefer **direct final generation** when the active image model can render legible Chinese and integrated typography, or when the user asks for direct generation, one-shot output, no compositing, or no post-production. Read [direct-generation.md](direct-generation.md) and generate the complete flattened poster in one call.

Use **layered production** when exact copy is contract-critical, the user requests editable typography, or direct generation fails the text gate after reasonable regeneration attempts.

Do not deliver a layered repair as a direct image. If direct mode is locked, regenerate the complete image when text or glyphs fail.

## Layered rendered poster workflow

Use a layered process for stable Chinese typography:

### Layer 1: cultural planning

Lock the theme, character, structure, supporting cue, palette, copy, and composition.

### Layer 2: visual foundation

Generate the spatial, architectural, material, and atmospheric foundation. Reserve the intended character and small-text regions. The image may contain an approximate glyph-shaped structural mass, but do not trust it as final text.

### Layer 3: exact typography

Set the correct Chinese character and all supporting copy using a suitable local font or deterministic graphics workflow. Check encoding, glyph support, punctuation, and line breaks.

### Layer 4: integration

Use masks, clipping, partial occlusion, stroke breaks, and material overlays to reconnect exact typography to the image. Avoid the pasted-on title effect.

### Layer 5: export

Export a high-resolution final plus a review preview. Keep working files in the active project or host-provided output directory. For shared or public workflows, avoid hard-coded personal paths, drive letters, temporary chat folders, or private workspace locations.

## Quality control

Inspect at full size and thumbnail size:

- correct and readable Chinese glyphs
- exact subtitle, keywords, and epigraph
- main character remains dominant
- structural transformation has a stated cultural basis
- no accidental extra text from image generation
- no landmark collage or tourism-ad tone
- genuine whitespace and controlled information density
- coherent palette and material logic
- recognizable difference from other entries in the series

If any Chinese text is malformed, replace it rather than explaining the defect.

For direct generation, replacement means regenerating the whole poster unless the user authorizes layered repair.
