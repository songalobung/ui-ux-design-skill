# Design intelligence architecture and evaluation

## Purpose and limits

This guide operationalizes the advanced capability proposals in the user's attached note. It describes methods an assistant can follow; it does not magically provide visual perception, browser access, analytics, durable project memory, user research, or automated testing. Use only capabilities actually available in the host session. If a capability is unavailable, ask for the relevant input or produce a transparent manual proxy, label the limitation, and do not claim the automated capability ran.

The system's purpose is to connect **project context → design decisions → implementation → observed evaluation → controlled improvement**. It should not make aesthetic decisions by detached trend matching, fabricate evidence, or rewrite its own operating rules from unreviewed feedback.

## The connected design model

Keep these entities linked, in the simplest artifact format available (design brief, repository docs, issue tracker, token file, structured JSON, or actual knowledge graph):

1. **Project context:** product/service, audience and access context, user jobs, business/service goals, constraints, risks, platforms, locales, and available evidence.
2. **Design DNA:** brand attributes, chosen style direction, key differentiator, content voice, imagery approach, motion/depth stance, and rejected directions.
3. **Experience structure:** journey, information architecture, task hierarchy, responsive layouts, components, content, and states.
4. **Design decisions:** selected option, alternatives considered, criteria, evidence, assumptions, constraints, trade-offs, accessibility/performance implications, and rationale.
5. **Implementation:** framework, tokens, component variants, asset/font sources, versions, licenses, interactions, and known deviations from the intended design.
6. **Evaluation evidence:** test method/date/environment, participants or automated tool, task, observed result, severity, screenshots/trace references if available, limits, and follow-up.
7. **Learning:** accepted or rejected changes, reason, owner/reviewer, version, and whether the change improved an agreed outcome.

Each record should have an identifier and links to the relevant design, source, route/component, test, or issue where feasible. Do not create a heavy database for a small project; use an appropriately lightweight, durable format. If the environment has no persistent project memory, ask the user to provide or save a decision log rather than promising recall across sessions.

## 1. Design Reasoning Engine

For each material decision, reason from goals and constraints, not aesthetic adjectives. Use this compact record:

```text
Decision:
User/product objective:
Evidence available:
Assumptions and confidence:
Alternatives considered:
Criteria and constraints:
Selection and rationale:
Trade-offs / risks:
Accessibility, responsive, localization, performance effects:
How to verify; result:
```

A decision rationale must be falsifiable or inspectable. Example: “Use a persistent filter rail on desktop because analysts compare results across multiple categories; collapse it into a labeled filter drawer on narrow screens; validate task completion and discoverability.” “Looks premium” is not sufficient. State when a choice is a design hypothesis rather than research-backed truth.

## 2. Visual Taste and Critique

Treat visual taste as disciplined comparison and explanatory critique, not a mysterious universal score. Inspect:

- **Hierarchy:** Can a viewer identify the page purpose, primary action, and next step quickly? Does contrast match importance rather than decoration?
- **Typography:** Does type express the intended identity while remaining readable in actual content, data, small sizes, and supported scripts? Are pairing and scale coherent?
- **Composition:** Are alignment, grid, rhythm, density, whitespace, crop, and asymmetry intentional? Does the layout support scanning and task completion?
- **Coherence:** Do tokens, components, image treatments, icon weights, radii, borders, and motion feel like one system? Are exceptions deliberate?
- **Restraint:** Which decorative effects compete with the task? What can be removed without losing meaning, identity, or feedback?
- **Product fit:** Does the visual language fit the domain, stakes, trust needs, user context, and device conditions, rather than copying a generic SaaS pattern?

For each critique, state **observable evidence → user/product consequence → severity → proposed repair → validation**. If the agent cannot inspect a rendering, say so and critique only the source/design information actually available. Do not report pixel-level properties inferred from an inaccessible image.

## 3. Design Alternative Simulator

Before committing to a major page or direction with meaningful uncertainty, produce 3–5 genuinely different compositions. Change the underlying organizing idea—not just the background color. Example lanes: structured utility, editorial narrative, product demonstration, data-first workspace, expressive campaign. Include at least one low-decoration solution where appropriate.

For every option, show a lightweight wireframe/section outline plus rationale, strongest advantage, primary risk, user/task fit, accessibility and responsive risks, engineering/performance cost, and what evidence could decide between options. Compare them against criteria defined from the brief. Recommend one, explain the trade-off, preserve rejected alternatives and why, and prototype/test the uncertain part before investing in polish. Do not imply options were user-tested unless they were.

## 4. Screenshot and Reference Understanding

When an image/screenshot is available to a vision-capable model or browser/image tool, record only what is visible or explicitly described: viewport and device if known; hierarchy; grid and alignment; type roles; color roles; spacing/density; imagery and crop; component/state; likely interaction; and uncertainty. Separate **observation**, **interpretation**, and **hypothesis**. Check source and capture date when recency matters. For competitor/research libraries, compare more than one example and preserve URLs; a gallery is not user-outcome evidence.

