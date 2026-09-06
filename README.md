# Ease IT

Static company website, built with HTML and [Pico CSS](https://picocss.com/) 2.1.1. No build step or JavaScript required.

## Publish

For GitHub Pages, select **Settings → Pages → Build and deployment → Source → GitHub Actions**. The workflow in `.github/workflows/pages.yml` publishes on pushes to `main`, or manually from the Actions tab. It stages only `index.html` and `assets/`.

The site is live at https://www.easeit.cz. The custom domain is pinned by the `CNAME` file, which the workflow copies into the published artifact on every deploy; `easeit.cz` redirects to `www.easeit.cz`. The default GitHub URL, https://easeit-cz.github.io/easeit-site/, still works.

For other static hosts, upload **only `index.html` and `assets/`** to your static hosting directory. Do not publish the repository root, which contains local context and Git metadata. Relative asset URLs support subdirectory hosting.

Team bios summarize public LinkedIn information, and the portraits in `assets/team/` come from the same public profiles. Pico CSS is vendored in `assets/vendor/` with its MIT license. Local working context is indexed in `.context/README.md` and intentionally ignored by Git. Shared agent guidance is in `AGENTS.md`.
