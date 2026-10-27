# Missing Elements

Useful web elements that work everywhere on the web.

https://missing-elements.github.io/

**Missing Elements** builds standalone, framework-agnostic web components for capabilities the web platform does not provide out of the box (yet 🙂).

Each component is built on browser standards and works with React, Vue, Svelte, Angular, server-rendered HTML, or no framework at all. 
They are designed to be easy to embed, safe to self-host, and useful in applications with strict **Content Security Policies**.

## Components

| Component | What it does | Status |
| --- | --- | --- |
| [pdfjs&#8209;viewer](https://github.com/missing-elements/pdfjs-viewer) | A self-hostable custom element for displaying PDF documents, powered by PDF.js. | ✅&nbsp;Released |
| [h5p&#8209;offline&#8209;player](https://github.com/missing-elements/h5p-offline-player) | A browser-only H5P player that plays `.h5p` packages from a URL or local file without server-side extraction. It can also power a fully offline PWA. | ✅&nbsp;Released |

## Principles

- **Browser-native** — Prefer platform APIs, standard web components, and small integration surfaces over framework lock-in.
- **Framework-agnostic** — Use the same component in React, Vue, Svelte, Angular, or plain HTML.
- **Self-hostable** — Host assets yourself without depending on a third-party viewer service or CDN.
- **CSP-conscious** — Support deployments with restrictive Content Security Policies and clear asset boundaries.
- **Encapsulated** — Keep component styles and behavior isolated from the surrounding application.
- **Practical** — Solve real document and learning-content viewing problems with a small, understandable API.

## Quick start

The common model is simple: load a component once, then use its custom element in your page.

```html
<script type="module" src="/path/to/component.js"></script>

<!-- The exact element and attributes depend on the component. -->
<your-element src="/files/example"></your-element>
```

See each repository for installation instructions, browser requirements, demos, API documentation, and self-hosting guidance.

## Why self-hosting?

Many viewer integrations send documents or learning content to a third-party service, require a backend conversion step, or rely on an external CDN at runtime.

Missing Elements components are intended to give hosts control over:

- where viewer code is served from;
- which origins a page can contact;
- how documents and packages are stored and loaded;
- whether an experience can work without a network connection.

Self-hosting does not make untrusted content automatically safe. Host applications should still apply an appropriate Content Security Policy, validate inputs where applicable, and choose a security policy that fits their users and content sources.

## Support the project

If these components are useful to you, you can support their development:

[Buy Me a Coffee](https://buymeacoffee.com/alekswebnet)

[Donatello](https://donatello.to/OleksandrShevchuk)
