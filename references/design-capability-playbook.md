# Design capability playbook

Use this playbook when the task involves a new screen, major redesign, design system, or an explicit request for high visual craft. It converts the user's capability list into observable design work. Do not merely name a color, font, or layout; explain why it fits the task, test it in context, and revise it when evidence or constraints disagree.

## 1. Design intelligence: reason from purpose, not trend

A design decision is good when it helps the intended person understand, decide, act, recover, or feel appropriately confident in context. Evaluate a proposal through five lenses:

1. **Task fit:** Does it make the user's next decision/action clearer or reduce unnecessary effort?
2. **Meaning:** Does visual treatment communicate structure, priority, status, or brand without requiring guesswork?
3. **Access:** Can people with different abilities, inputs, languages, devices, and contexts perceive and operate it?
4. **Coherence:** Does it fit the product's design system, content, tone, and platform conventions?
5. **Cost:** What complexity does it add in learning, performance, maintenance, privacy, error recovery, or accessibility?

For each major decision, distinguish evidence (observed or sourced), inference (reasoned interpretation), and hypothesis (to validate). When evidence is missing, prefer a reversible, low-risk choice and explain what should be tested. Reject a visual trend when it harms clarity, task completion, comfort, performance, or trust. Do not represent subjective taste as user research.

### Quality vs novelty

Novelty is useful when it clarifies a new concept, expresses a legitimate brand, or improves a task. It is harmful when a familiar action becomes hard to find, users must relearn common controls, animation competes with content, or decoration masks missing product value. Keep established interaction conventions unless user evidence supports a change; express originality through a coherent visual concept, content, illustration, and detail rather than reinventing basic controls.

## 2. Creative direction: create a distinct, coherent concept

Before selecting individual styles, define a product-specific creative direction. Derive it from audience, task, brand, context, content, market category, and existing identity. Use a short concept statement and a handful of principles; for each principle, state what it means in actual interface decisions.

A useful direction record includes:

- **Concept statement:** one sentence describing the intended experience, not a mood-board adjective pile.
- **Personality axes:** choose bounded positions such as quiet ↔ expressive, formal ↔ conversational, dense ↔ spacious, heritage ↔ technical. Give a reason for each.
- **Visual principles:** usually three to five, such as “editorial hierarchy,” “warm human tone,” “high-information clarity,” or “precise status cues.”
- **Translation to UI:** type character, palette behavior, density, shape language, imagery, icon treatment, motion, and surface treatment.
- **Do / avoid:** state which visual moves support the concept and which would undermine it.
- **Proof screen:** define one screen or component where the concept should be visible without being overdecorated.

Make the concept distinct from a generic template by anchoring it in real product material: user language, actual content, a credible brand asset, data, service context, or interaction behavior. Do not invent brand history, customer stories, or product claims to create a mood. Check that the concept remains coherent in a plain-text/low-motion state, at narrow sizes, and in relevant light/dark themes.

## 3. Design research: learn from competitors and references critically

Research references to understand expectations and opportunities, not to copy screens. Select a small, purposeful sample: direct competitors, adjacent products solving the same task, trusted category conventions, relevant platform patterns, and a few sources with a contrasting approach. Do not gather many screenshots without a question.

For each reference, record:

- What user and task it appears to serve.
- What is directly observed versus inferred.
- Information hierarchy, navigation, page composition, density, and action placement.
- Visual language: typography, color roles, surfaces, imagery, iconography, and motion.
- Interaction behavior, state feedback, responsive changes, accessibility evidence, and recovery.
- What appears effective, confusing, or risky—and for whom.
- Transferable principle, product-specific element not to copy, and any code/asset license concern.

Compare patterns by function: onboarding, search, pricing, account management, checkout, dashboards, editorial pages, forms, and empty/error states have different needs. Look at actual rendered behavior and content where possible. A screenshot cannot prove accessibility, backend behavior, conversion results, or user satisfaction. Avoid drawing conclusions about user preferences from competitor presence alone.

