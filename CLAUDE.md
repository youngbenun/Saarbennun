# CLAUDE.md — AI Assistant Guide for Saarbennun

## Project Overview

This is a **personal portfolio website** for Saar Ben Nun. It is a single static HTML file with embedded CSS — no build tools, no backend, no dependencies.

**Repository:** `youngbenun/Saarbennun`
**Live entry point:** `Index.html`

---

## Repository Structure

```
Saarbennun/
├── Index.html   # The entire website — HTML markup + embedded CSS
└── CLAUDE.md    # This file
```

There are no subdirectories, no configuration files, and no package managers involved.

---

## Tech Stack

| Layer      | Technology          |
|------------|---------------------|
| Markup     | HTML5               |
| Styling    | CSS3 (embedded)     |
| Scripting  | None (vanilla HTML) |
| Backend    | None                |
| Build tool | None                |

---

## Running the Site

Open `Index.html` directly in any browser, or serve it with any static file server:

```bash
# Python (no install needed)
python3 -m http.server 8080

# Node.js (requires npx)
npx http-server .
```

There is no build step, no compilation, and no dependency installation required.

---

## File Details: Index.html

The entire site lives in `Index.html`. Key sections inside the file:

| Section           | CSS class / element | Purpose                                    |
|-------------------|---------------------|--------------------------------------------|
| Page title        | `<header> h1`       | Displays "Saar Ben Nun" in cyan            |
| Biography         | `.bio`              | Short personal description paragraph       |
| Contact info      | `.contact`          | Email and phone number (currently placeholder values) |
| Social media      | `.social`           | LinkedIn, Twitter, GitHub links (currently placeholder URLs) |
| Footer            | `<footer>`          | Copyright notice                           |

### Design conventions (CSS)

- **Color scheme:** Dark background (`#1a1a1a`), light body text (`#e0e0e0`), cyan accent (`#00ffcc`)
- **Header/footer background:** `#333`
- **Font:** `Arial`, sans-serif
- **Link color:** `#00ffcc`; underline appears on `:hover`
- **Section headings (`h2`):** Underlined with a `2px solid #00ffcc` bottom border
- **Layout:** Simple vertical stack; sections use `padding: 20px`
- **CSS lives entirely inside a `<style>` block in `<head>`** — there is no external stylesheet

### Placeholder values that need real data

The following fields in `Index.html` are currently placeholders and should be updated with real information:

| Field         | Current placeholder value                                | Line |
|---------------|----------------------------------------------------------|------|
| Email         | `yourname@example.com`                                   | 87   |
| Phone         | `+123-456-7890`                                          | 88   |
| LinkedIn URL  | `https://www.linkedin.com/in/yourprofile`                | 92   |
| Twitter URL   | `https://twitter.com/yourhandle` / `@yourhandle`         | 93   |
| GitHub URL    | `https://github.com/yourusername`                        | 94   |
| Copyright year| `2024`                                                   | 98   |

---

## Development Workflow

Because there is no build system, the workflow is simple:

1. Edit `Index.html` directly.
2. Reload the browser to preview changes.
3. Commit and push when done.

```bash
git add Index.html
git commit -m "Describe what changed"
git push -u origin <branch-name>
```

### Branching

- `main` — production branch
- Feature work should be done on a dedicated branch and merged via pull request.

---

## What AI Assistants Should Know

- **Do not introduce JavaScript, external CSS files, or build tooling** unless the user explicitly requests it — the simplicity of a single HTML file is intentional.
- **Preserve the existing color scheme and layout** unless asked to redesign.
- **All CSS changes go inside the `<style>` block** in `<head>` — do not create a separate `.css` file.
- **There are no tests** — verify changes by opening the file in a browser.
- **The file uses standard HTML5 semantics** (`<header>`, `<section>`, `<footer>`) — continue using semantic elements for any additions.
- **Placeholder contact/social data** is still present (see table above) — avoid hardcoding or referencing these as real values.
- **Copyright year is `2024`** and should be updated if the site is actively maintained.
