# Overwhelmed by big data? Time to make reproducibility work for you!

An interactive comic-book-style explainer about reproducibility in computational biology research. Built for PhD students, postdocs, and PIs.

**Live site:** [UCL-Biosciences.github.io/me-me-me-producibility](https://UCL-Biosciences.github.io/me-me-me-producibility)

---

## What it does

- **Problems** you'll recognise if you've spent any time managing or analysing big data
- **Solutions** that actually help
- **Benefits** of getting it right, both for you AND the wider scientific mission. Win-win!
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
