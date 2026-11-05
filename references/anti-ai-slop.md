# Anti-AI-slop: evidence-informed design critique and repair

## What “AI slop” means here

“AI slop” is an informal criticism, not a standardized UX or visual-design term. This guide uses it operationally for an output that is plausible or polished at first glance but is generic, weakly grounded in product/user context, careless in execution, or presented with more certainty than its evidence deserves. It is not a label for work merely because AI helped make it. Nor is any individual style—gradients, cards, sans-serif fonts, minimalism, bento grids, dark mode, or rounded buttons—proof of slop. Judge the specific work against its purpose and users.

The research suggests two distinct problems that are often collapsed into one. **Convergence** means outputs across many people or projects become more similar; **contextual/design failure** means one artifact does not serve its particular product or users. An interface can be original yet unusable, or conventional yet excellent. Critique both dimensions separately.

## What the research supports

Nielsen Norman Group's 2025 evaluation used a real training-profile redesign scenario, several classes of AI prototyping tools, prompts with different levels of detail, design artifacts, and heuristic evaluation against human-designed work. The authors found that broad prompts left more decisions to the tools and produced generic or poorly matched designs, while explicit requirements and supplied design artifacts generally improved fit. Even stronger outputs still showed issues such as weak hierarchy/grouping, overused colors, poor contrast, and inconsistent spacing. This is a practitioner evaluation in one project context, not proof about every model or interface. [1]

A preregistered experiment in *Science Advances* assigned 293 writers to human-only or GPT-4 idea-assistance conditions and had 600 people evaluate the stories. AI idea assistance improved some individual-rated story outcomes, especially for less-creative writers, while AI-assisted stories were more similar to one another. This provides evidence for an individual-benefit/collective-diversity trade-off in short fiction, not direct evidence that generated websites all look alike. [2]

A 2025 study in *Computers in Human Behavior: Artificial Humans* compared three preregistered studies involving 2,200 college-admissions essays with GPT-4 outputs. It reported lower group-level diversity growth in the AI-generated essays, even after some prompt and parameter changes. The authors explicitly note that their controlled essay comparison is not the same as naturalistic, personalized human–AI co-creation and that the admissions-essay setting limits generalization to other domains. [3]

A 2026 ACM conference short paper reported a systematic review/meta-analysis of 19 empirical studies and 61 effect sizes, finding a small statistically significant homogenization effect (d = .334). It frames this as collective semantic/conceptual convergence, not proof that individual output is less creative or worse. It is an early synthesis of a newly developing research area, and its conclusions concern creative outputs broadly rather than UI alone. [4]

An ACM IUI companion paper evaluated 200 interfaces produced by five AI design tools against five selected accessibility criteria and interviewed six experienced designers. It reported at least one selected-criteria violation in 72% of the interfaces; the average severity was relatively minor in that particular measure. Accessibility-oriented initial prompts changed the result only slightly, while iterative designer–AI refinement was a recurring way to address issues. This small companion-proceedings study is not a full WCAG conformance audit, and its selected criteria/tool/sample do not represent every UI generator. [5]

Together, these findings support a practical conclusion: AI can accelerate exploration and improve some individual outputs, but a prompt or attractive first render does not reliably supply originality, context-sensitive judgment, interaction quality, or accessibility. Human specification, selection, implementation, and evaluation remain necessary. The evidence does **not** justify banning popular patterns, equating convention with poor quality, or assuming every AI-assisted interface is generic.

## A taxonomy for diagnosis

### 1. Product-blind sameness

**Signals:** The same generic hero, decorative gradient, oversized claim, three-column feature cards, faux dashboard, testimonial strip, and conversion CTA appear for an unrelated product. The screen could be relabeled with another company name without changing its information structure.

**Why it matters:** The layout fails to express the product's actual task, domain, information needs, trust context, or operating constraints. The issue is not that the layout is common; it is that the layout has no reason to be here.

**Repair:** Identify the primary user task, content model, domain stakes, and product promise. Compare at least two relevant products and one contrast case if research is available. Choose a composition that follows the task. Give each expressive element a job. Preserve familiar conventions when they lower learning cost.

### 2. Surface novelty without a concept

**Signals:** A random mixture of editorial serif, neon glow, glass panels, brutalist lines, sticker illustrations, 3D objects, and micro-animations. Individual effects are fashionable but do not reinforce one idea.

**Repair:** Define a short Design DNA: product promise, audience/context, desired tone, distinctive visual proposition, two or three supporting principles, and explicit avoid-list. Ask of each treatment: what product meaning, information hierarchy, or useful feedback does it improve? Remove decoration with no clear answer.

### 3. Beautiful shell, missing UX

**Signals:** Strong hero art but unclear next step; fake pricing; empty or implausible dashboard data; missing permissions, eligibility, privacy, or error states; forms that do not explain requirements; controls that look clickable but do nothing.

**Repair:** Map the task from entry through completion and recovery before polishing. Verify all product claims and content. Define control purpose, state transitions, feedback, error recovery, and cancellation/back behavior. Keep sample data conspicuously identified as sample; do not fabricate customer proof, metrics, logos, or testimonials.

### 4. Near-correct, low-craft execution

**Signals:** Related labels are far apart; every region has equal contrast; typography wraps poorly; contrast is weak; icons have inconsistent stroke; spacing is arbitrary; imagery crops away the subject; components do not share token or state rules.

**Repair:** Inspect actual rendered output at target widths with realistic content. Fix structure and grouping first, then hierarchy, type, spacing, color, media, and details. Use tokens and component variants to prevent drift. Compare against a reference only when it is authorized and rendering conditions are controlled.

