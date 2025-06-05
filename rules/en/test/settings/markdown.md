# Markdown Style Guide

**This document provides supplementary guidelines for the semantic structure and content of Markdown files in the project.**
**The primary rules for formatting are defined in the `.markdownlint-cli2.jsonc` file, and formatting is automatically corrected by the Lint process (typically `03_executor.mdc` Stage 3-d) based on those rules.**

This guide shows intentions that cannot be expressed by Lint rules alone and recommendations for writing.

---

## Formatting Rules (Supplementary)

The following are some of the rules defined in `.markdownlint-cli2.jsonc` and related supplementary recommendations.

### Lists

- **Use hyphens (`-`) for list markers.** (Corresponds to `MD004: { "style": "dash" }` setting in `.markdownlint-cli2.jsonc`)
- Nested list items should be indented with **two spaces** aligned to the start position of the parent list item marker (`-`). (Corresponds to `MD007: { "indent": 2 }` setting in `.markdownlint-cli2.jsonc`)

  ```markdown
  - Level 1
    - Level 2
      - Level 3
  ```

### Headings

- Use appropriate levels according to the document structure.
- The Lint rule (`.markdownlint-cli2.jsonc` `MD041: false`) does not require a level 1 heading at the beginning of the file.
- Please insert one blank line before and after headings (markdownlint: MD022).

### Code Blocks

- Always specify the language for code blocks (e.g., ```typescript). (Corresponds to `MD040: true` setting in `.markdownlint-cli2.jsonc`)

### Character Limit

- There is no character limit per line (markdownlint: MD013=false). However, from a readability perspective, it is recommended to break lines appropriately when they are too long.

### Inline HTML

- Use Markdown syntax in principle.
- The HTML elements exceptionally allowed are `<details>`, `<summary>`, `<br>` (corresponds to `MD033` setting in `.markdownlint-cli2.jsonc`).

## Linting Rule Set (Reference Information)

**The primary Lint rules that define and correct formatting are in the `.markdownlint-cli2.jsonc` file in the project root. Always refer to that file.**