When inspecting an existing website, do not assume a screenshot reveals semantics, focus behavior, responsive behavior, or hidden states. Inspect interactively or test those separately. Do not use screenshots as permission to copy proprietary visual assets or distinctive brand expression.

## 5. Design-to-Code Fidelity

Only perform fidelity checks if there is both an authorized reference (design file, specification, or supplied screenshot) and an actual implementation render. Match viewport, device scale, loaded fonts, data/content, theme, and state. Compare by region and prioritize:

1. content, hierarchy, and missing/extra sections;
2. container, column/grid, and alignment;
3. typography family, size, weight, line-height, wrapping;
4. spacing, control dimensions, radii, and borders;
5. image identity, crop, focal position, and responsive behavior;
6. colors, contrast, shadows, overlays, and surfaces;
7. interaction/focus/hover/active/disabled/loading states;
8. tablet/mobile transformations and overflow.

Use overlays, screenshot diffs, DOM geometry, or manual inspection only when the relevant tool is available. Pixel difference can be noisy from font rasterization, antialiasing, dynamic content, or browser variance; pair it with structural and human review. Report deviations with region, expected vs actual, impact, and proposed fix. Never state “pixel-perfect” without a defined reference, controlled environment, and actual comparison.

## 6. Visual Regression Intelligence

Choose stable representative routes, viewports, themes, and component states. Fix test data, animation timing, network dependencies, fonts, browser version, and color scheme as much as practical. Capture a baseline only after review and approval; use meaningful thresholding and exclude truly nondeterministic regions carefully. A screenshot change is a review signal, not automatically a defect. Inspect diffs, classify intended vs unintended changes, correct regressions, then rerun affected tests. Keep baseline updates auditable and do not accept them wholesale to silence failures.

## 7. Behavioral UX and Friction Analysis

For each critical task, map trigger → prerequisites → decisions → actions → system response → success/recovery. Identify unnecessary decisions, memory burden, repeated entry, ambiguous labels, delayed feedback, hidden costs/conditions, interruption risk, error-prone fields, inaccessible control modes, trust gaps, and dead ends. Consider frequency and consequence, not only step count: fewer steps are not automatically better if they hide a consequential choice. Use observed user evidence when available; otherwise label friction points as hypotheses.

Check prevention and recovery together: defaults, validation timing, undo/back, confirmation for high-impact irreversible actions, progress feedback, save/resume, and support routes. Avoid manipulative patterns, false urgency, coercive defaults, or dark patterns. In sensitive finance, health, identity, privacy, and security contexts, prioritize transparency, user control, and explicit consequence communication.

## 8. Accessibility Intelligence

Target WCAG 2.2 AA where applicable and requested, using the current normative text and exact conformance scope. A tool scan or this guide is not a conformance claim. Check semantics, names/labels, keyboard operation, focus order/visibility/management, contrast and non-color signals, touch/pointer alternatives, zoom/reflow, text spacing, error identification/recovery, status announcements, timing, reduced motion, and meaningful screen-reader output. Combine automation with manual evaluation and disabled-user input when feasible. Record exceptions, scope, test environment, untested areas, severity, and remediation. Never silently downgrade a known barrier.

## 9. Content and Information Architecture

Model the content hierarchy around user questions and decisions. Define page purpose, heading outline, information priority, navigation names, content model, field labels/help, calls to action, and empty/loading/error/success states. Use realistic copy early: strings affect wrapping, layout, translation, and trust. Avoid filler or fabricated claims, metrics, testimonials, logos, and guarantees. Review plain language, localization, inclusive wording, scannability, data provenance, date/number formats, and how users interpret consequential terms.

## 10. Responsive Intelligence

Design for actual task context at target sizes rather than scaling a desktop canvas down. Decide deliberately how navigation changes, which content keeps priority, how grids/columns transform, what becomes scrollable or collapsible, how controls adapt for touch, how charts/tables remain interpretable, and how media crops shift. Test narrow/wide breakpoints, intermediate widths, zoom, long labels, error messages, empty states, RTL, orientation, and actual touch/keyboard behavior. Use intrinsic layouts and content-driven breakpoints where suitable; do not assume a fixed set of devices covers every failure.

## 11. Performance Intelligence

Treat perceived and measured performance as design constraints. Inspect font loading and fallback shift; image/video format, size, dimensions, and responsive sources; lazy loading; layout stability; route/bundle weight; rendering and animation cost; third-party scripts; and low-end device/network behavior. Use Lighthouse or equivalent and real-user/Core Web Vitals data only when available. Distinguish lab metrics from field metrics; state sample, date, and device/network assumptions. Keep interactions responsive, animate transforms/opacity where suitable, avoid gratuitous scroll effects and excessive WebGL, and provide fallbacks. Do not promise improved conversions from speed scores alone.

## 12. Design-System Governance

