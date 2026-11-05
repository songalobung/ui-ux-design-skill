# UX patterns for common product tasks

Patterns are reusable hypotheses about what helps with a task. Select them based on user goals, context, risk, frequency, and platform. Do not use a pattern just because it appears in a library. Design success, error, interruption, recovery, and accessibility behavior as part of the pattern.

## Navigation and wayfinding

Use stable names that match users' language. Distinguish global destinations from local tools and page actions. Show current location where it helps orientation. Links should navigate; buttons should perform actions. Keep the back path understandable and preserve context when users return from a detail view. On small screens, ensure menu open/close, focus, expanded state, and current location are perceivable. Do not rely on hover or icons with unknown meaning.

## Onboarding and first-run experience

Ask what users need to accomplish before they can receive value. Prefer an immediately useful first task with contextual help over a compulsory tour. Request permissions only when a feature needs them, explain why, and allow users to decline where possible. Keep onboarding skippable when appropriate; preserve progress and give a route to learn later. Avoid fictional personalization questions, premature account creation, or collecting data without clear value. Measure whether people understand and complete the first meaningful task, not merely whether they clicked through the tour.

## Forms and multi-step workflows

Collect only necessary information. Use visible labels, meaningful grouping, familiar field types, examples, and clear required/optional indicators. Support autocomplete, paste, password managers, correction, and appropriate input modes. Show errors in text, next to the affected field and in a summary where useful. Preserve valid values and focus/announce errors responsibly.

Use a stepper only for genuinely multi-stage tasks. Explain prerequisites, progress, consequences, and what remains. Allow review/edit and predictable back behavior. Preserve data across steps and interruption. State whether submission is saved, received, processing, or complete. For high-consequence input, explain purpose and privacy before asking.

## Search and discovery

Label the scope. Make query, filters, and sort status visible. Preserve search state when opening and returning from results. Provide useful empty/no-results guidance and recovery. Use autocomplete only when it genuinely speeds entry; announce suggestions, support keyboard selection, and allow free input. Avoid making users learn internal taxonomy. For large catalogs, use task-based categories, search, and recent/recommended items only when relevance is explainable and not misleading.

## Checkout, booking, and transaction flows

Show total price, currency, timing, key conditions, taxes/fees where available, and cancellation/refund rules before commitment. Keep a review step for consequential transactions; allow users to correct details. Do not preselect costly extras, hide mandatory fees, create false urgency, or use confusing add-ons. Show pending/success/failure clearly and prevent duplicate submission without trapping the user. Provide a receipt/status and a route to support. For hotel or travel products, help users compare dates, location, room/offer terms, accessibility details where available, and total cost; never imply unverified availability or guarantee.

For ecommerce-specific browsing, search, product-list, and checkout heuristics, consult `curated-source-research.md` for the Baymard reference. Treat its article as commercial secondary guidance and adapt its examples to the actual product; it is not a universal standard or a replacement for current user research and testing.

## Dashboards and operational tools

Start with the user question: what changed, what needs attention, what action is possible? Give each metric a label, unit, time range, source/freshness, and interpretation as needed. Use status color sparingly and redundantly. Prioritize by impact and urgency, not decorative size. Distinguish no data from zero, stale data, loading, and failure. Provide a path from summary to evidence/detail. Avoid invented metrics and vanity charts.

## News and editorial products

Clearly distinguish editorial content, sponsored content, opinion, and advertisements. Present authorship, publication/update dates, and source context where appropriate. Preserve the reading experience while keeping navigation, share, save, and correction/report paths discoverable. Avoid recommendation systems that obscure chronology or source credibility without explanation. Do not let ads impersonate navigation or article controls.

## SaaS and collaboration products

Organize navigation around users' work, not internal departments. Make workspace/account context visible, clarify roles/permissions before a blocked action, and explain sharing scope. Support undo and version/history where feasible. Show collaboration status without exposing sensitive content unnecessarily. Use progressive disclosure for advanced configuration while keeping consequences visible. Distinguish local changes, saved changes, shared/published state, and permission errors.

## Empty, loading, success, and error states

- **Empty:** explain why there is no content and offer the most relevant next action; do not fabricate sample activity as if real.
- **Loading:** show progress when useful and avoid duplicate actions; use skeletons only when they match actual layout and do not cause jumps.
- **Success:** confirm the actual outcome and next step; do not report success before the operation completes.
- **Partial success:** specify what succeeded, what did not, and how to continue without duplicating work.
- **Error:** use plain language, preserve input, identify recovery, and clarify whether retry is safe.
- **Offline/stale:** distinguish current from cached data and explain when it was last updated.

## Dialogs, confirmations, and notifications

Use a modal for a short focused interruption, not as a container for a complex flow. Give it a title, focus behavior, keyboard support, and a logical return point. Match confirmation friction to consequence; use undo for reversible actions when more efficient. Do not use a transient toast for critical information that users must read or act on. Do not show notifications merely because an event occurred; make them relevant, timely, and controllable.

## Ethical defaults and user control

Defaults can reduce effort but also steer decisions. Choose defaults that are safe, explainable, and aligned with user intent. Make alternatives visible and easy to choose. Consent must be informed and unbundled where applicable. Avoid dark patterns such as hidden cancel, confirmshaming, false scarcity, forced continuity, disguised advertising, or asymmetric choices.

## Pattern evaluation

For each selected pattern, record user goal, context, evidence, risk, access behavior, alternate path, and success measure. Prototype alternatives when uncertainty is material. Test task completion and comprehension with realistic scenarios. Pattern familiarity is a starting hypothesis, not proof of usability.
