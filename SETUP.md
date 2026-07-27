# Hackathon Setup Guide for Organizers

Welcome to the **Reusable Science Hackathon Framework**! This framework allows any rare disorder community or team to set up, launch, and run a science hackathon in under 30 minutes.

---

## 🚀 Step 1: Create Google Forms for your Event

Go to [Google Forms](https://docs.google.com/forms/u/0/) and create two separate blank forms. Fill in the exact fields below:

---

### 📋 Form 1: Participant Registration Form

**Form Title:** `[Your Hackathon Name] - Participant Registration`

**Form Description (paste this at the top):**
```
Register to participate in [Hackathon Name]! Fill out the details below to secure your spot.

• Solo participants: Use your own name or a creative alias as your Team Name.
• Team members: Each member must register individually using the same Team Name.
• One registration per email address.

Registration Deadline: [Your Date Here]
```

**Settings (click the ⚙️ Settings tab in Google Forms):**
- ✅ Turn **ON** → `Collect email addresses`
- ✅ Turn **ON** → `Limit to 1 response` *(prevents duplicate registrations)*
- ✅ Turn **ON** → `Allow response editing` *(lets participants fix mistakes)*

**Fields to Add (in this order):**

| # | Field Label | Field Type | Required? |
|---|---|---|---|
| 1 | Full Name | Short Answer | ✅ Yes |
| 2 | Are you participating as? | Dropdown: `Solo` / `Team` / `Looking for a Team` | ✅ Yes |
| 3 | Team Name | Short Answer | ✅ Yes |
| 4 | Team Size | Dropdown: `1` / `2` / `3` / `4` | ✅ Yes |
| 5 | Challenge Track | Dropdown *(add your event tracks)* | ✅ Yes |
| 6 | Age Group | Dropdown: `Under 18` / `18–24` / `25 or above` | ✅ Yes |
| 7 | GitHub / LinkedIn URL | Short Answer | ❌ Optional |

> **Team Name Note:** In the field description write: *"Solo participants: please use your own name or a creative alias (e.g. 'Solo_Raj'). Team members: all team members must use the exact same Team Name."*

**After creating the form:**
1. Click the **Send** button (paper plane icon) at the top right.
2. Click the **🔗 Link icon** tab.
3. Click **"Copy link"** — this is your **Registration Form Responder Link**.
4. Save this link. You will paste it in Step 2.

---

### 📋 Form 2: Project Submission Form

**Form Title:** `[Your Hackathon Name] - Project Submission`

**Form Description:**
```
Submit your hackathon project here. Each team submits only once.

• Only one submission per team. The Team Lead should submit on behalf of the team.
• Make sure your GitHub repository is public before submitting.
• Submissions after the deadline will not be accepted.

Submission Deadline: [Your Date Here]
```

**Settings (click the ⚙️ Settings tab):**
- ✅ Turn **ON** → `Collect email addresses`
- ✅ Turn **ON** → `Limit to 1 response` *(prevents duplicate submissions)*
- ✅ Turn **ON** → `Allow response editing` *(lets teams update their links before deadline)*

**Fields to Add (in this order):**

| # | Field Label | Field Type | Required? |
|---|---|---|---|
| 1 | Team Name | Short Answer | ✅ Yes |
| 2 | Team Lead Email | Short Answer | ✅ Yes |
| 3 | Project Title | Short Answer | ✅ Yes |
| 4 | Challenge Track | Dropdown *(same tracks as Registration Form)* | ✅ Yes |
| 5 | Project Abstract | Paragraph *(max 200 words description)* | ✅ Yes |
| 6 | GitHub Repository URL | Short Answer | ✅ Yes |
| 7 | Live Demo / Website URL | Short Answer | ❌ Optional |
| 8 | Demo Video / Slides URL | Short Answer | ❌ Optional |
| 9 | Anything else to share? | Paragraph | ❌ Optional |

> **GitHub Repository Note:** In the field description write: *"Make sure your repository is set to Public before submitting. Private repositories cannot be reviewed by judges."*

**After creating the form:**
1. Click the **Send** button at the top right.
2. Click the **🔗 Link icon** tab.
3. Click **"Copy link"** — this is your **Submission Form Responder Link**.
4. Save this link. You will paste it in Step 2.

---

## 🛠️ Step 2: Configure Your Hackathon Website

1. **Fork or template-copy** this repository to your GitHub account.  
   *(Click the "Use this template" button at the top of this repo on GitHub.)*

2. **Open the Visual Config Generator** in your browser:  
   `https://<your-username>.github.io/<your-repo>/setup/`

3. **Fill out the form** with your hackathon details:
   - Event Name, Tagline, Dates, Tracks, Prizes, Judges, Schedule, FAQ, Colors

4. In the **Registration** section of the generator:
   - Paste your **Registration Form Responder Link** (from Form 1 above) in the **Registration Google Form URL** field.
   - Paste your **Submission Form Responder Link** (from Form 2 above) in the **Submission Google Form URL** field.

5. Click **"Download Config"** to save `hackathon.config.yml`.

6. Go to your GitHub repository → find `hackathon.config.yml` in the file list → click it → click the **pencil (edit) icon** → delete all existing content → paste the downloaded YAML content → click **"Commit changes"**.

---

## 🌐 Step 3: Deploy Your Live Website

GitHub Pages auto-deployment is already configured in this framework via GitHub Actions. Your site deploys automatically on every push.

**First-time setup only:**
1. Go to **Settings** → **Pages** in your GitHub repository.
2. Under **Build and deployment** → **Source**, select **"Deploy from a branch"**.
3. Choose `main` branch and `/ (root)` folder.
4. Click **Save**.

Your live hackathon site will be published at:  
`https://<your-username>.github.io/<your-repo>/`

> ⏱️ First deployment takes 2–3 minutes. After that, every push auto-deploys in under 1 minute.

---

## 📬 Step 4: How Participant Submissions Work

Once your site is live, participants will go through this flow:

### Registration Flow:
1. Participant visits your live hackathon website.
2. They click **"Register Now"**.
3. Your **Registration Google Form** opens in a new tab.
4. They fill it out. All responses are collected in your **Google Sheets** automatically.

### Submission Flow:
1. Participant visits your live hackathon website during the submission window.
2. They click **"Submit Project"**.
3. Your **Submission Google Form** opens in a new tab.
4. They fill out their project details. All submissions appear in your **Google Sheets**.

### Viewing Responses (as Organizer):
1. Open your Google Form.
2. Click the **"Responses"** tab at the top.
3. Click the **Google Sheets icon** to open all responses in a spreadsheet.
4. You can sort/filter by **Team Name**, **Track**, or any other field to manage registrations and submissions.

---

## 🔒 Security Guidelines

- Never commit real API keys or passwords to this repository.
- A `.gitignore` and `gitleaks` pre-commit scanning hook are pre-configured to protect the repo.
- For complete security instructions, read [`SECURITY.md`](SECURITY.md).
