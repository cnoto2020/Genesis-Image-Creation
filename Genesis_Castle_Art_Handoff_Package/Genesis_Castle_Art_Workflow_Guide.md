# Genesis Castle Artwork — Reproducible ChatGPT Handoff Guide
**Version:** 1.0 · **Reference:** Undead Castle v14 · **Updated:** 2026-11-03

> **INSTRUCTIONS FOR ANY CHATGPT SESSION WORKING ON THIS GAME:** Read this file completely before creating castle art. Treat **REQUIRED** statements as constraints. Do not confuse the *historically successful visual workflow* with the *user-authorized workflow for new assets*. Never claim a new image is Genesis-ready based on resolution and color count alone. Never show the user another Ironborn preview unless it genuinely meets the visual quality of Undead v14.

## 1. Objective and acceptance criteria

Create castle scene artwork for an original Sega Genesis/Mega Drive strategy game. Four castles—Undead, Ironborn, Fey, Brimstone—must feel like one coherent game. The **Undead Castle v14** scene is the **visual quality benchmark**, not merely a layout suggestion.

**REQUIRED for new work**
- Create/paint the actual game artwork **directly at 160 × 160 pixels**, not by generating a larger image and resizing or quantizing it.
- Use a deliberate indexed Genesis palette, tile-compatible dimensions, and an 8 × 8 tile workflow. Consider all game assets together, not the castle panel in isolation.
- Maintain intricate architecture, visual hierarchy, atmospheric lighting, coherent perspective, detailed but intentional stonework, and a readable focal point.
- Use the same shared Gothic UI/border framework across factions; differentiate mostly through palette accents.
- Do **not** show Ironborn artwork until it meets the benchmark on artistic merit. If unable to match it, say so rather than delivering another mediocre iteration.
- Never describe a ROM as emulator-tested or hardware-tested unless it was actually tested that way.

## 2. Evidence recovered from the successful Undead Castle

### 2.1 Artifacts independently inspected in this session

| Item | Observed fact |
|---|---|
| Approved native panel candidate | `Undead_Castle_Genesis_160x160_Edit.png` |
| SHA-256 | `c63ac02cff93592b014e8f1946088d3ddb143c259db20fa6fc4f2077b98f326b` |
| Dimensions | **160 × 160** |
| PNG storage mode | **P (indexed)** |
| Distinct visible RGB colors | **15** |
| 8 × 8 tile slots | **400** |
| Distinct 8 × 8 pixel tiles | **399** (deduplication by RGB pixels, not final SGDK tile indices) |
| Historical v14 ROM file | `Undead_Castle_Menu_v14.bin` present, 131,072 bytes |
| v14 ZIP | Contains only the `.bin` ROM, not source or conversion scripts |
| Native artwork preview | `Undead_Castle_v14_genesis_preview.png`, 640 × 640 enlarged preview |

**Important technical correction:** The 15 observed RGB colors in the surviving PNG are **not all exact values on a Genesis DAC ladder**. Therefore indexed PNG + 15 colors + tile-aligned dimensions **do not independently prove** the exact CRAM palette values were valid. SGDK may quantize colors at import. Inspect the built resource/ROM or emulator output before declaring exact palette fidelity.

### 2.2 Historical sequence (reconstructed from prior conversation)

1. **Whole-scene art direction.** The Undead Castle was described as a complete illustration: massive Gothic citadel on rocky cliffs; moon and purple sky; layered mountains; pointed roofs and spires; green-lit windows; carved skull above the gate; stone steps; banners; graveyard, fog, dead trees and waterfall. Architectural focal point, environment, and lighting were specified together.
2. **Illustration-first generation.** A detailed pixel-art-*style* image was generated at larger-than-native resolution. Historical notes cite a source around 724 × 784, but the exact original source/prompt/model/seed are not independently available.
3. **Visual selection.** The user liked/approved the image before it was adapted to hardware.
4. **Adaptation to hardware.** The image was cropped/resized to a 160 × 160 panel, palette-reduced to an indexed PNG with about 15 visible colors, and prepared for the 8 × 8 tile-based Genesis rendering pipeline.
5. **ROM integration.** The art was included in an SGDK castle menu ROM; the surviving v14 `.bin` is 128 KiB. Earlier assistants reported a successful build; this documentation does **not** claim to have recompiled or emulator-tested v14.
6. **Iteration.** Later v15–v20 versions changed UI, recruitment art, and borders. Their artistic results are **not** the reference for the castle scene.

