# DCC Reference Edition — Canonical Image Generation Standard

## Purpose
This is the persistent visual-generation contract for the DCC Reference Edition app. New chats should read this file before generating or regenerating any character, creature, boss, or grouped spread.

## Canonical visual anchor
Primary reference image: `assets/mordecai-book1-spread.webp` — the approved Mordecai Book I spread already used by the app.

The anchor is the baseline. Every new image must begin by explicitly re-anchoring to it before introducing the subject brief. Do **not** let the most recent generated image become the implicit template.

### Fixed visual grammar
- Wide, single-spread dossier composition, designed to behave as one image in the app.
- Target geometry: approximately **1180 × 680** (about 1.735:1); generate wide landscape and crop/fit only if needed after generation, never by stretching the character art.
- Left side: large cinematic hero strip with the subject in a themed environment.
- Right side: dense parchment study cards separated by distressed black dividers.
- Warm dungeon lighting, dark wood/stone/metal surroundings, amber highlights, sketchbook/concept-art finish.
- Expressive white brush-lettered subject name on the dark left strip, with `BOOK I` immediately below.
- Supporting panels should feel hand-labelled, archival, field-guide-like, and visually dense without turning into a modern website or clean infographic.
- Parchment is warm cream/tan, slightly dirty and distressed; borders are rough black ink/paint rather than neat UI boxes.
- Studies should use painterly character/gear sketches, silhouettes, closeups, and relevant visual callouts.
- The result must feel like the **same physical archive book** as the approved Mordecai spread.

## What may change per subject
Only subject-specific content should change:
- hero figure(s)
- character-specific environment
- head studies
- clothing / gear / anatomy details
- Book I recap
- key traits
- relevant secondary forms or creature variants

The underlying page architecture and visual language should remain recognisably the same.

## Source-grounding rule
**Description comes before image generation.**

For every entry:
1. Read the actual Book 1 EPUB.
2. Build a detailed visual brief from Book 1 only.
3. Prefer the **end-of-Book-1 state** when the book gives a later visual/equipment update.
4. Separate explicit text from safe inference.
5. Do not invent a signature weapon, race, ethnicity, outfit, companion, role, or later form simply to fill the page.
6. Do not use Books 2+ information unless the user explicitly requests it.

If Book 1 does not support a visual detail strongly enough, either omit it or hold the generation until another approved visual source is available.

## Spoiler-by-structure rule
An entry should exist in Book 1 because Book 1 itself makes it relevant, not because later books prove the character matters.

Do not visually over-signal minor Book 1 figures who become important later. Group them where appropriate. Examples already agreed:
- Brandon & Chris Andrews: one combined spread.
- Frank Q & Maggie My: one combined spread.
- Li Jun, Li Na & Zhang: one Death Watch group spread.
- Miriam Dom may have a standalone spread with both goats, but neither goat should be individually elevated or foreshadowed.
- Floor 2 Creatures groups Troglodytes, Clurichauns and Mind Horrors.

## Book 1 curated roster
### Main cast
- Carl
- Princess Donut
- Mordecai
- Mongo

### Allies
- Imani
- Brandon & Chris Andrews
- Agatha
- Miriam Dom + both goats
- Death Watch Crawlers (Li Jun, Li Na, Zhang)

### NPCs
- Zev
- Odette
- System AI

### Enemies
- Prince Maestro
- Frank Q & Maggie My

### Monsters
- Goblin Engineers / Murder Dozer
- Bad Llamas
- Laminaks
- Floor 2 Creatures (Troglodytes / Clurichauns / Mind Horrors)

### Bosses
- The Hoarder
- The Juicer
- Ball of Swine
- Krakaren
- Rage Elemental

## Generation workflow
For **every** new image:
1. Re-anchor to `assets/mordecai-book1-spread.webp` first.
2. State the fixed visual grammar in the image request.
3. Add the source-grounded character/creature brief second.
4. State explicit negative constraints third: no later-book traits, no invented gear, no generic modern UI, no cast collage, no different art style.
5. Generate **one dossier at a time**, except intentional duo/group spreads.
6. Review the result against the anchor before moving on.

Never chain style from the previous generation without re-anchoring.

