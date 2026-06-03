# AlignOne User Documentation — Guiding Plan

> **Status:** Draft for review · **Owner:** _TBD_ · **Audience of these docs:** End-users of the AlignOne app (not developers).
>
> This is the planning/scaffolding document. It defines *what* we're building, *for whom*, *where it lives*, and *in what order*. It is not itself user-facing content.

---

## 1. Goals & Success Criteria

**Why we're writing user docs:** Today, every piece of AlignOne documentation is developer-facing (`README.md`, `keyfam-api-reference.md`, `docs/architecture.md`, the schema dump). There is nothing that helps an actual **volunteer**, **advocate**, or **program staff member** learn to use the product. That gap creates onboarding friction and support load.

**What "done well" looks like:**

| Goal | How we'll know |
|---|---|
| A new volunteer can self-onboard without a phone call | Onboarding completion rate; fewer "how do I…" support messages |
| Staff can answer "how do I do X" by linking a page | Support replies increasingly cite doc links |
| Docs stay current as features ship | A docs check is part of the feature workflow; no "this screen looks different" reports |
| Non-technical staff can contribute edits | At least one program-staff edit merged without engineering help |

---

## 2. Audiences (in priority order)

AlignOne's roles are already defined by the Cognito auth model — that's our top-level structure. We will **not** write one undifferentiated manual; each role sees a different slice of the app.

1. **Volunteers** _(write first)_ — largest population, least technical, **narrowest** scope (one family). Smallest surface = fastest path to a *complete* set of guides that delivers the most value. This is the v1 target.
2. **Admins / program staff** _(write second)_ — power users, fewer in number, full access. They can lean on support short-term, but they need the management workflows documented (onboarding families, inviting people, oversight).
3. **Advocates** _(write third)_ — case leads, scoped to their church. Largely an Admin subset; much can be reused once Admin guides exist.

> **Recommended v1 scope:** A *complete* Volunteer set + a *thin* Admin "Getting Started" + the shared Concepts/Glossary. Resist documenting everything at once.

---

## 3. Hosting & Tooling

**Decision:** Source of truth in **Git/GitHub** (endorsed — your instinct is right), published as a **searchable website** so non-technical readers never touch raw markdown.

**Recommended stack:**

