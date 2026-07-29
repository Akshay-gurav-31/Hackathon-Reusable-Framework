# Security and Privacy Guide

This is a static website framework. It has no backend, database, API key, or server-side environment variables.

## No secrets are required

You do not need to add an API key, GitHub token, Google password, or payment credential to use this template. GitHub Pages hosting and Google Forms work without putting a secret in this repository.

The `.pre-commit-config.yaml` file is kept as optional protection. When a developer installs it locally, it runs Gitleaks before a commit and helps catch an accidentally pasted token or password. It does not affect the website or visitors.

To enable the optional check on a developer computer:

```powershell
python -m pip install pre-commit
pre-commit install
```

Organizers who only edit files through the GitHub website do not need to install or run this command.

## Keep these items private

Never commit or publish:

- API keys, access tokens, passwords, private keys, or `.env` files
- Google Form **edit** links or private Google Sheet links
- Participant names, emails, medical information, or other personal data
- Private documents, contracts, or internal contact lists

The repository is public when hosted through free GitHub Pages. Treat every file in it as public.

## Safe public content

It is safe to publish:

- Event name, schedule, tracks, rules, prizes, FAQs, and public contact email
- Public registration and submission **responder links** from Google Forms
- Public project repository, demo, sponsor, and social media links
- Logos and public profile photos that you have permission to use

## Google Forms

Only add the responder link that participants use to fill out a form. It typically ends in `/viewform`.

Before sharing, test the link in an incognito/private browser window. Keep form edit links and response spreadsheets private in your Google account.

## Reporting a security concern

If you find a security concern with this framework, open a GitHub Issue or contact the repository maintainer privately.
