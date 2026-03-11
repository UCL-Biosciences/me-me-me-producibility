# Reproducibility Crisis — Interactive Field Guide

An interactive comic-book-style explainer about reproducibility in computational biology research. Built for PhD students, postdocs, and PIs.

**Live site:** [your-username.github.io/repro-bio](https://your-username.github.io/repro-bio) *(update after deploying)*

---

## What it does

- **10 Problems** you'll recognise if you've spent any time in a bioinformatics lab
- **8 Solutions** that actually help
- **7 Benefits** of getting it right
- Click any problem to see which solutions address it and what you gain

## Suggesting edits

Found a mistake, a missing problem, or better wording? **[Open an issue](../../issues/new/choose)** using the "Suggest an Edit" template. You don't need to know how to code — just describe what should change.

## Editing the content yourself

All card text and links live in **`data.json`** — no HTML knowledge required.

```json
{
  "problems": [
    {
      "id": "P1",
      "group": "People & Handover",
      "label": "The Postdoc Vanishing Act",
      "body": "Key postdoc left the lab..."
    }
  ]
}
```

To add a new problem: add an entry to `problems`, give it a unique ID (e.g. `P11`), and add its links to the `links` object.

## Running locally

Because the page fetches `data.json`, you need a local server (browsers block `fetch()` from `file://`):

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000
```

Or install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) VS Code extension and click "Go Live".

## Deploying to GitHub Pages

1. Push this repo to GitHub (public)
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → `main` → `/ (root)`
4. Save — your site will be live in ~60 seconds at `https://your-username.github.io/repo-name`

## File structure

```
├── index.html          # The site (layout, styles, interaction logic)
├── data.json           # All card content and links — edit this to change content
├── _config.yml         # GitHub Pages config
├── README.md
└── .github/
    └── ISSUE_TEMPLATE/
        └── suggest_edit.yml   # Structured form for content suggestions
```

## Built with

Vanilla HTML/CSS/JS. No frameworks, no build step, no dependencies beyond Google Fonts.