Translate findings into decisions: “Use a persistent step indicator because participants need to resume a long process,” not “competitors use step indicators.” If there is no direct user research, label inferred expectations as hypotheses. Use [source-patterns.md](source-patterns.md) only as a directory of inspiration; independently verify current offerings, terms, and actual component behavior before adoption.

## 4. Layout intelligence: select composition by task and content

Start with the information and action hierarchy, not a template name. List the content units, their importance, relationships, decision sequence, interaction needs, and likely length. Choose the smallest composition that presents those relationships clearly.

### Common composition families and when to consider them

- **Single-column task flow:** best when users need focus, linear steps, or substantial reading. Risk: long pages need clear headings, progress/context, and navigation anchors where useful.
- **Split view:** useful when users must inspect a list while viewing a selected detail or editor. On narrow screens, define a clear transition between list and detail; do not squeeze both panes until illegible.
- **Dashboard grid:** useful for comparing a few independent status summaries or actions. Establish a clear primary metric/task and meaningful grouping. Avoid an arbitrary grid of cards or decoration-only charts.
- **Table/data workspace:** appropriate for scanning and comparing records with shared fields. Use semantic table relationships for static data; provide responsive strategy, sorting state, and accessible summaries. An interactive grid is a different, more complex widget.
- **Editorial/story layout:** useful for content where sequence, imagery, and reading rhythm matter. Keep heading hierarchy, line length, captions, and action placement predictable.
- **Marketing/landing-page sequence:** use only when the user's job is to evaluate an offer. Order hero/value proposition, evidence, features, objections, pricing/terms, and next action according to the audience's questions. Never invent testimonials, client logos, or metrics.
- **Canvas/map/timeline:** use when spatial or temporal relationships are essential. Provide list, text, or tabular alternatives and non-drag navigation where needed.
- **Bento/uneven modular grid:** use when modules represent distinct priorities or content types that benefit from varied scale. Do not use it as decoration that makes reading order or responsive reflow ambiguous.
- **Wizard/stepper:** use for a genuinely multi-stage task with dependencies or a need to focus. Avoid splitting a simple form; preserve data and let users review/edit where useful.

These are options, not prescriptions. A product may need a hybrid. State why the chosen composition fits this task and what happens at each responsive size.

### Compose deliberately

1. Put the primary user goal and next action in the initial viewport when useful, but do not force all content above the fold.
2. Group items by meaning and task sequence; use spacing, headings, alignment, and dividers intentionally.
3. Establish a grid with a clear content width and consistent alignment; use flexible/intrinsic sizing rather than brittle coordinates.
4. Keep text measures comfortable for reading and data density suited to the task and audience.
5. Use cards only for true grouping or independent modules; use headings/whitespace when boxes add noise.
6. Check visual and semantic reading order together. Ensure the responsive DOM/accessibility order remains logical.
7. Stress-test with long titles, empty states, errors, localization, enlarged text, and realistic data.

## 5. Typography: select, pair, scale, and test type

Typography communicates hierarchy, tone, pace, and credibility while carrying most interface content. Select fonts as a system, not from a trendy-font list.

### Typeface selection procedure

1. **Inspect constraints first:** existing brand/type tokens, platform, localization/language set, content volume, product personality, performance budget, licensing, and fallback needs.
2. **Choose by job:** interface/body faces should remain legible at small sizes and in dense text; display faces can carry more personality at large sizes but must remain readable in navigation, mobile headings, and text wrapping.
3. **Check script and glyph coverage:** verify every required language, accents, punctuation, currency, symbols, numerals, and fallback. Test mixed-script lines and actual localized labels. Do not choose based only on a Latin specimen.
4. **Evaluate functional traits:** x-height, character distinction (I/l/1, O/0), numeral forms, punctuation, weight range, variable axes, hinting/rendering, and readability at real sizes and devices.
5. **Pair only when the roles justify it:** a single well-chosen family with multiple weights is often more coherent and faster. If pairing, assign clear roles (e.g., expressive display + neutral UI/body), compare letterforms and proportions, and limit the system to a small number of families.
6. **Verify license, privacy, and delivery:** use properly licensed fonts. Consider self-hosting vs a third-party service in light of privacy, caching, performance, and product policy. Load only needed subsets and weights; include robust fallbacks.
7. **Test in context:** inspect realistic headings, body copy, forms, tables, error messages, long names, numbers, and localized strings at target sizes and zoom.

