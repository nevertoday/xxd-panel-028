---
name: xxd-panel-028
description: "Create XXD Panel 028 raster artwork while treating the bundled original style brief as the sole aesthetic authority. Supports one or more top-bottom, left-right, design-only, and four-device wallpaper outputs; multiple ratios or exact sizes; prompt-generated, user-exact, or text-free typography; and inline parameters. Use when the user invokes xxd-panel-028 or requests the exact Panel 028 style."
---

# XXD Panel 028

Create fresh PNG artwork with `references/028-source.md` as the **sole creative and aesthetic authority**. This Skill is a runtime shell: it resolves delivery variables, appends them to the untouched source brief, executes bitmap generation, and verifies the result. It must not write a second art direction.

## Authority boundary

1. Read `references/028-source.md` completely immediately before building every generation request.
2. Copy that brief verbatim into the generation prompt. Do not summarize, translate, polish, expand, reinterpret, or replace it with this file, a README, a sample, or either runtime-adapter reference.
3. The source brief owns subject transformation, composition inside the design region, colour, palette derivation or fixed colour choices, materials, texture, whitespace, text amount, wording logic, typographic character, and prohibitions.
4. Runtime instructions may change only: selected output mode, final canvas ratio or pixels, placement or visibility of the source photograph, device profile, wallpaper relationship, target text language, and user-exact text.
5. Append all runtime instructions **after** the complete source brief. Never insert them into, or rewrite, its aesthetic paragraphs.
6. When a source brief describes an old 3:4 top-bottom container, treat that as the original presentation container, not a mandatory default. A current explicit mode or size overrides only that container. The remaining style logic stays active.
7. Never create a generic palette, extract extra colours, lock a swatch set, invent an “aesthetic motive,” pre-compose a title, generate a copy package, or run an external semantic-reading framework. If the source brief itself asks for any of those things, let the image model perform them exactly there.
8. Samples show outcomes only. Do not copy their subject matter, colours, text, layout accidents, or aspect ratio.

Use these semantic mappings when the container changes:

```text
SOURCE REFERENCE = the source brief's “upper photo” or factual source
DESIGN REGION = the source brief's “lower half” transformation
```

- `top-bottom`: SOURCE REFERENCE is visible above; DESIGN REGION is below.
- `left-right`: SOURCE REFERENCE is visible on the left; DESIGN REGION is on the right.
- `design-only`: SOURCE REFERENCE remains an input reference but is not visible; DESIGN REGION expands to the whole canvas.
- `wallpaper-pack`: SOURCE REFERENCE remains an input reference but is not visible; DESIGN REGION is independently recomposed across each device canvas.

## Resolve only runtime variables

Every invocation is a new job unless the user explicitly asks to inspect, edit, continue, or reuse a named result. Repeating the same request requires fresh generation and a new task folder; an old matching file never completes a new request.

### Inline fast path

Parse parameters anywhere after the invocation and input:

```text
/xxd-panel-028 <source> --mode top-bottom,design-only \
  --size auto,3:4,9:16,2160x3840 \
  --text prompt --locale ja-JP
```

- `--mode`: one or more of `top-bottom`, `left-right`, `design-only`, `wallpaper-pack`. Repeated flags and comma-separated values accumulate; accept natural-language equivalents and `all` / `全部`.
- `--size`: one or more of `auto`, `source`, `1:1`, `3:4`, `4:3`, `4:5`, `5:4`, `2:3`, `3:2`, `9:16`, `16:9`, `21:9`, `5:7`, `7:5`, any custom ratio, or exact `WIDTHxHEIGHT`. Repeated flags accumulate; accept `×`.
- `--text`: `prompt`, `exact`, or `none`. Accept legacy aliases `auto` → `prompt` and `custom` → `exact` without presenting the old labels to users.
- `--copy "..."`: exact user text; implies `--text exact`. Do not rewrite or translate it.
- `--locale`: target language, market, or locale for visible text.
- `--wallpaper`: `linked` or `independent`.
- `--wallpaper-size`: labelled device sizes, for example `phone=1440x3200,ipad=2048x2732,desktop=3840x2160,watch=1024x1024`.
- `--out`: explicit output root.

Explicit parameters override ambiguous prose. Multi-value parameters accumulate and deduplicate in user order; single-value parameters use the last explicit value. If every required variable is resolved, skip preflight and generate. If values are partial, ask only for unresolved variables. Ask about a direct contradiction such as `--text none` with `--copy`.

