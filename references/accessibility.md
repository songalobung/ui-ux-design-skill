# Accessibility knowledge index

This file is the quick entry point for accessibility decisions. The detailed implementation guide is [`accessibility-inclusive-design.md`](accessibility-inclusive-design.md); source authority and current links are in [`standards-and-sources.md`](standards-and-sources.md); platform-specific considerations are in [`platform-guidelines.md`](platform-guidelines.md); test procedure is in [`visual-qa.md`](visual-qa.md).

## Non-negotiable working habits

- Design for perception, operation, understanding, and robust programmatic access.
- Prefer native semantics and controls. Use ARIA only when needed, and implement the behavior as well as the semantics.
- Every complete task must be possible without a pointer. Keep focus visible, predictable, and unobscured.
- Give controls clear accessible names and communicate relationships, state, errors, and important updates.
- Do not rely on color, position, sound, shape, or motion alone to convey essential meaning.
- Support text resizing/reflow, responsive content, captions/alternatives for media, and reduced motion as applicable.
- Include disabled people and assistive-technology users in research and testing when relevant.
- Treat automated tools, component libraries, design reviews, and one test session as partial evidence—not proof of universal usability.

## Standards vs guidance

For web conformance claims, use the normative [WCAG 2.2 specification](https://www.w3.org/TR/WCAG22/) and its exact success criteria and conformance conditions. The [WAI ARIA APG](https://www.w3.org/WAI/ARIA/apg/) is informative interaction-pattern guidance. Apple HIG, Material guidance, inclusive-design methodologies, and usability heuristics provide context-specific or recommended practices; do not label them as WCAG requirements.

Name the applicable version, level, scope, and evidence in any compliance report. If requirements are jurisdiction-specific, verify applicability with the appropriate specialist.

## Detailed route

Read `accessibility-inclusive-design.md` for semantic HTML, labels, keyboard/focus, forms, contrast, text, media, motion, touch, and layered evaluation. Read `quality-assurance.md` and `visual-qa.md` to plan manual and rendered checks. Never state “accessible” or “WCAG compliant” as a blanket guarantee without evidence and scope.
