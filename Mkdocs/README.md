# My Docs Project

This is a documentation website project built with [MkDocs](https://www.mkdocs.org/) and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

This document serves as the central README for the project, outlining its structure, features, and the specific details of each file.

---

## Chapter 1: Project Overview & Features

This project has been configured with several key features:

- **Theme:** Uses the powerful **Material for MkDocs** theme.
- **Custom Navigation:** A multi-level main navigation menu is configured in `mkdocs.yml`.
- **On-Page Table of Contents:** A right-side navigation menu ("On this page") is automatically generated for pages with subheadings, thanks to the Material theme and the `toc` extension.
- **Custom CSS:** A custom stylesheet at `docs/css/custom.css` has been implemented to apply unique styles.

---

## Chapter 2: File-by-File Analysis

This section provides a detailed breakdown of every file and its current configuration.

### 1. `mkdocs.yml` (The Master Configuration)

This is the central configuration file for the entire project, controlling its behavior and appearance. Here is a detailed look at its current settings:

- **`site_name: My Docs`**: Sets the main title for the entire website. This name typically appears in the browser tab, the site header, and is used for branding.

- **`nav`**: Defines the structure of the main, top-level navigation bar. Each entry corresponds to a page or a section in your documentation.
    - Home: `index.md`
    - Setup Guide: `setup-guide.md`
    - Markdown Guide: `markdown-guide.md`
    - About: `about.md`

- **`extra_css`**: Allows you to include custom CSS stylesheets to override or extend the theme's default styling.
    - `css/custom.css`: This line tells MkDocs to load your custom stylesheet located at `docs/css/custom.css`. This file contains rules to hide the navigation on the homepage and style custom buttons.

- **`theme`**: Specifies the visual theme for the site.
    - `name: material`: This enables the powerful [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme, which provides a modern design, excellent responsiveness, and advanced features like the right-side table of contents (TOC) and Admonitions.

- **`markdown_extensions`**: Enables additional features and syntax beyond standard Markdown. These extensions enhance what you can do with your content.
    - `toc` (Table of Contents extension):
        - `permalink: true`: Adds a small link icon next to each heading, allowing users to easily copy a direct link to that section.
        - `toc_depth: 2-3`: Controls which heading levels appear in the right-side "On this page" navigation menu. In this case, it will include `##` (level 2) and `###` (level 3) headings.
    - `admonition`: Enables the special "Boxes" (Admonitions) syntax (`!!! note`, `!!! warning`, etc.) that you saw in the Markdown guide.
    - `pymdownx.details`: Enables the `<details>` and `<summary>` HTML tags for creating collapsible sections, as demonstrated in the Markdown guide.
    - `pymdownx.superfences`: Improves the rendering of fenced code blocks, allowing for nested code blocks and better syntax highlighting.

### 2. The `docs/` Directory (Website Content)

This directory contains all the content for the website.

#### `docs/index.md`
- **Purpose:** The main homepage of the website.
- **Content Details:** It contains a main title (`# Welcome to My Docs`) and two primary sections: `## Key Features` and `## Getting Started`. These `##` sections are what cause the right-side navigation menu to appear on the homepage.

#### `docs/about.md`
- **Purpose:** A simple page to provide information about the project.
- **Content Details:** It currently contains a single heading: `# About This Project`.

#### `docs/setup-guide.md`
- **Purpose:** A comprehensive, step-by-step guide for setting up a similar project from scratch.
- **Content Details:** It is structured with 5 main steps, each as a `##` heading, covering Python installation, MkDocs installation, project creation, adding content, and using key MkDocs commands.

#### `docs/markdown-guide.md`
- **Purpose:** A detailed reference guide for all the Markdown syntax used in this project.
- **Content Details:** It is structured into 5 chapters using `##` headings. It covers basics, text formatting, lists, links/images/tables, and advanced elements. It provides detailed examples and previews for every syntax element, including special features like Admonitions and using HTML.

#### `docs/css/custom.css`
- **Purpose:** A custom stylesheet for applying unique styles to the website.
- **Content Details:** It currently contains two sets of rules:
    1.  A rule to hide the main navigation on the homepage (`.homepage nav { display: none; }`).
    2.  A set of rules to style any link with the `.button` class to make it look like a clickable button with a hover effect.

---

## Chapter 3: How to Use This Project

Follow these steps to run a local version of the website.

### 1. Prerequisites

Ensure you have Python and pip installed on your system. See the `setup-guide.md` for detailed instructions.

### 2. Install Dependencies

Install the necessary Python packages by running the following command in your terminal:

```bash
pip install mkdocs mkdocs-material
```

### 3. Run the Development Server

To preview the site locally, run this command from the project's root directory:

```bash
mkdocs serve
```

This will start a local web server at `http://127.0.0.1:8000/`.

### 4. Build the Final Site

When you are ready to deploy, run the following command:

```bash
mkdocs build
```

This will create a `site/` directory containing the complete, static HTML version of your website.
