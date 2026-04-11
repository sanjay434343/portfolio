# README.md
## Project Overview

A software project consisting of **6** source files spanning .md, .html. Documentation generated locally from file metadata (no remote AI).


## Features

- Command-driven CLI architecture
- Automated documentation generation
- GitHub repository integration
- Local fallback mode (no API required)


## File Structure

- `index.html` — 1123 lines · 17 fn · 0 imports *(large)*
- `README.md` — 56 lines · 0 fn · 0 imports
- `docs/architecture.md` — 9 lines · 0 fn · 0 imports
- `docs/usage.md` — 9 lines · 0 fn · 0 imports
- `docs/onboarding.md` — 8 lines · 0 fn · 0 imports
- `docs/security.md` — 8 lines · 0 fn · 0 imports


# Architecture

Command-driven single-responsibility modules under `commands/`.
An entry-point CLI (`index.js`) delegates to commands.

### Top modules (by heuristic score)

- **index.html** — complexity: 16, exports: 0
- **README.md** — complexity: 0, exports: 0
- **docs/architecture.md** — complexity: 0, exports: 0
- **docs/usage.md** — complexity: 0, exports: 0
- **docs/onboarding.md** — complexity: 0, exports: 0
- **docs/security.md** — complexity: 0, exports: 0


# Onboarding

1. Clone the repository: `git clone <repo-url>`
2. Install dependencies: `npm install`
3. (Optional) Link globally: `npm link`
4. Configure API key: `cdx config`
5. Generate docs: `cdx create README.md`


# Usage

```bash
cdx create README.md       # Generate full documentation
cdx create docs.md --all   # Include hidden files
cdx config                 # Set Gemini API key
cdx start                  # Interactive UI
```


# Security

- **No raw source code** is transmitted in local fallback mode.
- API keys stored in `~/.mycli-config.json` with `0o600` permissions.
- Sensitive files (`.env`, private keys, credentials) are excluded from AI payloads.
- GitHub tokens are redacted before any network call.
- Review and rotate credentials regularly.
