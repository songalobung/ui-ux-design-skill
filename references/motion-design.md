# Motion design for interfaces

Motion is communication through change over time. It can reveal causality, orientation, state, hierarchy, progress, or character. It can also distract, disorient, slow, exclude, and consume battery. Start from a user purpose and remove motion that cannot justify its cost.

## Motion decision framework

For each effect, specify:

- User question it answers.
- Trigger and source of the change.
- Start/end state and what remains interactive.
- Whether motion is spatial, opacity, scale, color, or a data transition.
- Duration range, delay, easing, and distance/scale.
- How it handles interruption, reversal, repeated activation, and loading failure.
- Keyboard/focus and assistive-technology behavior.
- Reduced-motion alternative and pause/stop controls where needed.
- Performance, layout, battery, and content stability implications.

If there is no clear user or brand purpose, prefer no animation or a simple immediate state change.

## Timing and easing

Timing should match the scale and consequence of the change. Small local feedback should feel immediate; large spatial transitions may take longer only when they help preserve orientation. Avoid delaying controls before they respond. Use easing to convey start/stop naturally, but do not apply exaggerated bounce or elastic motion by default. When many elements animate, stagger only if it improves comprehension; otherwise it delays information and harms scanability.

Do not treat one duration/easing table as universal. Platform, input, motion sensitivity, task speed, and device performance vary. Define a small token set for the product and test it in real interactions. Keep motion consistent across equivalent actions.

## Micro-interactions

A useful micro-interaction has a trigger, a response, and a clear meaning. Examples include a pressed state acknowledging activation, a save status confirming persistence, or a disclosure transition showing content expansion. Ensure that the state is also perceivable without motion: text/state, semantics, iconography, or direct content change. Do not animate every pointer hover, focus, and scroll event automatically. Focus feedback is required to be visible but need not be animated.

## Page and route transitions

Use transitions to preserve spatial or task continuity only when the relationship between views is real. Avoid hiding route changes behind long animations. Do not move content in ways that alter reading order or cause focus to be lost. Respect browser history and reduced-motion preference. Make loading and route errors understandable if transition data fails.

## Scroll effects and parallax

Do not hijack native scrolling for essential content. Avoid scroll-jacking, forced snap points that impede reading, parallax that causes discomfort, scroll-driven text that outruns readers, and sticky elements that obscure headings or focus. Essential text and controls must remain available when animation is disabled. Provide stable fallbacks for unsupported features and lower-powered devices. Check performance, keyboard operation, touch, and reduced motion.

## Data visualization and motion

Animate data only when the transition helps identify what changed or preserves object constancy. Do not animate values in a way that misrepresents scale, exaggerates change, or makes data hard to compare. Provide final values and summaries independent of animation. Avoid delaying important status behind an animation.

## Reduced motion and safety

Honor the user's system preference and product accessibility settings. Replace large movement with a fade or immediate state change when appropriate. Avoid flashing, rapid repeated motion, zooming interfaces, and auto-moving elements that cannot be controlled. Review exact applicable WCAG criteria for flashing, moving/auto-updating content, and timing; the criteria have specific thresholds, scope, and exceptions. “Supports reduced motion” is not a blanket accessibility claim.

If motion is essential to the task (for example, showing physical motion in a training simulation), provide clear controls, alternative explanation, and appropriate access accommodations. Test with users who experience motion sensitivity when movement is central.

## Implementation and performance

Prefer transform and opacity transitions when appropriate to avoid costly layout recalculation, but measure actual performance rather than assuming. Avoid animating large blurred layers, high-resolution backgrounds, or many offscreen objects. Pause nonessential animations when not visible. Keep input responsive and do not let animation block repeated safe actions. Test mobile hardware, lower frame rates, battery impact, and CPU/GPU fallback.

For implementation, select one animation approach that fits the stack and team skill. Libraries such as Motion/Framer Motion or GSAP may provide reusable tools, but library choice does not solve design purpose or accessibility. Verify current API, licensing, bundle impact, and reduced-motion behavior in the project's official documentation before use. Avoid adding a runtime dependency for a trivial CSS transition.

## Motion review

Disable motion and confirm the interface still makes sense. Enable reduced motion and test every transition. Check that focus is not obscured, state is not delayed, and movement does not impair reading. Record the specific purpose of each recurring motion pattern. If a reviewer cannot explain what information it communicates, simplify or remove it.