### Build a typographic system

Define semantic styles, not arbitrary one-off sizes: display, page title, section title, subheading, body, supporting body, label, button, caption/metadata, and code/data if needed. For each role specify font family, size, weight, line height, letter spacing, text transform, and responsive behavior. Use a restrained scale with clear jumps between roles. Let body text remain comfortable; do not reduce essential information to tiny metadata.

Use line height generous enough for the script and density; keep paragraph width suitable for reading. Use weight and size before all-caps or color to create hierarchy. Ensure labels remain distinguishable in disabled, focus, error, and selected states. Test type at 200% zoom/text enlargement and with long translations; no fixed-height text should clip.

Avoid relying on very light font weights, thin strokes over imagery, tightly tracked small text, long all-caps strings, or italics for extended passages. Do not treat a fashionable type scale formula as a rule; adapt it to content, platform, density, and accessibility.

## 6. Color intelligence: construct role-based accessible palettes

Color should identify hierarchy, action, status, grouping, and brand. It is not simply a list of attractive swatches.

### Palette construction procedure

1. **Start from brand and task:** inspect existing colors and user expectations. Determine whether the product needs calm, trust, energy, warmth, precision, or another quality, and why. Do not infer universal psychological meaning from a hue; cultural context and neighboring colors change interpretation.
2. **Define semantic roles first:** canvas, surface, elevated surface, primary/secondary text, muted text, border, primary action, secondary action, focus, selected, link, success, warning, error, and info. Add chart categories only when real data needs them.
3. **Build tonal ranges:** create useful light/dark steps for each important hue, plus neutral ramps. Choose hue, chroma/saturation, and lightness deliberately. Color-space tools such as OKLCH can help keep perceived lightness more consistent, but do not assume a generated scale is accessible or visually correct.
4. **Assign foreground/background pairs:** define which text, icon, border, and focus color belongs on each surface. Do not create tokens that permit invalid pairings without warning. Check overlays, opacity, gradients, images, and disabled states as rendered.
5. **Separate brand from status:** functional success/warning/error should be distinguishable and should not depend on the brand hue alone. Add text/icon/shape cues and suitable programmatic status.
6. **Design themes as systems:** specify semantic mapping for light and dark themes; do not merely invert colors. Recheck contrast, elevation, focus, borders, image treatment, chart colors, and selected states independently.
7. **Validate with actual content and tools:** test text and meaningful non-text contrast against applicable criteria. Check common color-vision deficiencies and grayscale where color distinctions matter. Contrast tools complement, not replace, human judgment.

Do not state that a palette is “accessible” because it looks balanced. Record exact foreground/background pairs and criterion checked. Preserve focus visibility in every theme. Never encode errors or data categories only in color. Avoid overusing saturated accents: reserve them for actions or information that merit attention.

## 7. Component architecture: make reuse reliable

A component is reusable when its purpose, behavior, API, styling, and accessibility contract are stable enough to benefit more than one use. Do not abstract merely to reduce line count.

### Architecture procedure

1. Inventory existing components, tokens, primitives, and variants before creating new ones.
2. Define component purpose, semantic element, content model, states, and responsive behavior.
3. Keep structure semantic and content-first. Prefer native HTML/platform controls or tested accessible primitives.
4. Separate stable behavior from customizable appearance. Expose a small, typed set of meaningful variants and slots; avoid dozens of boolean flags that combine into undocumented states.
5. Specify states and transitions: default, hover, focus-visible, pressed, selected, expanded, disabled, loading, success, error, empty, and responsive variants as applicable.
6. Define keyboard and assistive-technology behavior; test names, roles, values, focus, announcements, and fallback behavior.
7. Document when to use, when not to use, anatomy, content guidance, variants, dependencies, examples, and known limitations.
8. Test at realistic content extremes, themes, localization, and responsive widths. Keep design tokens and implementation behavior synchronized.

