# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Workspace Overview

Multi-project workspace containing static web projects for Jason Yang (BizOps Lead at D.CAMP). All projects are vanilla HTML/CSS/JavaScript with no build systems, bundlers, or package managers.

## Projects

- **my-profile-site/** — Personal portfolio single-page site. Has its own CLAUDE.md with detailed conventions. Uses Tailwind CSS (CDN) with custom theme config embedded in `index.html`.
- **output-style-test/** — Collection of small interactive web apps (counter, todo list, stopwatch) for testing purposes. Uses Tailwind CSS (CDN).

## Development

No build step, no linting, no tests across all projects. Open any `.html` file directly in a browser or use a local server:

```
python3 -m http.server
```

## Conventions

- All UI text content is in Korean. Section headings and code identifiers use English.
- Tailwind CSS is loaded via CDN (`cdn.tailwindcss.com`), not installed locally.
- All JavaScript is vanilla — no frameworks or npm dependencies.
- Each project is self-contained with no shared code between them.
