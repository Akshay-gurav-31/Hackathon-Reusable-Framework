# Simple Setup Guide for Organizers

This guide shows how to create, publish, and update your hackathon website without writing code.

You will do this once:

1. Fork the repository
2. Turn on GitHub Pages
3. Create two Google Forms
4. Fill in the website setup form
5. Paste the generated configuration into GitHub
6. Wait for the website to publish

After this, changing the website is easy: update the configuration file, commit it, and wait for the website to refresh.

## Before you start

You need:

- A GitHub account
- A Google account
- Your event name, dates, tracks, prizes, and contact email

You do **not** need an API key, database, server, or coding knowledge.

---

## Part 1: Fork the repository

1. Open the hackathon framework repository on GitHub.
2. Select **Fork** in the top-right corner.
3. Choose your GitHub account or organization.
4. Keep the repository name or change it to your event name.
5. Select **Create fork**.

Keep this repository **Public**. This is the easiest way to use free GitHub Pages hosting.

---

## Part 2: Publish the first version of the website

### Step 1: Turn on GitHub Pages

1. In your forked repository, select **Settings**.
2. In the left menu, select **Pages**.
3. Under **Build and deployment**, choose **GitHub Actions** as the source.
4. Leave **Custom domain** empty unless you already own a domain for the event.

Do not choose “Deploy from a branch”. This repository uses GitHub Actions.

### Step 2: Enable and run the deployment workflow

1. Select the **Actions** tab in the repository.
2. If GitHub shows an enable button, select **I understand my workflows, go ahead and enable them**.
3. In the left workflow list, select **Deploy to GitHub Pages**.
4. Select **Run workflow**.
5. Keep the branch as `main`.
6. Select the green **Run workflow** button.

GitHub will start the first deployment. Wait until the workflow has a green check mark.

The first deployment can take a few minutes. After it succeeds, your website address is:

```text
https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPOSITORY-NAME/
```

Example:

```text
https://elizabiopro.github.io/Hackathon-Reusable-Framework/
```

If the URL shows “There isn't a GitHub Pages site here”, wait for the workflow to finish and refresh the page.

---

## Part 3: Create Google Forms

Create one form for registration and one form for project submissions.