Use stable design tokens, variant naming, and semantic roles. Avoid a component that is visually reusable but behaviorally inconsistent. Avoid global overrides that cause unrelated variants to change. Keep dependencies current, licensed, and justifiable. If adopting copy-paste/catalog code, verify source, license, dependency, accessibility, and update path; never assume marketplace presence grants broad reuse rights.

## 8. UX psychology: lower cognitive cost ethically

Use cognitive psychology as a prompt to reduce unnecessary effort—not as permission to manipulate. People have limited attention and working memory, can be interrupted, may not recognize internal terminology, and often rely on visible cues rather than recalling instructions. Design to support these realities.

- **Recognition over recall:** show relevant choices, examples, constraints, status, and context where needed; avoid forcing users to memorize codes or rules.
- **Chunking and hierarchy:** group related information, use descriptive headings, and break complex tasks into meaningful steps. Do not split trivial tasks into needless screens.
- **Progressive disclosure:** reveal secondary detail when useful, while keeping fees, risks, eligibility, privacy, and consequential choices visible before commitment.
- **Choice architecture:** reduce redundant options, use meaningful defaults, explain default consequences, and let people change them. Do not use preselection to smuggle costs or consent.
- **Recognition of action effects:** label buttons with outcomes, show state, and give feedback at the right time. Keep the interface's status consistent with actual backend state.
- **Error prevention and recovery:** constrain inputs only when the allowed format is known; help correct mistakes; preserve work; offer undo when safe.
- **Cognitive load:** remove irrelevant repetition, simplify language, and place help in context. Do not oversimplify complex risk or remove information needed for informed choice.
- **Trust and agency:** explain data requests, permissions, price, and consequences. Offer cancel, back, or exit paths; avoid artificial urgency, shame, confirmshaming, hidden opt-outs, and deceptive friction.

Do not make universal claims such as “red always means danger” or “three choices is optimal.” Test language, ordering, defaults, and cues with the intended users and context. For consequential or sensitive tasks, involve the appropriate domain/legal/safety specialists.

## 9. Interaction design: fully specify meaningful states

Use an interaction state inventory for each functional element. Consider default, hover, focus-visible, pressed, selected, expanded/collapsed, disabled, loading, success, error, and empty states where relevant. Not every component needs every state; each omission should be intentional.

For each state, define visual treatment, accessible name/role/value, keyboard behavior, pointer/touch behavior, announcement, timing, and recovery. Hover is supplemental only. Focus must be visible, not confused with selection, and not obscured. Disabled controls should explain prerequisites when that helps. Loading should prevent duplicate submission when necessary and preserve clear status. Success should reflect true completion, not merely a click. Errors should be specific, non-blaming, and actionable.

Design state transitions, not only state screenshots. Specify what triggers the change, how quickly it appears, whether it persists, whether focus moves, whether data is saved, and what happens on retry or network failure. Use inline validation and persistent status appropriately; do not rely on ephemeral toasts for critical information. See `interaction-patterns.md` for pattern-level examples and accessibility requirements.

## 10. Motion design: purposeful transitions and micro-interactions

Begin with the reason to move: orientation, continuity, cause/effect, hierarchy, progress, confirmation, or delight. If the motion does not help users understand, act, or feel a legitimate brand quality, remove it.

For each motion, record trigger, start/end state, purpose, duration range, easing, distance/scale, interruption behavior, reduced-motion alternative, performance cost, and whether it repeats. Use shorter, subtle movement for direct feedback; reserve larger or slower transitions for spatial/scene changes only when users benefit. Keep content stable enough to read and controls responsive. Avoid decorative scroll-jacking, parallax that impairs reading, auto-playing loops, large bounce, excessive blur, and motion that moves a control away while a user targets it.

