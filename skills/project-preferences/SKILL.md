---
name: project-preferences
description: Apply repository-specific preferences when planning, implementing, or reviewing changes in this project.
---

<!--
This file is part of Gabriel Mongefranco's Open Source Portfolio
Copyright © 2026 Gabriel Mongefranco
Licensed under the GNU Free Documentation License v1.3 or later.
See <https://www.gnu.org/licenses/fdl-1.3.html>. See README for full license information.
-->

# Gabriel Mongefranco's Open Source Portfolio

## Project preferences

Use this skill when planning, implementing, or reviewing changes in this repository.
Keep all project-specific preferences and workflows in this single file. This skill
supplements `AGENTS.md` and cannot weaken its security, privacy, accessibility,
licensing, testing, or authorization rules.

### Purpose and scope

This repository is the GitHub Pages user site for the `gabrielmongefranco` GitHub
account. It is published at `https://dev.mongefranco.com` and will hold a portfolio
of Gabriel Mongefranco's open source apps. Each app keeps its own repository, and
GitHub Pages serves an app's site under this domain at
`https://dev.mongefranco.com/<repository-name>/`. Until the portfolio page exists,
`index.html` redirects visitors to `https://github.com/gabrielmongefranco`.

### Environment and structure

Follow the repository’s existing file and folder naming conventions when adding new files.

- The site is static HTML served by GitHub Pages from the root of the `main` branch.
  There is no build step and no server-side code.
- `CNAME` sets the custom domain to `dev.mongefranco.com`. Do not rename, move, or
  edit it without the owner's approval, because changing it moves the domain for
  this site and for every project site served under it.
- `.nojekyll` turns off Jekyll processing, so GitHub Pages serves files exactly as
  committed. Every tracked file, including Markdown and the `src/` samples, is
  publicly reachable on the site.

### Setup and verification

- Preview locally by opening `index.html` in a browser, or by running
  `python3 -m http.server` from the repository root and visiting
  `http://localhost:8000`.
- Validate HTML changes before merging, and check pages with an automated
  accessibility tool plus the manual checks in the accessibility skill.

### Project constraints

- Never commit secrets, private notes, or unpublished work. GitHub Pages publishes
  everything on `main`.
- Keep pages free of third-party scripts, trackers, and fonts unless the owner
  approves them.

### Project skills

None yet beyond the shared skills listed in [SKILLS.md](../../SKILLS.md).

### Conclusion

Treat every change as a public website change. Keep it static, accessible, and free
of anything that should not be published.

### Additional resources

- [Project README](../../README.md)
- [GitHub Pages documentation](https://docs.github.com/en/pages)
- [Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
