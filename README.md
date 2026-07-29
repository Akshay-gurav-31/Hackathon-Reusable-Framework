# Reusable Hackathon Framework

Launch a professional, zero-cost hackathon website without writing code. This template is designed for science and rare-disease communities, but it can be used for any hackathon.

The website is a static HTML site. All event content (name, dates, tracks, prizes, judges, forms, and more) is read from one file: `hackathon.config.yml`.

## What this template includes

- A responsive public hackathon website (`index.html`)
- A visual no-code configuration generator (`setup/index.html`)
- Google Form links for registration and project submissions
- A GitHub Issue submission template
- Free deployment to GitHub Pages through GitHub Actions
- Optional local secret scanning with Gitleaks

No database, server, API key, or paid hosting is required.

## Start here

For the complete organizer journey, follow [SETUP.md](SETUP.md). It explains how to create your repository, configure the event, test it, publish it, and update it later.

If you are working on your computer, read [LOCAL_PREVIEW.md](LOCAL_PREVIEW.md) before opening the site. Opening `index.html` by double-clicking it will not load your YAML configuration.

## The fastest no-code route

1. On GitHub, select **Use this template** and create a new **public** repository.
2. In the repository, open **Settings** -> **Pages** and set **Source** to **GitHub Actions**.
3. Open the site generator at `https://<your-github-username>.github.io/<your-repository-name>/setup/` after the first deployment finishes.
4. Fill in the generator and download `hackathon.config.yml`.
5. Replace the root `hackathon.config.yml` file in GitHub with the downloaded file and commit the change.
6. Wait for the GitHub Actions deployment to finish, then visit `https://<your-github-username>.github.io/<your-repository-name>/`.

Use the **responder links** from Google Forms (the links participants fill in), never a Google Form edit link or a Google Docs link.

## Important files

| File or folder | Purpose |
| --- | --- |
| `index.html` | The public hackathon website |
| `hackathon.config.yml` | All editable event content |
| `setup/index.html` | Visual configuration generator |
| `SETUP.md` | Complete organizer guide |
| `LOCAL_PREVIEW.md` | How to test the site on a computer |
| `SECURITY.md` | What is public and what must stay private |
| `.github/workflows/deploy.yml` | GitHub Pages deployment workflow |

## Help

If the site does not show your new content, use the troubleshooting section in [SETUP.md](SETUP.md). The most common cause when working locally is opening `index.html` directly instead of through `http://localhost`.