Scroll effects should never be required to reveal essential content or navigate. Preserve native scrolling and keyboard access. Ensure sticky effects do not obscure focus or headings. Pause or reduce nonessential offscreen animation. Honor reduced-motion preferences; replace spatial movement with a fade or immediate state change when appropriate. Check flashing and timing against exact applicable WCAG criteria. Test on lower-powered devices and with actual content, not only a smooth desktop preview.

## 11. Responsive design: compose separately for each class of context

Responsive design is not one desktop canvas squeezed down. Plan the information, navigation, actions, density, and input for narrow/mobile, intermediate/tablet, and wide/desktop contexts independently, then define how the experience transforms between them. Device categories are starting points; choose content-driven breakpoints where the current composition stops working.

For every target context, specify:

- **Content priority:** what stays first, what moves, what can collapse, and what must remain available.
- **Navigation:** visible destinations, menu behavior, current-page cue, keyboard/focus, and back path.
- **Layout:** columns, reading order, max width, grid behavior, sticky/fixed elements, and overflow policy.
- **Input:** touch target/spacing and gestures; pointer hover only as enhancement; keyboard focus and alternatives to dragging.
- **Density:** table/chart/data behavior, truncation policy, detail views, and readable text sizes.
- **Motion:** interactions that are reduced, removed, or simplified for context/preferences.
- **Content stress:** long labels, translation, user-generated content, errors, and text enlargement.

On mobile, do not merely stack every desktop card. Reconsider task sequence, visibility, navigation and controls. On tablet, do not assume either phone or desktop composition; use its actual available space and interaction mode. On desktop, use width intentionally without stretching reading text across the screen; support keyboard and zoom. Test portrait/landscape where relevant, browser zoom, and reflow. Avoid hidden hover actions, clipped focus rings, fixed overlays covering content, and horizontal page overflow.

## 12. Quality assurance: inspect the rendered interface and repair it

Quality assurance is a design capability, not the last checkbox. A design spec or screenshot is not proof of implementation quality.

### Visual/functional inspection sequence

1. Run the app and inspect the actual rendered routes at target sizes. If a browser is unavailable, state that and perform only static/code review.
2. Use realistic content and compare against the task, brief, component system, and existing product—not just a high-fidelity mockup.
3. Follow the primary task from entry to confirmed outcome. Test navigation, form validation, empty/loading/error/success states, back/undo, and interruption/recovery.
4. Inspect keyboard and focus, touch/pointer behavior, zoom/text resize, reduced motion, accessible names, and contrast as available.
5. Check mobile, tablet, and desktop as distinct compositions; test intermediate widths and long content for breakage.
6. Review console/network/build/test outputs and performance. Check image/font loading, layout shift, and unnecessary motion/dependencies.
7. Write the three highest-impact defects, fix by user impact, then re-open the interface and verify the fixes without creating regressions.
8. Record tested environment and remaining gaps. Do not claim conformance or usability validation from informal inspection.

### Visual critique protocol

Ask: Does the first view explain what the product is and what the user can do? Is there one clear hierarchy? Do spacing and alignment signal real relationships? Are typography and color choices legible in every state? Is each visual effect doing a job? Does the result feel specific to this product rather than copied from a starter? Does the interface hold up with actual text, empty states, localization, and constrained screens? Can a user who does not share the designer's assumptions complete the task?

## Required decision record for major interface work

For substantial designs, record these decisions concisely in the brief or implementation notes:

