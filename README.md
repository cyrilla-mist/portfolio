# Cyrilla — Portfolio & Web Lab

A curated home for my selected products, earlier AI experiments, and small web tools.

[View the portfolio](https://cyrilla-mist.github.io/portfolio/) · [Public repository map](docs/repository-map.md)

## Selected Products

### Sideglance

Internet context intelligence for moments where you understand the words but may still miss the tone, social meaning, cultural reference, or usage boundary.

- [Live demo](https://cyrilla-mist.github.io/sideglance/)
- [Repository](https://github.com/cyrilla-mist/sideglance)

### STATEWAKE

An interrupted-work recovery agent that validates whether a previously trusted project state is still safe to continue from before recovery begins.

- [Repository](https://github.com/cyrilla-mist/statewake)

### Nexus Atlas

Personal intelligence infrastructure for restoring project context, tracing decisions, and continuing long-running work with governed evidence and actions.

- [Live demo](https://cyrilla-mist.github.io/nexus-ai/)
- [Repository](https://github.com/cyrilla-mist/nexus-ai)

### English Radar

A local-first learning system for real internet English, organized around context, tone, usage boundaries, pronunciation, and personal mastery. The standalone product is now in maintenance and acts as the main learning-system foundation for future Sideglance Radar work.

- [Live site](https://cyrilla-mist.github.io/english-radar/)
- [Repository](https://github.com/cyrilla-mist/english-radar)

### Verity

An AI-assisted project-material review tool that helps teams inspect evidence coverage, likely reviewer questions, structural risks, and revision priorities before submission.

- [Live site](https://cyrilla-mist.github.io/verity/)
- [Repository](https://github.com/cyrilla-mist/verity)

## Earlier Experiments

These projects remain public for history and compatibility but are not current flagship work.

### Inkraft

Earlier AI writing-assistant experiment for Chinese academic writing workflows.

- [Live site](https://cyrilla-mist.github.io/inkraft/)
- [Source repository](https://github.com/cyrilla-mist/inkraft)

### PrismAI

Earlier multi-role AI review experiment for comparing reviewer perspectives and turning feedback into prioritized revision actions.

- [Live site](https://cyrilla-mist.github.io/prism-ai/)
- [Source repository](https://github.com/cyrilla-mist/prism-ai)

See [`experiments/`](experiments/) for the Portfolio experiment index.

## Web Lab

Small browser-based utilities and interface experiments live under the Portfolio rather than becoming separate repositories.

- [Prompt Builder](https://cyrilla-mist.github.io/portfolio/lab/prompt-builder/)
- [AI Tools Directory](https://cyrilla-mist.github.io/portfolio/lab/ai-tools/)
- [Color Palette Generator](https://cyrilla-mist.github.io/portfolio/lab/color-palette/)
- [Gradient Generator](https://cyrilla-mist.github.io/portfolio/lab/gradient-generator/)

The original root-level URLs are preserved as compatibility redirects while the Web Lab uses the cleaner directory-based paths above.

## Repository Role

This repository is the public presentation layer for my work.

- Larger products keep independent repositories, architecture, tests, and release history.
- Small static utilities go into `lab/`.
- Earlier standalone experiments are indexed in `experiments/`.
- Repository roles and maintenance rules are documented in [`docs/repository-map.md`](docs/repository-map.md).

```text
portfolio/
├── index.html
├── lab/
│   ├── index.html
│   ├── prompt-builder/index.html
│   ├── ai-tools/index.html
│   ├── color-palette/index.html
│   └── gradient-generator/index.html
├── experiments/
│   ├── README.md
│   ├── inkraft/README.md
│   └── prism-ai/README.md
├── docs/
│   └── repository-map.md
├── prompt-tools.html         legacy redirect
├── ai-tools.html             legacy redirect
├── color-palette.html        legacy redirect
└── gradient-generator.html   legacy redirect
```

## Technology

The Portfolio and Web Lab are intentionally lightweight:

- HTML
- CSS
- JavaScript
- GitHub Pages
- Responsive layouts
- Light and dark themes

Individual products may use additional services such as Cloudflare Workers, model APIs, TypeScript, testing frameworks, Google Cloud, or other infrastructure. See each product repository for its actual architecture.

## About

I build small products and experiments around AI, context, learning, writing, and information workflows. This Portfolio is maintained as a curated index rather than a complete archive of everything I have built.

— Cyrilla
