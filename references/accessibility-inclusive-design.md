# Accessibility and inclusive design

Accessibility is part of product quality and access. Design and implement for people with varied sensory, physical, cognitive, language, and situational needs. Do not equate accessibility with “works with a screen reader,” an automated scan, or passing selected WCAG checks. A technically conforming page may still be difficult to use; an attractive page may still block access.

## Be precise about requirements

For web content, use the applicable version and conformance target of [WCAG](https://www.w3.org/TR/WCAG22/). WCAG 2.2 organizes criteria under perceivable, operable, understandable, and robust principles. Identify the exact success criterion, level, scope, definitions, and exceptions before making a normative claim. Level AA conformance includes all applicable Level A and AA criteria; the conformance rules apply to complete pages and impose additional conditions. Checking a handful of criteria is not a conformance claim.

Examples to understand—not a complete checklist:

- **Keyboard (2.1.1, A):** functionality is operable through a keyboard interface without requiring specific timings for individual keystrokes, except where the underlying function depends on the user's movement path rather than endpoints.
- **No keyboard trap (2.1.2, A):** if keyboard focus can move to a component, it can move away using the keyboard; if a non-standard method is needed, users are advised how to do so.
- **Dragging movements (2.5.7, AA):** functionality using dragging must also be achievable by a single pointer without dragging unless an exception applies.
- **Target size minimum (2.5.8, AA):** pointer targets generally meet 24 by 24 CSS pixels or satisfy the criterion's defined spacing or other exceptions. This is a minimum criterion, not a universal ideal touch size.
- **Language of page (3.1.1, A):** the default human language is programmatically determinable.

These paraphrases are orientation only. Use the normative specification itself for exact wording and applicability. Applicable law, procurement terms, platform policies, and organizational requirements may add obligations; confirm jurisdiction and scope with qualified specialists.

## Design for diverse abilities and contexts

Ask what mismatches exclude people: visual contrast, small targets, poor captions, complex language, memory load, time pressure, fine motor demands, sound-only cues, unpredictable motion, limited bandwidth, shared devices, or a form that assumes one identity or document type. A permanent impairment and a temporary or situational constraint can create similar design barriers; accommodate the underlying need without assuming that all users experience it the same way.

Include disabled people in research and evaluate with the assistive technologies and input methods relevant to the product. Do not ask one participant to represent all disabled users. Offer alternatives when a method creates a barrier: captions and transcripts for audio, keyboard alternatives to dragging, adjustable text, clear labels, and error recovery. Avoid medicalizing users or requiring unnecessary disclosure.

## Semantics, names, and structure

Prefer native semantic HTML and platform controls. Native controls usually provide keyboard behavior, accessibility API mapping, focus, and expected interaction with less custom code. Use ARIA only when native semantics cannot express the needed role/state; apply its semantics correctly and implement the corresponding behavior. W3C APG states that it is informative, not normative, and examples are not production-ready components; its patterns are useful implementation guidance, not a substitute for WCAG evaluation.

Give every control a concise accessible name that describes its purpose in context. Prefer visible labels; associate form labels programmatically. Use descriptions for instructions, constraints, or supplemental detail—not to replace a name. Make headings, lists, tables, landmarks, and relationships meaningful. Do not add ARIA roles that conflict with native semantics or redundant landmarks that make navigation noisier.

Icons that act as controls need an accessible name. Decorative icons should not create duplicate announcements. Use status and error semantics appropriate to the technology; test that important changes are announced without stealing focus or overwhelming users.

## Keyboard, focus, and widget behavior

Every interactive path must work without a pointer. Tab order should follow reading and visual order. Keep a clearly visible focus indicator and ensure it is not obscured by sticky bars, dialogs, or overlays. Do not remove outline without an equally visible replacement. Focus and selection are different states; display them distinctly when both exist.

Use Tab/Shift+Tab to move among page-level controls. Some composite widgets use arrow keys within the widget while Tab moves into or out of it; follow the appropriate [ARIA APG pattern](https://www.w3.org/WAI/ARIA/apg/patterns/) and platform conventions. Do not apply one widget's keyboard model to another. On opening a modal dialog, move focus according to its purpose and contain it only when it is truly modal; on close, return focus to the trigger or a sensible next element. If an item is removed, place focus at a logical remaining item or status.

Test tab order, shortcuts, Escape behavior, selection, type-ahead where relevant, focus restoration, and whether keyboard users can escape every component. Include switch and voice-input considerations where applicable; do not rely on hover-only actions.

## Forms, errors, and high-consequence actions

- Associate visible labels, instructions, required indicators, and constraints with their fields.
- Do not communicate errors only through color, an icon, or a transient toast. Identify the field and problem in text and give a specific correction when possible.
- Preserve valid input after an error. Put help near the point of need and avoid forcing users to re-enter data.
- Validate on blur/submit in ways that do not interrupt typing or announce every keystroke. Summarize errors when a form submit fails and provide links/focus management to the affected fields where appropriate.
- Use suitable input types, autocomplete tokens, input modes, and examples to reduce memory and typing burden. Do not disable paste or password managers without compelling, verified need.
- Explain why sensitive data is needed and what happens next. Minimize collection.
- For irreversible or costly actions, explain the consequence before commitment and provide confirmation, undo, or recovery appropriate to the risk. Avoid confirmation for harmless routine actions that adds friction without protection.

## Text, color, contrast, and resizing

Use real text rather than text embedded in images when possible. Allow text to resize/reflow without loss of information or functionality. Avoid fixed-height text containers that clip translated or enlarged text. Use clear hierarchy, plain language, short paragraphs, descriptive headings, and explicit action labels. Translate jargon and provide help for genuinely necessary specialist terms.

Never rely on color alone. Pair color with text, icon shape, pattern, position, or another redundant cue. Check foreground/background contrast for text and meaningful interface components using the applicable criterion and state. Do not assume a color pair is safe based on hue alone; verify actual tokens in all themes, hover/focus/disabled states, and over images.

## Images, audio, video, and motion

Write text alternatives based on image purpose: informative images need a concise equivalent; functional images need the control's purpose; decorative images should be ignored by assistive technology. Avoid alt text that repeats nearby text or describes irrelevant visual detail. For complex charts, provide a nearby summary or data table.

Provide captions for prerecorded and live speech where applicable; provide transcripts and audio description when required by the content and applicable criteria. Pair audio-only alerts with a visual equivalent and do not autoplay sound unexpectedly.

Honor operating-system reduced-motion preferences. Avoid flashing content, parallax, looping background animation, and motion that obscures reading or causes discomfort. Use transitions to clarify a state change, not as a barrier. For automatically moving or timed content, review the exact applicable WCAG criteria for pause/stop/control and timing. Do not treat “prefers-reduced-motion” alone as proof that every motion issue is solved.

## Touch and responsive access

Controls should be large and well-spaced enough for real fingers and alternative pointing devices. WCAG 2.2 target size minimum is 24 by 24 CSS pixels subject to explicit exceptions; a product may choose larger targets for comfort. Make targets distinct, avoid tight clusters, and do not require dragging when a simpler pointer alternative is possible. Ensure orientation, zoom, viewport changes, text resizing, and reflow do not hide content or functionality, checking the exact applicable criteria.

## Practical accessibility evaluation

Use multiple layers:

1. **Automated checks** to find some detectable issues (missing labels, invalid markup, some contrast problems). Automated passes cannot determine whether an experience is understandable or usable.
2. **Manual code/design review** of semantics, names, contrast, focus, reflow, errors, status changes, and keyboard behavior.
3. **Keyboard-only task completion** through the full flow.
4. **Assistive-technology checks** with relevant screen readers, magnification, voice control, switch input, captions, and platform accessibility tools where available.
5. **Human testing** with disabled people and participants with varied contexts, followed by iteration.
6. **Normative conformance review** against every applicable success criterion at the chosen level, with scope and exceptions recorded.

Record environment, browser, assistive technology, version, task, findings, severity, and evidence. Do not claim WCAG conformance from an automated score, a design-system component, a sample audit, or one user test. Include open barriers and limitations in the handoff.

## Core references

- [WCAG 2.2](https://www.w3.org/TR/WCAG22/) — normative web content success criteria and conformance provisions.
- [WAI Understanding WCAG](https://www.w3.org/WAI/WCAG22/Understanding/intro) — informative explanation of principles, testability, and human review.
- [ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/) — informative widget patterns and keyboard practices; not a normative standard.
- [GOV.UK accessibility introduction](https://www.gov.uk/service-manual/helping-people-to-use-your-service/making-your-service-accessible-an-introduction) — UK government-specific requirements and process guidance; verify applicability.
- [Microsoft Inclusive Design](https://inclusive.microsoft.design/) — design methodology and tools, not a conformance standard.
