# Hackathon Setup Guide for Organizers

Welcome to the **Reusable Science Hackathon Framework**! This framework allows any rare disorder community or team to set up, launch, and run a science hackathon in under 30 minutes without needing a developer.

---

## Quick Start (3 Steps)

### Step 1: Create your Hackathon Repository
1. Click the **"Use this template"** button at the top right of this GitHub repository.
2. Select **"Create a new repository"**.
3. Name your repository (e.g., `pku-commons-hackathon-2026`).

---

### Step 2: Generate & Edit your Configuration
You can configure your hackathon in one of two ways:

#### Option A: Using the Visual Web UI (Recommended)
1. Open the visual generator: `https://<your-username>.github.io/<your-repo>/setup/`
2. Fill out the simple form:
   - Event Name, Tagline, Disorder Focus Area
   - Registration Link (e.g. Google Form)
   - Challenge Tracks, Prizes, Judges & Mentors
   - Event Schedule & FAQ
   - Theme Colors (Primary & Accent)
3. Click **"Download Config"** to save `hackathon.config.yml`.
4. Upload or drag & drop `hackathon.config.yml` into your GitHub repository to replace the default file.

#### Option B: Editing `hackathon.config.yml` Directly
1. Open `hackathon.config.yml` in your browser or editor on GitHub.
2. Edit text values directly and commit changes to `main`.

---

### Step 3: Deploy your Live Website
1. In your GitHub repository, go to **Settings** → **Pages**.
2. Under **Build and deployment** → **Source**, select **Deploy from a branch**.
3. Choose `main` branch and `/ (root)` folder.
4. Click **Save**.

Your live hackathon site will be published at:
`https://<your-username>.github.io/<your-repo>/`

---

## Submissions & Judging

### Participant Submissions (GitHub Issues)
By default, participants submit their project by opening a pre-formatted GitHub Issue:
- Go to `https://github.com/<your-username>/<your-repo>/issues/new?template=project-submission.md`
- Submissions automatically appear in your repository's **Issues** tab.

### Backup Option (Google Form)
If participants are non-technical, you can provide a Google Form link in `hackathon.config.yml` under `registration.form_url`.

---

## Security Guidelines

- Never commit `.env` files or API secrets to this repository.
- A `.gitignore` and `gitleaks` scanner are pre-configured to protect your repo.
- For complete security instructions, read [`SECURITY.md`](SECURITY.md).
