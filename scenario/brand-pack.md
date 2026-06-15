# YAT College — Brand Pack

**Document type:** Brand identity spec for the YAT scenario. Informs the mock website, in-scenario document templates (.docx / .pptx letterhead, deck masters), and the voice/tone of YAT-authored scenario content.

**Status:** v1.0 — approved by Tim 2026-05-26. Direction, palette, typography, logo direction, imagery direction, and disclosure-banner treatment are locked. Outstanding items (accessibility audit on final hex shades, logo sketch round, photography sourcing call) are tracked in §6 as operational follow-ups rather than open design questions.

**Companion artefacts:**
- `scenario/branding/assets/` — logos, favicons, photography references (to be authored once direction is approved)
- `scenario/website.md` — mock website spec, consumes this brand pack
- Document templates under `templates/` and `scenario/templates/` — will be restyled to match once brand is locked

---

## 1. Brand essence

> **YAT College — practical training for the next step in your working life.**

YAT is a single-campus private RTO that exists to move adult learners into employment. It is not a research institution, not a prestige play, and not a youth-focused academy. It is a credible, warm, outcomes-focused place where someone who has been working in one field for a decade can walk in and get the credential they need to move to the next field — without being patronised, and without academic ceremony.

## 2. Target audience

**Primary:** Adult career changers, 25–40, who already have work experience but need a credential (or different credential) to move sideways or upwards in their working life. They are pragmatic, time-constrained, often balancing study with paid work and family, and weighing this decision against opportunity cost.

What they care about (in order):
1. Will I get a job at the end of this — and which ones?
2. How long will it take, and can I fit it around work?
3. Is this credential recognised by employers?
4. What does it cost, and is there funding I qualify for?
5. Will the teaching meet me where I am (some prior knowledge, rusty study habits)?

What they don't care about: campus prestige, student-experience marketing, "the journey", glossy aspirational language.

**Secondary:** Recent school-leavers (17–22) exploring vocational pathways as an alternative to university. They benefit from the same direct outcomes-focused voice; the brand should not pivot tone when speaking to them.

**Tertiary:** Employers and industry partners who recognise YAT credentials as a hiring signal.

## 3. Brand personality + voice

### 3.1 Personality

Five adjectives YAT *is*:

- **Practical** — concrete outcomes, real classrooms, real placements
- **Inclusive** — meets learners where they are, no academic gatekeeping
- **Direct** — short sentences, plain words, no jargon-as-status-display
- **Warm** — adult-to-adult tone, not corporate-to-customer
- **Credentialed** — properly registered, properly mapped to industry standards

Five adjectives YAT *is not*:

- ~~Aspirational~~ (no "unlock your potential")
- ~~Elite~~ (no "join an exceptional cohort")
- ~~Casual / cute~~ (no playful illustrations, no emoji in formal copy, no first-name-only authority)
- ~~Academic~~ (no "scholarly community", no Latin mottos)
- ~~Hard-sell~~ (no countdown banners, no "limited places")

### 3.2 Voice

**Plain English, second person, active voice.** Audience often hasn't been in formal study for years; cognitive load on copy should be near zero.

**Examples of YAT voice vs. not-YAT voice:**

| Not-YAT (corporate edu) | YAT voice |
|---|---|
| *"Embark on a transformative learning journey."* | *"Get the qualification. Get the job."* |
| *"Our exceptional educators will unlock your potential."* | *"Our teachers have worked in industry. They'll show you what the work actually looks like."* |
| *"Join a vibrant community of passionate learners."* | *"Most of your classmates are also working adults. You'll have things in common."* |
| *"Limited spots available — apply today!"* | *"Intakes start in February and July. Applications close one month before each."* |

**Acknowledge the audience reality** without making a fuss of it:
- *"You've worked. You've changed your mind. We can help you change your direction."*
- *"Coming back to study after a long break is normal here. Most of our students have done exactly that."*

**Outcomes over abstractions.** Every course page should answer "what job does this lead to" near the top, before the unit list, with concrete role titles + employer types.

