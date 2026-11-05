# Curated UI/UX knowledge library

Use progressive disclosure: start with `SKILL.md`, identify the decision to make, and load the smallest useful group of references. Do not dump the entire library into every task. For substantial work, read a connected cluster rather than relying on generic model memory.

## Product, evidence, and design direction

- [`design-philosophy.md`](design-philosophy.md): product thinking, design reasoning, visual storytelling, trust, ethical persuasion, and restraint. Load for new products, a weak visual direction, or generic-looking screens.
- [`human-centered-process.md`](human-centered-process.md): ethical discovery, research, context, journey mapping, prioritization, and usability testing. Load when user need, flow, or evidence is uncertain.
- [`design-capability-playbook.md`](design-capability-playbook.md): decision procedures for product fit, research, creative direction, layout, typography, color, architecture, UX psychology, interaction, motion, responsiveness, QA, and multidisciplinary critique. Load for substantial design or high-craft work.
- [`design-intelligence-architecture.md`](design-intelligence-architecture.md): decision reasoning, visual critique, alternatives, screenshot interpretation, fidelity, regression, behavioral UX, content, responsive/performance checks, governance, project memory, benchmarking, controlled improvement, and cross-cutting capabilities. Load when designing an advanced design-assistant workflow or evaluating models/skills.

## Optional external tools and sources

- [`tool-selection-and-workflow.md`](tool-selection-and-workflow.md): operational method and catalogue for colors, fonts, typography research, UI/flow references, component libraries, motion, 3D, icons, illustration, photography, and QA. Load when selecting an external tool, asset, source, or implementation dependency. The list is optional, not an endorsed mandatory stack.
- [`tool-source-notes.md`](tool-source-notes.md): dated official-source URLs and role notes for a subset of listed tools. Use as starting links only; verify current documentation, compatibility, plan, terms, and licenses at the time of use.
- [`source-patterns.md`](source-patterns.md): patterns and cautions from the user's initial UI-library references. Use for inspiration research, never as user-outcome evidence or permission to copy assets/code.
- [`curated-source-research.md`](curated-source-research.md): verified source register for the user's added design books, UX articles, research overviews, and Apple/Meta references, with practical takeaways, evidence scope, provenance, and limitations. Load when choosing among these sources or adapting their advice.

## Choose by design problem

- **Style exploration:** [`design-styles.md`](design-styles.md) describes editorial, Swiss, minimal, brutalist, luxury, industrial, corporate, futuristic, playful, organic, and neo-brutal languages with contexts and risks. Treat styles as vocabulary, not presets.
- **Typography:** [`typography.md`](typography.md) covers typeface evaluation, pairing, scales, script coverage, font loading, licenses, and editorial systems.
- **Color:** [`color-theory.md`](color-theory.md) covers semantic roles, tonal scales, contrast, themes, charts, and cautious interpretation of color psychology.
- **Composition:** [`layout-patterns.md`](layout-patterns.md) covers grids, split view, dashboards, tables, editorial, landing pages, bento, asymmetry, full bleed, canvas, and responsive change.
- **Task patterns:** [`ux-patterns.md`](ux-patterns.md) covers navigation, onboarding, forms, search, checkout/booking, dashboards, news, SaaS, collaboration, and states.
- **Motion:** [`motion-design.md`](motion-design.md) covers purpose, timing, easing, micro-interactions, page/scroll transitions, reduced motion, and implementation cautions.
- **Systems:** [`design-systems.md`](design-systems.md) covers foundations, semantic tokens, component architecture, governance, adoption, and documentation.
- **Platforms:** [`platform-guidelines.md`](platform-guidelines.md) covers web, iOS/iPadOS, Android, desktop, tablet, and cross-platform adaptation. Check current official docs for exact platform details.

## Validation and access

- [`accessibility.md`](accessibility.md) is the quick index; [`accessibility-inclusive-design.md`](accessibility-inclusive-design.md) contains implementation guidance; [`standards-and-sources.md`](standards-and-sources.md) distinguishes normative and informative references.
- [`visual-qa.md`](visual-qa.md) covers rendered inspection, screenshot comparison, responsive coverage, defect severity, and correction loops. [`quality-assurance.md`](quality-assurance.md) adds usability and implementation evaluation.
- [`anti-ai-slop.md`](anti-ai-slop.md) defines AI slop as an informal term, synthesizes research on creative convergence and generated-interface gaps with scope caveats, then gives a practical critique/repair workflow. Use it as a product-specific review, not a ban on popular styles.
- [`interaction-patterns.md`](interaction-patterns.md) details interaction contracts, keyboard/focus, feedback, error recovery, and states.

## Templates

- [`../templates/design-brief.md`](../templates/design-brief.md): product context, evidence, composition, type, palette, architecture, interaction, motion, responsiveness, and validation.
- [`../templates/usability-test-plan.md`](../templates/usability-test-plan.md): respectful task-based usability sessions and evidence capture.
- [`../templates/design-decision-log.md`](../templates/design-decision-log.md): alternatives, evidence, rationale, trade-offs, implementation, validation, and revisit triggers.
- [`../templates/design-evaluation.md`](../templates/design-evaluation.md): actual test context, findings, coverage, limitations, and follow-up.

## Loading recipes

**New product or substantial redesign:** core + philosophy + human-centered process + capability playbook + design-intelligence architecture + brief; then load relevant style, layout, UX, accessibility, platform, and QA references.

**Visual refresh:** core + philosophy + styles + typography + color + layout + anti-AI-slop + visual QA; add product/competitor research and tool-selection guide if reference discovery or assets are needed.

**Choosing external references, assets, or libraries:** core + tool-selection-and-workflow + tool-source-notes + relevant design-system/accessibility/performance guidance. Check current docs and exact license/terms before reuse.

**E-commerce browsing or checkout:** core + UX patterns + interaction patterns + accessibility; consult `curated-source-research.md` for Baymard's ecommerce-specific heuristics and keep its scope/evidence caveats.

**Apple-platform implementation:** core + platform guidelines + accessibility + `curated-source-research.md`; use Apple HIG as Apple-specific guidance and verify current APIs and conventions at the official documentation.

**New interaction/component:** core + interaction patterns + design systems + accessibility + platform guidelines + visual QA; add the selected library's current official docs.

**Responsive screen:** core + layout patterns + UX patterns + platform guidelines + accessibility + visual QA; inspect actual renders across target widths and content.

**Accessibility review:** core + accessibility-inclusive-design + accessibility index + standards-and-sources + visual QA + evaluation template. State exact scope and avoid overclaiming.

**Design-to-code fidelity or regression:** core + design-intelligence architecture + visual QA + evaluation template; only report comparisons if reference and actual render were available under comparable conditions.

**Model/skill benchmark or improvement proposal:** core + design-intelligence architecture + decision log + evaluation template; define benchmark tasks/rubric first, record tool/model/version, and review changes before adoption.

## Maintenance policy

Keep durable methods separate from volatile facts. Standards, platform APIs, asset/font availability, package behavior, prices, licensing, and hosted-tool capabilities can change. Verify primary documentation before implementation or a compliance/legal claim, note review dates where useful, and never treat a source gallery as evidence that a design improved outcomes.
