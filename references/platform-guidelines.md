# Platform guidelines: web, mobile, and desktop

Platform conventions help users predict behavior, but they are not immutable laws. Use the conventions of the target platform unless a researched product need justifies a difference. Confirm current official guidance for exact dimensions, APIs, and requirements; those details change. The principles below are durable orientation, not a substitute for platform documentation or accessibility standards.

## First identify the actual target

Before design or implementation, determine:

- Web, native iOS, native Android, desktop, TV, wearable, embedded, or responsive cross-platform.
- Browser/runtime, OS versions, supported input devices, and target languages.
- Whether the app uses native navigation/controls or a custom design system.
- User expectations, technical constraints, accessibility requirements, and distribution policies.

Do not assume that a mobile viewport means a native mobile app or that a desktop means pointer-only. Web applications need keyboard, screen reader, browser history, zoom, responsive layouts, and varied input. Desktop tools may need keyboard shortcuts, large data density, resizeable windows, and system-level accessibility. Touch devices may also use keyboards or assistive switches.

## Web

Use semantic HTML and browser-native behavior wherever possible. Preserve URL, browser history, back/forward, link opening, keyboard operation, zoom, text reflow, and user control. Use responsive layouts based on content constraints. Distinguish links from buttons. Avoid hijacking scrolling, focus, or context menus without a strong task-based reason. Test progressive loading, errors, direct route entry, and network variation.

Web accessibility requirements depend on applicable law, policy, and standard. Use the normative WCAG specification for conformance claims. WAI APG is informative widget guidance, not the standard itself. See `accessibility.md` and `standards-and-sources.md`.

## iOS and iPadOS

Follow current Apple Human Interface Guidelines and native control behavior where applicable. Respect system text sizing, Dynamic Type, VoiceOver, Switch Control, Reduce Motion, appearance, safe areas, and navigation conventions. Avoid drawing custom controls when native controls provide a more predictable and accessible experience. For iPad, consider multitasking, resizable layouts, keyboard/trackpad input, and context-specific density rather than simply enlarging a phone UI.

Verify current Apple guidance for control dimensions, navigation, materials, and APIs in the official [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/). Product-specific exceptions need a clear user benefit and accessibility review.

## Android

Follow current Material Design guidance and Android platform conventions where appropriate. Support varied screen sizes, system font/display scaling, TalkBack, keyboard/switch access, back navigation, edge-to-edge/system bars, and platform settings. Accommodate device and manufacturer variation. Use Material components only if they fit the product and implementation system; do not assume visual adherence guarantees accessibility.

Consult current official [Material Design](https://m3.material.io/) and [Android accessibility guidance](https://developer.android.com/guide/topics/ui/accessibility) for APIs, components, and exact current recommendations. Verify platform version and target SDK before implementation.

## Desktop

Desktop interfaces may support higher information density, but only when users need it. Respect window resizing, keyboard navigation, focus, system text scaling, screen readers, high-contrast/forced-color settings, and platform shortcuts. Keep critical actions discoverable and avoid hover-only controls. For productivity software, consider command search and shortcuts as accelerators, not the only path. Preserve user work across resize, restart, and interrupted tasks where appropriate.

For desktop web, use browser standards rather than inventing native-like behavior that breaks links, selection, or history. For native desktop, follow the target OS conventions and verify current official accessibility and interaction guidance.

## Tablet and hybrid input

Treat tablet as its own context: users may switch between touch, keyboard, stylus, and pointer. Design for split-screen, changing orientation, window resizing, and intermediate widths. Provide touch-friendly controls without wasting space; make pointer hover supplemental and keyboard focus distinct. Do not force phone or desktop composition when neither fits.

## Cross-platform product strategy

Share user goals, content model, semantic roles, and design tokens where this helps consistency. Adapt navigation, controls, gestures, density, system integration, and motion to each platform. Do not force pixel-identical screens when platform expectations differ. Document intentional differences and test task parity: can users accomplish the same essential outcomes and recover in a comparable way?

## Platform review checklist

- Does navigation match platform expectations and preserve user orientation?
- Are back, cancel, close, and history behaviors clear?
- Are native controls/primitives used where they improve access and predictability?
- Are touch, keyboard, pointer, screen reader, switch, and voice input considered as relevant?
- Does text resizing, safe area/system UI, window resizing, and orientation work?
- Are platform motion, appearance, and accessibility settings respected?
- Is the interaction consistent with the current official guidance and SDK/runtime?
- Are differences between platforms intentional and documented?

## Official platform guidance

- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)
- [Google Material Design 3](https://m3.material.io/)
- [Android accessibility guidance](https://developer.android.com/guide/topics/ui/accessibility)
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [W3C ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/)

For Apple-specific design decisions, the [Apple Design hub](https://developer.apple.com/design/), [HIG design principles](https://developer.apple.com/design/human-interface-guidelines/design-principles), and [App design and UI overview](https://developer.apple.com/documentation/technologyoverviews/app-design-and-ui) are useful entry points. The App Design and UI overview contains Apple framework guidance; treat SwiftUI and UIKit/AppKit advice as Apple-specific, not cross-platform UX requirements.

For Meta ecosystems, consult [Design at Meta tools and resources](https://www.meta.com/design-at-meta/tools/) as a directory, and follow its linked Horizon OS human interface guidance for immersive Meta products. The directory itself is not a cross-platform standard; verify rights and terms at each linked asset or tool before reuse.

Check current pages and platform versions before relying on exact measurements, APIs, or policies.