**Inclusive without performing inclusion.** Photography and language should reflect the actual learner mix (age, ethnicity, gender, ability). Don't write an "inclusion statement"; show it.

## 4. Visual identity

### 4.1 Colour palette

**Anchor decision:** YAT's palette is built to be visibly *not* the Australian VET-website default of "deep navy + accent". The navy crowd includes Holmesglen, Chisholm, Angliss, and many others; we want YAT to look immediately distinguishable on a screenshot.

It also explicitly avoids:
- **Maroon / brick red** (reads as Kangan)
- **Mid-blue / teal-blue** (reads as BKI)
- **Burgundy / wine** (reads as Angliss)

Proposed palette — *warm earth* (a teal-green primary balanced with terracotta + cream):

| Role | Name | Hex | Notes |
|---|---|---|---|
| Primary | Deep Teal-Green | `#1F5A5C` | Headers, primary navigation, logo. Calm, credible, distinctly not navy. |
| Accent | Terracotta | `#C5613B` | Call-to-action buttons, links, key emphasis. Warm earthy, signals inclusivity without saccharine. |
| Highlight | Muted Ochre | `#C99932` | Sparingly — pull-quotes, callouts, the disclosure banner background (see §5.3). |
| Background | Warm Cream | `#F8F4ED` | Primary page background. Softer than pure white, less clinical. |
| Surface | Off-white | `#FDFCF9` | Cards, panels, raised content. |
| Text | Charcoal | `#1F2329` | Body copy. High-contrast against cream + off-white. |
| Muted text | Warm Grey | `#6B6660` | Captions, meta, secondary copy. |
| Border / divider | Soft Stone | `#E4DED3` | 1px rules, table borders, subtle separators. |

**Accessibility check (operational follow-up):** All combinations should meet **WCAG AA contrast (4.5:1 for body)** at least, **AAA (7:1)** where practical. Terracotta on cream needs verification at small sizes; expect to darken the terracotta one or two steps for body link colour vs. button background. Audit before site launch — tracked in §6.

**Intranet variant:** Same palette, but cream replaced by neutral very-light-grey (`#F4F4F2`) and primary teal-green saturation slightly desaturated, to give the intranet a more utility-tool / SharePoint-adjacent feel without feeling like a different brand. Reinforces the public-to-intranet shift through the SSO gate.

### 4.2 Typography

**Single-family humanist sans-serif** — warm, very readable, free/open licence, broadly supported.

Proposed: **Source Sans 3** (Adobe, OFL licensed, on Google Fonts) used across all contexts. Why:
- Humanist proportions read warmer than geometric sans (Inter, Helvetica)
- Very high legibility at small sizes (important for adult audience with potentially weaker near-vision)
- Mature, considered — not trendy, won't date
- Free to use anywhere (website + .docx templates + .pptx decks)

| Use | Family | Weight | Size guide |
|---|---|---|---|
| Display headings (H1) | Source Sans 3 | 800 ExtraBold | 40–56 px |
| Section headings (H2) | Source Sans 3 | 700 Bold | 28–36 px |
| Sub-headings (H3) | Source Sans 3 | 600 SemiBold | 20–24 px |
| Body | Source Sans 3 | 400 Regular | 17–18 px |
| Emphasis / UI labels | Source Sans 3 | 500 Medium | inherit |
| Captions / meta | Source Sans 3 | 400 Regular | 14 px |

**Optional secondary** (use sparingly, for pull-quotes or editorial emphasis on the homepage hero): **Source Serif 4** italic. Designed by the same team to harmonise with Source Sans 3.

**Monospace for technical content** (intranet wiki code blocks, IT documentation, the ICT environment overview pages): **JetBrains Mono** or **Inconsolata**.

### 4.3 Logo

**Direction:**

