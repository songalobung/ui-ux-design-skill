# Source patterns and reference directory

This document records high-level patterns observed on the supplied sites. Use the patterns as design/workflow inspiration; do not copy their code, branded expression, or assets into another product without permission.

## Transferable patterns

Across the sources, strong component catalogs let users inspect a live preview before adoption, browse by task/category, and see implementation guidance such as variants, dependencies, props, install steps, and customization hooks. Good libraries cover meaningful states rather than showing a single static appearance.

Motion works best when it communicates feedback, progress, or state change. Prefer restrained interaction-triggered motion, calm defaults, reduced-motion support, and pausing nonessential offscreen animation. A design system should make common choices coherent through semantic tokens, shared variants, theme support, and stable customization points.

For implementation, treat a reference as a starting point: identify the user's task and the design role, adapt the result to the product's identity and existing stack, then validate semantics, accessibility, responsive behavior, and performance. Catalogs may offer atoms, complete flows, and larger page sections; choose the smallest composition that solves the task.

## Site notes

- [Rare UI](https://rareui.com): animated React examples; categorized discovery, live previews, purposeful state motion, integration docs. Its site-specific terms include component-level restrictions and attribution conditions; verify before reuse.
- [Kobra Systems](https://kobra.systems): previews with variants and states, props/composition details, install instructions, customization hooks, reduced-motion examples; some offerings are paid.
- [EasyUI](https://easyui.site): browsable components, live demos, typed APIs, spring motion, keyboard/ARIA and reduced-motion guidance.
- [Pin UI](https://pinui.xyz): visual-reference-inspired components and larger sections; discover by category, preview interactions, and move from inspiration to reusable implementation.
- [Aceternity UI](https://ui.aceternity.com): composition from primitives to blocks and landing pages; purposeful visual effects and categorized page patterns; paid/free offerings differ.
- [Great UI](https://www.great-ui.com/): previewable, customizable React/Tailwind components; cohesive theming, accessible interaction, restrained motion. Review its current terms, which may be more restrictive than a repository badge suggests.
- [Amicro](https://amicro.dev/): motion-focused React examples; group motion by behavior and use small interaction patterns as feedback, not decoration.
- [Afterglow UI](https://afterglowui.vercel.app/): tactile surfaces, motion, theme, responsive and performance considerations; check the published license for each item.
- [Puffy UI](https://puffyui.com/#components): category browsing, configurable live previews, shared theme controls, realistic application contexts; free and Pro materials may differ.
- [21st.dev](https://21st.dev): community discovery with multiple authored approaches, searchable categories, live previews, source and install pathways; verify item-level terms.
- [Gradient Deck](https://ui.gradientdeck.com): design-reference-to-spec workflow using semantic tokens, component recipes, constraints, and explicit implementation guidance.
- [Uiverse](https://uiverse.io): community examples, tagging/search, multiple export formats, author/source context, and small composable interaction details; verify the individual item and associated asset terms.

These observations were checked against the live sites on 2026-11-05. Catalog contents, counts, prices, licenses, and stack details can change; consult the linked source and the specific component before relying on them.

## Licensing and originality

A site calling a collection “free” or “open source,” or providing copy/install controls, does not establish that every component, image, font, icon, dependency, or template has identical reuse rights. Before reusing any specific material, inspect the license and terms that apply to that item. Check attribution, commercial use, modification, redistribution, bundled dependency, and standalone resale conditions. Preserve required notices. When permission is unclear, implement the general interaction or layout principle independently rather than copying expressive details.
