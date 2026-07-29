# Reusable Hackathon Framework

Fork this repository to make and publish your own hackathon website. You do not need to write code.

## What you need

- A GitHub account
- A Google account for registration and submission forms
- Your event name, dates, tracks, prizes, and contact email

## Start in 5 simple steps

1. Open this repository on GitHub. Select the **Fork** button in the top-right corner, then select **Create fork**. Keep the new repository **Public**.

2. Open **Settings** -> **Pages** and select **GitHub Actions**.

3. Open the **Actions** tab. If this is a fork, enable workflows if GitHub asks. Then open **Deploy to GitHub Pages** and select **Run workflow** once.

4. When the workflow has a green check mark, open your setup page:

   ```text
   https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/setup/
   ```

5. Fill in the form, download `hackathon.config.yml`, and replace the file with the same name in your GitHub repository. Commit the change. Your site will update automatically.

Your website address is:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/
```

## Important

For registration and submission, use the public Google Form link that participants fill in. It should end in `/viewform` or start with `forms.gle/`.

Do not use a Google Docs link or a Google Form `/edit` link.

## Need help?

- [Full setup guide](SETUP.md)
- [How to test the site on your computer](LOCAL_PREVIEW.md)
- [What is safe to publish](SECURITY.md)
