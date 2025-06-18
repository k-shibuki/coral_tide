# Markdown Style Guide

**This document provides supplementary guidelines regarding the semantic structure and content of Markdown files in the project.**
**The primary formatting rules are defined in the `.markdownlint-cli2.jsonc` file, and formatting is automatically corrected through the Lint process based on those rules.**

This guide presents intentions that cannot be fully expressed through Lint rules alone and recommended practices during writing.

---

## Formatting Rules

The following are recommendations.

### Lists

- **Use hyphens (`-`) as list markers.**
- Nested list items should be indented with **two spaces** aligned to the beginning position of the parent list item's marker (`-`).

  ```markdown
  - Level 1
    - Level 2
      - Level 3
  ```

### Headings

- Use appropriate levels according to the document structure.
- Each section must have a unique heading.
- Lint rules do not require a level 1 heading at the beginning of the file.
- Include one blank line before and after headings.

### Code Blocks

- Always specify the language for code blocks (e.g., ```typescript)

### Character Limit

- There is no character limit per line. However, for readability, it is recommended to break overly long lines appropriately.

### Inline HTML

- Use Markdown syntax in principle.
- Exceptionally permitted HTML elements are `<details>`, `<summary>`, and `<br>`. 