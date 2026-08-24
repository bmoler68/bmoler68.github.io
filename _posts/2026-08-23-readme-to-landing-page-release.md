---
tags: ["2026", "Releases"]
---

## README to Landing Page

![README to Landing Page Banner](/images/README-to-landing-page/banner.png)

I'm excited to announce the release of **README to Landing Page** — a zero-configuration GitHub Action that converts your repository's `README.md` into a polished static landing page and deploys it to GitHub Pages.

### About the Project

README to Landing Page turns the documentation you already maintain into a shareable site. Drop a short workflow into a repository, and the action parses the README, generates HTML and CSS, and publishes the result to a `gh-pages` branch. No CLI, local Node.js, or extra hosting setup is required.

The action is delivered as a Docker container. GitHub builds the image from the `Dockerfile` on each run, so there is no container registry to manage.

### Features

Setup is intended to take about 30 seconds: add a workflow that checks out the repo and calls `bmoler68/readme-to-landing-page@v1`. The action creates the `gh-pages` branch if it does not exist and pushes `index.html`, `styles.css`, and `assets/` to that branch without changing `main`.

Optional inputs let you point at a different README path, choose an output directory, pick the publish branch, include a table of contents, or supply a custom GitHub token. Defaults are enough for most repositories.

### How It Works

When the workflow runs, GitHub checks out the action at the referenced tag, builds the Docker image, and runs it against the target repository. The container parses `README.md` into an AST, generates a static site, and pushes that site to `gh-pages`. After GitHub Pages is pointed at the `gh-pages` branch root, each push to `main` refreshes the published landing page.

### Resources

- **🔗 GitHub Repository**: [README-to-landing-page on GitHub](https://github.com/bmoler68/README-to-landing-page)

For questions, support, or feedback, please contact me at bmoler@brianmoler.com.
