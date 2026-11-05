# UX, accessibility, and implementation quality assurance

Quality assurance is an evidence-gathering activity, not a ritual checkbox. Choose tests that match the risk and intended outcome. A successful build does not prove a usable design; a successful usability session does not prove normative accessibility conformance.

## Match evaluation to the risk

- **Small visual/component adjustment:** inspect neighboring patterns and all affected states; run unit, lint, or snapshot checks available; verify keyboard focus and narrow layout.
- **New screen or moderate flow change:** perform a task walkthrough, responsive review, content/error-state review, and manual accessibility checks; test with representative users when feasible.
- **High-consequence or novel flow:** research the need, prototype alternatives, include disabled users and assistive technologies, conduct moderated or unmoderated task tests as appropriate, obtain specialist review for legal/security/safety implications, and define post-launch monitoring.

Automated tests efficiently catch regressions, but their scope is limited. Heuristic reviews identify potential problems but reflect evaluator judgment. User tests reveal observed usability in specific contexts, not population-wide rates by themselves. Conformance evaluation requires a systematic review of all applicable criteria and conformance conditions.

## Test the task, not only the screen

Write scenarios around outcomes: “Find out whether you can renew and submit the renewal” rather than “Click the Renew button, then fill out field 1.” Include prerequisites, realistic but safe data, interruptions, and a success condition. Observe whether people know where they are, what information is needed, what action is possible, and whether the final state means what they think it means.

For each flow, cover:

- First-time and returning user paths.
- Valid completion and likely invalid input.
- Empty, loading, success, partial success, timeout, and failure states where relevant.
- Cancel/back, interruption, refresh, retry, and resume behavior.
- Long text, localization, and content boundary cases.
- Keyboard-only and alternate input paths.
- Permissions, privacy, and consequential confirmation.

Do not test only the ideal path with a designer narrating the interface. Keep evidence separate from interpretation. Note where facilitation or prototype limitations affected the result.

## Manual interaction checks

1. **Keyboard:** complete every task using keyboard only. Check logical tab order, visible focus, no trap, expected widget keys, Escape/back behavior, and focus after dialog open/close, validation, deletion, route changes, and dynamic updates.
2. **Pointer/touch:** verify target size and spacing, no hover-only functions, drag alternatives where applicable, and behavior with imprecise input. Check touch while scrolling and at narrow widths.
3. **Zoom and reflow:** increase browser zoom and text size; inspect at narrow viewports and with long labels. Look for clipped, overlapping, fixed-height, obscured, or horizontally overflowing content.
4. **Visual access:** check text and non-text contrast in all relevant states, visible focus, chart distinctions, error/status cues, and dark/light themes. Do not infer contrast from brand palette alone.
5. **Assistive technology:** test relevant screen readers, magnification, voice input, switch access, captions, or platform accessibility tools. Verify reading order, names, roles, values, state announcements, and change announcements. Testing one combination does not prove universal support.
6. **Motion and time:** honor reduced-motion settings; inspect auto-advancing, timeouts, animated content, flashing, and progress. Check whether users can pause, extend, or recover as needed under applicable requirements.
7. **Content:** read labels, instructions, validation, warnings, success messages, and help aloud. Check clarity, tone, consistency, translation, date/number formats, and whether users can act on the information.
8. **Responsive and performance:** test real breakpoints and content, not only device presets. Inspect layout shift, loading behavior, input latency, and effects on low-powered or low-bandwidth devices where relevant.

## Evaluate usability sessions

Use a small number of realistic tasks that represent critical goals. Recruit relevant participants with variation in experience and access needs. Explain consent and recording; make sessions accessible. Ask neutral questions, let people attempt tasks, and avoid teaching the prototype. Record observable breakdowns, severity, context, and participant interpretation.

Classify issues by impact, not only frequency:

- **Blocker:** prevents task completion or creates likely serious harm/data loss.
- **Major:** causes a likely wrong outcome, repeated failure, or substantial exclusion/effort.
- **Moderate:** causes confusion or detour but has a discoverable recovery.
- **Minor:** small inconsistency or polish issue with little task impact.

Use labels as a shared triage aid, not a universal standard. A low-frequency barrier can still be severe for the people affected. Record confidence and affected context; don't claim prevalence from a small qualitative sample.

## Review design and implementation together

Compare implementation to the design intent, but do not assume the mockup is correct if implementation or user evidence exposes a better solution. Check:

- Content hierarchy and primary action.
- Component consistency and interaction states.
- Semantic structure, names, focus, keyboard, and status updates.
- Responsive behavior and real content.
- Contrast, enlarged text, motion, and reduced-motion behavior.
- Errors, persistence, data loss, network delay, and recovery.
- Performance, asset size, and unnecessary dependencies.
- Browser console, network errors, build/test results, and route regressions.

Inspect the rendered result at least once when a rendering environment is available. Fix functional and visual regressions, then repeat the critical flow. If no browser or assistive technology is available, say what was reviewed statically and what remains untested.

## Iterate with a decision log

For each issue, record: evidence; user/task/context affected; severity; confidence; recommended change; alternatives/tradeoff; owner or next step; retest result. Fix blocking and high-impact issues before visual polish. After changes, retest the affected flow and check for side effects. Avoid polishing one screen while a journey remains broken elsewhere.

Use a short critique loop:

1. Identify the three highest-impact uncertainties or failures.
2. Verify each against user evidence, applicable requirements, and implementation.
3. Make the smallest change that addresses the underlying cause.
4. Re-run the relevant task and access checks.
5. Record what improved and what remains uncertain.

## Conformance and reporting discipline

A practical QA checklist is not a WCAG audit. If the user asks for accessibility compliance, first establish the required jurisdiction, standard/version, level, product scope, technologies, and evaluation method. Review every applicable normative criterion and conformance condition; use automated tools only as support. Report scope, environment, exceptions, findings, remediation status, and limitations. Never describe a score or spot-check as conformance.

Final reports must distinguish:

- Implemented and verified.
- Implemented but not tested in the target environment.
- Known limitation or remaining barrier.
- Recommendation needing user research or specialist review.

Do not invent test results, user evidence, performance improvements, or compliance status.
