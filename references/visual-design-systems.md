# Visual design systems and interface craft

Visual design is how a product makes structure, priority, tone, and action perceivable. It should help people understand what matters and what to do. It is not a layer of decoration added after usability; it expresses the interface's information architecture and behavior.

## Establish a coherent direction

Before styling, inspect the product's current brand, audience, content, platform, and existing design system. Define a few principles (for example: calm and precise; warm and editorial; dense but highly scannable) and translate each into visible choices. Do not mix unrelated references into a mood board without a reason. Avoid defaulting every product to the same dark dashboard, giant gradient hero, pill button, blur, or card grid.

Use references to identify the role of a pattern, not to trace its exact appearance. Ask what the reference makes easy, which visual relationships carry meaning, and what should change for the user's task, brand, content, and platform. Avoid copying proprietary layouts, distinctive illustration, code, assets, or brand expression without permission.

## Hierarchy and composition

Design hierarchy through a consistent combination of size, weight, placement, spacing, contrast, grouping, and semantic structure. There should be a clear first read, useful secondary information, and an obvious next action. Do not make every element loud. Keep primary and secondary actions visually distinct without making secondary tasks impossible to find.

Align related elements to a deliberate grid. Use spacing to show grouping and separation rather than applying arbitrary gaps. Choose a content width that supports reading; avoid long unbroken text measures. Keep line lengths, text blocks, and page density appropriate to the task. Empty space should clarify relationships, not conceal a lack of content.

Use cards only when separation, grouping, or independent actions justify them. A border, heading, or whitespace may be clearer and less visually heavy. Avoid nested cards and piles of containers that flatten hierarchy.

## Typography and language

Use a type scale with a small number of roles: display, page title, section heading, body, supporting text, label, and metadata. Define line height, weight, and measure alongside size. Use the platform's readable system fonts unless brand needs justify a tested font. Check variable glyph support and licensing before adding a font.

Maintain readable size and contrast at normal and enlarged text settings. Do not use tiny low-contrast metadata as the only path to key information. Use weight and size consistently; reserve all caps, italics, and letter spacing for restrained purposes. Test long headings, translated strings, user-generated content, and text enlargement for clipping and awkward wraps.

Content is interface design. Use concise, concrete words; name actions with verbs and outcomes. Keep labels stable across the product. Use sentence case unless the existing design system has a reasoned convention. Avoid vague buttons such as “Continue” when the actual consequence can be named; avoid jargon, unexplained abbreviations, and decorative placeholder text.

## Color and semantic tokens

Create semantic roles rather than scattering raw hex values: canvas/background, surface/elevated surface, primary/secondary text, muted text, border, primary action, focus, selection, success, warning, error, and informational status. Map tokens to light/dark themes and ensure each relevant interactive state is covered. Keep brand color distinct from functional state color so an error is not confused with an accent.

Check contrast with the actual rendered colors and text sizes, including hover, focus, disabled, selected, overlays, charts, gradients, and imagery. A color palette that looks harmonious may still fail contrast. Never rely on color alone; pair it with text, shape, position, or iconography. Use accessible contrast checks against the applicable criterion; see the accessibility reference for normative scope.

## Spacing, shape, borders, and elevation

Define a consistent spacing scale and use it to express relationships. Repeated components should share alignment, padding, and dimensions unless a clear contextual difference exists. Establish a small, purposeful radius scale and use it consistently; do not round everything by default. Use borders to define boundaries and elevation only when layering matters. Avoid shadow stacks, heavy borders, and gradient outlines that create noise or reduce legibility.

## Layout and responsive systems

Create layouts that adapt to content and available space. Prefer intrinsic sizing, flexible grids, and sensible min/max constraints over brittle fixed widths. Define behavior at content-driven breakpoints where layouts stop working, not only at device labels. Check narrow and wide screens, zoom, text resizing, localization, and mixed content lengths.

On narrow screens, preserve task priority; stack or recompose content rather than shrinking all columns. Decide which secondary details can collapse, scroll, or move to another view without hiding critical information. Avoid horizontal scrolling for ordinary page content; when a wide data table genuinely requires it, make the scroll affordance clear and maintain access to headings and controls.

## Imagery, icons, charts, and data density

Use imagery only when it communicates product, context, evidence, or emotion meaningfully. Ensure the image is licensed for the intended use, represents people respectfully, and crops well at target sizes. Avoid generic stock imagery that implies false customers, locations, or product capabilities. Provide suitable text alternatives according to image purpose.

Use one coherent icon family with consistent size, stroke, alignment, and accessible labeling. Do not use an icon alone for unfamiliar or high-consequence actions. Ensure icon buttons have sufficient target area and clear focus. Use data visualization only when it helps compare or understand information; label axes, units, source, and uncertainty. Pair charts with text summaries or tables when needed. Do not decorate dashboards with meaningless metrics or invented data.

## Motion and visual effects

Treat motion as a design token and interaction language. Define purpose, duration, easing, distance, and reduced-motion alternative for recurring transitions. Use animation to show causality, state, or spatial relationship; keep decorative motion subordinate. Blur, translucency, shader effects, parallax, and 3D depth can hurt contrast, performance, battery, comprehension, or comfort. Apply them selectively and test actual content over actual backgrounds.

## Design tokens and component systems

Use a small token architecture that can be mapped to the current platform:

- **Foundations:** color, type, spacing, radii, borders, elevation, motion, breakpoints.
- **Semantic tokens:** roles that describe purpose rather than appearance.
- **Component tokens:** only where a component requires a deliberate exception.
- **Components:** semantic variants and interaction states, with documented behavior.

Do not create a token for every one-off value. Avoid token names tied only to a temporary visual (e.g., `blue-7`) when a stable role is available. Keep design tokens and implementation values synchronized. Document contrast and theme pairing constraints where useful.

Reuse platform-native components when they satisfy behavior and accessibility needs. A visually consistent component library is not automatically usable or accessible. Inspect its semantics, keyboard behavior, focus handling, reduced-motion support, localization, and terms before adopting it.

## Visual review questions

- What is the first thing a user notices, and is it the right thing?
- Can the user distinguish content, controls, and status at a glance?
- Are primary, secondary, and destructive actions visually and linguistically distinct?
- Does every decoration support hierarchy, meaning, brand, or feedback?
- Are spacing, type, color, borders, and motion consistent across states and pages?
- Does the interface stay clear with realistic content, long text, and enlarged text?
- Does the design remain coherent in all themes and responsive layouts?
- Are key meanings communicated beyond color and visual position?
