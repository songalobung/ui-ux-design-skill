# Visual QA: inspect, compare, correct

Visual QA verifies the interface people actually receive. A design file, code diff, screenshot at one size, or passing build is not sufficient. Combine visual inspection with interaction, accessibility, content, and technical checks.

## 1. Establish the reference and environment

Record the intended route, browser/device or simulator, viewport, scale/zoom, operating system, theme, font loading state, test account/data state, and build/version. Identify the source of truth: approved design, existing design system, product brief, or user-tested behavior. A screenshot comparison is misleading if the viewport, fonts, data, or state differ.

If the approved design conflicts with accessible behavior or user evidence, do not blindly reproduce it. Record the mismatch and resolve the higher-priority issue.

## 2. Build a coverage matrix

Select representative screens/states and target contexts. Cover the primary task plus failure and recovery. Include narrow/mobile, intermediate/tablet, wide/desktop, and intermediate widths where layout changes. Include light/dark themes if supported, enlarged text/zoom, long and short content, empty/loading/success/error states, and reduced motion.

Do not attempt every possible permutation blindly. Prioritize by usage, risk, complexity, and likelihood of layout/state failure. Record what is not covered.

## 3. Inspect visually at multiple scales

### Macro pass
Check page hierarchy, composition, primary action, density, content width, major alignment, responsive reflow, and overall product identity. Ask whether the screen answers the user's first questions.

### Component pass
Check spacing, dimensions, typography, color pairings, borders, elevation, icons, labels, state affordances, and consistency with the design system.

### Detail pass
Check wrapping, line-height, baseline alignment, focus outlines, clipped content, 1px seams, asset crops, shadows, animation artifacts, and text over image backgrounds.

### State pass
Inspect focus, hover, pressed, selected, disabled, loading, success, error, validation, empty, stale, and offline states as applicable. Do not approve a default-only render.

## 4. Screenshot comparison

When a reference screenshot exists, compare at the same viewport, zoom, route, content, and state. A side-by-side or overlay can reveal layout drift; pixel-difference images can highlight changed regions but cannot decide whether the result is better. Font rendering, anti-aliasing, dynamic data, browser differences, and image loading can create harmless diffs.

Use screenshots as a diagnostic tool, not as the product goal. Fix hierarchy, content, behavior, and accessibility before chasing subpixel differences. Maintain representative baseline screenshots only when visual regression automation has a clear owner and update process; avoid tests so brittle that every intentional change becomes noise.

## 5. Functional and responsive pass

Follow the primary user flow. Activate every visible control. Test navigation, form submission, field-level and summary errors, back/undo, focus behavior, asynchronous states, duplicate action prevention, and recovery. Check actual touch/pointer and keyboard use.

Inspect layout at widths just above and below breakpoints, not only familiar device presets. Look for overflow, overlap, clipped focus, fixed bars hiding content, unnatural reading order, overly long lines, collapsed navigation with no visible cue, and tables/charts without usable alternatives. Test long translated strings and enlarged text.

## 6. Accessibility pass

Use `accessibility.md` and the normative WCAG source. Check semantic structure, accessible names, keyboard completion, visible focus, contrast, text resize/reflow, target size, drag alternatives, motion, error relationships, and status announcements. Use automated tooling as one layer only. Test with relevant screen readers and assistive technologies where available. Record browser, OS, technology, and version.

## 7. Content and visual integrity pass

Verify that labels, units, prices, dates, status, source, and terms are accurate. Ensure examples or sample data are clearly identified. Check that imagery is appropriate, licensed, representative, and cropped without changing meaning. Ensure charts have adequate context and do not imply unsupported precision. Confirm legal/privacy claims with an appropriate owner.

## 8. Defect severity and triage

Classify by impact on user outcome, access, trust, and risk—not by how easy the bug is to fix:

- **Blocker:** prevents completion, causes likely serious harm/data loss, or excludes a user from a critical task.
- **Major:** likely causes wrong outcome, substantial repeated failure, or severe access barrier.
- **Moderate:** causes confusion or detour with a discoverable recovery.
- **Minor:** low-impact inconsistency or polish issue.

Frequency matters but does not erase severe impact on a smaller group. Record reproduction steps, expected/actual behavior, environment, evidence, affected task/context, and a suggested fix. Separate observation from interpretation.

## 9. Correction loop

1. Capture the issue and rank impact.
2. Identify root cause: content, information architecture, component, responsive rule, token, implementation, data, or test setup.
3. Apply the smallest coherent fix—not a local patch that creates inconsistent behavior elsewhere.
4. Re-run the affected task and relevant viewport/state checks.
5. Inspect for regressions in adjacent components/themes.
6. Record retest result and any limitation.

For major work, list the three highest-impact issues before polishing minor details. A “ruthless critic” should be direct about the artifact, not insulting to people.

## 10. Honest QA report

Report what was actually inspected, including route, viewport/browser, states, keyboard/AT tools, automated checks, and build/test results. Separate verified fixes from untested assumptions. Never claim WCAG conformance from screenshots, a few spot checks, or an automated score. Never claim that visual fidelity is exact if no reference comparison was run.