- **Authoring:** Markdown in a Git repo. Contributors only ever edit `.md`.
- **Site generator:** **[MkDocs](https://www.mkdocs.org/) + [Material theme](https://squidfunk.github.io/mkdocs-material/)** — one `mkdocs.yml`, excellent built-in search, professional out of the box, minimal build tooling to babysit.
- **Publishing:** **GitHub Pages**, built automatically by a GitHub Action on merge to `main`.

**Why MkDocs Material over Docusaurus:** Docusaurus (React-based) is more powerful — versioned docs, i18n, custom components — but heavier than a help center needs today. MkDocs Material stands up in an afternoon and keeps the contributor experience to "edit a markdown file." Revisit Docusaurus only if we later need versioned docs or rich interactive components.

**Decision (resolved) — the docs live in a dedicated `AlignOne-Docs` repo.** Neutral ground that both the frontend and backend agents contribute to via pull requests; neither product repo owns it, and it keeps CDK/infra noise out. The Phase 0 scaffold was prototyped in this repo under `user-docs/` and is being extracted to `AlignOne-Docs`.

**Privacy note:** The *content* of these docs is "how to use the app" — it contains **no family PII**, so a public GitHub Pages site is appropriate. If we ever want the help site private, note that Pages on a private repo requires GitHub Enterprise; flag before assuming public is fine.

---

## 4. Structure (the model)

We'll follow **[Diátaxis](https://diataxis.fr)** — the proven four-mode model — adapted to a help center:

- **Get Started** — one short, guided walkthrough per role ("your first day on AlignOne").
- **How-To Guides** — task-oriented, the *bulk* of the docs. One page = one job ("Claim a need").
- **Concepts** — understanding-oriented ("What is a WrapAround care circle?", "Roles & who sees what").
- **Reference / FAQ** — lookup: glossary, permissions matrix, statuses, troubleshooting.

People search for **tasks**, not features — so How-To guides carry the weight.

---

## 5. Information Architecture (proposed nav tree)

Derived directly from the live feature surface in `keyfam-api-reference.md`. This is the table of contents to fill in.

```
Home / Welcome to AlignOne
│
├── Get Started
│   ├── For Volunteers   ← v1
│   ├── For Program Staff (Admins)
│   └── For Advocates
│
├── Concepts
│   ├── What is WrapAround? (the care circle)
│   ├── Roles & who sees what (Volunteer · Advocate · Admin)
│   └── Key terms: needs, claims, schedules, threads, posts
│
├── How-To Guides
│   ├── Account & Profile
│   │   ├── Accept your invite & sign in
│   │   ├── Update your profile
│   │   └── Upload your photo
│   ├── Your Family (Volunteer)
│   │   └── View your family & its members
│   ├── Needs (WrapAround)
│   │   ├── Browse open needs
│   │   ├── Claim a need
│   │   ├── Withdraw a claim
│   │   └── Mark a need complete
│   ├── Schedules
│   │   ├── View the calendar
│   │   ├── Sign up for a slot
│   │   └── Understand recurring events
│   ├── Messaging
│   │   ├── Start a thread
│   │   ├── Reply & read receipts
│   │   └── Notifications
│   ├── Posts
│   │   └── Read & comment on posts
│   ├── Training
│   │   ├── Find your modules & track progress
│   │   └── Access training resources
│   └── Admin / Staff workflows
│       ├── Families & people: add a family, add parents/children, set primary contact, upload family photo
│       ├── Volunteers & advocates: invite, assign to a family, set roles & statuses
│       ├── Organizations: manage churches & counties
│       ├── Onboarding: initiate onboarding, resend an invite
│       └── Oversight: needs/claims overview, training matrix, audit log
│
└── Reference
    ├── Glossary
    ├── Roles & permissions matrix
    ├── Statuses explained (community, volunteer, etc.)
    ├── FAQ
    └── Troubleshooting (didn't get my invite, can't sign in, …)
```

---

## 6. Page Template (every How-To uses this)

```markdown
# <Verb-first task title>            e.g. "Claim a need"

**Who this is for:** <role(s)>
**When to use it:** <one sentence>
**Before you start:** <prerequisites, if any>

## Steps
1. <action> — <screenshot>
2. …

## What you'll see
<the expected result>

## Related
- [Linked guide], [Linked concept]
```

A consistent skeleton makes pages faster to write, easier to scan, and trivial to keep parallel across roles.

---

## 7. Style & Conventions (one-page guide to write up in Phase 0)

- **Voice:** second person, imperative ("Tap **Claim**"), present tense.
- **Terminology = UI labels.** The exact button/label text in the app is the source of truth. Keep a term map so docs and UI never drift.
- **Screenshots:** annotated, consistent frame, light redaction of any sample data. Define one source environment.
- **Reading level:** plain language, short sentences; assume no technical background.
- **Accessibility:** alt text on every image; don't rely on color alone; descriptive link text.
- **File naming:** `kebab-case.md`, one task per file, mirrors the nav tree.

---

## 8. Phased Backlog

| Phase | Deliverable | Notes |
|---|---|---|
| **0 — Setup** | Repo (decide 3.a vs 3.b), MkDocs+Material, GitHub Action → Pages, page template, style guide, empty IA skeleton | One-time foundation; unblocks everyone |
| **1 — Volunteer MVP** | Get Started (Volunteer) + top How-Tos: accept invite, update profile, browse/claim a need, sign up for a schedule slot, message the team, find training | The highest-value, self-contained set |
| **2 — Admin** | Get Started (Staff) + management workflows: onboard a family, invite/assign people, organizations, resend invites, oversight | Power-user workflows |
| **3 — Advocate + depth** | Advocate Get Started; flesh out Concepts; Glossary, permissions matrix, statuses | Reuses Admin content |
| **4 — Polish** | FAQ, Troubleshooting, search tuning, screenshot pass, release-notes page | Ongoing |

**Prioritize within a phase by:** most-used feature → highest support burden → onboarding-critical.

---

## 9. Ownership & Maintenance

- **Writer(s):** _TBD_ — can be staff once the template + style guide exist.
- **SME reviewer:** program staff who know the real-world workflow.
- **Approver / publisher:** _TBD_ (owns the merge to `main`).
- **Keeping it current:** add a **"docs updated?"** checkbox to the feature PR/release checklist so guides don't rot. Quarterly review of the full set.

**Two-agent coordination (frontend + backend).** User docs sit on the seam between the two product agents, so authorship is split **by doc type with mandatory cross-review**: Concepts/Reference are backend-authored; How-To/Get-Started are frontend-authored; each page has one required reviewer from the other side. Backend review is mandatory on any page asserting role scoping (who can see/do what). Hand-offs use page-level `status` front-matter and inline `@frontend` / `@backend` markers — full protocol in the docs repo's `CONTRIBUTING.md`.

---

## 10. Dependencies & Risks

- **UI stability.** End-user guides lean on screenshots and exact labels. The frontend is in flight (`frontend-merge-prompt.md`, `keyfam-photo-upload-frontend.md`) — write *text* first, add screenshots once screens settle, to avoid re-shooting.
- **Terminology drift** between app and docs — mitigated by the term map (§7).
- **API/feature changes** — mitigated by the PR docs gate (§9).
- **Single point of failure** — if only engineering can publish, docs stall. The MkDocs/Pages setup is chosen specifically so non-technical staff can contribute.

---

## 11. Definition of Done (per page)

- [ ] Follows the template (§6) and style guide (§7)
- [ ] Verified against the live app by an SME
- [ ] Screenshots current and annotated, with alt text
- [ ] Linked from the nav and from related pages
- [ ] No PII in examples

---

## 12. Decisions

**Resolved**

- ✅ **Repo placement** — dedicated `AlignOne-Docs` repo. (§3)
- ✅ **Delivery model** — site first (MkDocs → Pages); the same Markdown surfaced in-app later.
- ✅ **Authorship** — two agents, split by doc type with mandatory cross-review. (§9, `CONTRIBUTING.md`)
- ✅ **First audience** — Volunteers. (§2)
- ✅ **Generator** — MkDocs Material (revisit Docusaurus only for versioned docs / rich components).

**Still open**

- **Who owns/reviews content** day-to-day — human writer, SME reviewer, publisher. (§9)
- **Public vs private** help site — public is fine; content has no PII. (§3)
- **`AlignOne-Docs` creation mechanics** — how the remote repo is stood up and Pages enabled.
