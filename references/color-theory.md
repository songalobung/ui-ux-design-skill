# Color theory for usable interfaces

Color is a perceptual and cultural signal whose meaning depends on context, contrast, neighboring colors, display, and user. Use theory to generate and organize options, not to claim that a hue has a universal psychological effect. A useful palette is designed around roles and validated combinations.

## Start from purpose, content, and brand

Inspect existing brand assets and product conventions. Identify where color must help users distinguish action, selection, hierarchy, status, category, or data. Ask which information is safety- or decision-critical. Determine whether product content includes photography, charts, maps, or user-generated colors that constrain the palette.

Choose a deliberate color character based on product context, not stereotypes. A financial product may need calm and legibility, but “green means money” is not enough. A news product may use strong editorial identity while protecting neutrality and clear distinction between editorial content, advertising, and alerts. A hospitality brand may use atmosphere while preserving legible prices, booking details, and cancellation terms.

## Hue, chroma, and lightness

- **Hue** describes color family.
- **Chroma/saturation** describes intensity or vividness, depending on the color model.
- **Lightness/value** describes perceived light/dark appearance.

Changing one dimension can alter apparent contrast and emphasis. HSL/HSV values are convenient controls but are not perceptually uniform. Perceptual models such as OKLCH can help construct tonal ramps with more even perceived lightness; gamut mapping and display differences still require visual checking. No algorithmic palette is automatically accessible.

## Build semantic palette roles

Create roles before swatches:

- Canvas, page background, and raised surface.
- Primary and secondary text.
- Muted/supporting text and disabled content.
- Border, divider, and subtle interaction boundary.
- Primary, secondary, and destructive action.
- Link, focus, selected, hover, pressed, and visited states as relevant.
- Success, warning, error, and information statuses.
- Data series/category colors only for actual visualization needs.

For every role, define allowed foreground/background combinations and theme equivalents. Avoid raw colors scattered through components. Separate brand identity colors from functional status colors so a brand accent is not mistaken for error or success. Set focus colors for every surface and theme.

## Construct tonal scales

1. Select a primary brand hue or a neutral-first direction that fits real brand evidence.
2. Create a tonal range with enough lightness variation for text, surfaces, borders, selected states, and emphasis.
3. Create neutral ramps that coordinate without tinting every surface excessively.
4. Create status palettes distinguishable in hue and lightness; add non-color cues.
5. Test actual role pairings and states, not isolated swatches.
6. Validate under color-vision simulation and grayscale for information that depends on category/color distinction.

Use only as many hues as the product needs. Too many saturated accents cause competition. Keep charts' category colors distinguishable and meaningful; if the data has order or magnitude, use an appropriate sequential/diverging scheme rather than an arbitrary rainbow.

## Color harmony is not usability

Complementary, analogous, triadic, and monochromatic schemes are starting structures. They can make palettes feel related, but do not determine semantic meaning or contrast. A harmonious low-contrast palette still fails users. A vivid complementary combination may cause visual vibration. Check text, icons, borders, focus indicators, charts, and disabled states against their actual backgrounds and sizes.

Do not rely on generic color psychology charts. Interpret color in cultural, product, and task context. Validate emotionally loaded use—such as danger, finance, health, success, or political content—with appropriate domain experts and representative users.

## Contrast and non-color cues

Use the relevant WCAG success criteria for the specific content and component. WCAG 2.2 includes distinct criteria for text contrast and non-text contrast, and their exact applicability/definitions matter; see the normative specification and `accessibility-inclusive-design.md`. Do not cite a single contrast ratio as universal for every element or state. Record exact foreground/background tokens, font size/weight where relevant, and the criterion checked.

Pair color with labels, icons, shapes, line styles, patterns, or position. For charts, label series directly where practical and include a text/data alternative. For errors, include clear text and field association. For selected controls, use shape/border/checkmark as well as color. Check focus in light/dark themes and over images.

## Themes and surfaces

Design light and dark themes as semantic mappings, not simple inversion. Dark surfaces need appropriate tonal relationships; pure black and pure white can be harsh or flatten depth depending on context. Verify text contrast, subdued text, borders, overlays, elevation, selected states, focus, charts, and imagery separately. Avoid translucent surfaces unless all backgrounds keep content legible. Test operating-system forced colors/high-contrast settings where applicable.

## Color and data visualization

Select colors based on the data's semantics and analytical task. Use sequential color for ordered magnitude, diverging color around a meaningful midpoint, and categorical colors for distinct groups. Label axes, units, dates, source, and uncertainty. Do not use red/green as the sole distinction. Use direct labels, patterns, line styles, markers, or accompanying tables. Choose palettes that remain distinguishable for color-vision differences and in grayscale when needed.

## Color decision record

For each palette, document the source/brand rationale, semantic roles, token definitions, allowed pairings, light/dark mapping, status behavior, contrast checks, non-color cues, data visualization strategy, and unresolved risks. Retest the rendered implementation, since alpha compositing, gradients, images, anti-aliasing, and themes alter the actual color.

## Useful tools and caution

Contrast calculators and color-vision simulators can help identify likely issues. They do not establish overall accessibility or usability. Test real rendered pairs and use the normative standard for compliance. Do not trust screenshot sampling alone when translucency, dynamic content, or display differences are involved.
