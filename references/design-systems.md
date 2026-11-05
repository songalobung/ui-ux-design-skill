# Design systems: foundations, components, and governance

A design system is a maintained agreement about visual language, content, interaction, implementation, and ownership. It is more than a component library, and reusing a component does not guarantee a coherent or accessible experience. Build the smallest system that improves repeated work and quality.

## Start with an audit

Inspect existing design files, code, tokens, components, content guidelines, platform patterns, and known accessibility issues. Map duplicate or inconsistent patterns. Identify who maintains the system, how teams contribute, and which products/platforms it serves. Do not create a new token architecture over an established system without understanding migration cost.

## Layered architecture

### Foundations
Color ramps and roles, typography, spacing, grid/breakpoints, radii, borders, elevation, icon rules, motion, and content conventions. Define platform differences intentionally.

### Semantic tokens
Names describe purpose, such as `text-primary`, `surface-raised`, `border-subtle`, `action-primary`, `focus-ring`, or `status-error`. Provide theme mappings and allowed pairings. Separate brand values from functional status.

### Component tokens
Use only when a component needs a deliberate local role. Avoid redundant aliases that obscure the source of truth.

### Components and patterns
Components implement reusable structure and behavior. Patterns compose components into repeatable tasks such as search, onboarding, or a confirmation flow. Document both anatomy and user intent.

### Templates and page compositions
Templates define layouts for content types or task contexts. They should not force unrelated products into identical structure.

## Token design

Tokens should be stable, meaningful, discoverable, and mapped to implementation. Avoid names tied only to raw appearance when a semantic role is known. Preserve raw primitives where useful but restrict direct use in feature code. Document allowed pairings, states, theme behavior, and exceptions.

Do not create a token for every value. Tokens are useful when a value is reused, meaningful, or expected to change systematically. A one-off value may remain local. Establish naming, deprecation, versioning, and migration rules before a token set grows.

## Component contract

For each component, document:

- Purpose and appropriate/non-appropriate use cases.
- Semantic element/role and content structure.
- API, slots, props, defaults, variants, and controlled/uncontrolled behavior.
- All relevant states and transitions.
- Keyboard, focus, naming, announcements, and screen-reader behavior.
- Responsive and localization behavior.
- Theming and customization boundaries.
- Dependencies, performance implications, and license.
- Examples, edge cases, known limitations, and test coverage.

Prefer composition and a small number of clear variants over a large flag matrix. Keep appearance customizable without allowing teams to break semantic behavior. Do not hide implementation details that teams need to maintain or debug.

## Accessibility built into the system

Use native semantics and tested primitives. Include visible focus, keyboard interaction, reduced motion, labels, error states, status announcements, contrast-safe tokens, text resize, and localization in component design and tests. Test components in realistic compositions, since overlays, sticky bars, and surrounding layout can introduce failures. State supported browser/assistive-technology coverage honestly. A design system cannot certify the product assembled from it.

## Contribution and governance

Define how requests are proposed, who reviews, how accessibility is assessed, how changes are released, and how consumers migrate. Allow product-specific exceptions when they are justified and documented. Do not centralize every decision if doing so blocks local learning; do not permit uncontrolled forks that create incompatible behavior. Track adoption and recurring defects as evidence of system health, not only component counts.

## Documentation quality

Good documentation answers: What problem does this solve? When should I use it? What should I not use it for? How does it behave? What content belongs in it? What are the variants/states? How do I make it accessible? How does it adapt? How do I install/test/update it? Include live examples only when they demonstrate meaningful behavior and edge states, not merely a pretty default.

## System health signals

Consider consistency across products, adoption, duplicate patterns, accessibility findings, support burden, contribution flow, release stability, and time-to-completion. Do not equate adoption with usability; a mandated component may be widely used and still harmful. Seek evidence from teams and end users.

## Adoption and third-party libraries

Before reusing a library or catalog component, inspect implementation, dependencies, accessibility, maintenance activity, license, theming, framework fit, and update path. “Copy-paste” can create ownership but also makes updates and provenance harder. Record origin and license in the project. Do not copy code or assets into the knowledge library unless the rights explicitly allow it.
