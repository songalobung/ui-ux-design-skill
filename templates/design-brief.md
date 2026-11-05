# Human-centered UI/UX design brief

> Use this for a substantial screen, flow, redesign, or design system. For a small change, fill only relevant fields. Label evidence, interpretation, and hypothesis separately; do not invent research, user data, or product claims.

## 1. Problem and outcome

- **User task:** Who needs to do what, in which context?
- **Desired outcome:** What should people be able to complete, decide, or understand?
- **Why it matters:** User impact, service/product context, and cost of failure.
- **Scope / non-goals:** What will and will not change?
- **Evidence:** Research, support feedback, analytics, policy, existing product behavior. Include source/date and limitations.
- **Assumptions / open questions:** What is inferred or still unverified?
- **Success evidence:** Observable outcomes and how they will be measured without overstating causality.

## 2. People and context

- **Relevant tasks and user contexts:** Avoid unsupported demographic generalizations.
- **Environment:** Device, input, time, interruptions, connectivity, privacy, language, location, accessibility needs.
- **Potential barriers:** Vision/hearing/mobility/cognitive/language/literacy needs and temporary or situational constraints.
- **Support and recovery:** Help path, non-digital/alternate channel, save/resume, undo, contact route.
- **Research needed:** What decision is uncertain, who should be involved, and what method fits?

## 3. Journey and information architecture

- **Entry point and prerequisites:**
- **Key user questions:**
- **Steps, decisions, and handoffs:**
- **Required information/evidence:**
- **Primary outcome and confirmation:**
- **Error, interruption, abandonment, and return paths:**
- **Dead ends or redundant effort to remove:**
- **Page/screen purpose and information hierarchy:**

## 4. Creative direction and research references

- **Concept statement:** [One sentence for the product-specific experience]
- **Personality axes:** [e.g. expressive/quiet, dense/spacious, formal/conversational]
- **Visual principles:** [3–5 principles translated into design choices]
- **Do / avoid:** [Rules that make the concept distinctive and coherent]
- **Existing product/brand identity:**
- **References reviewed:** [Link and what was directly observed]
- **Transferable insight vs. element not to copy:**
- **User expectation hypothesis:** [How to validate]

## 5. Layout and composition

- **Chosen composition:** [Single-column task flow, split view, dashboard, table, editorial, wizard, etc.]
- **Why it fits the task/content:**
- **First read / primary action:**
- **Grouping and sequence:**
- **Grid/content width/density:**
- **Reading order and semantic structure:**
- **Responsive transformation:** What changes on mobile, tablet, desktop and why?
- **Stress cases:** Long content, no data, error, translation, enlarged text.

## 6. Typography decisions

- **Font families and roles:** [Display/body/interface/data; explain why]
- **Pairing rationale:** [Or say one family is sufficient]
- **Language/script and glyph coverage:**
- **Scale roles:** Display, page/section heading, body, label, supporting text, metadata.
- **Size/weight/line-height/measure:**
- **Responsive behavior and text enlargement:**
- **Fallback, loading/performance, and font license:**
- **Validation examples:** [Long heading, form label, table, error, localization]

## 7. Color decisions

- **Brand and emotional/task rationale:** Avoid universal claims about color psychology.
- **Semantic palette:** Canvas, surface, text, muted text, border, primary action, focus, selection, success, warning, error, information.
- **Light/dark theme mapping:**
- **Foreground/background pairs checked:**
- **Non-color meaning cues:** Text, icon, shape, pattern, position.
- **Contrast test method/results:** Record actual rendered pairs and criterion where applicable.
- **Color-vision / grayscale check:**

## 8. Component architecture

| Component | Purpose | Reuse or new | Variants/states | Input/accessibility contract | Dependencies/license |
|---|---|---|---|---|---|
| [Name] | [User goal] | [Existing/new] | [Relevant states] | [Semantics/keyboard/focus] | [Verified] |

- **Existing tokens/primitives to reuse:**
- **Variants/API kept intentionally small:**
- **Responsive/content behavior:**
- **Documentation/usage constraints:**

## 9. Interaction and UX psychology

- **Actions and expected outcomes:**
- **Status feedback:** Saved, pending, processing, complete, failed.
- **Error prevention and recovery:**
- **Cognitive load reduced:** [Recognition, chunking, defaults, contextual help]
- **User control:** [Back, cancel, undo, pause, edit]
- **Consequential decisions:** [Fees, privacy, permission, deletion, legal/safety implications]
- **Dark-pattern risks reviewed:** [No hidden opt-out, coercive default, deceptive friction]

| Element / purpose | Input methods | States/transitions | Feedback | Error/recovery | Accessible name/focus/announcement |
|---|---|---|---|---|---|
| [Control] | [Keyboard/touch/pointer/etc.] | [Default/focus/loading/etc.] | [What and when] | [Undo/retry/etc.] | [Expected behavior] |

## 10. Motion design

- **Purpose:** [Orientation, feedback, transition, status, or justified delight]
- **Trigger and start/end state:**
- **Duration/easing/distance:**
- **Reduced-motion alternative:**
- **Repeat/scroll/offscreen behavior:**
- **Performance and comfort risks:**

## 11. Responsive plans by context

| Context | Composition/navigation | Input and target behavior | Priority/content changes | Risks to test |
|---|---|---|---|---|
| Mobile/narrow | | Touch + keyboard | | |
| Tablet/intermediate | | Touch/pointer/keyboard | | |
| Desktop/wide | | Pointer + keyboard | | |

Also check intermediate widths, zoom/text size, orientation where relevant, localization, and realistic content lengths.

## 12. Requirements and constraints

- **Framework/repository conventions:**
- **Normative accessibility standard, version, level, and scope:** [If unknown, say unknown]
- **Jurisdiction/organizational policy:** [Verify applicability]
- **Privacy, security, safety, performance, content constraints:**
- **Dependencies/assets/fonts and license verification:**

## 13. Quality assurance and evaluation

- **Critical task scenario(s):**
- **Research/test method and participants:**
- **Keyboard-only checks:**
- **Assistive technology checks and environment:**
- **Responsive/rendered inspection:** [Viewports, browsers, actual routes]
- **Automated tests/tools:** [What they can and cannot establish]
- **Top three defects and fixes:**
- **What remains untested or uncertain:**
- **Conformance claim evidence, if applicable:** [Full evaluation scope; do not infer from spot checks]
