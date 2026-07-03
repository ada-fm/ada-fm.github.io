# ada-fm.github.io

Personal blog built with [Hugo](https://gohugo.io) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed to GitHub Pages.

## Local development

```bash
# install the theme submodule
git submodule update --init --recursive

# run the dev server with drafts visible
hugo server -D
```

The site is served at http://localhost:1313/.

## Writing a post

Posts are written in [Org mode](https://orgmode.org/) (`.org`). Create one with:

```bash
hugo new posts/my-post.org
```

Edit the generated file under `content/posts/`, then set `#+draft: false` when you're ready to publish. Org dates need a day of the week, e.g. `#+date: [2026-07-02 Thu]`.

## Deployment

Pushing to `main` triggers the GitHub Actions workflow in `.github/workflows/hugo.yml`, which builds the site and deploys it to GitHub Pages. Make sure the repository's **Settings > Pages > Source** is set to **GitHub Actions**.

## Structure

- `content/`  &mdash; posts and pages
- `hugo.toml` &mdash; site configuration
- `themes/PaperMod/` &mdash; theme (git submodule)
- `.github/workflows/hugo.yml` &mdash; build & deploy pipeline
