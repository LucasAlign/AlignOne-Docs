# Contributing to AlignOne Help

This help site is written by **two AI agents working in different repos** — the
**backend agent** (AlignOne API / `Align-Core`) and the **frontend agent** (the AlignOne app) —
plus human reviewers. This file is the contract that keeps their work consistent.

> New here? Read this once, then see the [how-to template](templates/how-to-template.md)
> and the guiding plan (`user-docs-plan.md`).

## 1. One canonical copy

The Markdown in this repo is the **single source of truth**. Don't fork pages into either
product repo. Both agents open pull requests *here*; the strict MkDocs build
(`mkdocs build --strict`) is the shared gate — broken links or missing nav entries fail CI.

## 2. Who owns what (by doc type)

Each page has **one primary author** and **one required reviewer from the other side.**

| Section | Primary author | Required reviewer | Why |
|---|---|---|---|
| Concepts | **Backend** | Frontend (label consistency) | Concepts describe how the system actually works |
| Reference (glossary, permissions, statuses) | **Backend** | Frontend | Data model, scoping, and status values are defined server-side |
| How-To Guides | **Frontend** | **Backend (correctness)** | The steps are UI clicks; backend confirms the rules and effects |
| Get Started | **Frontend** | Backend | Onboarding walkthroughs are UI-driven |
| Style guide, nav / IA | **Shared** | — | Agreed jointly |

**Backend review is mandatory** on any page that asserts *what a role can see or do.*
Volunteer→single-family scoping is enforced server-side; a how-to that implies a volunteer
can see another family is a correctness bug, not a typo.

## 3. Page lifecycle

Every page carries front-matter:

```yaml
---
status: draft        # draft → needs-ui → needs-review → ready
primary: frontend    # backend | frontend
---
```

Typical flow for a How-To:

1. **Backend** drafts the spine — concept, rules, effects, edge cases — and leaves
   `@frontend` markers where UI details are needed. → `status: needs-ui`
2. **Frontend** fills exact labels, navigation, and screenshots; resolves `@frontend`
   markers; raises any `@backend` questions. → `status: needs-review`
3. The **other agent reviews** for correctness/consistency. → `status: ready`

Concepts/Reference run the same loop with backend as primary.

## 4. Hand-off markers

Leave questions for the other agent inline as HTML comments tagged with their role. Each
agent finds its queue by searching its own tag:

- `<!-- @frontend: confirm the exact button label here -->`
- `<!-- @backend: is withdrawal allowed after the need is completed? -->`

```bash
grep -rn "@frontend" docs/   # frontend's open items
grep -rn "@backend"  docs/   # backend's open items
```

Resolve and delete a marker when you've handled it. A page can't reach `status: ready`
while any marker remains.

## 5. The glossary is the anti-drift contract

[`docs/reference/glossary.md`](docs/reference/glossary.md) maps each concept term to its
**exact in-app label.** Backend owns the *What it means* column; frontend owns the *In-app
label* column. Both agents use these spellings everywhere — if the app and the glossary
disagree, fix the glossary in the same PR.

## 6. Style

See the guiding plan (§7) and the [how-to template](templates/how-to-template.md): second
person, imperative, present tense; one task per page; `kebab-case.md`; alt text on every
image; never include real family data.
