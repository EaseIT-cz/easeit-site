# Ease IT

Static company website, built with HTML and [Pico CSS](https://picocss.com/) 2.1.1. No build step or JavaScript required.

## Publish

For GitHub Pages, select **Settings → Pages → Build and deployment → Source → GitHub Actions**. The workflow in `.github/workflows/pages.yml` publishes on pushes to `main`, or manually from the Actions tab. It stages `index.html`, `404.html`, `assets/`, and the `CNAME` file.

The site is live at https://www.easeit.cz. The custom domain is pinned by the `CNAME` file, which the workflow copies into the published artifact on every deploy; `easeit.cz` redirects to `www.easeit.cz`. The default GitHub URL, https://easeit-cz.github.io/easeit-site/, redirects to the custom domain.

For other static hosts, upload **only `index.html`, `404.html`, and `assets/`** to your static hosting directory. Do not publish the repository root, which contains local context and Git metadata. `index.html` uses relative asset URLs and still works under a subdirectory, but `404.html` references `/assets/...` from the root, because the host serves it for unknown paths at any depth. The `og:` and `canonical` tags likewise hardcode `https://www.easeit.cz/`, since both require absolute URLs.

Team bios summarize public LinkedIn information, and the portraits in `assets/team/` come from the same public profiles. Pico CSS is vendored in `assets/vendor/` with its MIT license. Local working context is indexed in `.context/README.md` and intentionally ignored by Git. Shared agent guidance is in `AGENTS.md`.