### Capability-adaptive preflight

Do not switch the user's session into Plan mode merely to obtain a question UI. A Skill describes behaviour but cannot create UI capabilities that the host has not exposed. Detect the actual question-tool schema and follow this order:

1. **Real multi-select tool available — for example Claude Code `AskUserQuestion` with `multiSelect: true`:** use genuine checkbox questions for modes and sizes. Use single-select questions for text mode and wallpaper relationship. Do not print a redundant numbered menu after showing the form.
   - First form: modes (`top-bottom`, `left-right`, `design-only`, `wallpaper-pack`) with `multiSelect: true`; size route (`自动适配`, `跟随原图`, `常用比例`, `自定义`) with multi-select enabled when the host permits combined size sources; text mode as single-select.
   - When `常用比例` is selected, show real checkbox groups for all concrete ratios, split only as required by host option limits: square `1:1`; portrait `3:4`, `4:5`, `2:3`, `9:16`, `5:7`; landscape `4:3`, `5:4`, `3:2`, `16:9`, `21:9`, `7:5`. Accumulate selections across groups. When `自定义` is selected, collect one or more ratios or exact pixel targets through the host's free-input/Other path.
   - If wallpaper is selected, ask `linked` versus `independent` as a genuine single-select. Ask only unresolved questions and respect answers already present in prose or parameters.
2. **Only a mutually exclusive question tool is available — for example Codex `request_user_input`:** use it only for genuinely single-choice fields such as text mode, wallpaper relationship, or the size-entry route. Never represent modes or concrete sizes as a single-select when the user may choose several. Collect those multi-value fields with the two-round combination input below. Do not claim that a single-choice card is a checkbox.
3. **No interactive question tool is available:** use the same two-round combination input below. It is typed multi-value input, not a clickable form. Never draw Markdown `- [ ]` boxes or other fake controls.

Inline parameters and clear natural language always take priority. Skip every field already resolved. When all required values are present, skip every question and generate immediately.

#### Two-round combination-input fallback

First round — modes. This is a typed combination question, so label it honestly instead of calling it a checkbox:

```text
请选择一个或多个成品类型：

1. 上下对照（原图在上，028 设计在下）
2. 左右对照（原图在左，028 设计在右）
3. 只要设计图（原图仅作参考，不出现在成品中）
4. 四端壁纸（手机、iPad、电脑、儿童手表）

可回复：1｜1+3｜2、4｜全部
```

Second round — when at least one ordinary mode is selected, ask size route and text mode together. If the selection contains only `wallpaper-pack`, skip the ordinary-size part and resolve text plus device sizes and wallpaper relationship.

```text
请选择尺寸，可多选：

1. 智能推荐（显示本次计算出的比例与像素）
2. 跟随原图
3. 常用比例（可直接写 3:4、9:16 等一个或多个比例）
4. 自定义（输入一个或多个比例／准确像素）

请选择文字方式：

A. 模型根据原始提示词生成文字（注明语言或地区）
B. 使用我的准确文字（发送原文并注明语言或地区）
C. 不要文字

可回复：尺寸 1＋9:16；文字 A，日语
可回复：尺寸 3:4、16:9；文字 B，准确文字「……」，简体中文
```

If the user answers only `常用比例`, show the grouped library once and accept any combination:

```text
方形：1:1
竖版：3:4、4:5、2:3、9:16、5:7
横版：4:3、5:4、3:2、16:9、21:9、7:5
也可以直接输入准确像素。
```

Do not decide wording outside the source brief. For option A, provide only the target language to the image model; the image model follows the source brief's existing text logic. For option B, pass the user's characters verbatim and add no other copy. For option C, prohibit all visible text and pseudo-text.

Do not infer language or market from a person's appearance, name, clothing, scene, filename, metadata, signage, or the language used to operate the Skill. Resolve it explicitly whenever text is requested. Use natural target-language shaping, direction, punctuation, spacing, and line breaking. For Arabic, preserve connected forms and right-to-left text flow without indiscriminately mirroring the artwork.

If `wallpaper-pack` is selected, ask one additional single-choice question unless resolved:

