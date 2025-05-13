# Webflow-Boiler 🚀

A personal collection of reusable code snippets, techniques, and best practices for Webflow projects. The goal is to have a quick-reference library to speed up development and maintain consistency across projects.

## How to Use This Repository

1.  **Browse the Table of Contents** below or navigate the folders directly to find a snippet.
2.  Click on a snippet link to view its dedicated Markdown file.
3.  Each snippet file contains:
    *   A description of what it does.
    *   The code itself (CSS, JavaScript, etc.).
    *   Detailed instructions on how to use and customize it.
    *   Placement instructions specific to Webflow (e.g., Page Head, Site Head, before `</body>`).
    *   Example scenarios where applicable.
4.  Copy the relevant code and follow the instructions to implement it in your Webflow project.

## Table of Contents

### CSS Snippets
*   [Limit Displayed List Items by Breakpoint](./css-snippets/limit-items-by-breakpoint.md)
*   *(Add links to new CSS snippets here as you create them)*

### JavaScript Snippets
*   *(Add links to new JS snippets here as you create them)*

### Integrations & Other Snippets
*   *(Add links to other types of snippets here)*

## Suggested Directory Structure

For organizational purposes, snippets are categorized into folders:

Webflow-Boiler/
├── README.md # This file: Main overview & Table of Contents
├── css-snippets/ # Folder for CSS-only snippets
│ └── limit-items-by-breakpoint.md
│ └── ... (other .md files for CSS snippets)
├── js-snippets/ # Folder for JavaScript snippets
│ └── ... (other .md files for JS snippets)
├── integrations/ # For snippets integrating third-party services
│ └── ...
└── assets/ # Optional: For images used in .md explanations
└── ...


## Contributing (To My Own Boilerplate)

1.  **Identify the Category:** Determine if the snippet is CSS, JavaScript, an integration, etc.
2.  **Create a New Markdown File:**
    *   Navigate to the appropriate sub-folder (e.g., `css-snippets/`).
    *   Create a new `.md` file with a descriptive name (e.g., `custom-animated-button.md`).
3.  **Document the Snippet:** Use a consistent format within the `.md` file:
    *   Title
    *   Category, Author/Source, Date Added
    *   Description
    *   Code Block(s)
    *   How to Use and Customize
    *   Placement Instructions (Webflow specific)
    *   Example Scenario (if helpful)
    *   Tags (optional, for searchability)
4.  **Update Table of Contents:** Add a link to the new snippet in this main `README.md` file under the relevant category.
5.  **Commit and Push:**
    ```bash
    git add .
    git commit -m "Add: [Brief description of the new snippet]"
    git push origin main # or your default branch
    ```

---
*This boilerplate is for personal use and continuous improvement. Feel free to adapt it to your own needs.*
