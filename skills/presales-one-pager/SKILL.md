---
name: presales-one-pager
description: |
  Generates a polished, branded Technical Pre-Sales One-Pager Website
  from a short brief. The user provides the client, use case, solution
  details, architecture, business value, outcomes, and contributors —
  and Cowork produces a self-contained HTML one-pager ready to share
  with prospects, partners, or internal stakeholders.
  Covers: case studies, solution showcases, proof-of-concept summaries,
  hackathon demos, partner solution stories, and any deliverable that
  tells a "we built this, here's why it matters" story in a single
  scrollable page.
  Use when the user asks to "create a pre-sales one-pager",
  "build a case study website", "generate a solution showcase page",
  "make a one-pager for [project / client / use case]", "create a
  technical pre-sales page for [solution]", or produces any single-page
  deliverable that must follow the org's branding and pre-sales
  structure.
  Always layered on top of presales-brandkit — branding details
  (colours, type, logo, tone, anonymisation) are delegated to that
  skill. This skill never re-defines brand identity.
cowork:
  category: writing
  icon: Globe
  keywords:
    - pre-sales
    - one-pager
    - presales-one-pager
    - case study
    - solution showcase
    - technical one-pager
    - client story
    - proof of concept
    - hackathon demo
    - solution page
    - HTML one-pager
    - architecture overview
    - business value
    - customer story
---

# Technical Pre-Sales One-Pager Generator (presales-one-pager)

A scenario-aware generator that turns a short brief into a finished,
branded, single-page HTML website showcasing a delivered solution.
**Branding is handled by presales-brandkit.** Always invoke
presales-brandkit as the foundational layer. This skill never
re-defines colours, type, logo rules, or tone — it composes inside
them.

## Core Principle

**Brief in, share-ready one-pager out.** The user should only need
to provide the what (use case), the who (client + contributors), and
the so-what (value + outcomes). This skill handles structure, layout,
copy framing, anonymisation, and HTML generation — the user reviews
and ships.

## Scope

The skill is **open-ended on solution types** — any project that
needs a pre-sales story can be turned into a one-pager. The scenario
families below are navigational aids, not a fixed menu.

### Scenario families (navigational, not exhaustive)

| Family                        | Examples (illustrative — extend as needed)                                      |
|-------------------------------|---------------------------------------------------------------------------------|
| **AI & Copilot Solutions**    | Copilot Studio agents, Azure OpenAI apps, AI assistants, intelligent automation |
| **Power Platform Solutions**  | Power Apps, Power Automate flows, Power BI dashboards, Dataverse solutions       |
| **Cloud & Infrastructure**    | Azure migrations, modernisation, hybrid setups, DevOps pipelines                |
| **Data & Analytics**          | Data platforms, lakehouse builds, BI dashboards, ML pipelines                   |
| **Modern Workplace**          | M365 rollouts, Teams integrations, SharePoint intranets, Viva deployments       |
| **Security & Governance**     | Zero Trust implementations, compliance automation, DLP setups                   |
| **Integration & Automation**  | API integrations, RPA, iPaaS, MCP server integrations, connector builds         |
| **Hackathon & PoC Demos**     | Hackathon entries, proof-of-concept showcases, innovation sprint outputs        |
| **Partner & Joint Solutions** | Microsoft co-sell stories, ISV integrations, joint GTM deliverables             |

If the user describes a solution outside these families, adapt the
nearest pattern — never block the work to debate categorisation.

## Required User Inputs

Before generating, collect these from the user. If critical inputs
are missing, batch a single ask — never ask twice.

| Input                 | Required? | Description                                                        |
|-----------------------|-----------|--------------------------------------------------------------------|
| Client Name           | Yes       | Actual client name (will be anonymised if requested)               |
| Anonymise?            | Yes       | Yes / No — whether to mask the client identity                     |
| Industry              | Yes       | Client's industry (e.g., Logistics, Finance, Retail, Healthcare)   |
| Use Case / Project    | Yes       | What was built — short description                                 |
| Solution Overview     | Yes       | What the solution does — 2-3 sentences                             |
| Current Challenges    | Yes       | Pain points the client faced before the solution (minimum 3)       |
| Architecture / Tech   | Yes       | Key technologies, services, frameworks, integration points         |
| Business Value        | Yes       | Quantifiable benefits (time saved, cost reduced, quality improved) |
| Business Outcomes     | Optional  | Measurable post-deployment results                                 |
| Contributors          | Yes       | Names and roles of people who built it                             |
| Timeline              | Optional  | Project duration or delivery phases                                |
| Tags / Keywords       | Optional  | For metadata or internal discovery                                 |

