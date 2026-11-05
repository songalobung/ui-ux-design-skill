# Human-centered design process

This guide helps an assistant make design decisions from user evidence rather than taste alone. Use the depth proportionate to the task. A small component change may need a quick context check and state review; a new service or high-impact flow usually needs discovery, prototyping, and evaluation.

## Frame the problem before the screen

Write the task as a user outcome, not a feature request. “Help a resident renew a permit without losing their saved information” is a useful outcome; “add a wizard” is an implementation proposal. Identify:

- Who needs to act, and what task or decision are they trying to complete?
- What triggers the task, what do they know already, and what information or evidence do they need?
- Where, when, and with what device, input method, network, language, privacy, time, or support constraints will they use the service?
- What is at stake if the flow is confusing, delayed, inaccessible, or wrong?
- What must the service do, what is outside scope, and what evidence supports those assumptions?

Separate fact, interpretation, hypothesis, and decision. If the evidence is weak, make uncertainty explicit and design a cheap way to learn. Do not invent a persona biography or research result to make a design sound grounded. Use task/context descriptions or evidence-backed archetypes, not stereotypes.

## Choose research that answers the decision

Start with what is already known: prior studies, support contacts, search logs, analytics, complaints, operational policies, accessibility findings, and field staff insight. Check the recency, source, coverage, and limitations before using it. Quantitative data can reveal where people stop or struggle, but rarely explains why. Interviews and observation explain context and reasoning, but small samples do not establish population prevalence.

Use proportionate methods:

- **Interview:** learn goals, language, constraints, and reasoning. Ask about recent specific behavior rather than hypothetical preference.
- **Contextual observation:** see the real environment, interruptions, tools, workarounds, and social context.
- **Task analysis:** break an activity into goals, decisions, inputs, feedback, and failure paths.
- **Journey map/service blueprint:** show the end-to-end experience, channels, backstage dependencies, handoffs, waiting, and help.
- **Prototype evaluation:** test whether a person can understand and complete a realistic task with a proposed flow.
- **Heuristic/accessibility review:** identify probable issues efficiently; treat findings as hypotheses until checked where needed.
- **Analytics/support review:** locate friction and outcomes; protect privacy and avoid overinterpreting correlation.

Do not ask a method to answer what it cannot: a preference survey is not a substitute for observing task performance; a prototype test is not a reliable estimate of population conversion.

## Recruit and conduct research respectfully

Recruit participants based on relevant tasks, contexts, and barriers. Include disabled people and people using assistive technology when the experience could affect them; include variation in age, language, literacy, device, connectivity, confidence, and environment when relevant. Do not treat one person as a representative of everyone with a diagnosis or identity.

Explain purpose, activities, recording, data use, retention, and withdrawal options in accessible language. Obtain appropriate consent. Offer reasonable accommodations and accessible study materials; do not make a participant disclose more than needed. Avoid collecting sensitive information unless essential and properly protected. In sessions, allow time, do not coach users to a preferred answer, and distinguish facilitator-induced confusion from interface confusion.

Ask neutral prompts: “What would you do next?” “What do you expect this label to mean?” “Tell me about the last time you did this.” Avoid leading prompts such as “Was this easy?” or “Would you use this feature?” Watch actions, hesitations, re-reading, navigation, errors, confidence, and workarounds. Ask about intent after observing behavior.

## Map journeys and expose service gaps

Map the user's path from trigger through completion and what happens afterward. Include:

1. Entry point and eligibility/prerequisites.
2. User questions and decisions at each step.
3. Information or evidence needed and how it is obtained.
4. System response, waiting, status, and next action.
5. Errors, interruptions, abandon/restart, correction, and return paths.
6. Offline, phone, human-support, or other channel dependencies.
7. Privacy, trust, accessibility, and emotional concerns.

Mark duplicate entry, unjustified steps, jargon, hidden requirements, missing confirmation, dead ends, delayed status, inaccessible evidence demands, and moments when a human should help. Optimize the whole service, not just the polished front end. Remove unnecessary steps, but do not collapse steps if that hides consequences or deprives people of needed context.

## Structure information around user questions

For each page or view, answer: What is this? Is it for me? What do I need before proceeding? What can I do here? What happens next? How do I get help or recover? Put key information at the point of decision. Use meaningful headings, descriptive links, predictable groupings, and navigation that matches the user's mental model. Keep names stable across menus, pages, and help content.

Use progressive disclosure for secondary complexity, not for fees, eligibility, risks, privacy consequences, or other information users need to make an informed decision. Ensure hidden content is discoverable and operable by keyboard and assistive technology.

## Prioritize with a visible rationale

Compare opportunities by:

- Severity of harm or task failure.
- Number and diversity of affected users, with attention to excluded groups.
- Task frequency and importance, not frequency alone.
- User effort, time, uncertainty, and repeated work.
- Accessibility, safety, legal, privacy, and trust risk.
- Evidence confidence and cost of learning.
- Feasibility, maintenance cost, and dependencies.

Do not let an average score hide severe barriers for a smaller group. Rank critical accessibility, safety, and compliance blockers as release risks, not cosmetic polish. Record tradeoffs and who might bear them.

## Define researchable success

Choose observable outcomes tied to the user task, such as: correctly finding an answer; completing a flow without facilitator help; recovering from a recoverable error; understanding a fee before paying; or correctly identifying the saved/completed state. Capture task success, critical errors, time only where meaningful, confidence, comprehension, and qualitative observations. Avoid optimizing a single proxy (e.g., clicks or conversion) when it could reward pressure, dark patterns, or exclusion.

Set a baseline when available. State the sample, task conditions, device, assistive technology, and measurement limits. Do not claim that a redesign caused a metric change without a suitable evaluation design and accounting for other factors.

## Run a practical usability session

Prepare a realistic scenario with a clear goal, not a click-by-click script. Use realistic but safe data. Confirm consent, device and input method, assistive technology needs, and recording preferences. Ask participants to think aloud if comfortable, but do not confuse narration skill with ability. Let them try before intervening.

Observe whether participants:

- Recognize the page and task.
- Know what information they need and where to find it.
- Understand labels, options, consequences, and feedback.
- Complete the primary task and interpret the result correctly.
- Notice and recover from errors or interruptions.
- Operate controls with their actual input method.
- Feel in control and understand data/privacy implications.

Record evidence without turning every comment into a design request. A participant's proposed fix is one clue; diagnose the underlying issue. Summarize: observation, evidence, impact, affected context, confidence, recommendation, and open question. Fix severe blockers first, then retest the changed behavior.

## Close the loop

Share findings in a useful form with designers, engineers, content authors, support, and decision makers. Preserve dissent and uncertainty. After release, monitor support issues, task outcomes, accessibility feedback, and unintended consequences. Provide a way to report barriers and a process to act on them. Treat design as ongoing service improvement, not a one-time handoff.

## Useful source guidance

The [GOV.UK Service Manual](https://www.gov.uk/service-manual/user-research) provides practical user-research guidance and [service design principles](https://www.gov.uk/service-manual/design/introduction-designing-government-services). [Microsoft Inclusive Design](https://inclusive.microsoft.design/) offers a methodology for recognizing exclusion and learning from diversity. The [NN/g usability heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) are review heuristics, not user research or compliance criteria. See `standards-and-sources.md` for source scope and cautions.
