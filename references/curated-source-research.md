# Curated UI/UX Source Research

This note synthesizes verified source inspections for the UI/UX design skill. It is a research aid, not a new standard or a substitute for current platform documentation, accessibility standards, or product-specific user research.

## Integration principle

Use sources according to their evidence and authority: official Apple/Meta materials for their own platforms; practical commercial guides as nonbinding heuristics; and academic or secondary-hosted material only within the scope actually verified. Translate transferable ideas into review questions, not universal rules. Validate choices against the target users, task, accessibility needs, platform, and observed usability. The reviewed material does not establish causal or universal usability outcomes.

## Official Apple and Meta product/platform guidance

### Apple — official platform resources

**[1] Design — Apple Developer** — *Official platform design-resource landing page.* The hub directs designers to Apple’s Human Interface Guidelines, assets, symbols, icon tooling, videos, and learning pathway. Treat it as a pointer to authoritative Apple-specific references, not as the detailed rules or evidence itself. The page showed no individual author or date; the linked materials were not assessed as part of this page. [1]

**[2] Human Interface Guidelines** — *Official platform guidance.* Transferable review prompts include begin with user goals, preserve user control and recovery, use consistent familiar patterns and clear feedback, design inclusively for varied needs and input methods, and be transparent about permissions and data. Apple explicitly frames principles as decision tools rather than one prescribed solution. This is vendor guidance, not empirical proof; platform conventions apply to Apple targets. [2]

**[3] Design principles** — *Official Apple Human Interface Guidelines.* Useful prompts: prioritize the product value and users’ important tasks; make mistakes recoverable; explain behavior and data practices; provide consistent patterns and feedback; account for accessibility, diverse input, and platform context; remove elements that do not serve goals. These are normative recommendations, not tested universal effects. [3]

**[4] App design and UI** — *Official Apple developer technology overview.* Apple advises considering platform-standard and custom views, accessibility and internationalization, platform-specific interaction/layout contexts, and testing across relevant Apple devices. Its SwiftUI recommendation for new Apple apps is framework advice specific to Apple development, not a general UX rule. The page is an overview, not a study or complete specification. [4]

### Meta — official product/design resource index

**[5] Resources to help with the design process** — *Official Meta resource directory.* For immersive Meta work, consult the separately linked Horizon OS human-interface guidance; use mockups and prototyping/animation to explore interaction; consider sound where relevant; and use the separate brand resource for Meta identity. This index is not itself a cross-platform standard or evidence. Linked destinations were not evaluated in depth. The page describes its sound collection as globally rights-cleared; do not extend that claim to other listed assets. No author/date was displayed. [5]

## Commercial and authored design advice

**[6] UI Design Principles: Learn to create beautiful and usable interfaces from scratch** — *Commercial instructional eBook; authored by Michael Filipiuk, hosted by a secondary ebook site.* Selectively useful visual heuristics: establish hierarchy, use consistent grid/spacing and type systems, keep typography legible, assign semantic status colors, and avoid impractical concepts. The author’s mobile-grid and 4-point spacing suggestions are starting points, not standards. This 323-page PDF was directly inspected; it is instructional, not empirical, and says it focuses on visual UI rather than UX methodology. Cover names the author; no publisher/date was identified. The hosting domain is not shown as publisher, the PDF’s modification metadata is not publication-date evidence, and copy authorization/license was not established. Paraphrase only; do not treat the guide as platform authority. [6]

**[7] Practical UI: Quick and practical UI design guidelines to design intuitive, accessible, and beautiful interfaces (Free preview)** — *Commercial book preview by Adham Dannaway, published/promoted by Practical UI.* The preview suggests reducing avoidable task effort, making relationships legible through proximity/alignment/consistency, distinguishing unlike controls, and using line length as a responsive readability consideration (the publisher gives 40–80 characters as a guideline). Treat examples and numeric advice as hypotheses to test, not universal requirements. The supplied PDF and publisher page were inspected; preview says it samples three of 100+ guidelines. It is not empirical research or a platform/accessibility standard. PDF says “All rights reserved”; no reuse license was established, so paraphrase and link. Date absent in inspected PDF/page; an indexed date was not verified from the document. [7]

**[8] The Best Practices and Key Principles of UX Design** — *Baymard commercial secondary guidance, by Christian Holst; ecommerce-oriented.* Useful checklist prompts include consistency, navigable wayfinding, task-focused forms, accessibility/mobile considerations, and iterative testing. Examples primarily concern ecommerce browsing, product lists, search, and checkout; adapt rather than generalize. The article reports Baymard research activity and figures, but this overview does not provide per-finding methods, recruitment, dates, or uncertainty; treat reported figures as the publisher’s claims, not independently verified evidence. Page was inspected directly; no reuse terms were established. [8]

## Academic/empirical sources and scholarly overviews

