# AlignOne-Docs — AlignOne user documentation

End-user help for the AlignOne app, written in Markdown and published as a searchable
website via [MkDocs](https://www.mkdocs.org/) + [Material](https://squidfunk.github.io/mkdocs-material/).

- **Audience:** volunteers, advocates, and program staff who *use* AlignOne (not developers).
- **Source of truth:** the Markdown in `docs/`. The same content can later be surfaced
  in-app contextually.
- **How the two agents work together:** see [`CONTRIBUTING.md`](CONTRIBUTING.md).
- **The plan behind this site:** [`user-docs-plan.md`](user-docs-plan.md).

## Run it locally

```bash
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve         # live-reload preview at http://127.0.0.1:8000
```

Build the static site (what CI publishes):

```bash
mkdocs build --strict     # output in ./site (git-ignored)
```

`--strict` fails the build on broken links or nav entries that point at missing files —
CI runs it in strict mode, so run it locally before opening a PR.

## Add a page

1. Create the Markdown file under `docs/…` (mirror the section it belongs to).
2. Add it to the `nav:` tree in `mkdocs.yml` so it appears in the sidebar.
3. For a how-to, start from [`templates/how-to-template.md`](templates/how-to-template.md).
4. `mkdocs serve` to preview, then open a PR.

## Conventions

- Voice: second person, imperative ("Tap **Claim**"), present tense.
- Terminology must match the **exact labels in the app** — keep the
  [glossary](docs/reference/glossary.md) in sync.
- One task per page; file names are `kebab-case.md`.
- Annotate screenshots; add alt text to every image; never include real family data.

## Publishing

`.github/workflows/docs.yml` builds on every PR (validation) and deploys to **GitHub
Pages** on merge to `main`. One-time setup: **Settings → Pages → Build and deployment →
Source → GitHub Actions**.
