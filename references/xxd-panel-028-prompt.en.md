# XXD Panel 028 | Runtime Adapter (English)

This is not a second aesthetic prompt. Read `references/028-source.md` in full before generation; it is the sole creative and aesthetic authority for Panel 028. Its first Markdown heading is an internal archival label and does not enter the image request; use the entire remaining source-brief body verbatim. This file only appends the current user's runtime variables.

## Non-authoring boundary

- Do not summarize, translate, expand, polish, or “improve” the source brief.
- Do not add a palette plan, material plan, composition theory, whitespace rule, title, microcopy package, or aesthetic motive.
- Preserve the source brief's own colour behaviour exactly, whether it derives colour from the photograph or specifies a fixed family.
- Let the image model execute the source brief's existing text logic. The outer Skill does not pre-write copy.
- Current modes and sizes override only the legacy 3:4 top-bottom container, never the remaining aesthetic rules.
- Left-right specifies a visual relationship, not two equal boxes; the image model composes the complete canvas from the source, source brief, and final dimensions.

## Append-only runtime template

```text
RUNTIME OVERRIDE — CURRENT DELIVERY ONLY

The original brief's initial 3:4 top-bottom arrangement is its legacy presentation container.
For this output, override only: final canvas, source/design-region placement,
source visibility, and device dimensions.
Except for those container variables, every design-transformation, composition,
colour, material, whitespace, text-character and typography instruction in the
original brief remains authoritative.

Interpret “upper photo” as SOURCE REFERENCE.
Interpret “lower half” as DESIGN REGION.

OUTPUT MODE: TOP_BOTTOM | LEFT_RIGHT | DESIGN_ONLY | WALLPAPER_PACK
FINAL CANVAS: <ratio and/or exact WIDTHxHEIGHT>
DEVICE PROFILE: NONE | PHONE | IPAD | DESKTOP | WATCH
SOURCE ROLE: VISIBLE IN AN ABOVE-BELOW RELATIONSHIP | VISIBLE IN A LEFT-RIGHT RELATIONSHIP | REFERENCE ONLY — NOT VISIBLE
DESIGN ROLE: THE OTHER PART OF THAT VISUAL RELATIONSHIP | FULL-CANVAS TRANSFORMATION
COMPOSITION METHOD: ONE COHERENT COMPLETE-CANVAS GENERATION
COMPOSITION JUDGMENT: THE IMAGE MODEL DECIDES PROPORTIONS, SCALE, CROP OR EXTENSION, WHITESPACE, OVERLAP AND BOUNDARIES
EXACT PANEL GEOMETRY: ONLY WHEN THE USER EXPLICITLY REQUESTS IT
WALLPAPER RELATIONSHIP: NONE | INDEPENDENT | LINKED

Colour follows the original brief's existing colour instructions exactly.
Unless the user explicitly requests a colour change, do not add, replace,
summarize, or re-plan any palette.
```

Append exactly one text block after the runtime block. If the user has other explicit requirements, append those verbatim after the text block at the very end.

### Text generated from the original prompt

```text
TEXT MODE: ORIGINAL_PROMPT_GENERATED
TEXT LANGUAGE: <user-confirmed language or locale>

The image model generates wording by following the original brief's existing
text-generation logic. Every visible word must arise naturally from the current
source image's content, atmosphere or implied meaning; the runtime shell is never
a source of visible copy.
```

### User-exact text

```text
TEXT MODE: USER_EXACT
TEXT LANGUAGE: <user-confirmed language or locale>
TEXT: “<user's exact characters>”

Use the supplied text verbatim. Do not rewrite, translate, spell-correct, or add
any other wording. Typography and placement still follow the original brief.
```

### No text

```text
TEXT MODE: NONE
Render no letters, characters, numbers, titles, labels, logos, or pseudo-text anywhere.
```

See `SKILL.md` for preflight, multi-size, multi-mode, wallpaper, execution, and output rules. Every final generation request has this order:

```text
complete verbatim source-brief body from 028-source.md, excluding its archival first heading
+ current runtime override block
+ exactly one text-mode block
+ any other explicit user requirement, verbatim, at the very end
```