**Use placeholders for non-essential gaps** — [Add deployment date],
[Add exact metric] — don't block the build.

## Brief Intake Protocol

Before generating, run this sequence:

1. **Parse the user's request.** Extract client, use case, solution
   name, industry, anonymisation flag, contributors, and any details
   already provided.
2. **Resolve facts via M365 before asking the user.**
   - **People** (contributors, stakeholders) → search People for
     role, team, office to auto-fill contributor cards.
   - **Project context** → search Files + Emails for proposals,
     architecture docs, SOWs, or prior case studies related to the
     project name or client.
   - **Meetings** → search Meetings for demo walkthroughs, client
     calls, or sprint reviews related to the project.
   - **Prior one-pagers** → check if a one-pager for this client /
     project already exists to avoid duplication and to maintain
     consistency.
3. **Batch a single ask** only for genuinely missing essentials.
   Never interrupt the user multiple times.
4. **Use placeholders** for non-critical gaps — [Add exact ROI
   figure], [Add deployment date] — and flag them in the response.

## One-Pager Section Structure

The HTML one-pager follows this exact section order. Every section
is mandatory unless marked optional.

### Top Navigation Bar (mandatory)
- A **sticky top navigation bar** pinned to the top of the page, visible
  while scrolling, providing **anchor links to every major section**
  below.
- **Left side:** the logo or text wordmark (per presales-brandkit logo
  rules — real asset → `[Add company logo]` placeholder → text wordmark).
- **Right side:** in-page anchor links, one per section, in section
  order — e.g. *Challenge · Solution · Technology · Architecture ·
  Impact · References · Team*. Use the section's short label, not its
  full header.
- **Behaviour:** clicking a link smooth-scrolls to that section. The
  link for the section currently in view is highlighted (active state in
  the Secondary colour). Every nav link must resolve to a real `id` on
  its section — no dead anchors.
- **Styling:** brand colours per presales-brandkit (Primary or White
  background with sufficient contrast); slim, uncluttered; never overlaps
  hero content (hero gets top padding equal to nav height).
- **Responsive:** on narrow viewports the links collapse into a compact
  menu (hamburger or horizontally scrollable row) — no overflow, no
  horizontal page scroll.
- Optional sections (Business Outcomes, References) appear in the nav
  **only when that section is present**.

### Section 1: Hero Banner
- **Solution / project name** — display heading, bold, prominent
- **One-line tagline** summarising the solution's impact in ≤ 12 words
- **Industry badge** (pill/tag) and **client label** (anonymised if
  requested)
- **Background:** brand primary colour or dark background with white
  text
- **Layout:** clean, minimal — name + tagline + badge only. No
  paragraphs in the hero.

### Section 2: Problem Statement / The Challenge
- **Header:** "The Challenge", "Problem Statement", or "Why This Mattered"
- Open with a **1-2 sentence problem statement** framing the situation,
  then present the specific pain points.
- Present **3-5 pain points** the client faced
- **Format:** Icon + short heading + 1-line description per pain point
- **Tone:** Empathetic — show understanding of the client's struggle,
  not judgment
- **Example structure:**
  - ⏱️ **Manual Process Overhead** — Teams spent 10+ hours weekly
    on repetitive sprint planning
  - 🔄 **Inconsistent Outputs** — Lack of standardisation led to
    duplicated work items and missed context
  - 📉 **Delayed Execution** — No real-time bridge between planning
    conversations and engineering tools

### Section 3: Solution Overview
- **Header:** "Solution Overview", "The Solution", or "What We Built"
- **2-3 sentence overview** of the solution — what it does and why
  it matters
- **3-5 key features** presented as cards
- **Each card:** Icon + Feature Name + 1-line description
- Focus on WHAT it does and WHY it matters — not deep implementation
  details
- **Example structure:**
  - 🤖 **AI-Powered Extraction** — Converts unstructured meeting
    notes into structured sprint items automatically
  - 📚 **Knowledge Enrichment** — Enriches every story with
    documentation, acceptance criteria, and implementation guidance
  - 🔗 **Seamless Tool Integration** — Creates execution-ready
    issues directly in the project management tool

