# Typography for interfaces and editorial products

Typography is functional infrastructure and visual voice. Select it for reading, scanning, language, product character, platform, performance, and license—not because a specimen looks fashionable.

## Begin with the content and language

Inventory the actual text: short labels, body copy, long headings, numbers, prices, tables, code, dates, names, and error messages. List every required language and writing system. Verify the font contains necessary glyphs, punctuation, currency, diacritics, numerals, and combining marks. Check fallback behavior for mixed scripts and emoji. A typeface that looks excellent in a Latin demo may fail for Arabic, Devanagari, CJK, or another script; use an appropriate script-specific family when needed and check shaping, direction, line breaking, and joining in real text.

For multilingual interfaces, allow text expansion, right-to-left layout, locale-specific number/date forms, and different line-height needs. Avoid truncation as the default response to translated text. Test navigation, buttons, validation, and dense data at realistic lengths.

## Typeface categories and roles

Serif, sans serif, slab, monospaced, humanist, grotesque, geometric, and display labels are broad descriptions, not quality rankings. Evaluate actual letterforms, rhythm, numerals, and language support.

- **Interface/body face:** clear at small sizes, distinguishes similar characters, has useful weights, and behaves consistently across target rendering environments.
- **Display face:** carries identity in large headlines or editorial moments; confirm readability in mobile wrapping, navigation, and long text before using it broadly.
- **Data/monospaced face:** useful for aligned code or fixed-width values; avoid for ordinary prose unless content benefits from it.
- **System face:** often a strong option for performance and platform familiarity; still test cross-platform differences and brand needs.

A single family with a strong weight range is often enough. Add a second family only when it has a distinct role and creates a worthwhile hierarchy. Pairing requires both contrast and compatibility: compare x-height, proportions, stroke contrast, apertures, terminals, numeral design, and tone. Do not pair fonts solely because they are individually popular.

## Selection scorecard

For candidate typefaces, rate each factor against the actual use case rather than using a universal score threshold:

- Readability in body and dense UI text.
- Distinct character forms and numeral legibility.
- Language/script coverage and shaping quality.
- Weight/style range and variable-font support.
- Tone fit with product concept and content.
- Small-size and high-density rendering.
- Responsive wrapping and long-string behavior.
- File size, subset strategy, rendering and loading behavior.
- License scope, redistribution, embedding, and commercial terms.
- Fallback quality when custom fonts fail.

Use representative samples from the product to compare candidates: a realistic heading, paragraph, button, form label, price, error, table row, long name, and translated phrase. Compare at actual viewport sizes and on available target devices. Inspect font rendering in browser/platform, not only a design canvas.

## Build a type system

Define semantic roles rather than styling each text node independently:

- Display/hero title.
- Page title.
- Section heading.
- Subheading or card/list heading.
- Body primary and supporting.
- Label/control text.
- Button/action text.
- Metadata/caption.
- Data/code/numeric value where needed.

For each role, specify family, size, weight, line height, letter spacing, text transform, maximum measure, and responsive behavior. Use a modest scale with enough separation to show hierarchy. A mathematical scale can help generate options, but content and visual testing decide the final values. Define minimum readable sizes based on context and applicable platform/accessibility expectations; never shrink text merely to fit a fixed box.

Line length should support reading and scanning. Line height should suit font, script, size, and density. Use weight and spacing with restraint. Avoid long all-caps, excessive tracking on small text, ultra-light type on busy surfaces, and italics for long passages. Do not use size alone if it causes large text to overpower task content.

## Responsive and accessible type

Support browser zoom and text enlargement. Avoid fixed heights, clipped ellipses on essential content, and absolute positioning that breaks when text wraps. Check contrast for text in all states. Test line breaks at narrow widths, intermediate widths, large text, high contrast modes where relevant, and localization. Ensure links and controls remain distinct without relying only on color.

## Font loading and implementation

Use approved and licensed font files. Verify terms for web embedding, app embedding, modification, redistribution, self-hosting, and commercial use. If using a hosted font service, evaluate privacy, network dependencies, caching, and organizational policy. Do not assume a catalog entry or open-source code license covers the font file.

Load only required weights, styles, and subsets. Use robust local/system fallbacks with similar metrics where possible. Avoid invisible text while fonts load; choose a loading strategy that reduces layout shift without compromising readability. Test slow network and blocked third-party requests. Consider variable fonts when they reduce payload or support a coherent system, but verify actual file size and browser rendering.

## Editorial typography

Long-form products need a reading system: title/deck/byline/date, heading levels, body measure, paragraph rhythm, captions, quotes, links, lists, tables, footnotes, and related content. Keep source/author/date context clear. Distinguish headings semantically, not just visually. Use typographic contrast and whitespace to create rhythm without inserting arbitrary interruptions. Design a quiet reading mode only if it improves the reader's task and preserves navigation and accessibility.

## Common failures

- Choosing a display font for small interface controls because it looks distinctive.
- Using too many font families or weights without clear roles.
- Picking a font from Latin-only specimens for a multilingual product.
- Using tiny gray metadata for important terms, units, or prices.
- Fixing awkward wrapping with clipped content or smaller type.
- Ignoring numeral legibility in financial or analytical products.
- Using a font whose license or loading behavior is unknown.
- Trusting a design mockup while actual browsers render differently.

## Reference catalogs

Use catalogs to explore candidates, not as an endorsement. [Google Fonts](https://fonts.google.com/) provides searchable families; check each family’s specific license, script coverage, file variants, and current terms. Other commercial or foundry catalogs require the same item-level license and embedding checks. Verify current availability and licensing before shipping.
