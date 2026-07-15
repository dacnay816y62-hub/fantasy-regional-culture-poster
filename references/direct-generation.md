# Direct Final Generation

Use this workflow when a capable image model must generate the complete flattened poster in one call, including the dominant character, imagery, material, exact copy, masking, and layout.

## Contents

- Lock the contract
- Build the prompt in five blocks
- Complete scaffold
- Batch execution
- Proven structural patterns

## Lock the contract

- Output one finished image; no placeholders, reserved post-production zones, local typography, masking pass, or compositing.
- Prefer one culturally condensed exact Chinese character as the dominant visual body. Make it occupy about 45-60% of the poster and remain broadly readable at thumbnail size. Use a full exact place name only as a fallback when the single-character route becomes misleading, generic, or unreadable.
- Merge the character with one cultural structure through masking, negative space, partial occlusion, material transitions, nested architecture, or spatial cuts. The character-image relationship is the core value of the poster.
- Pass the text-removal recognition gate: if all city labels and explanatory copy were covered, the remaining image still needs one non-substitutable local cultural mechanism. Generic glass, water, bridge, skyline, fog, concrete, neon, or clean editorial layout is insufficient unless tied to a place-specific typology, craft, terrain, climate behavior, or street-life structure.
- Keep one supporting cue, genuine whitespace, no more than two type families, and sparse margin copy.
- Add richness primarily through custom typography before adding more imagery: controlled stroke weight, serif shape, counter space, terminals, measured cuts, edge wear, material texture, and title spacing.
- Keep the result closer to an exhibition key visual, art-book cover, or cultural research poster than to a movie poster, commercial campaign, or tourism KV.
- Preserve conceptual tension. A strong single-character direct result with minor model imperfections can be preferable to a clean but ordinary full-name wall poster.
- Keep the result contemporary, not rustic. Avoid heritage-board mood, folk-tourism styling, dusty ochre palettes, faux-ancient rubbing, old-wall nostalgia, seal-like layouts, heavy stone inscription texture, and museum-souvenir aesthetics unless explicitly requested.
- If text fails, regenerate the entire poster. Switch to layered repair only with user approval.

## Build the prompt in five blocks

### 1. Direct-generation declaration

State that this is a `DIRECT FINAL IMAGE GENERATION` task. Require the model to generate artwork, exact typography, masking, and layout together in one pass. Explicitly prohibit placeholders and post-production zones.

### 2. Dominant character

Provide the exact character in Chinese quotation marks, its target scale, and its evidence-based transformation:

```text
Render one huge, exact, perfectly legible Chinese character: “{CHARACTER}”.
It must occupy roughly 50% of the poster and remain readable at thumbnail size.
Transform its strokes according to: {CHARACTER_LOGIC}.
Merge it physically with {PRIMARY_STRUCTURE} through masking, negative space,
partial occlusion, and material transitions. It must not look pasted on top.
```

### 3. Exact-copy block

Put every required string on its own labeled line. Tell the model to use only this copy and invent nothing:

```text
Typeset only the following exact copy, with no invented words or duplicate characters:
City: “{CITY}”
Theme: “{THEME}”
Keywords: “{KEYWORDS}”
Epigraph: “{EPIGRAPH}”
English metadata: “{ENGLISH} / CITY CULTURE”
```

Use a contemporary Chinese Song/serif or restrained custom display treatment for the dominant title, and a quiet Chinese sans-serif or small Song style for supporting copy. Keep small copy in compact aligned groups near the margins. The title may be custom-designed through stroke weight, serif shape, counters, terminals, measured cuts, worn edges, or material behavior, but every Chinese character must remain instantly readable.

### 4. Cultural art direction

Specify exactly one primary structure, one supporting cue, one temperament, composition, palette, materials, climate, and light. Demand cropped structural evidence rather than a landmark panorama.

### 5. Negative constraints

Include place-specific exclusions plus:

```text
No tourism advertising, no postcard panorama, no icon collage, no crowded symbolism,
no generic calligraphy-and-seal shortcut, no flashy red-and-gold national-trend styling,
no extra text, no gibberish, no misspelled Chinese, no mockup frame.
```

## Complete scaffold

