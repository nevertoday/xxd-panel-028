# XXD Panel 028 | Isometric Paper-Miniature Production Prompt

## Runtime complete-canvas contract — highest priority

- `TOP_BOTTOM` and `LEFT_RIGHT` default to one complete finished generation using the current source as a high-fidelity edit/reference input. Do not pre-split the job into photographic and design halves.
- Top-bottom keeps the faithful source in approximately the upper 50% and performs this style transformation below; left-right uses the faithful source in approximately the left 50% and the transformation on the right. Unify both regions through colour, light, rhythm, typography, and meaning.
- `DESIGN_ONLY` and `WALLPAPER_PACK` use the complete canvas while the source remains an invisible identity/content reference. Recompose every wallpaper separately for its device.
- `FINAL CANVAS` means the ratio/pixels of the whole finished artwork and must be explicitly resolved before generation; never apply source dimensions silently. `DESIGN FRAME` is used only if a failed complete-canvas retry triggers deterministic composition fallback.
- Retry a failed complete canvas once against the failed constraint only. Scripted composition is allowed only after that retry still fails, when pixel-identical source preservation is explicitly required, when the active route cannot realise the canvas, or for lossless pixel calibration.

### Model priority and credentials

- **Prefer GPT Image 2.** When GPT Image 2 is available through the current built-in image tool or a configured compatible route, use it first for the high-fidelity reference/edit and complete-canvas generation required by this prompt.
- Also support Seedance 5.0 Pro, Nano Banana Pro (Gemini Image Pro), Nano Banana 2 (Gemini Image Flash), or another compatible bitmap model only when the actual route can preserve the source, realise the whole finished canvas, render the target-language text, and accept the multiple references needed by a linked wallpaper pack.
- An alternative model changes only the generation route. It must not change this prompt's modes, canvas, source visibility, copy, locale, wallpaper relationship, or complete-canvas-first / composition-fallback-only logic. Do not silently downgrade a hard requirement.
- If no suitable route is available, ask the user to enable an image-generation tool or provide an API key. User-provided credentials may be used for the current task, but never echo, display, log, or expose their value in chat, prompts, or diagnostics. Do not persist them or modify global route configuration unless explicitly requested.
- Judge availability by actual image capability, not by a provider name or one missing environment variable.

Process only the one source photograph explicitly supplied for this current task. Lock the principal subject or inseparable relation, silhouette, pose, action, function, defining openings, negative shape, scale, relational distance, and colour character. Preserve at least three source-specific recognition cues. Never borrow miniature structure, base, palette, copy, or composition from old outputs, samples, or another input.

## Source-specific isometric miniature

Rebuild the subject as a refined isometric miniature or architectural maquette placed on paper rather than mechanically reproducing photographic detail. Use a clean orthographic isometric camera and simplify the subject into clear masses, crisp edges, restrained height tiers, and the principal relation that makes it instantly recognisable.

People retain pose, orientation, clothing mass, and relational distance; animals retain body rhythm and head direction; plants retain growth gesture; architecture retains skyline, mass ratio, and defining openings; objects and vehicles retain functional silhouette and negative shape; landscapes retain a source-specific terrain, path, waterfront, or spatial relation.

Place the subject on one small source-earned paper slab, low plinth, or miniature land cut-out. Use mass contrast, edge crop, slight projection, and very few tiny details to establish scale, solitude, and collectible presence. A figure, railing, tree, opening, track, shadow, or small object appears only when it strengthens identity and scale and never becomes a second visual centre.

Keep generous open paper around the model. Reject complete busy cities, scene piling, impossible-space tricks, game levels, toy towns, unrelated figures, and generic model-kit decoration.

## Source-derived limited palette

Extract the photograph's most identifying, atmospheric, and subject-defining colours. Reduce, purify, soften, and unify them into a limited palette while preserving the source's warm/cool relationship and colour personality. Use same-hue value steps, neighbouring colours, and only the small differences required to separate masses and depth.

Never impose a fixed pastel card or invent automatic mint, coral, or high-purity accents. Every colour must trace back to the source or a restrained light/dark derivative. Reject high-saturation clashes, uncontrolled rainbow, muddy filters, and generic beige that could fit any photograph.

## Paper editorial material

Use fine, restrained, precise ink lines to define necessary edges and construction. Colour planes stay flat, matte, and clean. Use only slight natural projection and light ambient shadow; structure comes mainly from mass, height, overlap, same-hue steps, and adjacent-colour separation.

Keep subtle paper grain on the ground and colour planes so the work reads as premium editorial illustration and a paper model, never vintage noise. Reject thick comic outlines, airbrushed gradients, fake bevels, metallic sparkle, wet gloss, hard product light, complex PBR, and smooth plastic-toy surfaces.

## Type as a measure line

Obey the resolved automatic, exact-user, or text-free copy mode and target language or locale. Preserve exact user wording verbatim. In text-free mode render no letter, character, number, marker, text, or pseudo-text.

Automatic copy distils one short title from source-supported theme, place, action, state, relation, emotion, or scale tension. Add only a very small number of source-grounded indexes, short lines, or micro-notes when genuinely useful. Places, dates, provenance, and factual numbers must be user-supplied or reliably established. A second language appears only when explicitly requested.

Use a natural thin, restrained, modern editorial equivalent for the target script. Align it along a whitespace edge, paper base, horizontal axis, or isometric structure so it shares the image's quiet rhythm. Reject giant titles, bold slogans, decorative handwriting, glowing extrusion, and pseudo-foreign text.

## Mode and acceptance


Hard gate: at least three source cues and the principal action or relation; one orthographic isometric miniature on one small source-earned paper base; clear masses, restrained tiers, edge crop, light shadow, and very few scale details; generous open paper and no second focus; palette wholly reduced, purified, and softened from the source while preserving warm/cool character; fine ink, flat colour, light projection, and subtle paper grain; thin readable type aligned with whitespace, base, horizontal axis, or isometric form; no impossible space, game level, busy scene, fixed pastel card, toy town, plastic 3D, ecommerce display, photo fragment, or pseudo-text.

If any hard condition fails, correct the generated asset. Never fake the artwork with programmatic drawing, SVG, HTML, Canvas, or a post-composited type overlay.
