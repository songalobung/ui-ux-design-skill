# Tool selection and design workflow

## Guiding principle

> **Discover broadly. Select intelligently. Implement consistently. Evaluate objectively.**

This is a decision discipline, not an instruction to use every site or install every library. Start from the product, users, task, constraints, and existing codebase. Choose only tools that improve a real decision or implementation outcome. A tool's presence in this catalogue is not an endorsement, a guarantee of quality, or a license grant.

## Tool-selection rules

1. **Inspect before introducing.** Check the existing framework, design system, tokens, component primitives, dependencies, and team conventions. Prefer extending the established system over adding a competing stack.
2. **Separate discovery from evidence.** Inspiration galleries show examples; flow libraries show captured behavior; neither proves usability, accessibility, conversion, or business success. Describe observations separately from hypotheses.
3. **Compare options against the brief.** Use a small, decision-relevant set. Explain the strongest benefit, trade-off, and risk of the selected option. Do not produce a long undifferentiated list.
4. **Verify current details at primary sources.** Package APIs, release status, compatibility, prices, permissions, image terms, font licenses, and catalog contents change. Confirm at selection/implementation time.
5. **Respect ownership and rights.** Prefer copying the idea of a pattern, not proprietary code, illustrations, images, or distinctive compositions. Check exact asset/license terms, attribution, redistribution, modification, and commercial-use conditions. Keep a source record.
6. **Use the least capable tool that solves the problem.** Avoid high-cost or high-complexity systems (for example, WebGL, a new animation runtime, or multiple component kits) when CSS and native controls meet the need.
7. **Maintain one coherent implementation system.** A chosen design system governs tokens, components, icons, and interaction conventions. Do not mix libraries opportunistically without an integration plan.
8. **Evaluate the result, not the tool's promise.** Run the UI, inspect screenshots at target breakpoints, test real interactions, and document unverified areas. Automated checks are partial evidence, never the entire accessibility or usability evaluation.

## Discovery-to-delivery sequence

### 1. Discover broadly

Use more than one kind of evidence when the decision merits research:

- **Product/user context:** brief, existing support feedback, observed tasks, analytics if genuinely available, stakeholder constraints, user interviews/usability studies where feasible.
- **Market and visual references:** relevant competitors and category conventions; Awwwards, Godly, or the user's listed visual galleries for creative direction; actual shipped product interfaces for task patterns.
- **Task flows:** Mobbin, Page Flows, Refero, or observed products to trace end-to-end steps such as signup, search, booking, checkout, settings, and recovery.
- **Asset exploration:** font catalogs, icon libraries, stock photography, illustration catalogs, and motion/3D examples as needed.

For each reference, record: source and capture date if relevant; product/platform; user's task; observed layout/behavior; what works or fails in this context; what is an inference; what should be adapted; rights/implementation caveats. Seek contrasting examples rather than merely collecting similar screenshots.

### 2. Select intelligently

Write the selection criteria before choosing. Typical criteria are product fit, audience/context, legibility, task efficiency, accessibility, consistency, responsive behavior, localization, performance, implementation fit, maintainability, license, cost, and operational risk. Compare at least two plausible options for consequential choices; for low-risk routine decisions, one reasoned option plus a fallback is enough.

Before implementation, define a short **design DNA**: product purpose; user promise; audience/context; brand attributes; visual tension (for example, calm precision vs. energetic optimism); selected design principles; signature element; avoid-list; type/color/layout direction; and non-negotiable usability/accessibility constraints. Translate this identity into tokens and component rules, not just adjectives.

### 3. Implement consistently

Use the existing framework and repository conventions. Select a single primary component foundation and a single icon family unless there is an explicit reason to differ. Add motion or 3D as progressively enhanced layers around a useful, readable baseline. Keep content, structure, and interaction functional if decorative media or advanced rendering fails. Make assets responsive and optimize font/image payloads.

### 4. Evaluate objectively

Evaluate with evidence at three levels:

