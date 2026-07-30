# 🧬 Reusable Rare Disease Hackathon Framework

A flexible, config-driven, open-source web application framework designed to quickly launch hackathons for any rare disease or metabolic disorder community (**PKU First**).

---

## 🌟 Key Features

- 🧬 **PKU First Baseline**: Pre-configured defaults tailored specifically for Phenylketonuria (PKU) science hackathons.
- 🔄 **Disease Agnostic & Multi-Disease Presets**: Easily switch between **PKU**, **MSUD (Maple Syrup Urine Disease)**, or custom rare disease hackathons in seconds.
- 🎨 **Visual Setup Generator**: Built-in 1-click visual GUI tool at `/setup` to customize tracks, prizes, dates, judges, mentors, rules, and colors without touching code.
- 📱 **Cross-Device Responsive**: Optimized layout for Mobile (iOS & Android), Tablet, and Desktop.
- 🚀 **Zero-Build GitHub Pages**: Instant static deployment powered by GitHub Actions.

---

## 📁 Pre-Configured Disease Presets

The repository includes pre-built disease configuration templates under the [`configs/`](file:///c:/Users/aksha/Desktop/Reuseable-Framework/configs) directory:

| Disease / Template | File Path | Description |
| :--- | :--- | :--- |
| **PKU (Phenylketonuria)** | [`configs/hackathon.config.pku.yml`](file:///c:/Users/aksha/Desktop/Reuseable-Framework/configs/hackathon.config.pku.yml) | Default live site baseline (phenylalanine accuracy, diet tracking) |
| **MSUD (Maple Syrup Urine Disease)** | [`configs/hackathon.config.msud.yml`](file:///c:/Users/aksha/Desktop/Reuseable-Framework/configs/hackathon.config.msud.yml) | MSUD science hackathon preset (BCAA, keto-acid tracking) |
| **Generic Template** | [`configs/hackathon.config.generic.yml`](file:///c:/Users/aksha/Desktop/Reuseable-Framework/configs/hackathon.config.generic.yml) | Blank starting template for any rare disease community |

---

## ⚡ How to Reuse for a New Disease

1. **Option A (Visual GUI Generator)**:
   - Open [`/setup`](setup/index.html) in your browser.
   - Enter your hackathon name, disease focus, tracks, prizes, and judges.
   - Click **Download YAML** and replace `hackathon.config.yml` in your repository.

2. **Option B (Switch Presets)**:
   - Copy any preset from the `configs/` folder to the root `hackathon.config.yml`:
     ```bash
     # Example: Switch to MSUD Hackathon
     cp configs/hackathon.config.msud.yml hackathon.config.yml
     ```
   - Push your changes to GitHub and GitHub Pages will auto-deploy!

---

## 📚 Documentation Links

- 📖 [Full Setup & Customization Guide](SETUP.md)
- 💻 [Local Preview Guide](LOCAL_PREVIEW.md)
- 🔒 [Security & Compliance](SECURITY.md)
