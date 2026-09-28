<!--
This file is part of Gabriel Mongefranco's Open Source Portfolio
docs/architecture.md
Author(s): Gabriel Mongefranco
Created: 2026-09-27
Last Modified: 2026-09-27
Summary: Explains how the site is hosted on GitHub Pages and how app sites share the custom domain.
Notes: See README file for documentation and full license information.

Copyright © 2026 Gabriel Mongefranco

Licensed under the GNU Free Documentation License v1.3 or later.
See <https://www.gnu.org/licenses/fdl-1.3.html>. See README for full license information.

-->

# Gabriel Mongefranco's Open Source Portfolio

## Site hosting and structure

[Back to project README](../README.md)

This page explains how the site at dev.mongefranco.com is hosted and how each app
gets its own address under it. It is for anyone who maintains this repository or
publishes a new app. You do not need to know GitHub Pages well to follow it.

### How the site is served

GitHub Pages is a free GitHub service that turns files in a repository into a
website. This repository is a *user site*, because its name matches the account
name followed by `.github.io`. GitHub Pages publishes it from the root folder of the
`main` branch.

Three files control how the site works:

| File | What it does |
| --- | --- |
| `CNAME` | Sets the custom domain to `dev.mongefranco.com`. |
| `.nojekyll` | Turns off Jekyll, a tool GitHub Pages would otherwise use to build the site. Files are published exactly as they are in the repository. |
| `index.html` | The home page. For now it sends visitors straight to the [GitHub profile](https://github.com/gabrielmongefranco). |

There is no build step. When a change is merged into `main`, GitHub Pages publishes
it within a few minutes.

Every file on `main` is public on the website, not just `index.html`. For example,
this page can be opened at `https://dev.mongefranco.com/docs/architecture.md`.
Never commit anything you would not want published.

### How app sites share the domain

Each app lives in its own repository. A repository that is not the user site is a
*project site*. When you turn on GitHub Pages for a project site, GitHub serves it
under this site's custom domain, in a folder named after the repository.

For example, a repository named `sample-app` with GitHub Pages turned on appears at:

```text
https://dev.mongefranco.com/sample-app/
```

To publish a new app:

1. Open the app's repository on GitHub.
2. Go to **Settings**, then **Pages**.
3. Choose the branch and folder to publish from, then save.
4. Leave the custom domain field empty. The app inherits `dev.mongefranco.com` from
   this repository.

Do not give a top-level file or folder in this repository the same name as an app
repository, because both would claim the same address.

### The home page redirect

GitHub Pages cannot send server redirects, so `index.html` uses an HTML
`meta refresh` tag with a zero-second delay. Browsers move to the GitHub profile
right away. The page also shows a link to the profile, in case a browser blocks
automatic redirects. The page is marked `noindex` so search engines do not list it.

Replace `index.html` with the portfolio page when it is ready.

### Conclusion

You now know which files control the site and how to publish an app under
dev.mongefranco.com. Start with the [project README](../README.md) for a quick
overview, or read the GitHub Pages documentation below for more detail.

### Additional resources

- [Project README](../README.md)
- [Documentation index](README.md)
- [Gabriel Mongefranco's GitHub profile](https://github.com/gabrielmongefranco)
- [GitHub Pages documentation](https://docs.github.com/en/pages)
- [About custom domains and GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)
- [Configuring a publishing source for your GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

[Back to project README](../README.md)
