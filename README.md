<h1>
  <img src="./rhf-logo.png" alt="Reusable Hackathon Framework logo" width="38" valign="middle" style="vertical-align: middle; margin-right: 8px;" />
  Reusable Rare Disease Hackathon Framework
</h1>

A flexible, configuration-driven web application framework designed to quickly launch hackathons for Phenylketonuria (PKU), Maple Syrup Urine Disease (MSUD), or any rare disease community (**PKU First**).

---

## Getting Started & Deployment Guide

To deploy your own rare disease hackathon site:

1. Follow the step-by-step instructions in the **[Full Setup Guide (SETUP.md)](SETUP.md)** to fork this repository and enable GitHub Pages.
2. Customize your hackathon details via `hackathon.config.yml` or use the visual generator at `/setup` on your deployed site.

Your website address will be:
```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/
```

---

## Pre-Configured Disease Presets

The repository includes pre-built disease configuration templates under the [`configs/`](configs) directory:

| Disease / Template | File Path | Description |
| :--- | :--- | :--- |
| **PKU (Phenylketonuria)** | [`configs/hackathon.config.pku.yml`](configs/hackathon.config.pku.yml) | Default live site baseline (phenylalanine accuracy, diet tracking) |
| **MSUD (Maple Syrup Urine Disease)** | [`configs/hackathon.config.msud.yml`](configs/hackathon.config.msud.yml) | MSUD science hackathon preset (BCAA, keto-acid tracking) |
| **Generic Template** | [`configs/hackathon.config.generic.yml`](configs/hackathon.config.generic.yml) | Blank starting template for any rare disease community |

---

## How to Reuse for a New Disease

### Option A: Visual GUI Generator
1. Open `/setup` on your deployed site or locally.
2. Enter your hackathon name, disease focus, tracks, prizes, and judges.
3. Click **Download YAML** and replace `hackathon.config.yml` in your repository.

### Option B: Switch Presets
Copy any preset from the `configs/` folder to the root `hackathon.config.yml`:

```bash
# Example: Switch to MSUD Hackathon
cp configs/hackathon.config.msud.yml hackathon.config.yml
```

Push changes to GitHub to trigger automatic deployment.

---

## Documentation

- [Full Organizer Setup Guide (SETUP.md)](SETUP.md)
- [Local Preview Guide](LOCAL_PREVIEW.md)
- [Security & Compliance](SECURITY.md)