- **Wordmark-led** — "YAT" as a confident monogram in primary teal-green, with "COLLEGE" as a smaller secondary lockup beneath or to the right
- One letterform carries subtle personality — the specific letterform treatment (slightly opened counter, custom terminal, connecting ligature, etc.) to be explored in a sketch round before vector mark is finalised
- Full-name lockup ("YAT College") for primary application; monogram-only ("YAT") for favicon + small contexts
- **No crest, no shield** (reads traditional/academic, wrong for community-RTO)
- **No swoosh, no abstract motion mark** (reads corporate, wrong for warm-inclusive)
- **No book/graduation-cap/lightbulb iconography** (reads cliché-education)

**Variants to produce:**
1. Primary lockup — colour, on cream/light background
2. Reversed lockup — cream/off-white, on teal-green dark background
3. Single-colour black — for fax-quality print + documents that may be photocopied
4. Single-colour white — for dark-photo overlays
5. Monogram only — favicon, app icon, social avatar
6. Wordmark + tagline (optional, sparingly used) — for the rare context that needs the positioning statement

**Favicon:** monogram only, on a flat teal-green background. Recognisable at 16×16 px.

### 4.4 Iconography

**Style:** simple line icons, 1.5–2 px stroke, rounded line caps and joins (matches the humanist sans-serif warmth). Single weight. Use only when an icon adds clarity — never as decoration.