**Historical reality:** The old visual success came from a *high-quality composed illustration followed by conversion*. This is **not allowed as the production method for new artwork** under the user's current rule. Preserve the artistic principles, not the disallowed conversion technique.

## 3. Why Undead succeeded visually

**Composition:** Castle dominates, framed by landscape and foreground. The silhouette is complex but legible at 160 × 160.

**Depth:** Sky → distant mountains → rock face → towers → main gate → staircase → foreground props. Each layer differs in value and detail.

**Lighting:** A small number of clear light sources: cool moonlit stone versus saturated supernatural green. Shadows make architectural relief visible.

**Architecture:** Asymmetric Gothic masses, overlapping towers, parapets, varied roof heights, arches, gate sculpture, masonry and small decorative motifs. These are not identical rectangular towers.

**Detail hierarchy:** Large masses first, medium architecture second, pixel clusters last. Detail reinforces materials, planes and light; it is not uniform noise.

**Palette:** Strong dark purples and blue-gray shadows, medium stone values, pale highlights and green glow. Colors serve distinct jobs.

## 4. Failed Ironborn approach — explicitly prohibited as primary method

Versions v1–v4 were mostly constructed using Python/Pillow primitives: polygons for mountains, rectangles for walls/towers, repeated horizontal masonry lines, randomly placed texture dots, and decorative machinery added late. This yields technically small, indexed pictures but poor visual quality.

**Do not** build a scene by writing hundreds of `draw.rectangle`, `draw.polygon`, or random-noise loops and assume added surface detail makes it comparable to Undead v14. Programmatic tools are fine for **validation, packing, palette checking, and selective pixel edits**; they are not a substitute for intentional pixel-art illustration.

## 5. New authorized art-production workflow (PROPOSED; not yet proven equal to v14)

### Stage A — reference study, no new artwork shown
1. Open the actual 160 × 160 Undead panel at **native size and nearest-neighbor zoom**.
2. Analyze its silhouette, dominant light sources, spatial layers, value grouping, palette roles, and distribution of detail.
3. Record *what makes the image readable and atmospheric*, not just its list of objects.
4. Establish a matching target for the next castle, with comparable architecture-to-background ratio and amount of visual information.

### Stage B — art direction at native size
1. Create a **160 × 160 indexed canvas** from the start.
2. Block in 3–5 major value masses *at native resolution*. Ensure the castle is immediately recognizable in thumbnail view.
3. Establish depth planes and a distinct focal point.
4. Build custom pixel clusters, silhouettes, arch shapes, masonry patterns and shadows **at the final pixel scale**. Avoid cloned towers.
5. Add secondary detail only after the underlying architecture looks compelling.
6. Evaluate at **100% and nearest-neighbor 400%**; zoomed preview is a viewing aid only, never a new production source.

### Stage C — Ironborn-specific visual direction
- **Core concept:** Mountain fortress carved and constructed by dwarves; gnomes contribute machines and precision engineering.
- **Dominant shape:** A vast stone gate and irregular terraced citadel embedded in a dramatic mountain wall.
- **Dwarven language:** Massive buttresses, sculpted stone arches, carved reliefs, retaining walls, stone bridges, excavated galleries.
- **Gnomish language:** Intricate lift mechanisms, gear trains, crane, ventilation pipes, furnace works, compact workshops integrated into fortress architecture.
- **Lighting:** Steel-blue/cold mountain shadows, pale stone edge highlights, localized amber forge windows; avoid filling the entire scene with evenly spaced orange dots.
- **Scale:** Tiny mine carts and figures should make the fortress feel monumental.
- **Avoid:** Castle floating in front of a generic mountain; repetitive rectangular turrets; huge foreground machinery obscuring the gate; uniformly textured surfaces.
- **Palette:** Build one purpose-designed 16-entry hardware-compatible palette for the scene (including transparent index if the rendering method requires it). Do not merely reuse Undead's purple/green values.