```text
四端壁纸采用哪种关系？

1. 连贯套装：先生成并确认一张定调图，其余三张参考原图＋定调图独立重构
2. 四张独立：四张都只参考原图，各自构图
```

Neither option crops or mechanically resizes one wallpaper into the other devices. Use the common device preset above unless the user supplies labelled device sizes. Ordinary-size choices do not multiply wallpaper outputs.

### Size resolution

- No silent default ratio exists.
- For `auto`, calculate a source- and mode-aware whole canvas before generation. Preserve the photograph without forced crop and use the source brief's paired relationship as a visual planning target: when it calls for equal halves, top-bottom may resolve near source `W:2H` and left-right near `2W:H`; when it suggests a different relationship, calculate from that relationship instead. Design-only starts from the source aspect unless the source brief or intended use clearly supports a better recommendation. Show the resolved ratio and pixels. This planning ratio does not authorize a pixel-level seam or midline audit after generation.
- `source` means the source photograph's aspect for the whole requested ordinary output.
- Exact pixels override a ratio.
- Every distinct aspect ratio is a separate complete-canvas composition from the same source and the same verbatim style brief. Never crop one ratio from another. Multiple resolutions sharing one aspect may be exported from the highest-quality approved composition.
- A size set applies to every selected ordinary mode unless the user maps sizes per mode.
- Before generation, state the resolved modes, concrete sizes, text mode and locale, wallpaper relationship if relevant, and total output count. Do not ask for another confirmation when they are complete and consistent.

## Build the generation prompt

For each distinct asset, concatenate exactly:

```text
[VERBATIM CONTENT OF references/028-source.md]

[RUNTIME OVERRIDE BLOCK]
```

Use this runtime block, removing irrelevant fields but adding no aesthetic prose:

```text
RUNTIME OVERRIDE — CURRENT DELIVERY ONLY

The original brief's initial 3:4 top-bottom arrangement is its legacy presentation container.
For this output, override only:
- final canvas
- source/design-region placement
- source visibility
- device dimensions

Except for those container variables, every design-transformation, composition,
colour, material, whitespace, text-character and typography instruction in the
original brief remains authoritative.

Interpret “upper photo” as SOURCE REFERENCE.
Interpret “lower half” as DESIGN REGION.

OUTPUT MODE: TOP_BOTTOM | LEFT_RIGHT | DESIGN_ONLY | WALLPAPER_PACK
FINAL CANVAS: <resolved ratio and/or exact WIDTHxHEIGHT>
DEVICE PROFILE: NONE | PHONE | IPAD | DESKTOP | WATCH
SOURCE VISIBILITY: UPPER HALF | LEFT HALF | REFERENCE ONLY — NOT VISIBLE
DESIGN REGION: LOWER HALF | RIGHT HALF | FULL CANVAS
PAIRED BALANCE: USE THE ORIGINAL BRIEF AS A VISUAL COMPOSITION TARGET | NOT APPLICABLE
MIDLINE AUDIT: NONE — MINOR GENERATIVE SPLIT OFFSETS ARE ACCEPTABLE
WALLPAPER RELATIONSHIP: NONE | INDEPENDENT | LINKED

Colour follows the original brief's existing colour instructions exactly.
Unless the user explicitly requests a colour change, do not add, replace,
summarize, or re-plan any palette.
```

Append exactly one text block after the runtime block. If the user has other explicit requirements, append those verbatim after the text block at the very end.

Prompt-generated text:

```text
TEXT MODE: ORIGINAL_PROMPT_GENERATED
TEXT LANGUAGE: <resolved language or locale>

The image model must generate any wording by following the original brief's
existing text-generation logic. The outer Skill supplies no title, microcopy,
copy package, or additional semantic framework.
```

User-exact text:

```text
TEXT MODE: USER_EXACT
TEXT LANGUAGE: <resolved language or locale>
TEXT: 「<user's exact characters>」

Use the supplied text verbatim. Do not rewrite, translate, spell-correct, or add
any other wording. Typography and placement still follow the original brief.
```

Text-free:

```text
TEXT MODE: NONE
Render no letters, characters, numbers, logos, captions, labels, or pseudo-text anywhere.
```

If the user explicitly changes colour or another style variable, append that exact request at the very end, after the text block, and identify it as a user override. Do not elaborate it.

## Bitmap execution