| Capability | Decision to record | Evidence/check |
|---|---|---|
| Design intelligence | User outcome, constraints, assumptions, tradeoffs | Existing research, task analysis, or labeled hypothesis |
| Creative direction | Concept, principles, do/avoid rules | Coherence across representative screens and states |
| Design research | References and transferable insight | Direct inspection; no claims inferred from screenshots alone |
| Layout | Composition chosen and why; reflow behavior | Task hierarchy and responsive renderings |
| Typography | Families, roles, scale, fallback, language coverage | Real copy, zoom, contrast, license, rendering |
| Color | Semantic roles, themes, pairings, status cues | Measured contrast and non-color cues |
| Components | Reused/new components, API, variants, states | Consistency, accessibility and maintainability review |
| UX psychology | Friction reduced without removing informed choice | Recovery, privacy, fees, consent, user comprehension |
| Interaction | State transitions, input methods, feedback, recovery | Full flow with keyboard, touch, pointer and assistive tech where possible |
| Motion | Purpose, trigger, timing, reduced alternative | Reduced-motion and performance checks |
| Responsive | Mobile/tablet/desktop composition | Target viewport and intermediate-width inspection |
| QA | What was inspected, failures fixed, limitations | Browser/test evidence with environment recorded |


# Multidisciplinary expert lenses

Use these as review responsibilities, not fictional biographies. One assistant can apply the lenses in sequence; separate agents are optional and should be used only when helpful and authorized. Keep one shared design brief so the perspectives converge on the same user outcome rather than producing disconnected opinions. Do not claim human credentials or present simulated critique as user evidence.

## World-class product designer

**Accountability:** Connect user outcomes, product strategy, content, interaction, and feasibility into a complete experience. Own the problem framing and the coherence of the whole journey rather than polishing isolated screens.

**Ask:** What is the user trying to accomplish? Why does this product need this flow? Does every screen earn its place? What is the primary action and what must be understood before it? Are business goals aligned with user benefit and trust? What happens before and after this interface?

**Deliver:** A clear problem/outcome statement, journey and screen hierarchy, prioritized scope, decision rationale, and an experience that is coherent from entry through recovery and completion.

## Senior UX researcher

**Accountability:** Protect the distinction between evidence and assumption. Match research method to the decision, include relevant participants and access needs, and translate observations into testable design implications.

**Ask:** What do we actually know? Who was included or missing? Is this behavior observed or inferred? Are our questions leading? Could a measurement reward a harmful or exclusionary outcome? What is the lightest credible way to reduce uncertainty?

**Deliver:** A concise evidence/assumption register, research plan when needed, participant/context limitations, observed task breakdowns, and hypotheses to validate. Never invent findings, sample sizes, quotes, or statistical confidence.

## Creative director

**Accountability:** Establish a product-specific visual concept and ensure every expressive choice contributes to identity, comprehension, or emotional tone. Protect distinctiveness without sacrificing access or task clarity.

**Ask:** Could this look belong to any generic template? What is specific to this product and its users? Are typography, color, imagery, shape, density, and motion expressing one coherent idea? Is the visual drama competing with the task?

**Deliver:** A concise concept, a few visual principles, a do/avoid direction, and representative examples that translate the concept into real interface choices. Do not use unsupported claims or imitate another brand's distinctive expression.

## Design systems architect

**Accountability:** Make interface decisions consistent, reusable, adaptable, and maintainable without turning every local need into a global abstraction.

**Ask:** What tokens/components already exist? Is this behavior repeated enough to justify a component? Are variants and states explicit? Are semantic roles stable across themes? Can content, localization, and platform variation fit the API? Will this create conflicting sources of truth?

**Deliver:** Reuse/extend/create decisions, semantic token mapping, component contracts, variant/state definitions, usage guidance, and governance/update implications. Prefer compatible existing primitives; identify accessibility and licensing risks in dependencies.

## Frontend engineering specialist

**Accountability:** Turn intent into reliable rendered behavior in the actual stack. Preserve semantic structure, component boundaries, performance, and testability; report when a design cannot be implemented as specified.

**Ask:** Does the DOM/native structure match the visual and reading order? Does behavior survive network delay, errors, long content, route changes, and real devices? Are dependencies and assets justified? Are keyboard and assistive-technology semantics implemented, not merely drawn into the mockup?

**Deliver:** A maintainable implementation, working states, appropriate responsive behavior, build/test evidence, and honest technical constraints. Inspect the rendered product rather than assuming that code or a screenshot proves the result.

