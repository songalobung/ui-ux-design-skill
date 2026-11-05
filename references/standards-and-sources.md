# Standards and source guide

Use the source that matches the question. A design system, heuristic, or platform guide can inform a decision; it does not automatically create a standards conformance claim. Always check the current source text before stating a legal obligation, success criterion, numerical threshold, or platform-specific rule. The links below were reviewed on 2026-11-05; standards and sites can change.

## How to interpret source authority

- **Normative specification:** defines testable requirements and conformance conditions within its scope. For web accessibility, WCAG 2.2's normative specification is the source for its success criteria and conformance model.
- **Informative implementation guidance:** explains or illustrates patterns but is not itself a conformance model. WAI Understanding documents, techniques, and the ARIA Authoring Practices Guide (APG) are informative.
- **Service or legal policy:** may be mandatory for a specific organization, jurisdiction, procurement, or service. Verify who is covered and which version applies; do not universalize a government service manual.
- **Platform design guidance:** explains platform conventions and recommendations for that platform. Apple HIG and similar guides are not universal legal standards.
- **Heuristic or methodology:** helps identify design issues and structure learning, but cannot establish conformance or replace user research. Nielsen Norman Group heuristics and Microsoft's Inclusive Design methodology fall here.
- **Library/vendor content:** demonstrates examples and workflows. It is not blanket permission to reuse components or proof they meet accessibility standards.

Do not write “WCAG requires” unless the claim maps to an exact applicable WCAG success criterion. Use “guidance recommends” for informative material. If a public-sector policy or law makes a requirement applicable, name the jurisdiction/organization and source separately.

## W3C WCAG 2.2

[Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/) is the normative W3C Recommendation for web content accessibility. Its conformance section defines scope and requirements. A Level AA claim includes all applicable A and AA success criteria and must satisfy the specification's complete-page and other conformance conditions. Selected checks or a tool score are not sufficient.

Orientation examples from the normative specification (verify exact wording and exceptions in the criterion itself):

- 2.1.1 Keyboard, Level A: keyboard operation without specific keystroke timing, except when the underlying function depends on the path of the user's movement.
- 2.1.2 No Keyboard Trap, Level A: keyboard focus can be moved away, with instructions if a non-standard method is needed.
- 2.5.7 Dragging Movements, Level AA: a single-pointer alternative exists for functionality using dragging, unless the criterion's exception applies.
- 2.5.8 Target Size (Minimum), Level AA: targets meet 24 by 24 CSS pixels or satisfy the criterion's spacing or other exceptions. This is not a universal ideal target size.
- 3.1.1 Language of Page, Level A: the default human language is programmatically determinable.

Useful informative WAI materials:

- [Understanding WCAG 2.2](https://www.w3.org/WAI/WCAG22/Understanding/intro) explains the principles, guidance layers, and need for human review.
- [WCAG 2 Overview](https://www.w3.org/WAI/standards-guidelines/wcag/) points to standards and supporting resources.
- [WCAG Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/) helps locate criteria and techniques; use the normative spec for conformance claims.
- [Understanding Keyboard](https://www.w3.org/WAI/WCAG22/Understanding/keyboard.html) and [Target Size Minimum](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html) explain selected criteria.

## W3C ARIA Authoring Practices Guide

The [ARIA APG](https://www.w3.org/WAI/ARIA/apg/) gives patterns, semantics, and keyboard interaction guidance for accessible widgets. It is **informative, not normative**, has no conformance model, and examples are illustrative rather than production-ready. It is not a UI design system and is not exhaustive.

- [APG introduction and scope](https://www.w3.org/WAI/ARIA/apg/about/introduction/)
- [APG practices](https://www.w3.org/WAI/ARIA/apg/practices/) including the principle that no ARIA is better than bad ARIA.
- [Names and descriptions](https://www.w3.org/WAI/ARIA/apg/practices/names-and-descriptions/)
- [Keyboard interface](https://www.w3.org/WAI/ARIA/apg/practices/keyboard-interface/)
- [Landmark regions](https://www.w3.org/WAI/ARIA/apg/practices/landmark-regions/)
- [Widget patterns](https://www.w3.org/WAI/ARIA/apg/patterns/)

Prefer native semantic controls. If using a custom pattern, implement its complete keyboard and focus behavior, test the actual browser/assistive-technology combinations, and separately assess applicable WCAG criteria.

## Human-centered service design and research

- [GOV.UK Service Manual](https://www.gov.uk/service-manual/) covers public-service delivery, research, inclusion, content, accessibility, and end-to-end service design. Its [user research guidance](https://www.gov.uk/service-manual/user-research) and [service design introduction](https://www.gov.uk/service-manual/design/introduction-designing-government-services) are useful beyond government, but specific legal/process requirements are UK service-context dependent.
- [Making your service more inclusive](https://www.gov.uk/service-manual/design/making-your-service-more-inclusive) discusses exclusion and inclusive design. [Writing for user interfaces](https://www.gov.uk/service-manual/design/writing-for-user-interfaces) covers clear UI content.
- GOV.UK's [accessibility introduction](https://www.gov.uk/service-manual/helping-people-to-use-your-service/making-your-service-accessible-an-introduction) describes requirements for covered UK government services. Confirm current scope and applicability with qualified specialists.
- The [GOV.UK Design System](https://design-system.service.gov.uk/components/) provides tested components and guidance, but explicitly notes that adopting components does not automatically make a service accessible: [accessibility guidance](https://design-system.service.gov.uk/accessibility/).

## Heuristics and inclusive design methods

- [Nielsen Norman Group's 10 usability heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) are general rules of thumb: status visibility, real-world match, user control, consistency, error prevention, recognition, flexibility, minimalist design, error recovery, and help. They are not a specific checklist, normative accessibility standard, or substitute for user tests.
- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/) provide Apple-platform guidance. The [design principles](https://developer.apple.com/design/human-interface-guidelines/design-principles), [accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility), [layout](https://developer.apple.com/design/human-interface-guidelines/layout), [inclusion](https://developer.apple.com/design/human-interface-guidelines/inclusion), and [writing](https://developer.apple.com/design/human-interface-guidelines/writing) sections are useful examples. Do not describe all HIG recommendations as WCAG criteria.
- [Microsoft Inclusive Design](https://inclusive.microsoft.design/) is a design methodology emphasizing recognition of exclusion, learning from diversity, and solving for one while extending to many. Its [tools and guidance](https://inclusive.microsoft.design/tools-and-guidance) and [examples](https://inclusive.microsoft.design/examples) are methods/examples, not a conformance standard.

## Choosing among conflicting advice

1. Follow applicable law, contract, policy, safety, and normative standards first; verify exact scope.
2. Respect platform conventions where they support the user's task and accessible operation.
3. Use user research and product context to select among valid patterns.
4. Treat heuristics as prompts, not absolute rules. Record the user benefit and tradeoff when deviating.
5. Prefer an accessible, understandable, recoverable experience over visual novelty.
6. Test where evidence is uncertain; do not settle conflicts by personal taste alone.
