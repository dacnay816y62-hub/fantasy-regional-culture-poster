# MODE B：地域编辑海报模式 / Regional Editorial Poster Mode

MODE B is for regional editorial posters where the city image, cultural reasoning, and text hierarchy carry the work. It is not a giant-character mask poster and not a normal city photography poster.

One-line principle:

> The city is the subject, the typography is the entry point; cultural reasoning drives the composition, and regional structure changes the layout.

## When to use MODE B

Prefer MODE B when the user wants:

- stronger editorial or magazine feeling;
- richer text hierarchy and cultural explanation;
- city culture to be clear without relying on one huge glyph;
- different compositions for different cities rather than a fixed template;
- larger but controlled city-name typography;
- cultural keywords, short prose, material notes, or atmosphere notes;
- a cultural research poster, exhibition poster, or editorial city poster.

Do not use MODE B for:

- pure typography experiments;
- fully textless cultural posters;
- tourism templates;
- simple landmark photography;
- a layout that only swaps city name and image.

## Required reasoning flow

Before generating each image, complete these six decisions internally.

### Step 1: Core cultural judgment

Choose exactly one core judgment for the city. Do not use vague claims such as “deep culture” or “famous landmark”.

Examples:

- Shanghai: a time crack between old lane houses and the modern riverfront.
- Harbin: conflict between cold ice material and European street-arch structure.
- Urumqi: everyday bazaar courtyards and huge snow mountains existing in the same visual field.
- Guiyang: humid mountain terrain where corridors, slopes, and settlements connect.
- Lanzhou: Yellow River line, iron bridge, and riverbank walking order forming horizontal rhythm.

### Step 2: Primary spatial prototype

Choose one main spatial prototype:

- gate slit
- alley
- continuous arcade
- courtyard gate
- rain corridor
- stone steps
- bridge deck
- riverbank
- city wall
- mountain pass
- roof window
- repeated window apertures
- deep courtyard
- stepped skyline

Each poster gets only one primary spatial prototype.

### Step 3: Dedicated composition action

Every city must have a composition action that cannot be reused unchanged for three other cities.

Examples:

- Shanghai: a vertical “mirror crack” between Shikumen and river reflection.
- Harbin: ice blocks replacing parts of a street-arch wall.
- Urumqi: a courtyard gate frames bazaar life and terminates in the Tianshan snow line.
- Guiyang: wet stone steps lead the eye into a rain corridor and karst hill structure.
- Lanzhou: Yellow River line, iron bridge truss, and riverbank path form three horizontal layers.

If the action can be applied to three or more cities without modification, it is a template and must be revised.

### Step 4: Four visual information layers

Richness must come from four controlled layers, not from landmark stacking:

1. **Main structure**: gate, bridge, alley, corridor, courtyard, wall, riverbank, etc. Choose one.
2. **Material layer**: brick, ice, rammed earth, timber, iron, stone, glass, wet floor, etc. Choose one or two.
3. **Climate layer**: rain, fog, wind, cold light, humidity, highland sun, river wind, etc. Choose one.
4. **Daily-life trace**: one lamp, one boat, one textile, one window, grape shadow, one passerby, etc. At most one focus.

Never pile multiple landmarks, legends, folk objects, or symbolic props into the same image.

### Step 5: Typography intervention level

In MODE B, Chinese typography is not the main image container. It can intervene in three limited ways:

- **B1 Regional title typography**: the city name is enlarged as the visual anchor, usually occupying about 18–30% of the text-area height.
- **B2 Boundary borrowing**: the border between text area and image area may borrow a city silhouette, architectural section, bridge pier, mountain ridge, or skyline contour.
- **B3 Local stroke tuning**: only 10–20% of the city-name glyph structure may be adapted. It must remain instantly readable.

Avoid:

- cropping the whole photograph into a giant Chinese character;
- filling separate strokes with unrelated city elements;
- letting the title overpower the city image;
- illegible calligraphy or model-garbled Chinese;
- using the same calligraphic style for every city.

### Step 6: Layout reasoning

Do not choose a template first and then fill it. Look at the primary image structure first, then decide text position.

Allowed layout families:

- left text / right image
- top image / bottom text
- central image cut
- diagonal structure
- bottom text band
- narrow slit composition
- deep gate-hole composition
- horizontal bridge composition
- surrounding boundary
- partial bleed image

The layout must be derived from the city structure, not randomly varied.

## Regional typography rules

Regional title design must stay within 10–20% structural adaptation.

Examples:

- Harbin: high-contrast, narrow, cold-edged; terminals may have slight ice-cut facets.
- Urumqi: heavier, flatter, open; turns can borrow adobe wall or courtyard gate cuts.
- Guiyang: slightly narrow, humid, upward-guiding; rhythm can borrow rain lines and bridge eaves.
- Lanzhou: horizontally stretched and stable; strokes can borrow river flow and iron-bridge folds.
- Shanghai: urban, restrained, precise; negative space may borrow Shikumen arches without copying retro type.
- Kunming: open, bright, light; strokes keep breathing room and highland wind cuts.

Regional typography should come from spatial structure and material behavior, not symbol stickers.

## Text hierarchy

MODE B should keep five information levels:

1. **City name**: largest text; 2–4 Chinese characters; horizontal or vertical; must be proofread.
2. **English city name**: optional, small, index-like.
3. **Theme phrase**: 4–8 Chinese characters.
4. **Short paragraph**: 30–55 Chinese characters; explains the city spatial relationship, not empty lyricism.
5. **Keywords / notes**: one compact group of 3–5 keywords or material/climate notes.

Avoid meaningless labels such as:

- DESIGN LOGIC
- CULTURAL CLUES
- CITY CULTURE RESEARCH
- decorative information icons
- repeated seals
- meaningless English columns

Use them only when they have real editorial value.

## Image/text ratio

Recommended ratio:

- city image: 55–68%
- text + whitespace: 32–45%

Main title:

- normal: 18–24% of the text-area height
- strong: 25–30%
- never more than 35% of the whole poster

Text amount:

- not fewer than 45 Chinese characters;
- not more than 110 Chinese characters;
- must form a clear hierarchy;
- no scattered microcopy added only for “richness”.

## Cultural boundary rules

One important identifier of MODE B is the “cultural boundary” between text area and image area.

Allowed boundary sources:

- city skyline contour
- mountain ridge
- bridge truss
- corridor eave
- city-wall section
- ice-brick section
- Shikumen facade
- riverbank curve
- roof rhythm
- stepped terrain

The boundary must:

- be one continuous whole;
- have a clear source;
- relate to the main image;
- avoid repeated landmark icons;
- avoid sticker-like decorative edges;
- avoid the same zigzag cut on every city.

## Generation and post-production workflow

### Generation stage

Prefer generating:

- no-text visual foundation, or
- minimal text only, or
- main structure, cultural boundary, material, climate, and light.

### Post-typesetting stage

Use real typography for:

- city name;
- theme phrase;
- short paragraph;
- keywords;
- English index.

This makes MODE B more suitable for `layered` production when exact Chinese copy is important. Direct generation is allowed only when the user explicitly wants one-shot image output and accepts text imperfections.

### Required checks

- Is the city name correct?
- Is all Chinese readable?
- Is English spelling correct?
- Are the city cultural elements coherent?
- Could the main image be swapped into another city?
- Is the boundary repeated mechanically?
- Is regional typography still readable?
- Does the work look like a template swap?

If any three checks fail, redo the reasoning and regenerate.

## MODE B prompt scaffold

```text
Create a premium vertical editorial cultural poster for [CITY].

The city image is the main subject, not a giant Chinese character.
Use [SPATIAL PROTOTYPE] as the primary spatial structure.
The composition must express [CULTURAL JUDGMENT].
Introduce [MATERIAL] and [CLIMATE] as supporting layers.
Include only one subtle daily-life trace: [LIFE TRACE].

The boundary between the text area and image area must be derived from
[BOUNDARY SOURCE] as one continuous silhouette, never repeated icons.

Reserve a clear editorial text area for:
- a large city name,
- a 4–8 character theme phrase,
- a 30–55 Chinese character paragraph,
- one compact keyword or material/climate note.

The city name should use a refined Chinese Song-style typeface with
10–20% regional structural adaptation inspired by [FONT LOGIC],
while remaining fully legible.

No giant character mask.
No landmark collage.
No repeated skyline icons.
No tourism advertising.
No generic Chinese-style template.
No decorative information icons.
No meaningless English labels.
No model-generated long Chinese text.
Vertical 3:4.
```

## Difference from MODE A

### MODE A / structural character poster

- Chinese character structure is the main visual body.
- City elements grow into the glyph.
- Best for cultural typography experiments.
- Strongly emphasizes glyph skeleton, strokes, counterforms, and structural fusion.

### MODE B / regional editorial poster

- City space is the main visual subject.
- City name is an editorial anchor.
- Typography receives limited regional adaptation.
- Strongly emphasizes cultural reasoning, image/text hierarchy, dedicated boundaries, and magazine-like editorial feeling.

Selection rule:

> Use MODE A when the user wants “the character becomes the city”.  
> Use MODE B when the user wants “the city is editorially interpreted through culture”.