## Interaction and motion designer

**Accountability:** Make actions, state transitions, system response, and feedback understandable across pointer, touch, keyboard, and assistive technology. Use animation only where it explains or improves the experience.

**Ask:** What triggered this transition? What should the user learn from it? Does motion preserve control and reading? Is focus preserved? What is the reduced-motion behavior? Can the same meaning be conveyed without movement?

**Deliver:** Interaction contracts, state/transition map, feedback timing, keyboard/focus behavior, purposeful motion specification, interruption/reduced-motion alternatives, and performance considerations.

## Usability and accessibility auditor

**Accountability:** Find practical barriers and distinguish normative requirements from recommendations. Evaluate complete tasks, not just static visual compliance. Include human and assistive-technology perspectives.

**Ask:** Can the task be completed without a pointer? Is focus visible and unobscured? Are names, roles, states, and relationships exposed? Are errors recoverable? Does status reach assistive technology? Are contrast, reflow, target size, timing, and motion reviewed against the exact applicable criteria? What did automation miss?

**Deliver:** Findings with evidence, environment, affected task/users, impact/severity, exact criterion or guidance source where applicable, remediation, and retest status. Do not claim conformance from a spot-check, automated score, APG example, or design-system component.

## Ruthless design critic

**Accountability:** Stress-test the finished experience for avoidable confusion, generic choices, missing states, inconsistent logic, visual noise, and false confidence. Be direct about the artifact and kind toward participants and colleagues.

**Ask:** What is the weakest part? Which element looks clickable but is not? What would fail first on a small screen, with a keyboard, under an error, or with translated text? Which visual choice has no reason? Is the primary action obvious without narration? What assumption is disguised as fact? What is being hidden, and could it harm trust? Is this truly better than the existing product?

**Deliver:** The three highest-impact defects, each with evidence or a clearly labeled hypothesis, a proposed fix, and the smallest retest that can verify it. Do not equate harsh wording with rigor; critique should make the work more useful.

## Review sequence and resolution of disagreement

1. The **product designer** frames user outcome and scope with the **researcher** marking evidence and uncertainty.
2. The **creative director** proposes a distinctive direction and the **systems architect** checks consistency and reuse.
3. The **interaction/motion designer** defines behavior while the **frontend specialist** checks native-stack feasibility and implementation consequences.
4. The **accessibility/usability auditor** reviews the complete flow and applicable standards, not only the visual layer.
5. The **ruthless critic** challenges the integrated result, then the product designer decides what to change against user value, evidence, risk, and constraints.
6. Re-test the changed experience and record remaining disagreements or gaps.

When lenses disagree, do not resolve the conflict by majority vote or personal taste. First separate normative requirement, user evidence, product constraint, heuristic, and aesthetic preference. Normative requirements and safety/legal constraints are not overridden by style. Strong user evidence should outweigh an unsupported assumption. Where evidence is absent and multiple choices remain valid, select a reversible choice that best balances task clarity, inclusion, coherence, performance, and maintainability; label the uncertainty and test it later.


# Additional capabilities: product thinking, visual storytelling, and restraint

## Product thinking: understand the business and service before screens

Treat a product as a promise delivered through capabilities, policies, content, operations, and interfaces. A design must reflect what the product truly does and what the user needs to accomplish—not just its category or marketing language.

Before designing, create a one-page product model:

- **Audience and jobs:** Who uses it, what they need to get done, and how often or under what conditions?
- **Core value:** What user outcome does the product provide? What verified capability enables that outcome?
- **Business/service model:** What does the organization need to achieve, and where could it conflict with the user's interest?
- **Trust/risk:** What money, identity, safety, privacy, reputation, eligibility, or time is at stake?
- **Operating reality:** What data, staff, policy, inventory, support, latency, and technical constraints shape the service?
- **Lifecycle:** How do people discover, start, complete, resume, get help, cancel, renew, or leave?
- **Success and harm:** What user outcome indicates success? What harmful incentive or failure should be monitored?

