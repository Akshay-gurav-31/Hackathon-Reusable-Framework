# Hackathon Setup Guide for Organizers

Welcome to the **Reusable Science Hackathon Framework**! This framework allows any rare disorder community or team to set up, launch, and run a science hackathon in under 30 minutes.

---

## 🚀 Step 1: Create Google Forms for your Event

Go to [Google Forms](https://docs.google.com/forms/) and create two simple blank forms. Fill in the exact fields below:

### 1. Participant Registration Form
* **Form Title:** `[Your Hackathon Name] - Participant Registration`
* **Form Settings:**
  - Turn **ON** `Collect email addresses`
  - Turn **ON** `Limit to 1 response` (Prevents duplicate entries)
  - Turn **ON** `Allow response editing` (Allows participants to update team details)
* **Fields to Add:**
  1. **Full Name** (Short Answer, *Required*)
  2. **Participation Type** (Dropdown: `Solo` / `Team` / `Looking for a Team`, *Required*)
  3. **Team Name** (Short Answer, *Required* - *Note: Ask Solo participants to write their own name or creative alias*)
  4. **Team Size** (Dropdown: `1`, `2`, `3`, `4`, *Required*)
  5. **Challenge Track** (Dropdown: Enter your event tracks, *Required*)
  6. **GitHub / LinkedIn URL** (Short Answer, *Optional*)

---

### 2. Project Submission Form (Alternative Submission Method)
* **Form Title:** `[Your Hackathon Name] - Project Submission`
* **Form Settings:**
  - Turn **ON** `Collect email addresses`
  - Turn **ON** `Limit to 1 response`
  - Turn **ON** `Allow response editing`
* **Fields to Add:**
  1. **Team Name** (Short Answer, *Required*)
  2. **Project Title** (Short Answer, *Required*)
  3. **Challenge Track** (Dropdown, *Required*)
  4. **GitHub Repository URL** (Short Answer, *Required*)
  5. **Demo Video / Slides URL** (Short Answer, *Optional*)

---

## 🛠️ Step 2: Configure your Hackathon Website

1. Fork or template-copy this repository to your GitHub account.
2. Open the Visual Config Generator in your browser:  
   `https://<your-username>.github.io/<your-repo>/setup/`
3. Fill out the form with your hackathon details.
4. **Important:** Copy the **Send/Responder links** of the Google Forms you created in **Step 1** and paste them into the **Registration** and **Submission** URL input fields in the generator.
5. Click **Download Config** to save `hackathon.config.yml`.
6. Replace the `hackathon.config.yml` file in your repository's root directory with the downloaded file.

---

## 🌐 Step 3: Deploy your Live Website

1. Go to **Settings** → **Pages** in your GitHub repository.
2. Under **Build and deployment** → **Source**, select **Deploy from a branch**.
3. Choose `main` branch and `/ (root)` folder.
4. Click **Save**.

Your live hackathon page is automatically built, optimized, and deployed!

---

## 🔒 Security Guidelines

- Never commit real secrets or credentials to this repository.
- A `.gitignore` and `gitleaks` pre-commit scanning hook are active by default to protect the repo. For details, read [`SECURITY.md`](SECURITY.md).