### 5. Accessibility by slogan

**Signals:** “Make it accessible” appears in the prompt, but the interface still lacks correct names/labels, keyboard operation, focus management, contrast, non-color cues, usable error messages, reduced-motion behavior, or screen-reader announcements.

**Repair:** Convert the target into concrete requirements and acceptance tests. Inspect semantics and real states, not only a screenshot. Combine automated scans with manual keyboard and assistive-technology checks, zoom/text resizing, touch checks, and user testing where feasible. Record untested criteria and known exceptions. A clean automated scan is not proof of accessibility or WCAG conformance.

### 6. The one-shot final

**Signals:** The first generated screen is treated as finished. No alternatives are compared, no route or state inventory exists, and no browser/rendered inspection is performed.

**Repair:** Use generation for exploration, not sign-off. Iterate from identified findings: render, inspect, test tasks, document problems, fix, and retest. Preserve rejected directions and why they were rejected so exploration does not repeatedly restart from the same default.

### 7. Copying rather than learning

**Signals:** A reference or component is replicated without its original context, responsive behavior, content, accessibility, license, or project conventions.

**Repair:** Extract the principle (“keeps category switching visible during comparison”) rather than copying the signature look. Adapt it to the product's task and design system. Verify code, asset, font, and package rights and current dependency details before reuse.

### 8. Unsubstantiated certainty

**Signals:** The result is called “high-converting,” “user-validated,” “WCAG-compliant,” “pixel-perfect,” or “production-ready” based on a screenshot, prompt, or automated score alone.

**Repair:** Report exactly what was tested, by whom or which tool, under what conditions, what passed, and what remains unknown. Do not claim causality or user preference without appropriate evidence.

## The anti-slop workflow

1. **Ground the work.** Summarize the verified product purpose, primary user task, context, constraints, existing design system, content, platforms, and risks. Separate evidence from assumptions. If important product details are missing, ask a focused question or state a testable assumption.
2. **Research with discrimination.** Inspect a small but varied set of relevant examples: shipped products and user flows for conventions, plus visual references for creative possibilities. Capture the source, what was actually observed, what is inferred, and what should not be copied. Do not treat a gallery as usability evidence.
3. **Generate distinct concepts before polishing.** When the direction is uncertain, sketch three genuinely different information/composition strategies, not three colorways of one template. Consider a functional/conventional direction and one expressive direction; include one option without decorative effects. Compare by task fit, clarity, distinctiveness, accessibility, feasibility, and risk. Choose and explain a trade-off.
4. **Specify Design DNA and systems.** Set type roles, semantic color roles, content hierarchy, layout logic, image treatment, component rules, interaction states, responsive transformations, motion stance, and an avoid-list. Tie choices to product needs. Check script support, licensing, load cost, and accessible states.
5. **Build complete behavior.** Include useful copy and credible data; make apparent controls work; implement keyboard/focus behavior; provide empty, loading, success, and error states where relevant. Keep the core experience useful if advanced images, motion, or 3D fail.
6. **Render and critique.** Inspect desktop and narrow screens, intermediate widths, and realistic states. Critique with evidence: observation → user consequence → severity → proposed correction. Check hierarchy, relationship/grouping, content truth, type, contrast, focus, responsive behavior, motion, performance, and consistency.
7. **Fix and re-evaluate.** Correct high-impact task/accessibility failures before aesthetic micro-polish. Rerun relevant functional, screenshot, accessibility, and responsive checks. Record what could not be evaluated.

## Critique prompts

Ask these after the interface is rendered:

- Does the page make its actual task and next useful action clear?
- Which elements make this product recognizably itself, and what evidence or product truth supports them?
- Could the screen be relabeled for a different product? If yes, is that reuse justified by a common convention or is the design under-specified?
- Are visual references broad and relevant, or is one source dominating the design?
- Does each section answer a user question, support a task, or express a defensible identity principle?
- Is emphasis aligned to importance? Are related items grouped and distinct items separated?
- Can someone use every apparent control? What happens on keyboard, touch, error, loading, no data, or return visit?
- Does the interface remain understandable with reduced motion, narrow width, larger text, long translated strings, or different input methods?
- Which effect, card, icon, label, image, or step can be removed without losing meaning?
- Was the rendered result actually inspected? What evidence is missing?

## Repair order

1. Remove invented claims, misleading content, or fake functionality.
2. Clarify user task, product truth, content hierarchy, and task flow.
3. Fix safety, trust, accessibility, and interaction blockers.
4. Recompose for the actual content and responsive contexts.
5. Establish coherent type, color, tokens, and component states.
6. Correct visual details such as spacing, grouping, crops, alignment, and rhythm.
7. Reintroduce only visual character that strengthens identity, comprehension, or useful feedback.
8. Inspect and retest the actual implementation; document remaining uncertainty.

## Research references

[1]: https://www.nngroup.com/articles/ai-prototyping/ "Good from Afar, But Far from Good: AI Prototyping in Real Design Contexts"
[2]: https://www.science.org/doi/10.1126/sciadv.adn5290 "Generative AI enhances individual creativity but reduces the collective diversity of novel content"
[3]: https://www.sciencedirect.com/science/article/pii/S294988212500091X "Homogenizing effect of large language models on creative diversity"
[4]: https://dl.acm.org/doi/10.1145/3822301.3822304 "Generative AI Makes Creative Output More Homogeneous"
[5]: https://dl.acm.org/doi/10.1145/3708557.3716347 "Understanding and Improving Accessibility in AI-Generated Interfaces"
[6]: https://playwright.dev/docs/accessibility-testing "Playwright accessibility testing"