Translate this model into design choices. A hotel booking product should help people compare location, dates, room/offer terms, total price, and cancellation conditions before purchase; beautiful imagery cannot compensate for unclear terms. A financial dashboard should preserve units, time range, data freshness, risk context, and distinctions between balance, performance, forecast, and recommendation; celebratory green must not falsely imply gain. A news publication should support reading, source/context, byline/date, correction transparency, and clear distinction between reporting, opinion, sponsored content, and advertising. A SaaS tool should orient users to workspace/project, permissions, saved/shared state, and task-based navigation rather than reflecting internal org charts. These are diagnostic examples, not exhaustive blueprints.

Do not extrapolate product truths from a logo, brief fragment, or competitor. Inspect the product, ask focused questions, and label assumptions. When the business goal and user interest conflict, do not conceal the conflict with visual persuasion. Make consequential terms legible and escalate unresolved policy, safety, privacy, or legal questions to the responsible owner.

## Visual storytelling: shape a truthful sequence of attention

Visual storytelling gives content an intentional beginning, development, evidence, and resolution. It can happen on one screen, a landing page, a dashboard, or a long editorial story. Use composition and rhythm to help people understand; do not turn user attention into a captive audience.

Plan this sequence:

1. **Orient:** What is this product/page and why is it relevant now?
2. **Establish context:** What should the person know before interpreting the content?
3. **Guide attention:** Which content block or action comes next, and what visual cue establishes that relationship?
4. **Support meaning:** What real image, data, example, source, or demonstration provides evidence?
5. **Resolve:** What should the user conclude, decide, or do? What alternative or caveat matters?

Use whitespace to separate ideas and set pacing. Use contrast to establish priority, not to shout at every step. Use imagery for authentic context, documentation, illustration, or emotional tone; choose crop and responsive art direction so the subject's meaning survives. Use depth to distinguish layers only when those layers matter. Use rhythm to alternate dense and quiet sections without interrupting the user's task. In editorial work, protect reading flow and source context. In a product task, keep current state and next action visible.

For every image and data display, ask whether it is verified, representative, licensed, and accurately framed. Captions should clarify context; chart axes and units should prevent misinterpretation. Do not use generic stock photographs, fabricated dashboards, synthetic customer quotes, or dramatic crops to imply evidence that does not exist. Provide accessible text alternatives and a non-visual route to essential information.

## Design restraint: justify every expressive layer

Restraint is not the absence of personality. It is control over emphasis and complexity. Begin with content, hierarchy, and function. Add one expressive layer at a time and evaluate its benefit and cost.

For every gradient, card, border, shadow, blur, glass panel, animation, scroll effect, 3D object, icon, badge, or decorative line, record a concise reason:

- Does it communicate information, grouping, action, state, brand, or legitimate atmosphere?
- Does it improve comprehension or task completion for the intended user?
- Does it create contrast, motion, battery, bandwidth, performance, maintainability, comfort, or accessibility risk?
- Does it make important information harder to read or action harder to find?
- Is there a simpler treatment with equal or better benefit?

Use a **subtraction pass** after the first visual design: remove non-functional effects in turn, compare the result, and retain only those whose contribution is clear. This guards against layered decoration that looks polished in a screenshot but competes during use. Do not remove useful brand, editorial expression, or delight merely to achieve bland minimalism. Preserve an element when it carries verified identity or supports the user's task; document the rationale and test it.

## Product-specific design review

Ask the multidisciplinary reviewers to answer three questions together:

1. **Product designer/researcher:** Is this the right experience for the actual product, user task, and evidence?
2. **Creative director/storyteller:** Is the visual concept specific, coherent, truthful, and memorable for the right reason?
3. **Ruthless critic:** What is generic, unsupported, inaccessible, excessive, or confusing—and what can be removed?

Then use engineering, systems, interaction, and accessibility reviews to verify the design can be implemented and operated as intended. Record disagreements as evidence questions or tradeoffs rather than resolving them by taste.