```text
Create one finished, flattened, print-ready Chinese cultural poster for {CITY} ({ENGLISH}).
This is a DIRECT FINAL IMAGE GENERATION task: generate the complete artwork, exact typography,
architectural imagery, masking, and layout together in one pass. Do not leave placeholders and
do not reserve space for post-production.

TYPOGRAPHY IS THE PRIMARY VISUAL BODY.
Render one huge, exact, culturally condensed Chinese character: “{CHARACTER}”. It must occupy roughly
45-60% of the poster and remain broadly readable at thumbnail size. Transform it structurally
according to: {CHARACTER_LOGIC}. Merge it physically with {PRIMARY_STRUCTURE} through masking,
negative space, partial occlusion, nested architecture, material transitions, or spatial cuts. It
must not look pasted on top. Use a full place-name title only if the single-character idea fails;
when using a full place name, preserve the same level of spatial tension and typographic invention.

Typeset only the following exact copy, with no invented words or duplicate characters:
City: “{CITY}”
Theme: “{THEME}”
Keywords: “{KEYWORDS}”
Epigraph: “{EPIGRAPH}”
English metadata: “{ENGLISH} / CITY CULTURE”

Use no more than two type families. Check every Chinese glyph carefully. Keep small copy sparse in
compact aligned groups near the margins. Enrich the clean structure through the title's custom
typographic system: deliberate stroke weight, serif or terminal design, counter spacing, measured
cuts, material edge behavior, and precise title spacing. Keep the title readable before making it
clever.

Cultural direction: {THEME}. Primary structure: {PRIMARY_STRUCTURE}. Supporting cue: {SUPPORT}.
Temperament: {TEMPERAMENT}. Composition: {COMPOSITION}. Palette: {PALETTE}. Use real material detail,
cropped structures, boundaries, thresholds, apertures, wall cuts, infrastructure fragments, light,
and genuine whitespace. High-design contemporary editorial and exhibition design, strong hierarchy,
one visual center. The primary structure must be non-substitutable local evidence: after covering the city name and all small text, the viewer should still see a culturally specific mechanism from this place. Prefer abstract spatial section, material cut, void, or threshold over a heroic
building facade. Do not make the image merely a clean wall with a title; the poster needs one strong
mechanism, such as gate-void cutting through the glyph, arcade rhythm swallowing strokes, bridge
piers splitting the character, water reflection entering counters, kiln seams shaping strokes, plane-tree shadows crossing a city-wall aperture, lane-house stone gates compressing the glyph, arcade columns trapping humid river light, or layered stairs interrupting
the title. Keep the palette and material language contemporary: fog white, cool grey, deep green-black,
glass reflection, wet concrete, brushed metal, polished stone, abstract water plane, precise shadow,
or restrained sodium/neon accent. Avoid default earth yellow, sepia, cracked plaster, old brick,
heavy rubbing texture, and nostalgic heritage-board atmosphere.

Avoid: {PLACE_EXCLUSIONS}. No tourism advertising, no postcard panorama, no icon collage, no crowded
symbolism, no generic calligraphy-and-seal shortcut, no flashy red-and-gold national-trend styling,
no commercial campaign polish, no movie-poster drama, no cinematic spectacle, no centered heroic
landmark facade, no rustic cultural-promo style, no dusty ochre nostalgia, no faux-ancient rubbing,
no old-wall-only composition, no museum souvenir styling, no generic modern-city abstraction that becomes unrecognizable without the text, no extra text, no gibberish, no misspelled
Chinese, no mockup frame. Vertical 2:3.
```

## Batch execution

1. Complete global cultural and visual deduplication before rendering.
2. Lock one render mode for the whole series.
3. With GPT Image 2 Mode A, use `1024x1536`, `quality=high`, `background=opaque`, and PNG output.
4. Use two concurrent generations by default. Reduce to one if the gateway returns rate limits or transient upstream errors.
5. Save each rendered prompt beside the series drafts and each direct PNG in a distinct final-export directory.
6. Inspect the dominant character and all exact-copy lines in every image. Regenerate only failed entries; do not composite repairs into a direct series.

## Proven structural patterns

- ceremonial axis + gate void + long shadow
- wall thickness + rammed-earth strata + gate cut
- lane compression + stone gate + tidal reflection
- garden window + borrowed scenery + water reflection
- swallowtail ridge + red brick + maritime line
- arcade rhythm + humid river light
- courtyard void + eave + bamboo shadow
- stair ascent + bridge pier + river fog
- highland sky aperture + mountain layers + tile edge
- brick arch + ice plane + winter light