Define a source of truth for design tokens, components, variants, content patterns, and platform exceptions. Review for duplicate components, semantic token drift, arbitrary values, inconsistent names/states, unapproved fonts/colors, unsafe overrides, accessibility regressions, and unnecessary dependencies. Use a contribution process with owner, rationale, usage examples, variants, accessibility contract, responsive behavior, version/change notes, and deprecation/migration plan. Permit justified exceptions and document them; governance serves products and teams rather than enforcing uniformity for its own sake.

## 13. Project Design Memory

Maintain a short decision log within a project repository or memory mechanism when one is actually available. Preserve the current Design DNA, approved tokens, component choices, constraints, accessibility needs, asset/license notes, decisions, rejected options with reasons, known defects, evaluation findings, and unresolved hypotheses. Store decision date/version and source links for volatile facts. Revisit stale choices when product context, user evidence, platform, or standards change. Never claim cross-session memory unless it is available and persisted.

## 14. Benchmark and Evaluation Engine

When comparing models, prompts, or skill revisions, use a small benchmark suite of representative tasks with identical inputs and constraints. Include varied domains (for example, booking, finance, editorial/news, SaaS), task types (new design, existing-system change, responsive fix, complex interaction, accessibility issue), and quality risks. Use a rubric defined before seeing outputs: user/task fit; visual hierarchy and distinctiveness; behavior/states; accessibility; responsive robustness; content accuracy; implementation correctness/maintainability; performance; and honest evidence reporting.

Use blinded evaluation when possible, multiple evaluators or repeat runs where variance matters, and record model/version, tools, environment, tokens/cost/time if available. Keep output artifacts and evaluation evidence. Report sample size and uncertainty; avoid claiming benchmark superiority from a few subjective examples. Distinguish model capability from tool access, prompt, and human intervention. Protect private project data and honor evaluation consent/retention rules.

## 15. Controlled continuous improvement

Turn recurring failures into a proposed change with a traceable problem, examples, root-cause hypothesis, affected instruction/reference/tool, expected result, possible regressions, and benchmark cases. Change one coherent factor at a time when practical. Run the same benchmark and review for regressions before adoption. Preserve previous versions and a rollback path; request human review for high-impact rule, policy, or standard changes. Do not let a model silently rewrite core instructions because of one task or user preference. Record accepted/rejected changes and the rationale.

## Cross-cutting capabilities

### Internationalization and localization

Plan for target languages/scripts, font glyph and shaping support, variable text length, RTL and bidirectional content, locale-specific date/time/number/currency formats, pluralization, reading order, culturally appropriate imagery/examples, and local conventions. Keep strings externalizable; avoid concatenation assumptions; test pseudo-localized and RTL layouts if supported. Locale choice must follow the actual user/service market, not stereotypes.

### Data visualization intelligence

Identify the decision users need to make, data provenance/uncertainty, units, temporal context, meaningful comparisons, and appropriate chart/table form. Make axes, labels, legends, keyboard access, summaries, color-safe distinctions, and nonvisual alternatives usable. Avoid deceptive scales and color-only encoding. Test small screens, high density, large values, missing data, and table alternatives. Do not invent or smooth data to improve aesthetics.

### Trust and security UX

For permissions, account changes, payments, security, privacy, deletion, and sensitive data, clearly identify actor, data, purpose, consequences, scope, reversibility, and time. Use least surprise, proportionate confirmation, accessible authentication, explicit permission controls, and truthful success/failure states. Do not create fake security assurance or overburden low-risk actions with friction. Consider abuse, shared devices, recovery, audit history, and safe defaults.

### Microcopy intelligence

Use concise, concrete, respectful language that tells the user what is happening, what information/action is needed, why it matters when consequential, and how to recover. Prefer specific labels over clever ambiguity. Validate examples with realistic content, localization, assistive technology announcements, and legal/product owners for regulated claims. Avoid blame, false certainty, manipulation, and unsupported promises.

### Design experimentation

State one testable hypothesis linking a change to an expected user behavior or outcome. Define eligibility, variants, primary and guardrail metrics, duration/sample assumptions, instrumentation, accessibility/privacy safeguards, and analysis plan before launch. Avoid experimentation on high-stakes flows without appropriate ethical and product review. Do not infer causality from uncontrolled comparisons. Use qualitative research alongside metrics; retain the better experience, not just the higher short-term conversion if harm or comprehension declines.

## Practical completion checklist

Before handoff, confirm or disclose:

- Are product goals and user tasks explicit, with evidence vs. assumptions separated?
- Was more than one plausible design direction explored when uncertainty warranted it?
- Are visual and implementation decisions connected through rationale, tokens, and components?
- Was the actual rendered interface inspected at relevant viewports and states, if tools allowed?
- Were interactions, errors, keyboard/focus, reduced motion, and responsive transformations evaluated?
- Were assets, fonts, components, packages, and reference sources checked for current compatibility and rights?
- Are automated/manual/user checks identified precisely, with limitations and open issues?
- Are project decisions and lessons persisted only where actual project memory exists?
- Is any suggested improvement tested against a benchmark and reviewed rather than self-applied blindly?
