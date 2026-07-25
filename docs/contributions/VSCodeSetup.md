---
icon: lucide/git-fork
title: How To Setup Zensical In VSCode
---

Welcome to the local development guide for **FRCElectrical.org**. This guide covers the complete end-to-end process for cloning, setting up, and building the documentation site locally.

Our site runs on **Zensical**, the modern, blazing-fast static site generator built by the creators of Material for MkDocs.

---

## 1. Prerequisites

Before you begin, ensure you have the following installed on your machine:
*   **Git:** To clone the repository. ([Download Git](https://git-scm.com/))
*   **Python 3.10 or newer:** Required to run Zensical. ([Download Python](https://www.python.org/downloads/))

Verify your installations by running the following commands in your terminal:
```bash
git --version
python --version
```

---

## 2. Cloning the Repository

First, download the source code from GitHub to your local machine.

Open your terminal or command prompt and run:
```bash
git clone https://github.com/FRCElectrical/FRCElectrical.org.git
cd FRCElectrical.org
```
---

## 3. Setting Up the Environment

It is highly recommended to use a Python virtual environment to prevent dependency conflicts with other projects on your machine.

**Create the virtual environment:**
```bash
python3 -m venv .venv
```

**Activate the virtual environment:**

*   **On macOS and Linux:**
    ```bash
    source .venv/bin/activate
    ```
*   **On Windows:**
    ```cmd
    .venv\Scripts\activate
    ```

Once activated, your terminal prompt should be prefixed with `(.venv)`.

---

## 4. Installing Zensical

With your virtual environment active, install Zensical via `pip`. Zensical is written in Rust and Python, and installing it via pip will automatically fetch the correct binaries for your system.

```bash
pip install zensical
```

---

## 5. Running the Site Locally

To preview your changes as you edit the markdown files, use Zensical's built-in development server. This server leverages the ZRX differential build engine, meaning only changed files are rebuilt, making live reloads 4-5x faster than legacy SSGs.

Run the following command:
```bash
zensical serve
```

Open your web browser and navigate to `http://localhost:8000` (or the port specified in the console output). The site will automatically refresh whenever you save a change to a Markdown file.

---

## 6. Building for Production

When you are ready to deploy the site, you need to compile the Markdown files into static HTML, CSS, and JavaScript.

```bash
zensical build
```

This command generates a `site/` directory (or whichever output directory is specified in your configuration) containing the fully compiled static assets.

---

## 7. Project Structure

Because Zensical maintains high compatibility with Material for MkDocs, the directory structure is intuitive:

```text
FRCElectrical.org/
├── .venv/                 # Local virtual environment (ignored by git)
├── docs/                  # The actual markdown content
│   ├── index.md           # The homepage of the site
│   ├── includes/          # Where the Technical Glossary lives 
│   ├── assets/            # Pictures for the site
│   └── stylesheets/       # Please do not touch this, it is the CSS for the site.
└── zensical.toml          # The main Zensical configuration file 
```

---

## 8. Troubleshooting

**"zensical: command not found"**

- **Cause:** Your virtual environment is likely not activated, or the installation failed.
- **Fix:** Ensure you run `source .venv/bin/activate` (or the Windows equivalent) before running `zensical` commands.

**Build Errors after migrating from MkDocs**

- **Cause:** While Zensical supports `mkdocs.yml` natively, some legacy legacy plugins are not yet fully supported by Zensical's module system.
- **Fix:** Check your `zensical.toml` or `mkdocs.yml` for incompatible plugins and temporarily comment them out, or consult the [Zensical Compatibility Docs](https://zensical.org/compatibility/).

**"Python version not supported"**

- **Cause:** Zensical requires Python 3.10+.
- **Fix:** Upgrade your system's Python version, or use a tool like `pyenv` to manage multiple Python versions.

---

*For more information on contributing to the site content, please see our contributing guidelines. For Zensical specific documentation, visit [zensical.org](https://zensical.org).*