### Stage D — technical validation (must be recorded)
1. Assert image is exactly **160 × 160**, indexed, and divisible into **20 × 20 tiles**.
2. Verify the actual palette assignments and each RGB component's mapping to the Genesis **3-bit-per-channel** hardware color steps; distinguish editor RGB display values from CRAM encoding. SGDK may map/quantize on conversion.
3. Confirm <= 16 entries in the assigned palette, with transparency policy appropriate to sprite/background use. The Genesis supports four 16-entry palette lines globally, shared by the scene and UI.
4. Compute 8 × 8 tile count and unique tiles; check total VRAM budget, tile index allocation, and reuse against UI/fonts/other graphics. The VDP has **64 KiB VRAM**; a tile is **32 bytes** at 4 bits per pixel. The inspected v14 image has 399 unique RGB tiles, approximately **12,768 bytes** if each were encoded as one tile, **excluding** tilemaps and other graphics. This is an estimate, not verified ROM usage.
5. Export in the actual format expected by the SGDK project; check resource compiler (`rescomp`) output and palette metadata. Record exact commands.
6. Build a `.bin` ROM and verify build return code, ROM header, and resource size. Then **run an emulator** and inspect screenshots for palette, tile alignment, clipping, scrolling, and UI overlap. Real hardware testing is a separate claim.
7. Preserve source, indexed PNG, palette metadata, validator report, and buildable ROM with versioned names.

### Stage E — visual acceptance gate (before user sees anything)
Compare side by side with Undead v14 **at identical native scale**:
- Is the architecture as intricate and organically varied?
- Is there comparable depth, atmospheric lighting, and material differentiation?
- Is the gate/focal point legible and visually compelling?
- Is the fortress genuinely part of the mountain?
- Are small details intentional and well-integrated?
- Does the scene look like the same art team made both castles?

**If any major answer is no, keep working privately or state inability to meet the standard. Do not present another incremental version as a finished castle.**

## 6. Handoff contract — paste into a fresh ChatGPT session

```text
You are working on an original Sega Genesis strategy game's castle art.
Read Genesis_Castle_Art_Workflow_Guide.md and Genesis_Castle_Art_Workflow_Manifest.json.
The visual benchmark is the attached Undead_Castle_Genesis_160x160_Edit.png (v14).
The user requires ALL new art to be authored directly at native 160x160, in a hardware-valid indexed palette and 8x8 tile workflow. Do not generate high-resolution art and downscale/quantize it. Do not replace art direction with procedural rectangles and random textures.
For Ironborn: dwarven mountain fortress with gnomish machines, carved stone, immense gate, layered architecture, steel-blue stone and warm forge light. Match Undead v14's quality of silhouette, depth, detail, lighting, and atmosphere.
Do not show any Ironborn art until you sincerely judge it to match Undead v14. If you cannot, explain the limitation. Validate palette, tile usage, VRAM, SGDK resource processing, and ROM separately. Never claim emulator/hardware testing without performing it.
Preserve versioned source, final indexed PNG, palette, validation results, and working .bin.
```

## 7. Reproducibility status and open gaps

| Question | Status |
|---|---|
| Exact successful visual approach | **Reconstructed with high confidence**: full-scene detailed illustration → approval → Genesis conversion |
| Exact original image generation prompt | **Not recovered** |
| Exact source artwork, model and seed | **Not verified** |
| Crop, resampling, dithering, palette reduction code | **Not recovered** |
| Surviving native 160 × 160 artwork | **Verified** in current container |
| v14 ROM bytes | **Verified present**; no execution test |
| Exact Genesis palette CRAM mapping | **Not verified** |
| New native-first process matching v14's quality | **Not yet demonstrated** |

## 8. Files to carry forward

- `Undead_Castle_Genesis_160x160_Edit.png` — benchmark image, SHA-256 above.
- `Undead_Castle_Menu_v14.bin` — historical build (reference only).
- `Undead_Castle_v14_genesis_preview.png` — enlarged viewing reference, **not a production source**.
- `Genesis_Castle_Art_Workflow_Guide.md` — this document.
- `Genesis_Castle_Art_Workflow_Manifest.json` — structured machine-readable reference and constraints.

**Critical rule:** Do not silently substitute the historical high-resolution-then-convert pipeline for the user's explicitly requested native-first pipeline. The historical process explains *why the art looked good*, but is not permission to violate current production constraints.
