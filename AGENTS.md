# Working on the Ease IT site

This is a static company website: HTML, CSS, and only necessary JavaScript.

## Load context selectively
- Start with `.context/README.md` when it exists; it is the context index.
- Read `.context/company.md` for copy, team, or project changes.
- Read `.context/design.md` for layout, styles, or accessibility changes.
- Read `.context/development.md` for implementation, validation, or deployment work.
- Read `.context/decisions.md` when changing an established choice; update it when a decision changes.
Do not load all context by default. `.context/` is intentionally ignored by Git and may be absent in a fresh checkout. This file and README.md contain the essential shared instructions.

## Shared rules
- Ease IT owns Vornik; link to https://vornik.io/.
- Team: Veaceslav Mindru, Vadim Grinco, Jana Grinco. Bios summarize public LinkedIn information; do not invent responsibilities, credentials, clients, locations, or contact details.
- Keep the design quiet, readable, responsive, and accessible. Avoid stock marketing claims and decorative dashboard cards.
- Use the locally vendored Pico CSS 2.1.1 framework, with custom styles in assets/site.css. Preserve its license.
- No build step or runtime dependencies. All site assets must work on a basic static host and under a subdirectory.
- Before finishing, check local links/assets, HTML structure, responsive layout when a browser is available, and `git diff --check`.
- Publish only index.html and assets/. Never expose .context/, .git/, or repository instructions on a public host.
