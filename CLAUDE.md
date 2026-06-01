# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A single-file static HTML portfolio page (`index.html`) built as the submission response to a UNU-INWEH longlist notification for the **Geospatial Application and Data Analytics Associate (PSA5)** position. The page directly addresses the 7 evaluation areas requested by UNU-INWEH HR (contact: Jeeyun Han). No build tools, package managers, frameworks, or tests — everything is self-contained in one file.

## UNU-INWEH submission context

All content in `index.html` maps to the 7 categories explicitly requested in the longlist email. Each section must demonstrate, per project:

- Exact role and responsibilities
- Tools/technologies used
- Live reference links (where available)
- Screenshots or sanitized code snippets
- GitHub repositories (where available)

**The 7 required categories and their nav anchors:**

| # | Category | Anchor |
|---|----------|--------|
| 1 | Geospatial & GIS Experience | `#geo` |
| 2 | Web Applications & Full-Stack Development (Python/Django or React) | `#web` |
| 3 | Cloud Infrastructure (AWS, Google Cloud, etc.) | `#cloud` |
| 4 | Version Control & Deployment Workflows | `#devops` |
| 5 | Content Management Systems (WordPress, Drupal, etc.) | `#cms` |
| 6 | LMS Management | `#lms` |
| 7 | ICT / SharePoint Administration | `#ict` |

The submission deadline was **Sunday 31 May 2026 at 11:59 PM EST**. The page was built and submitted in response to this deadline.

## Development

Open `index.html` directly in a browser. No server required.

## Architecture

All HTML, CSS, and JavaScript live in `index.html`:

- **Styles** — inline `<style>` block with a CSS custom properties design system (CSS vars for colors, spacing, radius). Color palette: `--navy`, `--teal`, `--amber`, `--green`, `--purple`, `--slate`, `--rose`.
- **Fonts** — Google Fonts: DM Serif Display (headings), DM Sans (body), DM Mono (code/stats).
- **Layout** — sticky nav + 7 content sections (`#geo`, `#web`, `#cloud`, `#devops`, `#cms`, `#lms`, `#ict`), each with a consistent `.section-header` + `.pcard` card pattern.
- **JavaScript** — a small scroll listener (~8 lines) that updates the active nav item based on scroll position. No external JS libraries.

## Key conventions

- Badge/tag colors follow a consistent naming scheme: `.b-teal`, `.b-amber`, `.b-navy`, `.b-green`, `.b-purple`, `.b-rose`, `.b-slate`, `.b-live`.
- Section icons use `.sec-icon` + a color modifier (`.si-teal`, `.si-amber`, etc.) matching the section's theme color.
- Cards use `.pcard` > `.pcard-head` + `.pcard-body`. Inside body: `.hq` for strategic impact quotes, `.role-block` for role descriptions, `.bullets` for bullet lists, `.tech-row` + `.tech-tag` for tech stacks, `.links-row` + `.lbtn` for action buttons.
- Architecture diagrams use `.arch` > `.arch-node` + `.arch-arr` (arrow `→`) in a flex row.
- Code samples use `.code-block` > `.code-lbl` + `<pre>` with syntax color classes: `.cc` (comment), `.ck` (key), `.cv` (value), `.cs` (string).