[Open Google Forms](https://docs.google.com/forms/u/0/)

Tip: open this link in a new tab so you can come back to the setup guide easily.

### Form A: Participant registration

Create a blank form with this title:

```text
YOUR HACKATHON NAME - Participant Registration
```

Suggested required questions:

1. Full Name
2. Email Address
3. Are you participating solo or in a team?
4. Team Name
5. Team Size
6. Challenge Track
7. Age Group
8. GitHub or LinkedIn URL (optional)

Suggested description:

```text
Register to participate in our hackathon. Solo participants and teams are welcome.
Each team member must register separately. Use the same team name for every member of a team.
```

Suggested question types:

| Question | Type | Required |
| --- | --- | --- |
| Full Name | Short answer | Yes |
| Email Address | Short answer | Yes |
| Are you participating solo or in a team? | Multiple choice | Yes |
| Team Name | Short answer | Yes |
| Team Size | Short answer | Yes |
| Challenge Track | Dropdown | Yes |
| Age Group | Dropdown | Yes |
| GitHub or LinkedIn URL [optional] | Short answer | No |

### Form B: Project submission

Create a second blank form with this title:

```text
YOUR HACKATHON NAME - Project Submission
```

Suggested required questions:

1. Team Name
2. Team Lead Email
3. Project Title
4. Challenge Track
5. Project Summary
6. Public GitHub Repository URL
7. Live Demo URL (optional)
8. Demo Video or Slides URL (optional)

Suggested description:

```text
Submit one project per team. Your GitHub repository must be public so judges can review it.
```

Suggested question types:

| Question | Type | Required |
| --- | --- | --- |
| Team Name | Short answer | Yes |
| Team Lead Email | Short answer | Yes |
| Project Title | Short answer | Yes |
| Challenge Track | Dropdown | Yes |
| Project Summary | Paragraph | Yes |
| Public GitHub Repository URL | Short answer | Yes |
| Live Demo URL [optional] | Short answer | No |
| Demo Video or Slides URL [optional] | Short answer | No |

### Copy the correct form links

For each Google Form:

1. Select **Send** in the top-right corner.
2. Select the link icon.
3. Select **Copy**.
4. Save the copied link.

This is the public link participants use. It normally starts with `https://forms.gle/` or ends in `/viewform`.

Do **not** copy:

- A link ending in `/edit`
- A `docs.google.com/document/...` link
- Your private Google Sheets response link

Before moving on, test both copied links in an incognito/private browser window. A participant should be able to open them without seeing an edit screen.

---

## Part 4: Fill in the website setup form

After the first website deployment succeeds, open this address:

```text
https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPOSITORY-NAME/setup/
```

Example:

```text
https://elizabiopro.github.io/Hackathon-Reusable-Framework/setup/
```

This is the **Hackathon Config Generator**. Fill in the fields you want to show on the public website:

- Event name, tagline, and description
- Dates and deadlines
- Challenge tracks
- Prizes
- Judges, mentors, and sponsors
- Rules, schedule, FAQ, and contact email
- Registration Google Form link
- Submission Google Form link
- Colors and logo URL

The setup page saves your work in the same browser automatically. If you refresh the page, your draft stays there. Select **Reset** only if you want to clear your saved draft and return to the example values.

The form checks your Google Form links. A Google Docs or `/edit` link will show an error and cannot be downloaded.

When you finish, select **Download Config**. Your browser downloads a file called:

```text
hackathon.config.yml
```

---

## Part 5: Put the configuration file into GitHub

1. Return to the main page of your GitHub repository.
2. Open the root file named `hackathon.config.yml`.
3. Select the pencil icon: **Edit this file**.
4. Select all existing content in the file.
5. Open the downloaded `hackathon.config.yml` file and copy all its content.
6. Paste it into GitHub, replacing the old content.
7. Scroll down and select **Commit changes**.
8. Commit directly to the `main` branch.

Do not rename the file. It must stay exactly:

```text
hackathon.config.yml
```

Do not upload or save it as `hackathon.config.yml.txt`.

---

## Part 6: Wait for the updated website

1. Open the **Actions** tab in your GitHub repository.
2. A new **Deploy to GitHub Pages** workflow should be running automatically.
3. Wait until it has a green check mark.
4. Open your public website URL in a new browser tab or an incognito/private window.
5. Refresh the page.

The update usually appears within a few minutes. Sometimes GitHub Pages needs a little longer after the workflow turns green. If you still see the old page, wait 2–3 minutes and refresh again.

Check these items before sharing the website:

- Event name, dates, tracks, prizes, and contact email are correct
- **Register** opens the registration Google Form
- **Submit Project** opens the submission Google Form
- The forms are participant forms, not edit forms
- The website looks good on a phone as well as on a computer

---

## How to change the website later

You have three simple options.

### Option 1: Use the setup page again

Open your `/setup/` URL, edit the fields, download a new `hackathon.config.yml`, and replace the file in GitHub again.

### Option 2: Edit one small item directly in GitHub

For a small change, such as a date, prize amount, or email address:

1. Open `hackathon.config.yml` in GitHub.
2. Select the pencil icon.
3. Change only the text you need.
4. Select **Commit changes**.
5. Wait for the new Actions workflow to finish with a green check mark.

Use spaces, not tabs, when editing YAML. Keep the same indentation as the lines around it.

### Option 3: Ask an AI chat tool to update the YAML

You can copy your full current `hackathon.config.yml` file into ChatGPT, Claude, Gemini, Grok, or another AI chat tool.

Use this prompt:

```text
This is my current hackathon.config.yml file.
Make only this change: [DESCRIBE THE CHANGE].

Keep every other value and the same YAML structure unchanged.
Return the complete updated YAML file only. Do not add explanations or Markdown.
```

Copy the complete YAML response, replace the full content of `hackathon.config.yml` in GitHub, commit the change, and wait for the deployment to finish.

Never paste passwords, API keys, private Google Sheet links, Google Form edit links, or participant data into an AI chat tool or this public repository.

---

## If something does not work

### The website shows a 404 page

Open **Settings** -> **Pages** and make sure the source is **GitHub Actions**. Then open **Actions**, run **Deploy to GitHub Pages**, wait for the green check mark, and refresh the website URL.

### The website still shows old content

Make sure your change was committed to `main`. Then wait for the newest Actions workflow to finish. Open the website in an incognito/private browser window and refresh after a few minutes.

### The Register or Submit button opens the wrong page

Replace the link in the setup form with the public Google Form responder link. Do not use an `/edit` link or a Google Docs link.

### I changed YAML and the website looks broken

Go back to the setup page and create a new configuration file. It is safer than manually changing a large YAML file.

---

Once you complete this workflow once, future updates are simple: change the configuration, commit it, wait for the green check mark, and refresh your website.
