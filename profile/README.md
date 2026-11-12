# Missing Elements

Web components and browser-based tools. Elements you host yourself,, and tools built on them that run in your browser, your editor and your AI agent, with no
server of ours between you and your files.

**[missing-elements.github.io](https://missing-elements.github.io/)**

## Web components

Standalone custom elements for what the web platform does not provide out of the box (yet 🙂).
Each works in React, Vue, Svelte, Angular or plain HTML, can be served entirely from your own
host, and runs under a strict Content Security Policy.

| Element | What it does | Links |
| --- | --- | --- |
| [pdfjs&#8209;viewer](https://github.com/missing-elements/pdfjs-viewer) | Views and edits PDF files in Firefox's PDF.js viewer, in an isolated iframe, with no runtime dependencies | [Docs and playground](https://missing-elements.github.io/pdfjs-viewer/) · [npm](https://www.npmjs.com/package/@missing-elements/pdfjs-viewer) |
| [h5p&#8209;offline&#8209;player](https://github.com/missing-elements/h5p-offline-player) | Plays `.h5p` files from your own URLs or from disk with no H5P server, offline too, and reports results as xAPI, cmi5 or SCORM | [Demo](https://h5p-offline-player.vercel.app/) · [npm](https://www.npmjs.com/package/@missing-elements/h5p-offline-player) |

## Tools

### In your browser

Nothing to install and no account, and the files you open stay on your computer.

- **[Build an H5P activity with AI](https://missing-elements.github.io/h5p/build/)**: describe a
  lesson to ChatGPT, Claude or Grok, paste the JSON it writes, then play the activity and download
  a `.h5p` file for Moodle or another H5P site.
- **[H5P to SCORM](https://h5p-offline-player.vercel.app/demo/scorm.html)**: turns a `.h5p` file
  into a SCORM zip that an LMS plays and grades.
- **[H5P Offline Player](https://h5p-offline-player.vercel.app/app/)**: an app you install from
  the browser that plays `.h5p` files with no network.

### In your editor

- **[H5P Preview](https://marketplace.visualstudio.com/items?itemName=MissingElements.h5p-preview)**:
  plays `.h5p` files in VS Code, and from [Open VSX](https://open-vsx.org/extension/MissingElements/h5p-preview)
  in Cursor and VSCodium.

### In your AI agent

Five skills for Claude Code and other agents that run commands. None needs an API key or an H5P
server.

```bash
npx skills add missing-elements/h5p-offline-player
```

| Skill | What it does |
| --- | --- |
| [`h5p-author`](https://github.com/missing-elements/h5p-offline-player/tree/main/skills/h5p-author) | Turns a prompt or a lesson into H5P content of any of 28 types, and checks it in the real player |
| [`h5p-verify`](https://github.com/missing-elements/h5p-offline-player/tree/main/skills/h5p-verify) | Checks that a package plays, and opens it for you to try |
| [`h5p-to-scorm`](https://github.com/missing-elements/h5p-offline-player/tree/main/skills/h5p-to-scorm) | Turns a package into a SCORM zip for an LMS |
| [`h5p-player-setup`](https://github.com/missing-elements/h5p-offline-player/tree/main/skills/h5p-player-setup) | Puts H5P on a website |
| [`h5p-normalize`](https://github.com/missing-elements/h5p-offline-player/tree/main/skills/h5p-normalize) | Rewrites a package whose video will not stream |

A chat that cannot install a skill reads `h5p-author` from
[missing-elements.github.io/h5p/skill/](https://missing-elements.github.io/h5p/skill/).

### On the command line

The packages behind the tools, on npm:
[`h5p-author`](https://www.npmjs.com/package/@missing-elements/h5p-author) builds a `.h5p` from a
short JSON source, [`h5p-verify`](https://www.npmjs.com/package/@missing-elements/h5p-verify)
checks that one plays, [`h5p-normalize`](https://www.npmjs.com/package/@missing-elements/h5p-normalize)
makes its video stream, [`h5p-embed`](https://www.npmjs.com/package/@missing-elements/h5p-embed)
writes a player site to embed packages from, or a SCORM zip, and
[`h5p-cmi5`](https://www.npmjs.com/package/@missing-elements/h5p-cmi5) makes a page that holds the
player a cmi5 unit.

## Principles

- **Yours to host.** The code and your files are served from where you choose, and no service of
  ours sits between your users and your content.
- **Private by default.** No accounts, cookies or telemetry, and no server of ours sees what you
  open or make.
- **Standards first.** Custom elements and platform APIs, for any framework or none.
- **Ready for strict CSP.** Each element runs under a restrictive Content Security Policy, with
  clear boundaries for its assets.
- **Open source.** The elements and tools are MIT. What they bundle keeps its own licence: PDF.js
  is Apache-2.0, H5P's libraries each have their own, and the H5P core is GPL-3.0, published
  apart.

## Support the project

If these are useful to you, you can support their development on
[Donatello](https://donatello.to/OleksandrShevchuk).