- **Task and behavior:** Can the target user understand and complete the task? Are choices, errors, progress, and recovery clear?
- **Accessibility and robustness:** Keyboard, focus, semantic names, touch, zoom/text size, contrast, reduced motion, screen-reader support where possible, network/device limitations, and RTL/long-content behavior.
- **Visual and technical quality:** Actual render at target widths, hierarchy, density, spacing, type, crop, consistency, interaction states, console/network errors, test results, and relevant performance measures.

If a defect appears, describe its observed consequence, severity, reproduction context, and correction. Re-run the relevant checks after changes. Do not use a numeric “design score” as a substitute for user outcomes or professional judgment.

## Tool categories and choosing among named options

The links below are starting points, not required integrations. Use official documentation and source terms, not secondary summaries, for final decisions.

| Need | Candidate sources | Choose when / selection test |
|---|---|---|
| **Color scales and contrast-aware palettes** | [Radix Colors](https://www.radix-ui.com/colors), [Leonardo](https://leonardocolor.io/), [Huetone](https://huetone.ardov.me/) | Use a palette tool to explore perceptually coherent scales and semantic roles. Test actual text, controls, states, light/dark themes, charts, and translucency. Do not assume a generated palette passes every contrast requirement; measure the real foreground/background pairs and validate non-text cues. |
| **Font discovery and delivery** | [Google Fonts](https://fonts.google.com/), [Fontshare](https://www.fontshare.com/), [Fontsource](https://fontsource.org/) | Use catalogs to compare family traits, language coverage, weights/axes, variable-font support, and implementation. Choose delivery based on project constraints (hosted vs. self-hosted, caching/privacy/performance). Verify the individual font's current license and exact glyph coverage. |
| **Typography research and pairing** | [Typewolf](https://www.typewolf.com/), [Fontjoy](https://fontjoy.com/) | Use Typewolf for applied typography references and Fontjoy for candidate-pair exploration. Treat pair suggestions as hypotheses. Preview the actual brand name, headings, paragraphs, numerals, UI labels, and supported scripts at real sizes/line lengths; check visual hierarchy and readability. |
| **Product/UI and flow research** | [Mobbin](https://mobbin.com/), [Page Flows](https://pageflows.com/), [Refero](https://refero.design/) | Use searchable shipped screens and recorded/organized flows to understand conventions and alternatives. Trace the whole user task rather than cloning one screen. Record what is visible versus what is inferred; these libraries do not establish user success or causal outcomes. |
| **Creative website/visual research** | [Godly](https://godly.website/), [Awwwards](https://www.awwwards.com/) | Use as visual exploration for composition, art direction, atmosphere, interaction ideas, and craft. Translate inspiration into a product-appropriate principle. Do not let award aesthetics override clarity, accessibility, performance, or mobile behavior. |
| **Functional components/primitives** | [shadcn/ui](https://ui.shadcn.com/docs/components), [Base UI](https://base-ui.com/), [Radix Primitives](https://www.radix-ui.com/primitives) | Decide by framework/version fit, existing project, primitive behavior, keyboard/focus semantics, customizability, maintenance, and accessibility documentation. shadcn/ui supplies code intended to be customized; Base UI and Radix are lower-level primitive foundations. Never assume components are accessible in the app without correct composition, names, labels, and tests. Check current compatibility and shadcn's current underlying/default primitives before adopting. |
| **Creative/animated components** | [21st.dev](https://21st.dev/), [Magic UI](https://magicui.design/), [Aceternity UI](https://ui.aceternity.com/) | Browse for visual ideas or narrowly selected implementation blocks. Inspect dependencies, source code, keyboard/touch/reduced-motion behavior, responsive constraints, license/tier, and component quality before copying. Treat complex backgrounds/effects as optional decoration; test hierarchy and performance in the actual page. |
| **2D interface animation** | [Motion](https://motion.dev/), [GSAP](https://gsap.com/), [Rive](https://rive.app/) | Choose based on the animation: simple state transitions often need CSS; Motion fits UI/layout/gesture work in supported frameworks; GSAP fits timeline/choreography and broader DOM/SVG/WebGL sequences; Rive fits authored interactive vector/character assets with state logic. Avoid overlapping animation frameworks. Confirm current bundle/engine and licensing details. Respect reduced-motion settings and provide static/functional alternatives. |
| **3D and real-time scenes** | [Three.js](https://threejs.org/), [React Three Fiber](https://r3f.docs.pmnd.rs/) | Use only when spatial interaction or 3D imagery is central enough to justify runtime, asset, performance, accessibility, and fallback costs. Three.js is the underlying JS 3D library; React Three Fiber is a React renderer for Three.js. Design a non-WebGL fallback, optimize assets, support touch/keyboard alternatives where interaction matters, and test on lower-power devices. |
| **Icons** | [Lucide](https://lucide.dev/), [Phosphor](https://phosphoricons.com/), [Tabler](https://tabler.io/icons) | Pick one coherent family by semantics, coverage, style, available packages, RTL/filled/weight needs, and license. Use icons consistently and provide accessible names for icon-only controls; decorative icons should be hidden from assistive technology. Do not use an icon where a text label is necessary to disambiguate an action. |
| **Illustration** | [unDraw](https://undraw.co/), [DrawKit](https://www.drawkit.com/) | Use when illustration contributes to brand, explanation, or empty-state tone. Verify exact asset license, attribution, editability, export format, and whether free/paid collections differ. Maintain consistent stroke, palette, perspective, and scale; do not use illustrations to obscure the actual task or substitute for missing product content. |
| **Photography** | [Unsplash](https://unsplash.com/), [Pexels](https://www.pexels.com/) | Select imagery for subject relevance, cultural representation, focal point, crop resilience, authenticity, and legal suitability. Read current platform and item-specific terms; do not equate a stock library's general license with clearance for every recognizable person, trademark, property, or sensitive use. Use appropriate responsive formats, dimensions, and alternative text. |
| **Visual and component QA** | [Playwright](https://playwright.dev/), [Storybook](https://storybook.js.org/), [axe-core](https://github.com/dequelabs/axe-core) | Use Playwright for repeatable browser flows, responsive checks, and screenshots; Storybook for isolated component/state review; axe-core for automated detection of some accessibility issues. Automate stable checks and compare screenshots only under controlled viewport/font/data conditions. Add manual keyboard, screen-reader, zoom, and usability checks. A clean axe scan is not proof of WCAG conformance. |

## Palette, type, and composition decision records

For each consequential selection, leave a short rationale in the design brief or code/design-system documentation:

- **Color:** semantic role; why the hue/chroma/lightness fit brand and context; tested foreground/background pairs; status colors; dark/high-contrast variants; chart palette if needed; contrast and non-color cues; color vision considerations; token mapping.
- **Typography:** primary/secondary roles; rationale against brand, task, audience, reading conditions, and scripts; hierarchy/scale; weight and line-height choices; number/data treatment; fallback stack; loading strategy; license and coverage checks.
- **Layout:** task priority; information hierarchy; chosen grid/composition; reading/scan path; content density; responsive transformations (not merely shrinkage); placement of actions; expected empty/loading/error states.
- **Visual identity:** distinctive elements and their product purpose; image/illustration style; surface/depth strategy; decoration intentionally rejected; consistency rules and exceptions.

Rationale must be testable and specific (“the comparison matrix keeps the three eligibility differences visible before checkout”), not empty praise (“more premium”).

## Cross-library and license safety

Do not confuse source discovery permissions with rights to reuse. A screenshot, demo, template, font preview, photograph, icon set, or component may have different licenses. Keep records of asset URL, creator/source, date, downloaded file, license text/version, attribution obligations, edits, and intended use. Do not hotlink or redistribute content contrary to terms. Treat paid tiers, MCP/API access, quotas, and commercial rights as volatile; check the official page immediately before use.

## Accessible evaluation: automation plus people

Use automated tools for repeatable, machine-detectable issues, not as the sole audit. Run keyboard-only tasks, check focus order and visibility, test dynamic announcement/focus management with relevant screen readers when feasible, zoom/reflow, reduced motion, high contrast/forced colors where applicable, touch targets, and real copy. Include disabled users in research/testing when appropriate and feasible. Record not-tested items explicitly.

## Sources and maintenance

A set of primary-source notes is in [`tool-source-notes.md`](tool-source-notes.md). Catalog links and product features are volatile. Re-check them at the time of use; this reference intentionally avoids asserting current prices, availability, or blanket license rights.