**Library suggestion:** [Phosphor Icons](https://phosphoricons.com/) (regular weight) or [Tabler Icons](https://tabler.io/icons). Both are free, broad coverage, internally consistent.

**Do not use:** filled-glyph icons (read corporate), illustrated/cartoon icons (read childish), emoji as icons (read informal).

### 4.5 Imagery

**Photography direction:**

- **Documentary, not lifestyle.** Real students in real classrooms / workshops / placements, not models in staged "study" tableaux.
- **Visibly adult learners.** Cohort photos should show a clear majority of 25–40 year olds. School-leavers can appear but should not dominate. Career-changer audience needs to see themselves.
- **Genuine diversity** — age, ethnicity, gender, ability — represented in hero imagery proportionally to the actual learner mix.
- **Hands-on contexts.** Practical settings (workshop benches, hospital sim rooms, server racks, hospitality kitchens), not lecture halls or library shots.
- **Natural light, slightly warm white balance** to align with the cream + terracotta palette. Avoid blue-cool tints.
- **Real environments only.** Photography is briefed onto YAT's Cremorne campus + partner placement sites — not stock-photo classrooms that could be anywhere.

**Illustration:**

- Used sparingly, only where photography can't tell the story (process diagrams, abstract concepts).
- Match the line-icon weight + style — same stroke width, same warmth.
- Avoid character illustration (cartoon people), 3D renders, or hand-drawn-looking marks.

**Stock photo guidance:** treat as a last resort for v1 site launch only; replace with bespoke campus photography in v2. Stock images carry strong "we couldn't be bothered" signal that undermines the brand.

## 5. Application

### 5.1 Public site vs. intranet — distinct expressions, single identity

YAT's brand has one identity across both contexts, but expresses with different *density* and *temperature*:

| | Public site | Intranet |
|---|---|---|
| Primary purpose | Persuade prospective students; explain offerings | Operational reference for staff (in-scenario) |
| Layout | Spacious, generous whitespace, hero-led | Denser, more functional, SharePoint/Confluence-adjacent |
| Background | Warm Cream (`#F8F4ED`) | Neutral light-grey (`#F4F4F2`) |
| Imagery | Documentary photography, large hero shots | Sparse — mostly diagrams + screenshots; photography only where relevant (e.g. people pages, building info) |
| Voice | Marketing-adjacent, slightly aspirational ceiling | Procedural, instructional, no marketing voice |
| Navigation | Marketing IA (Courses, About, Locations, Apply) | Functional IA (ICT, Policies, Project, Reference, Templates) per `scenario/website.md` §2 |

The shift through the SSO gate (`scenario/website.md` §3) is the moment the visual register changes. Same logo, same palette, same type — but more density, less hero copy, more tables and lists.

### 5.2 Document templates

In-scenario documents (policies, role briefs, meeting notes, deployment reports etc.) and the assessment delivery templates students receive should both carry YAT identity in a restrained way:

- **Letterhead:** YAT lockup top-left, address block top-right, thin teal-green rule across the page below
- **Type:** Source Sans 3 (or fallback to Calibri / Arial where Word users won't have Source Sans loaded — embed in template where possible)
- **Heading colour:** Deep teal-green for H1/H2; charcoal for body
- **Footer:** YAT lockup small + page number + simulated-environment disclosure (see §5.3) on every page
- **Tables:** thin Soft Stone (`#E4DED3`) 1px borders; header row in muted teal background with white text
- **Templates affected:** all `.docx` and `.pptx` deliverables in `templates/` and `scenario/templates/` — see existing checklists for the full inventory

### 5.3 Site-wide simulated-environment disclosure banner

**Hard constraint:** every page of both public site and intranet carries a thin top-strip banner declaring this is a fictional organisation used as a case study in an educational context.

**Specification:**

- **Position:** the very top of every page, above the masthead / main navigation, on every public page, every intranet page, and the SSO sign-in page
- **Height:** ~0.5–0.75 cm rendered (≈ 24–30 px at standard zoom)
- **Background:** Muted Ochre (`#C99932`) — distinct from the cream page background, clearly chrome rather than content; consistent across public + intranet so the banner reads as cross-cutting site infrastructure
- **Text colour:** Charcoal (`#1F2329`) for AA contrast against ochre
- **Type:** Source Sans 3, 13–14 px, Medium weight (500), small-caps optional
- **Alignment:** centred horizontally
- **Copy (proposed):** *"This is a fictional organisation used as a case study in an educational context."*
- **Behaviour:** **persistent and non-dismissable**. Reason: a dismissed banner defeats the disclosure purpose; students share screenshots and the disclosure should travel with them.
- **Print stylesheet:** banner must also appear on the printed version of any intranet page that could plausibly be printed (procedures, policies, role briefs)
- **Document templates equivalent:** in `.docx` and `.pptx` artefacts, the same disclosure appears in the page header (Word) or master slide footer (PowerPoint), in the same Muted Ochre + Charcoal combination

This banner is *intentional brand chrome*, not an apologetic afterthought. Treat it as a design element from day one, not a CSS overlay tacked on at the end.

## 6. Operational follow-ups

These are not open design questions — direction is locked. These are downstream tasks the locked direction generates:

1. **Accessibility contrast audit** on the final hex shades (§4.1). Expect to nudge terracotta darker by one or two steps for body-link / button-on-cream contrast at small sizes. Run before site launch.
2. **Logo (optional future enhancement)** — the typographic wordmark per §4.3 direction is in use and accepted by Tim (2026-05-26) as the working logo for v1. A vector sketch round to add the subtle letterform personality treatment is not blocking and can run when/if there's time; the current treatment reads on-brand and works at all scales required by the site and document templates.
3. **Photography sourcing decision** — commission bespoke campus photography for v1 launch (cost / time / coordination with YAT site shoots) vs. accept temporary stock with a roadmap to replace in v2. Recommendation: ask Tim before committing either way.
4. **Source Sans 3 + Source Serif 4 font-file licensing** — both are OFL-licensed and free for any use including embedding in `.docx` / `.pptx` templates, but verify before redistributing the templates externally.

---

## Changelog

- **2026-05-26 v1.0:** Approved by Tim. Direction set: warm/inclusive community-college positioning for adult career-changer audience, distinct from the navy + maroon Australian VET-website crowd. Visual palette locked (warm earth: teal-green + terracotta + cream + ochre); typography locked (Source Sans 3, optional Source Serif 4 for editorial accents, JetBrains Mono for code); wordmark-led monogram logo direction locked (sketches still to author); documentary photography direction locked (sourcing call deferred); persistent ochre disclosure banner locked as intentional brand chrome.
- **2026-05-26 v0.1:** Initial draft prepared for Tim's review.
