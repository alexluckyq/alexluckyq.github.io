# Alex Qin — personal website

A focused portfolio and writing site for Alex Qin, Staff Software Engineer specializing in Android and XR. Built with Hugo, local templates, and CSS; no theme downloads, JavaScript dependencies, or third-party fonts are required.

## Local development

Use Hugo **0.119.0 extended** (the version pinned in GitHub Actions):

```sh
hugo server --bind 127.0.0.1
```

Open the local URL printed by Hugo. To create the production output:

```sh
hugo --minify
```

Generated files go to `public/`, which is ignored by Git.

## Editing

- Homepage and sections: `layouts/index.html`
- Career history: `data/career.json`
- Contact and site metadata: `config/_default/params.yaml`
- Navigation: `config/_default/menus.yaml`
- Styling: `assets/css/site.css`
- Posts: add a folder with `index.md` under `content/post/`
- Resume downloads: `static/uploads/resume.pdf` (two pages) and `static/uploads/alex-qin-android-engineer.pdf` (one page)

Use front matter with `title`, `date` (including a time zone), `description`, `summary`, and `author` for new posts. Future-dated posts remain hidden until their date. The homepage automatically displays the three newest posts, and `/post/` lists all posts. An RSS feed is available at `/post/index.xml`.

## Deployment

The GitHub Actions workflow builds and deploys on pushes to `main`, or manually via Actions. In repository Settings → Pages, select **GitHub Actions** as the source. The workflow obtains the correct base URL from `actions/configure-pages`.

## Content and attribution

Career content is based on the supplied one-page Android Engineer resume and two-page resume. Employment dates, overlapping roles, and the Google XWF-via-Magic-Leap relationship are preserved. The first post links to its source and distinguishes commentary from unverified article claims.

This repository originally used the Wowchemy Academic starter. Its MIT license notice is retained in `LICENSE.md`; sample content and unused integrations have been removed.