**[9] A Study on User Interface and User Experience Designs and its Tools** — *WJRR narrative review/overview (2021), by Vatsal Sharma and Ankit Kumar Tiwari.* Offers basic background: distinguish task interaction from visual interface, consider the full journey and outcome, and use user feedback to identify problems. It reports no participants, measurements, experiments, or systematic review protocol, so it is not empirical evidence or a validated standard; its tool discussion is dated. Journal landing page and PDF were inspected. Landing page gives pages 41–43 while PDF says 41–44. No specific reuse license was visible; paraphrase. Use only as optional background. [9]

## Secondary-hosted or access-limited documents

**[10] User Interface and User Experience (UI/UX) Design** — *Secondary-hosted Academia.edu 12-page instructional/reference document; uploader shown as “khabar laila,” not verified as author.* Accessible abstract/outline supports a limited checklist: distinguish interface controls from the broader interaction experience; diagnose breakdowns by interaction stage; make actions discoverable and outcomes legible through affordance and feedback; ensure operations/input modes fit tasks. The visible record frames the work around cartography/visualization and supplies no study method or outcomes. Full PDF was gated by a sign-up/login prompt, so authorship, full text, references, and date could not be checked. DOI is displayed, but its landing page was not verified as a canonical author/publisher source. Do not cite as empirical, normative, or fully inspected. [10]

**[6]** above is also secondary-hosted; provenance and licensing caveats apply. The Practical UI preview [7] is a publisher-provided preview, not a full book.

## Unverified / failed access

**E-Commerce UI/UX Outline (title inferred from filename; contents unverified).** The supplied PIKOM URL did not return a valid PDF: retrieval yielded HTML/malformed input and extraction returned no document content. The filename and host do not establish title, author, date, content, or license. No takeaways are attributed to it and it should not inform the skill unless an inspectable copy is obtained. [11]

## Best fit with the existing skill

- **Design philosophy and human-centered process:** Use Apple HIG principles [2,3] as supplementary prompts for goals, agency, recovery, privacy, and inclusion alongside `design-philosophy.md` and `human-centered-process.md`. Keep the skill’s own evidence discipline: these principles are guidance, not outcome data.
- **Visual craft, layout, typography, and color:** Filipiuk [6] and Practical UI [7] can supplement `visual-design-systems.md`, `layout-patterns.md`, `typography.md`, and `color-theory.md` with clearly labeled heuristics. Avoid importing their suggested measurements as standards.
- **Ecommerce UX patterns:** Baymard [8] fits `ux-patterns.md` and `interaction-patterns.md` as a domain-specific checklist, particularly forms, navigation, browsing, and checkout. Preserve the ecommerce scope and test against the actual product.
- **Platform guidelines:** Add Apple hub/HIG/app-design links [1–4] and Meta index [5] to `platform-guidelines.md` or `standards-and-sources.md` under vendor-specific guidance. Follow linked primary documentation for detailed or changing requirements; never generalize vendor conventions to all platforms.
- **Accessibility:** The sources provide only high-level reminders. Keep normative requirements and conformance claims in `accessibility-inclusive-design.md`, `accessibility.md`, and `standards-and-sources.md`; none of these sources substitutes for applicable standards or assistive-technology/user evaluation.
- **Interaction concepts / background:** Academia.edu record [10] and WJRR overview [9] may be optional reading for `interaction-patterns.md` or `knowledge-library.md`, with their access/evidence limitations visible.
- **New files/sections:** No new core guidance file is justified by this research. This curated note is suitable as a provenance-aware source register. If integrated, add a short cross-reference in the existing `standards-and-sources.md` or `knowledge-library.md`; do not create a new normative checklist. Do not incorporate the failed PIKOM source.

## References

[1]: https://developer.apple.com/design/ "Design — Apple Developer"
[2]: https://developer.apple.com/design/human-interface-guidelines "Human Interface Guidelines"
[3]: https://developer.apple.com/design/human-interface-guidelines/design-principles "Design principles"
[4]: https://developer.apple.com/documentation/technologyoverviews/app-design-and-ui "App design and UI"
[5]: https://www.meta.com/design-at-meta/tools/ "Resources to help with the design process"
[6]: https://ebooks.karbust.me/Technology/UI%20Design%20Principles%20-%20Michael%20Filipiuk.pdf "UI Design Principles: Learn to create beautiful and usable interfaces from scratch"
[7]: https://www.practical-ui.com/practical-ui-preview.pdf "Practical UI free preview"
[8]: https://baymard.com/blog/ux-design-principles "The Best Practices and Key Principles of UX Design"
[9]: https://www.wjrr.org/a-study-on-user-interface-and-user-experience-designs-and-its-tools "A Study on User Interface and User Experience Designs and its Tools"
[10]: https://www.academia.edu/44315428/User_Interface_and_User_Experience_UI_UX_Design "User Interface and User Experience (UI/UX) Design"
[11]: https://pikom.org.my/wp-content/uploads/2021/04/E-Commerce-UI_UX-Outline.pdf "E-Commerce UI/UX Outline (unverified; supplied URL)"
