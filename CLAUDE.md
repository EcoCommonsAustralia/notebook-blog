# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **EcoCommons Notebook Blog** — a [Quarto](https://quarto.org) website that publishes ecological and spatial analysis tutorials as HTML pages. The site is hosted on GitHub Pages and served from the `docs/` folder.

## Key Commands

```bash
# Build the entire site (run from repo root)
quarto render

# Preview with live reload
quarto preview

# Render a single notebook
quarto render notebooks/<folder>/<file>.qmd
```

## Architecture

- **`_quarto.yml`** — controls site structure, navbar menus, output directory (`docs/`), and global HTML format settings. Adding a new notebook to the navbar requires editing this file.
- **`notebooks/`** — source QMD files, organized by topic (mirrors the navbar hierarchy). Each notebook lives in its own subfolder.
- **`docs/`** — generated HTML output. **Never edit manually** — it is entirely produced by `quarto render`.
- **`_freeze/` and `.quarto/_freeze/`** — execution cache (freeze: auto). Notebooks re-execute only when their source changes.
- **`styles/ec_html_template.css`** — global site styling.
- **`footer.html`** — injected after every page body. Edit via the upstream `ec-notebook_site_materials` repo (render `footer.qmd` there, then replace here).

## Adding a New Notebook

1. Create `notebooks/<name>/` and place the `.qmd` file there.
2. Add a `.gitignore` inside that folder to exclude large downloaded datasets.
3. Add the notebook to the appropriate navbar menu in `_quarto.yml`.
4. Run `quarto render` from the repo root.
5. Commit everything including the updated `docs/` output.

## Related Repositories

- **[EcoCommonsAustralia/notebooks](https://github.com/EcoCommonsAustralia/notebooks)** — the upstream source repo containing all `.ipynb` and `.qmd` notebook files. This blog renders the `.qmd` files from there into HTML. The notebooks repo also maintains `automation/notebooks-table-data.csv`, which stores the `econotebook_blogpost_path` links pointing back to pages on this site.
- **[EcoCommons-Australia-2024-2026/ec-notebook_site_materials](https://github.com/EcoCommons-Australia-2024-2026/ec-notebook_site_materials)** — shared images and the `footer.qmd` source.

**Data flow:** The `notebooks` repo is the source of truth for executable content. This blog renders those `.qmd` files as HTML and publishes them via GitHub Pages. The `notebooks` repo README table links back here using auto-generated EcoNotebook badges.
