# Interaction patterns and behavior

Choose a pattern based on the user's task, risk, frequency, device, and context. A familiar pattern is useful when it matches user expectations; it is not automatically right for every product. Document behavior and state transitions alongside appearance. Use native platform patterns unless research or product context justifies a different interaction.

## Every control has a contract

For each interactive element, specify:

- **Purpose:** what user goal it serves and what its label promises.
- **Input:** pointer, touch, keyboard, assistive technology, voice, or another method.
- **State:** idle, focused, pressed, selected, disabled, loading, success, error, or expanded/collapsed as relevant.
- **Transition:** what action changes state and what the new state means.
- **Feedback:** visible and programmatic signal, timing, and whether it persists.
- **Recovery:** undo, cancel, retry, edit, or help route.
- **Constraints:** permissions, network delay, data loss, privacy, or irreversible effect.

A control that only looks interactive but has no working action is misleading. A disabled control should have a reason that users can discover; when possible, prefer an enabled path with validation that explains what is needed.

## Navigation and orientation

Use information architecture that mirrors user tasks and language. Keep primary navigation limited to stable top-level destinations; use local navigation for a coherent sub-area. Show current location where useful, including selected navigation state that is not conveyed only by color. Keep labels consistent across navigation, page headings, breadcrumbs, and help.

Do not make users infer hierarchy from hover alone. On narrow screens, preserve key destinations and a clear way to open/close navigation. Manage focus when menus open; support keyboard operation and Escape where appropriate. Use breadcrumbs for meaningful hierarchy, not as a substitute for a clear page title or back action.

Links navigate; buttons perform actions. Use descriptive link text that makes sense out of context when practical. Do not use vague “click here” text or make large regions clickable without an understandable affordance.

## Forms and data entry

Ask only for information necessary to complete the task. Group fields in the order users can answer them. Use one question per field where possible, visible labels, helpful examples, appropriate autocomplete, and clear format requirements. Do not rely on placeholders as labels; placeholders disappear and often have weak contrast.

Choose an input control that fits the choice:

- Use radios for a small set of mutually exclusive options that should be visible together.
- Use a select when the option set is long or space is constrained and users can identify the choice.
- Use checkboxes for independent selections, not mutually exclusive choices.
- Use a switch for an immediate on/off preference whose effect is clear; avoid it for a choice that needs a separate submit step unless the design communicates that clearly.
- Use date/time controls only if they are easier than direct entry for the audience and platform; support typing and assistive technology.

Indicate required/optional status plainly. Avoid asking the same information twice. Support paste, autofill, password managers, and correction. Preserve valid entries if a later field fails. If validation can be done locally, give feedback at a useful moment; avoid repeatedly interrupting users while they type. On submit, identify errors in text, summarize if there are several, and offer a direct way to reach each problem. Explain whether a successful submission is final, saved, or still pending.

For multi-step flows, tell users how many steps remain only when that information is reliable, indicate progress and current step, preserve inputs, allow review/editing, and make Back behavior predictable. Do not split a short form into needless steps. Do not use progress percentages that imply precision the system cannot support.

## Search, filters, and sorting

Provide a label or accessible name that explains the search scope. Make query submission behavior clear; show results count or status when helpful. Preserve query and filters when navigating back. Support empty, no-results, loading, and failure states. Offer useful recovery such as clearing a filter, correcting a spelling, or changing scope.

Use filters for meaningful refinements; show active filters and make them removable. Distinguish filter from sort. Keep applied state visible and update results predictably; on slower operations show progress. Avoid unexpectedly refreshing or resetting scroll/query state in ways that lose a user's place.

## Dialogs, menus, popovers, and overlays

Use an overlay only when it improves focus or context. Prefer a page or inline disclosure for information users need to compare with the underlying screen. A modal dialog blocks interaction with the background by design; use it for a focused task or decision, not as a default container for complex journeys.

Give dialogs a clear title and purpose. Move focus into the dialog appropriately, constrain focus only while truly modal, allow keyboard users to close or complete it, and restore focus logically on close. Do not close after an accidental backdrop click if that risks losing entered work. Menus should expose their expanded state and follow the platform's keyboard interaction. Do not implement a menu as a dialog or a dialog as a menu just because the visual surface is similar.

## Tables, lists, cards, and data displays

Use a semantic table for tabular relationships; a grid is an interactive widget with additional keyboard behavior and should only be used when users need spreadsheet-like interaction. Identify column and row relationships. Support sorting with a clear indicator and announced state. Do not encode status only through color. Provide a concise summary and accessible data alternative for complex visualizations.

Use lists for repeated items with meaningful labels and actions. Cards should have one clear grouping and avoid nested interactive controls that create ambiguous click/focus behavior. Ensure each repeated item has a distinct accessible name and action. Provide empty, loading, partial, and error states for data-driven views.

## Feedback and system status

Acknowledge user actions at the right time and with the right persistence. Use inline feedback for field-level validation, a persistent status for saved/pending work, and a toast only for brief, non-critical confirmation that does not require action. Important error or success information must not vanish before users can perceive it. Expose asynchronous updates programmatically when needed, without moving focus or announcing noisy intermediate events.

Distinguish “saved,” “saving,” “submitted,” “received,” “processing,” and “complete.” Do not say “success” while a backend operation is still pending. If an operation takes time, show progress or a clear pending state and tell users whether they can leave safely.

## Errors, empty states, and recovery

Design errors as part of the primary flow. State what happened, what remains safe, what action is possible, and whether retry may duplicate an operation. Use plain, non-blaming language. Preserve entered data. If an external dependency fails, explain what users can do now and when to seek help.

An empty state should explain why there is no content and offer a relevant next action (create, import, adjust filters, or learn more). Do not fabricate activity to make the view appear populated. Loading skeletons should resemble the eventual structure without causing layout jumps; use a spinner only where its duration/state meaning is clear.

## Destructive and consequential actions

Match friction to risk. For reversible actions, immediate execution with undo may be kinder than a confirmation dialog. For costly, irreversible, or legally consequential actions, clearly explain consequences before commitment, require deliberate confirmation where appropriate, and provide a receipt or status afterward. Avoid dark patterns: no disguised ads, forced continuity, hidden cancellation, shame-based language, preselected costly choices, or confusing opt-outs.

## Motion and micro-interaction

Motion should answer at least one question: What changed? Where did it go? What is interactive? Is the operation still in progress? Keep duration and distance proportionate, avoid excessive bounce, and ensure content remains readable. Honor reduced-motion settings and provide a non-motion equivalent when motion conveys important information. Do not animate every hover, load, and scroll event by default. Test performance on lower-powered devices and reduce offscreen work.

## Responsive interaction

Design for input mode and context, not just viewport width. Touch users need forgiving targets and spacing; keyboard users need visible focus and predictable order; pointer users benefit from hover only as supplemental feedback. Never make a core task hover-only or require precision dragging without an alternative. Re-test menus, tables, charts, forms, dialogs, and sticky controls at narrow sizes, zoom, and text resizing.

## Source guidance

Use the [W3C ARIA APG patterns](https://www.w3.org/WAI/ARIA/apg/patterns/) as informative behavior references for custom widgets; they are not a normative standard and examples require production testing. Use [NN/g's 10 usability heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) as review prompts, not compliance requirements. For the exact applicable accessibility criteria, consult [WCAG 2.2](https://www.w3.org/TR/WCAG22/).
