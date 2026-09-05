# CHIPS

A long-form, diagram-heavy course on how an AI accelerator moves from design to
data center, and which companies control each step.

## Contributing

Edit the layer that owns the thing you want to change. Existing slides are
examples rather than required templates.

Each segment lists the research files it uses in its first-slide frontmatter:

```yaml
---
layout: default
sources: [research/nvidia.md]
---
```

Put evidence and links in the relevant research file. Speaker notes are ordinary
trailing HTML comments in each slide. Unresolved claims can stay marked with a
`VERIFY` comment in research, but should not move into the published deck. For
generated SVGs, edit the JavaScript in `diagrams/src/` and run `npm run diagrams`;
other images can be placed directly in `diagrams/rendered/` or `public/assets/`.

## Local development

```bash
npm install              # install dependencies
npm run dev              # open the deck at localhost:3030
npm run dev -- --presenter
npm run diagrams         # regenerate code-built SVGs
npm run check            # validate links and citations, then build
npm run export           # export the deck to PDF
npm run build:pages      # production build with the GitHub Pages base path
```

Pushes to `main` deploy through `.github/workflows/deploy-pages.yml`.