### Section 4: Key Technical Details & Technology Stack
- **Header:** "Built With", "Key Technical Details", or "Technology Stack"
- Open with **1-2 sentences** on the technical approach — the core
  pattern that makes the solution work (e.g., "An agentic pipeline
  that turns conversation into execution-ready work items.").
- Display the stack as a **visual grid of cards** — icon/emoji +
  technology name + role in the solution.
- **Group into categories:**
  - **AI & Intelligence** (e.g., Azure OpenAI, Copilot Studio)
  - **Integration & Connectivity** (e.g., MCP Servers, Power
    Automate, APIs, Connectors)
  - **Data & Storage** (e.g., Dataverse, SharePoint, SQL, Cosmos DB)
  - **Frontend / Interface** (e.g., Copilot Chat, Power Pages,
    Teams, Web)
  - **DevOps & Delivery** (e.g., Azure DevOps, Jira, GitHub)
  - **Frameworks & Patterns** (e.g., MCP, Agentic AI, Low-Code /
    Pro-Code Hybrid)
- Keep it visual and scannable — minimal text per card.
- Never list more than 12 items — curate the most important.
- For any technical term, add a one-line plain-language explanation
  so a business reader can follow.

### Section 5: Solution Architecture
- **Header:** "Solution Architecture", "How It Works", or "Architecture Overview"
- Describe **how the components fit together** — the flow of data or
  requests from input to outcome. This is the technical narrative
  that ties the stack from Section 4 into a working system.
- **Preferred format — a labelled flow** rendered in HTML/CSS (no
  external image dependency): a horizontal or vertical sequence of
  **stages** (boxes/cards connected by arrows or connectors), each
  stage a short label + 1-line description. Example flow:
  *Input / Trigger → Processing / AI Layer → Integration / Orchestration
  → Data / Storage → Output / Interface.*
- If the user supplies an **architecture diagram image**, embed it
  responsively (with descriptive alt-text per presales-brandkit
  accessibility rules). If none is supplied, build the CSS flow above
  — never fabricate or download a diagram.
- Optionally follow the flow with a short **numbered walkthrough**
  (3-6 steps) explaining each stage in one line.
- Keep it scannable: the reader should grasp the architecture in
  under 30 seconds. Detail lives in the walkthrough, not the diagram.
- Use brand colours per presales-brandkit for stage boxes and
  connectors — Primary/Secondary for boxes, Accent for connectors.

### Section 6: Business Value & Impact
- **Header:** "The Impact" or "Value Delivered"
- Present as **metric cards** — big number + label + 1-line context
- **Minimum 3 metrics, ideally 4-5**
- Use the Success/Value colour (#107C10) for metric numbers
- **Example structure:**
  - **70%** — Reduction in manual planning effort
  - **3x** — Faster sprint turnaround
  - **100%** — Documentation consistency across stories
  - **0** — Manual errors in task creation
- If exact numbers aren't available, use directional metrics
  ("Significant reduction in…", "Measurable improvement in…")
  and flag as a placeholder

### Section 7: Business Outcomes (Optional)
- **Header:** "Outcomes & What's Next"
- **2-3 sentences** on post-deployment results and adoption
- Include any **future roadmap** or expansion plans if available
- **Tone:** Forward-looking, confident, grounded in results

### Section 8: References (Optional)
- **Header:** "References" or "Proof Points"
- Include this section **only when reference material exists** — a
  client testimonial quote, a linked case study, a demo recording, a
  supporting document, or a named reference contact's *role* (never
  personal contact details).
- **Format options:**
  - **Testimonial** — a short pull-quote (≤ 40 words) + attribution by
    role and organisation type (anonymised if requested), styled as a
    callout panel in the Accent tint.
  - **Linked artefacts** — a tidy list of related materials (case
    study, architecture doc, demo) as labelled items. Only include a
    URL if the user supplies it verbatim — never fabricate links.
- If no reference material exists, **omit the section entirely** and
  drop its nav link — do not leave an empty shell.
- **No personal contact details** — no emails, phone numbers, or
  social links, consistent with the contributor and footer rules.

### Section 9: Contributors
- **Header:** "The Team Behind This"
- Display as a **card grid:** Initials Avatar (brand-primary circle)
  + Full Name + Role
- **No email addresses, phone numbers, social links, or employee IDs**
- Clean, minimal design — initials as avatar placeholders
- Order: as specified by user, or alphabetical by first name

### Section 10: Footer
- Company name + tagline
- Year + "Confidential — For Pre-Sales Use Only"
- **No external URLs, no social links, no email addresses**

## Output Format

- Generate as a **single self-contained HTML file** with all CSS
  inlined (no external stylesheets, no CDN dependencies).
- **Must follow all branding** from presales-brandkit — colours,
  typography, logo, tone, layout principles.
- **Responsive-friendly** layout using CSS flexbox / grid.
- Clean, modern, professional aesthetic — generous whitespace.
- File naming: `[SolutionName]-OnePager.html`
- Save to the user's OneDrive.

## Content Rules

- Write in **third person** ("The team delivered…" not "We
  delivered…") unless the user explicitly requests first person.
- Keep each section **concise** — this is a ONE-PAGER, not a
  whitepaper. Every sentence must earn its place.
- **No jargon without context** — assume the reader is a business
  stakeholder who may not know the tech. One line of plain
  explanation per technical term.
- Every claim should be **backed by a metric or outcome** where
  possible. Unsubstantiated claims ("dramatically improved") are
  not allowed — use a number or use a placeholder.
- **Anonymisation must be consistent** — if anonymised, the actual
  client name must not appear anywhere: title, body, footer,
  alt-text, file name, HTML comments, metadata.
- **No fabricated facts.** If a metric, date, or detail is unknown,
  insert a clearly-marked placeholder: [Add exact ROI], [Confirm
  deployment date]. Never invent numbers.

## Composition Patterns

Four reusable page styles. Pick one based on the solution type;
**vary across a series** if generating multiple one-pagers.

- **A. Metric-Led** — Hero opens with the biggest impact number
  (e.g., "70% faster"). Best for solutions with strong quantifiable
  outcomes.
- **B. Story-Led** — Hero opens with the client's pain point as a
  narrative hook (e.g., "Every sprint started with 3 hours of
  manual work."). Best for solutions where the before/after
  contrast is compelling.
- **C. Tech-Led** — Hero opens with the architecture visual or
  tech stack highlight (e.g., "Copilot Studio + MCP + Jira").
  Best for technically impressive solutions targeting technical
  audiences.
- **D. Outcome-Led** — Hero opens with the business outcome
  (e.g., "From planning to execution in one conversation.").
  Best for solutions targeting C-level or business stakeholders.

## Pre-Delivery Validation

Run before announcing the one-pager is ready:

- [ ] **Run presales-brandkit Validation Checklist** — all items
      must pass.
- [ ] **Section completeness** — all mandatory sections present and
      populated: Hero, Challenge, Solution Overview, Key Technical
      Details & Tech Stack, Solution Architecture, Business Value &
      Impact, Contributors, Footer. Optional sections (Business
      Outcomes, References) included only if data exists.
- [ ] **Navigation bar** — sticky top nav present; one anchor link
      per visible section, in section order; every link resolves to a
      real `id` (no dead anchors); active-section highlight works;
      collapses cleanly on narrow viewports; optional-section links
      appear only when that section is rendered.
- [ ] **Architecture check** — Solution Architecture section renders
      a labelled flow (CSS) or an embedded supplied diagram with
      alt-text; no fabricated or downloaded diagram.
- [ ] **Metric check** — minimum 3 metrics in the Value section.
      Placeholders flagged.
- [ ] **Anonymisation check** (if requested) — client name absent
      from every location including HTML comments and file name.
- [ ] **Contributor check** — no email addresses, phone numbers, or
      social links exposed.
- [ ] **Content check** — no fabricated facts, no banned phrases,
      no unsubstantiated claims.
- [ ] **HTML check** — self-contained, no external dependencies,
      renders correctly in a browser.
- [ ] **File saved** — to OneDrive with correct naming convention.
- [ ] **Placeholder list** — any unfilled placeholders listed in
      the response so the user can fill them.

## Response Format to the User

Every successful generation reports back, in plain language:

- **What was created** — the solution name and that the one-pager is ready.
- **Where it was saved** — the file name and OneDrive location.
- **Composition pattern used** — which of the four styles (Metric-Led,
  Story-Led, Tech-Led, Outcome-Led) was applied and why.
- **Anonymisation status** — whether the client identity was masked.
- **Placeholders to fill** — a bulleted list of any [Add …] markers
  left in the page so the user knows exactly what to complete.
- **Next step** — a short prompt offering to adjust sections, swap the
  composition pattern, or generate a PDF version.
