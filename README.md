# Ease IT

Static company website, built with HTML and [Pico CSS](https://picocss.com/) 2.1.1. No build step or JavaScript required.

## Preview

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000. Edit copy in `index.html` and styles in `assets/site.css`. Team bios summarize public LinkedIn information; source notes live in local context.

## Publish

For GitHub Pages, select **Settings → Pages → Build and deployment → Source → GitHub Actions**. The workflow in `.github/workflows/pages.yml` publishes on pushes to `main`, or manually from the Actions tab. It stages only `index.html` and `assets/`.

The default site URL is https://easeit-cz.github.io/easeit-site/.

For other static hosts, upload **only `index.html` and `assets/`** to your static hosting directory. Do not publish the repository root, which contains local context and Git metadata. Relative asset URLs support subdirectory hosting.

Pico CSS is vendored in `assets/vendor/` with its MIT license. Local working context is indexed in `.context/README.md` and intentionally ignored by Git. Shared agent guidance is in `AGENTS.md`.
