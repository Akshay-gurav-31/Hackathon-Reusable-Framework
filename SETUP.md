# Organizer Setup Guide

This guide takes you from a new GitHub repository to a live hackathon website. No coding is required.

## Before you begin

You need:

- A GitHub account
- A public GitHub repository created from this template
- A Google account if you will use Google Forms
- Your event details: name, dates, tracks, prizes, judges, and contact email

The website has no backend and does not need an API key, database password, or payment setup.

## 1. Create your repository

1. Open the template repository on GitHub.
2. Select **Use this template** -> **Create a new repository**.
3. Choose the account or organization that will own the event.
4. Give the repository a short name, such as `ai-innovation-challenge-2026`.
5. Select **Public**. This is the simplest free GitHub Pages setup.
6. Select **Create repository**.

Do not delete `index.html`, `setup/`, `.github/`, or `hackathon.config.yml`.

## 2. Turn on GitHub Pages

This repository deploys with GitHub Actions. Do not select “Deploy from a branch”.

1. In your new GitHub repository, open **Settings**.
2. In the left menu, select **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Open the **Actions** tab in the repository.
5. Forked repositories may show that workflows are disabled. If you see the prompt, select **I understand my workflows, go ahead and enable them**.
6. Open **Deploy to GitHub Pages** in the left-hand workflow list.
7. Select **Run workflow**, choose the `main` branch, then select the green **Run workflow** button.
8. Wait for the workflow to finish with a green check mark.

Your site address will be:

```text
https://<your-github-username>.github.io/<your-repository-name>/
```

The first manual run is important for a fork. Enabling workflows does not automatically rerun the original fork event. The first deployment can take a few minutes. Every later change to the `main` branch starts a new deployment.

## 3. Create registration and submission forms

Google Forms is the simplest option because it stores responses in your private Google Sheets account.

Create two separate Google Forms:

| Form | Suggested required fields |
| --- | --- |
| Registration | Full name, email, team name, team size, chosen track, age group, GitHub or LinkedIn URL (optional) |
| Project submission | Team name, team lead email, project title, track, abstract, public GitHub repository URL, demo URL (optional), video or slides URL (optional) |

For each form:

1. Select **Send**.
2. Select the link icon.
3. Select **Copy**.
4. Save this link; it is the **responder link** that participants can open.

### Use the correct kind of link

Paste only a Google Form responder link in the configuration. It normally ends with `/viewform`.

Good example:

```text
https://docs.google.com/forms/d/e/FORM_ID/viewform
```

Do **not** paste either of these:

- A link ending in `/edit` (it gives access to edit the form)
- A `docs.google.com/document/...` link (it is a Google Doc, not a participant form)

Before publishing, open each responder link in an incognito/private browser window. It must load for a participant who is not signed in as you.

## 4. Generate your website configuration

The configuration generator creates the `hackathon.config.yml` file for you.

### Option A: Use the live generator (recommended)

After Step 2 is deployed, open:

```text
https://<your-github-username>.github.io/<your-repository-name>/setup/
```

Fill in the fields for your event. At minimum, add:

- Event name, tagline, and short description
- Registration, start, submission, and results dates
- Tracks and prizes
- Registration and submission **responder links**
- Judges, mentors, sponsors, FAQ, and contact details as needed

Select **Download hackathon.config.yml** when finished.

### Option B: Use the generator before the site is published

You may open `setup/index.html` directly in a browser and generate the file. The generator works on its own because it does not need to read another file.

If you want to preview the public website on your computer, use the local-server steps in [LOCAL_PREVIEW.md](LOCAL_PREVIEW.md); do not double-click `index.html`.

## 5. Replace the configuration file in GitHub

1. In your GitHub repository, open the root file named `hackathon.config.yml`.
2. Select the pencil icon (**Edit this file**).
3. Select all existing text and paste the contents of the downloaded `hackathon.config.yml` file.
4. Confirm that the file name is exactly `hackathon.config.yml`.
5. Select **Commit changes** and commit directly to the `main` branch.

Do not upload a file named `hackathon.config.yml.txt`. It must keep the `.yml` extension.

## 6. Publish and check the update

1. Open the **Actions** tab after committing your configuration.
2. Wait for **Deploy to GitHub Pages** to finish with a green check mark.
3. Visit your site address.
4. Refresh the page. If it still looks old, do a hard refresh:
   - Windows: `Ctrl + Shift + R`
   - macOS: `Cmd + Shift + R`

The page adds a cache-busting value when it loads the configuration, so updates usually appear as soon as the deployment is complete.

## 7. Test as a participant before sharing

Open the website in an incognito/private browser window and check:

- The event name, description, dates, tracks, prizes, and contact email are correct
- The **Register** button opens the registration form
- The **Submit Project** button opens the submission form
- Both forms are responder forms, not owner/edit forms
- Any judge, mentor, and sponsor links work
- The website looks acceptable on a phone as well as on a computer

Do not publish participant names, emails, medical details, or private Google Sheet links in `hackathon.config.yml`; this file is public.

## 8. Update the website later

To change content at any time:

1. Open the generator again and create a new `hackathon.config.yml`, or edit the existing YAML carefully.
2. Replace the root `hackathon.config.yml` in GitHub.
3. Commit the change to `main`.
4. Wait for the GitHub Actions deployment to succeed.
5. Refresh the live website.

For winners, set `winners.announced` to `true` and add the winning teams in the `winners.list` section. The website will show the winners after deployment.

## Local preview

For detailed local testing instructions, including the common “I changed YAML but nothing changed” problem, follow [LOCAL_PREVIEW.md](LOCAL_PREVIEW.md).

## Troubleshooting

### I changed `hackathon.config.yml`, but the local website did not change

Do not open `index.html` by double-clicking it. When opened as `file:///...`, the browser blocks the page from loading `hackathon.config.yml`.

Run a local web server and open `http://localhost:8000/` instead. See [LOCAL_PREVIEW.md](LOCAL_PREVIEW.md).

### I changed the config on GitHub, but the live website did not change

1. Open the **Actions** tab and wait for the new deployment to finish.
2. Ensure the commit is on the `main` branch.
3. Ensure the edited file is in the repository root and is named exactly `hackathon.config.yml`.
4. Hard refresh the website.

### GitHub Pages shows an error or no site URL

1. Go to **Settings** -> **Pages**.
2. Ensure the source is **GitHub Actions**.
3. Open **Actions** and select the failed workflow to see its error message.
4. Confirm that `.github/workflows/deploy.yml` still exists and has not been changed or deleted.

### Actions says “0 workflow runs” after I fork the repository

GitHub disables workflows in forks until you enable them. Open **Actions**, select **I understand my workflows, go ahead and enable them** if prompted, then open **Deploy to GitHub Pages** and select **Run workflow** for the `main` branch. Wait for the green check mark before opening the Pages URL.

### The Register or Submit button opens the wrong page

Replace the URL with the Google Form responder link. The correct link is a Google Forms URL ending in `/viewform`, not an `/edit` link or a Google Docs link.

### The website stops updating after I edit YAML manually

YAML is sensitive to indentation. Use spaces (not tabs), keep quoted text quoted, and keep child entries indented beneath their headings. The visual generator is the safest way to create the file.

## Security and privacy

This template does not need secrets. Keep all public website content in the configuration file, but never add API keys, passwords, private Google Sheets URLs, form edit links, participant data, or private documents. See [SECURITY.md](SECURITY.md) for details.
