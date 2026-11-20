# Publishing Pipeline

One source, three outputs. No Medium API exists for automated publishing, so the pipeline is: **write once in markdown, export to each format manually.**

## The Three Outputs

| Output | Format | Tool |
|--------|--------|------|
| Medium post | Clean markdown with Medium conventions | Paste into Medium editor |
| Discussion paper | Markdown (this repo) | Native |
| Journal manuscript | LaTeX or Word | `pandoc` |

## Medium Conventions

See [medium-style.md](medium-style.md) for the formatting rules that make a paste into Medium render correctly.

## Export Commands

```bash
# Word
pandoc papers/01-trauma-and-misdiagnosis.md -o exports/01-trauma.docx

# LaTeX
pandoc papers/01-trauma-and-misdiagnosis.md -o exports/01-trauma.tex --standalone

# PDF (for review copies)
pandoc papers/01-trauma-and-misdiagnosis.md -o exports/01-trauma.pdf --pdf-engine=xelatex
```

## Folder Layout

```
open-discussion-papers/
├── README.md
├── papers/
│   ├── 01-trauma-and-misdiagnosis.md
│   ├── 02-reintegration-and-recovery.md
│   └── 03-economics-of-lived-experience.md
├── pipeline/
│   ├── README.md          ← this file
│   └── medium-style.md
└── exports/               ← generated outputs, gitignored ideally
```

## Workflow

1. Edit the markdown source in `papers/`.
2. Commit and push — the repo is the single source of truth.
3. Run pandoc for Word/LaTeX/PDF when a review copy is needed.
4. Paste into Medium when ready to publish publicly.
5. Open an issue on this repo for any discussion that belongs in public.

Nothing leaves this pipeline without the author's sign-off. The markdown is the draft. The published version is a decision.