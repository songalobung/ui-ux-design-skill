# Layout patterns and composition

Choose layout from task, content relationships, priority, device, and workflow—not from a fashionable component grid. The following patterns are starting points. Combine them only when their purposes remain clear.

## Composition decision sequence

1. List the user's primary task and decisions.
2. Inventory content units, actions, relationships, sequence, importance, and likely length.
3. Decide whether the task is linear, exploratory, comparative, monitoring-oriented, editorial, or spatial.
4. Choose a composition that exposes those relationships with the least unnecessary navigation or cognitive switching.
5. Define reading order, keyboard order, and semantic structure before visual polish.
6. Plan how the composition transforms at narrow, intermediate, and wide widths.
7. Stress-test content, localization, zoom, empty/error/loading states, and real behavior.

## Common patterns

### Single-column flow
Best for reading, forms, onboarding, and focused sequential tasks. It supports a clear reading order and narrow screens. Risks include excessive scrolling, buried progress, and weak orientation in long processes. Use section headings, meaningful progress, save/resume when needed, and contextual summaries; do not split a simple task into artificial steps.

### Two-column or split view
Useful when the user must keep a list, navigation, or summary visible while inspecting a detail/editor. Keep a clear master/detail relationship. On narrow screens, transition to an explicit list then detail view, with a visible return path and preserved selection. Do not squeeze columns until text and controls are unusable.

### Dashboard / overview
Useful for answering “what needs attention?” or comparing a small number of meaningful summaries. Put the highest-priority task/status first; distinguish urgent from informational; make date range, units, and data freshness visible. Avoid card grids full of vanity metrics and decorative charts. Provide drill-down and useful empty/error states.

### Table / data workspace
Useful for scanning and comparing records with shared fields. Choose columns by decision value, align numeric values, label units, expose sorting/filtering state, and preserve context when opening a record. At narrow widths, prioritize columns, allow a clearly signaled horizontal region, or provide a record-detail mode. Static semantic tables differ from interactive grids; custom keyboard behavior adds complexity.

### Editorial / article layout
Useful for long-form narrative, explanation, or analysis. Use a clear title, deck/summary, byline/date/source when relevant, readable measure, semantic heading levels, captions, links, and intentional paragraph rhythm. Ensure images are evidence/context rather than unsupported decoration. Keep related navigation and actions available without interrupting the reading task.

### Marketing/landing-page sequence
Useful when users need to evaluate an offer or product. Organize by the audience's questions: what it is, who it helps, why it matters, how it works, evidence, costs/terms, risks/objections, and next step. Use real product evidence and actual terms. Do not invent customer logos, reviews, certifications, outcomes, or urgency. Keep a clear path to pricing, support, and cancellation information.

### Bento / modular uneven grid
Useful when modules have genuinely different importance, content forms, or interaction needs. Establish a clear reading sequence and shared alignment. On mobile, reorder by task importance, not by the visual shape of the desktop grid. Risks include arbitrary card mosaics, inconsistent module sizes, and inaccessible source order.

### Asymmetric composition
Useful for editorial emphasis, distinctive brand expression, or a focal interaction. Keep alignment and hierarchy intentional. Check that the unusual geometry does not cause reading-order confusion, awkward empty zones, hidden actions, or mobile breakage.

### Full-bleed image or media hero
Useful when a real visual asset is central to context or story. Use a crop strategy that preserves subject meaning at multiple widths, provide text alternatives, and maintain contrast for overlaid text. Provide a non-image route to the essential message. Avoid using generic stock photography as false evidence or as a substitute for value proposition.

### Wizard / stepper
Useful when information is dependent, lengthy, or benefits from focused decisions. Show current position and consequences; preserve entries; support back/edit/review; make progress truthful. Avoid arbitrary steps and fake percentages. Give users a way to save or resume when interruption is likely.

### Map / timeline / canvas
Useful when spatial or temporal relationships are essential. Pair with a structured list or textual alternative. Provide keyboard navigation and non-drag controls. Explain scale, range, units, and current selection. Do not make the canvas the only way to access important information.

### Search-first / command interface
Useful when users know what they want and the dataset supports fast retrieval. Preserve scope, query, filters, and result context. Make empty and no-results states useful. Do not force memorized syntax when natural labels and controls can do the job; provide discoverable shortcuts rather than requiring them.

### Split narrative / scrollytelling
Useful when a guided sequence of content and visual evidence improves understanding. Ensure scroll is natural, content remains accessible without animation, and sticky visual regions do not obscure focus or reading. Provide reduced-motion behavior and a clear route through the content.

## Hierarchy, grid, and whitespace

A grid should support alignment and change gracefully as content and space change. Define a readable content width, flexible columns, gutters, and alignment anchors. Do not treat a 12-column grid as mandatory. Use consistent spacing to show grouping and separation. Whitespace is active structure: it can isolate a task, create rhythm, and reduce clutter, but excessive space can hide relationships or force needless scrolling.

Use contrast, size, position, weight, and grouping to establish the first read. Do not make all modules equally prominent. Keep labels close to controls and explanatory text close to decisions. Use cards only for genuine groupings or independent modules; avoid nested card-on-card stacks.

## Responsive composition is not simple shrinking

Define mobile, tablet/intermediate, and desktop layouts independently. At each context, specify priority, navigation, content order, density, input behavior, and overflow. Content-driven breakpoints are points where the current composition stops working, not merely a list of device sizes.

On narrow screens, simplify or re-sequence. Consider a list/detail transition, progressive disclosure, sticky action only when it does not obscure content, or a compact navigation pattern. On intermediate screens, avoid both oversized empty gutters and crammed desktop columns. On wide screens, use width for comparison and workflow, not excessively long text lines. Test intermediate widths, zoom, text expansion, orientation, keyboard focus, and real content.

## Pattern selection matrix

Ask what the task requires: sequential completion suggests a flow; comparison suggests aligned rows/columns; discovery suggests taxonomy and filters; monitoring suggests prioritized status; reading suggests editorial rhythm; spatial reasoning suggests map/canvas plus alternatives. If multiple tasks coexist, make the primary task clear and ensure secondary tasks do not compete. Record why the chosen composition is suitable and what evidence would change the decision.
