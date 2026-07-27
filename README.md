# Hackathon Reusable Framework

A zero-cost, plug-and-play framework designed for rare disease communities to launch a full science hackathon website in under 30 minutes.

## 🌟 Key Features

- **No-Code Configuration**: Organizers can generate and update `hackathon.config.yml` visually using the built-in UI Generator (`/setup/index.html`).
- **Zero-Cost Static Hosting**: Deploy instantly to GitHub Pages with no backend or database required.
- **Standardized Submissions**: Peer-reviewed audit trails powered by pre-formatted GitHub Issue templates.
- **Security-First**: Pre-configured secret scanning via Gitleaks pre-commit hooks and `.gitignore`.
- **Dynamic & Customizable**: HSL-tailored color themes, customizable SVG branding, and clean responsive layouts.

---

## 🚀 Quick Start for Organizers

1. **Generate Configuration**:
   Open `setup/index.html` in your browser (or via the live site) to use the UI Generator and build your custom `hackathon.config.yml`.
2. **Add to Repo**:
   Place your generated `hackathon.config.yml` into the root directory of your repository.
3. **Deploy**:
   Enable GitHub Pages under **Settings > Pages** (Source: `main` branch).

For a complete step-by-step setup guide, see [SETUP.md](SETUP.md).

---

## 🛠️ Security & Compliance

Secret protection rules and pre-commit hook setups are documented in [SECURITY.md](SECURITY.md).

---

## 📄 License

Distributed under the MIT License. See [SETUP.md](SETUP.md) for full project setup and guidelines.