## Prompt skeleton
> **TEMPLATE ANCHOR FIRST:** Use the approved Mordecai Book I dossier spread as the primary and dominant visual reference. Preserve its wide single-spread architecture, left cinematic hero strip, right parchment study-card grid, distressed black dividers, warm dungeon lighting, brush-lettered white title, `BOOK I` subtitle, sketchbook/concept-art rendering and dense physical archive-book feel. Do not redesign the page.
>
> **SUBJECT SECOND:** Replace Mordecai-specific material with the following Book 1 source-grounded subject brief: [insert detailed brief]. Use end-of-Book-1 gear/state where explicitly supported.
>
> **GUARDRAILS:** Do not introduce later-book information. Do not invent weapons, companions, races, outfits, backstory, jobs or personality details not supported by Book 1. Do not create a cast lineup, modern infographic, generic fantasy journal, photorealistic poster, or unrelated page architecture. Keep the result recognisably from the same archive volume as the canonical Mordecai spread.

## Approval / failure criteria
### Pass
- Immediately looks like the same project as the Mordecai spread.
- Subject is source-accurate for Book 1.
- Character age/build/ethnicity/species are consistent with the book.
- No later-book leakage.
- No random companion/weapon/lore invention.
- Layout remains a single usable wide spread for the app.

### Fail — regenerate, do not rationalise
- Cast collage / lineup.
- Generic journal or concept sheet unrelated to the canonical layout.
- Photorealistic/cinematic poster replacing the sketchbook dossier style.
- Invented cat, staff, weapon, armour, role, quote, history, companion, or other unsupported content.
- Character looks materially too young/old, wrong ethnicity/species, or wrong build.
- Two intended brothers/family members do not visibly read as family.
- Major visual hierarchy differs from the anchor.

## Current generation status
### Approved / directionally approved examples
- Mordecai — **canonical style anchor**.
- Brandon & Chris Andrews — current good generation; clear family resemblance and Book 1 gear direction.
- Frank Q & Maggie My — current good duo generation.
- Prince Maestro — current good correction; huge young orc, gold left tusk, hot-pink silk shirt, gold chains.
- Floor 2 Creatures — current good grouped monster direction.
- Imani — current good direction.
- Li Jun / Li Na / Zhang — current good grouped Death Watch direction.
- Zev — current good direction.

### Needs regeneration / not approved
- Agatha — current attempts drifted from the canonical template and repeatedly invented a staff/cat/lore-keeper identity. Start again from the canonical anchor, with the Book 1 text only.

### Hold
- Miriam Dom + both goats — Book 1 gives too little direct appearance information for Miriam herself. Do not invent a highly specific canonical face/outfit until an approved visual source or stronger source detail is available.

## Key source facts already established
- Brandon: chubby/stocky Black man, heavy winter jacket, enormous round-headed magical hammer.
- Chris: Brandon’s clearly recognisable brother; Black, taller and less stocky, metal skullcap, no supported signature weapon by end of Book 1.
- Imani: about 20, ~90 lb, very slight, scrubs, magical cloak, longsword, terrified/hollowed-out eyes.
- Agatha: clearly an **old** homeless woman, shopping cart, distant stare, gnawing a blackened fingernail; first voluntarily enters via the cart/ramp and cackles. Do not invent a cat or staff.
- Li Jun: Asian man, acne scars.
- Zhang: Asian man, bald; physically tough/high constitution; Li Jun’s friend and treats Li Na like family.
- Li Na: Li Jun’s sister; seen reaching for a sword during Death Watch.
- Frank Q: white man around 40, tall/lean, stubble, Seahawks beanie, ripped jeans, black T-shirt, spiked glowing black-metal shoulder pads, heavy boots, massive single-headed battle axe, throwing knives, gun exists but is not always visible.
- Maggie My: white woman around 40, athletic, closely cropped brown hair, metallic pants/boots, leather jacket with both sleeves, gun.
- Prince Maestro: huge muscular young orc (~6'6), dark flesh with black bristly hair, wild-boar impression, completely gold left tusk, earrings around left ear, hot-pink silk shirt half-buttoned, hairy chest, gold chains.
- Troglodyte pygmies: ~3 ft, upright Komodo-dragon-like upper bodies, long bent scaly kangaroo-like legs, muscular, fast, venomous; bashers larger; virtuosos later variant.
- Clurichauns: grubby fairy-class, hillbilly/leprechaun relatives, runny noses, toxic, slingshots; do not turn them into cute fairies.
- Mind Horrors: floating brain bodies with dangling tentacles, jellyfish/blimp movement, psionic presence, physically weak.
- Bad Llamas: horse-sized scorched/tan llamas, giant yellow buck teeth, spit lava.

## Handover rule for a new chat
Before generating anything, the assistant should read:
1. this standard;
2. the Book 1 image-generation briefs document;
3. the actual Book 1 EPUB if a new visual detail is needed;
4. the canonical style-anchor image at `assets/mordecai-book1-spread.webp`.

Do not start an image generation pass from memory alone.