- Prefer GPT Image 2 whenever the host's built-in image capability or an already configured compatible route exposes it.
- Also support Seedance 5.0 Pro, Nano Banana Pro (Gemini Image Pro), Nano Banana 2 (Gemini Image Flash), or another compatible bitmap model only when it can preserve the reference, requested canvas, language, and multi-reference needs. Changing the model must not change this workflow or the prompt-authority boundary.
- Judge readiness by an actual image-capability check, not one missing tool or environment variable. Never name or expose a provider, endpoint, credential, header, account, route, or secret.
- If the built-in image tool is exposed, follow the installed `imagegen` Skill and make one generation/edit call per distinct asset. A wallpaper pack requires four outputs, not one contact sheet.
- If built-in generation is not exposed, run `python3 scripts/configured_imagegen.py probe`. Its sanitized result is the only allowed diagnostic surface. If ready, use `edit` with the source and a private prompt file; use `generate` only when no image reference genuinely exists.
- Do not echo a credential or full prompt in shell history or logs. Do not inspect configuration files manually. Do not modify provider, account, billing, credential, or global routing settings unless the user explicitly requests that separate change.
- If no compatible route is verified, ask the user to enable a suitable image tool or voluntarily provide an API key for the task. Never ask them to expose an existing secret, and never assert that a key is missing without a trusted sanitized result.
- Generate finished raster imagery. SVG, HTML, CSS, Canvas, diagrams, and programmatic vector drawing are not substitutes.

Use **one complete-canvas generation per output**. For paired modes, generate the faithful photo region and transformed design region together in the requested whole canvas. Retry a failed complete canvas once by restating only a meaningful failed content or delivery constraint. Never retry, reject, or invoke `compose_panel.py` merely because the generated boundary is a little above or below the mathematical midpoint. Use `scripts/compose_panel.py` only when the user explicitly requires pixel-exact panel geometry, the user requires pixel-identical source preservation, the route cannot realize the requested canvas, or lossless pixel calibration is necessary. The script may crop/paste/size/audit raster files; it must never invent the artwork or judge style.

For a linked wallpaper pack, generate one device image first as the visual anchor, then supply both the original source and that approved anchor to each remaining device generation. Recompose each canvas; never crop an earlier wallpaper or chain derivatives. For an independent pack, every device sees only the original source.

## Source and output isolation

Use only sources attached to the current invocation, explicit paths, or a prior source explicitly identified by the user as “the same image.” Never scan Desktop, workspace roots, output folders, or unrelated directories for a substitute. Historical outputs and sample assets are not inputs unless explicitly named.

Write selected outputs only:

```text
~/Desktop/xxd/xxd-panel-028/<fresh-task>/
└── source-01/
    ├── top-bottom/<size-label>.png
    ├── left-right/<size-label>.png
    ├── design-only/<size-label>.png
    └── wallpaper-pack/phone.png · ipad.png · desktop.png · watch.png
```

`--out` replaces the root but not fresh-task isolation. Reserve a collision-safe task name before generation. Do not create an automatic collage, overview, mockup, or combined preview. Return absolute PNG paths in source order, then mode order 1→4; wallpaper order is phone, iPad, desktop, watch.

## Acceptance gate

Inspect every final PNG at full size and thumbnail size. Accept only when:

- it is a fresh result from the correct current source or theme;
- mode, source visibility, whole-canvas ratio or exact pixels, count, and PNG format match the resolved runtime variables;
- paired source regions preserve identity and structure without stretching or replacement;
- paired regions feel intentionally balanced, but no seam detection, coordinate measurement, midpoint percentage, or pixel-level split audit is performed; a minor generative offset is not a failure unless the user explicitly requested exact geometry;
- the result follows `references/028-source.md`, especially its own colour, material, composition, whitespace, and typography requirements, without an outer Skill palette or added art direction;
- prompt-generated text uses the requested language and the source brief's own text logic; user-exact text is verbatim with no additions; text-free output contains no text or pseudo-text;
- linked and independent wallpaper rules are respected;
- no SVG/code-rendered substitute, watermark, UI, route information, or secret appears.

When a result fails, retry only the failed source-brief or runtime requirement. Do not “improve” it by introducing a new aesthetic theory.

## Runtime adapters

- `references/xxd-panel-028-prompt.zh-CN.md`
- `references/xxd-panel-028-prompt.en.md`

These files document the same minimal adapter. They never replace `references/028-source.md`.
