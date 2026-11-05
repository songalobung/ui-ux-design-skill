# Human-Centered UI/UX Design Skill

A practical design and implementation playbook for AI assistants that build or review digital products. It brings product thinking, UX research, visual design, interaction craft, accessibility, frontend implementation, and rendered-interface QA into one repeatable workflow.

The goal is not to make every product look alike. The goal is to help each product become clear, useful, accessible, coherent, and recognizably its own.

> Discover broadly. Select intelligently. Implement consistently. Evaluate objectively.

This project is independently maintained and is not affiliated with, endorsed by, or sponsored by Apple, Google, Anthropic, OpenAI, or any other platform or company referenced here. It links to official guidance where appropriate; it does not reproduce their brands or design systems.

## What this skill helps an assistant do

- Understand the product, its users, their tasks, and the evidence behind design decisions.
- Choose a distinct visual direction, then make deliberate decisions about layout, hierarchy, typography, color, imagery, and restraint.
- Design complete interaction behavior, including focus, hover, pressed, loading, success, empty, and error states.
- Adapt experiences for mobile, tablet, desktop, assistive technology, and different input methods.
- Build reusable components and tokens that fit the project’s existing technology and design system.
- Inspect rendered interfaces, find defects, correct them, and report what was and was not tested.

The skill is a structured guide, not a claim that an AI assistant is a human designer, that it has conducted user research, or that a generated interface is automatically accessible or production-ready.

## Use it with an AI assistant

Clone or download the repository, then provide the assistant with the complete skill folder. Keep `SKILL.md`, `references/`, and `templates/` together so the relative links and detailed guidance remain available. Load the core instructions and the references relevant to the task rather than pasting the entire library into every prompt.

For Claude, Gemini, Codex, Manus, or another assistant, adapt the file location and activation method to that assistant’s current supported skill or project-instruction format. The content is plain Markdown and framework-neutral; the repository does not claim that one filename or installation command works identically across all assistants.

## The design workflow

1. **Understand the product and people.** Identify the intended users, their goals, context, constraints, risks, and what evidence is available.
2. **Research and frame the task.** Study relevant products and flows. Separate observed facts from assumptions and use references to learn principles, not to copy distinctive layouts.
3. **Explore alternatives.** Compare plausible content structures, interaction models, and visual directions against user needs, product fit, accessibility, and feasibility.
4. **Specify the experience.** Define hierarchy, content, type and color roles, components, behavior, responsive changes, and meaningful states.
5. **Implement with the project’s conventions.** Reuse suitable tokens and components. Add dependencies and effects only when they solve a real need.
6. **Inspect and refine.** Check actual renders at relevant sizes, test important interactions and accessibility behaviors, fix high-impact issues, and disclose remaining uncertainty.

The detailed guides cover human-centered discovery, design philosophy, design styles, typography, color, layout, UX patterns, design systems, interaction, motion, accessibility, platform adaptation, anti-generic-design critique, and quality assurance.

## Repository map

- `SKILL.md` — core operating instructions and end-to-end workflow.
- `references/` — detailed guidance, research notes, source register, patterns, platform guidance, and QA methods.
- `templates/` — reusable design brief, usability-test plan, decision log, and evaluation records.
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — how to propose evidence-based improvements and source changes.
- `COPYRIGHT.md` — copyright and reuse notice.
- `SECURITY.md` — private vulnerability and security-reporting guidance.

## Contributing

Focused corrections and evidence-backed improvements are welcome. Read [`CONTRIBUTING.md`](CONTRIBUTING.md) before opening a pull request; it explains source quality, accessibility, attribution, and the repository's current licensing status.

## Design references

The skill treats vendor documentation as guidance for the vendor’s platforms, not as universal law. For Apple-platform work, consult [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/). For Android and Material Design contexts, consult [Google Material Design](https://m3.material.io/) and [Android accessibility guidance](https://developer.android.com/guide/topics/ui/accessibility). For web accessibility conformance, use the applicable normative requirements such as [WCAG 2.2](https://www.w3.org/TR/WCAG22/); do not treat a visual checklist or automated scan as proof of conformance.

The bundled source register distinguishes official platform guidance from commercial heuristics, academic work, and secondary-hosted materials. Sources have limits; product-specific user research and evaluation still matter.

## Quality and trust

- Do not invent product facts, user evidence, metrics, testimonials, or customer logos.
- Do not claim accessibility conformance, usability validation, or performance gains without appropriate evidence.
- Treat color, type, spacing, motion, layout, and component choices as decisions to justify—not decoration to apply by default.
- Preserve familiar conventions when they help users; originality is not an excuse to make common tasks harder.
- Verify current platform docs, package behavior, licensing, and asset rights before implementation or reuse.

## Copyright and license

See [`COPYRIGHT.md`](COPYRIGHT.md). This repository currently has no open-source license. Public visibility does not grant permission to copy, modify, or redistribute the skill. External names, marks, and linked resources belong to their respective owners.

## Security

See [`SECURITY.md`](SECURITY.md). Please do not post sensitive vulnerability details in a public issue.
