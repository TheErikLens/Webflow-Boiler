# Webflow-Boiler
A boilerplate for Webflow development.

- css-snippets/: For pure CSS solutions. Each snippet gets its own Markdown file.
- js-snippets/: For JavaScript solutions. Each snippet gets its own Markdown file.
- integrations/: For more complex snippets that involve integrating external services or libraries (e.g., custom Mailchimp form handling, Typeform styling).
- assets/: If your explanations need images or diagrams, store them here and link to them from your .md files.

Individual Snippet File Format (e.g., limit-items-by-breakpoint.md)
Each .md file for a snippet should follow a consistent format. Using the example you provided:
File: css-snippets/limit-items-by-breakpoint.md
# Limit Displayed List Items by Breakpoint

**Category:** CSS
**Author/Source:** Érick Vallart (adapted)
**Date Added:** YYYY-MM-DD (when you added it to your repo)

## Description

This CSS snippet allows you to control the number of items displayed in a list (e.g., a Webflow Collection List, blog post feed, product grid) based on the screen width. It's particularly useful for showing fewer items on smaller screens (mobile/tablet) to improve layout and user experience, while showing all or more items on larger screens.

## Code

```html
<style>
  /*
    Limit items displayed in a list on smaller screens.
    Example: Show only the first 3 items on screens 991px wide or less.
  */
  @media screen and (max-width: 991px) {
    .your-collection-list-wrapper .your-collection-item:nth-child(n+4) {
      display: none;
    }
  }
</style>
