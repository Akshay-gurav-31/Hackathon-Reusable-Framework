# Security Policy & Credential Hygiene

Security is a core requirement for this framework. Accidental credential leaks (e.g. OpenAI or Anthropic API keys pushed to public GitHub repositories) expose organizers to financial risk and compromised infrastructure.

This framework enforces zero-trust credential hygiene by design.

---

## Preventative Measures

### 1. `.env` Secret Protection
- **No secrets in git:** All API keys, passwords, and private tokens must stay in local `.env` files.
- `.env` files are strictly listed in `.gitignore` and must **NEVER** be committed.
- A template file [`.env.example`](.env.example) is provided with placeholder names.

### 2. Pre-Commit Credential Scanning (`gitleaks`)
This repository includes a pre-configured `.pre-commit-config.yaml` using **gitleaks**.

To activate local scanning before every commit:
```bash
pip install pre-commit
pre-commit install
```
If you accidentally stage a string matching an API key, `gitleaks` will automatically abort the commit.

---

## What to do if a Secret is Exposed

If an API key or credential was committed in past git history:
1. **Immediately Revoke / Rotate the Secret:**
   - Log into the provider dashboard (e.g. OpenAI, Anthropic, AWS) and delete/revoke the exposed key immediately.
2. **Purge Git History:**
   - Use `git-filter-repo` or BFG Repo-Cleaner to strip the secret from all historic commits.
   - Do not simply delete the line in a new commit; git history preserves deleted lines.
3. **Notify Repository Admin:**
   - Report any credential leaks to the repository maintainers.
