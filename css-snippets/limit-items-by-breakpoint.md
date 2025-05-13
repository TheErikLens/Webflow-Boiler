# Limit Displayed List Items by Breakpoint

**Category:** CSS
**Author/Source:** Érick Vallart (Original snippet), Adapted for boilerplate by [Your Name/Handle]
**Date Added:** YYYY-MM-DD <!-- Replace with actual date, e.g., 2024-07-02 -->

## Description

This CSS snippet allows you to control the number of items displayed in a list (e.g., a Webflow Collection List, blog post feed, product grid) based on the screen width. It's particularly useful for showing fewer items on smaller screens (mobile/tablet) to improve layout and user experience, while showing all or more items on larger screens.

This technique hides elements using `display: none;` starting from a specified child element within a media query.

## Code

The core CSS snippet. Remember to wrap this in `<style>` tags when adding to Webflow's custom code areas.

```css
/*
  Limit items displayed in a list on smaller screens.
  Example: Show only the first 3 items on screens 991px wide or less.
*/
@media screen and (max-width: 991px) {
  .your-collection-list-wrapper .your-collection-item:nth-child(n+4) {
    display: none;
  }
}
```

How to Use and Customize
------------------------

1.  **Identify Your Target Classes:**
    
    *   Replace .your-collection-list-wrapper with the CSS class of the parent element that directly contains your list items. In Webflow, this is typically the "Collection List Wrapper" or a custom-classed div you've placed around the Collection List element.
        
    *   Replace .your-collection-item with the CSS class of the individual items within that list. In Webflow, this is the "Collection Item" itself, or a primary div inside the Collection Item that you've styled.
        
2.  **Adjust the Number of Visible Items:**
    
    *   The key is the :nth-child(n+X) selector. This selector targets all sibling elements starting from the X-th child.
        
    *   If you want to show **Y** items, you need to hide items starting from the **(Y+1)**\-th child. So, set X in n+X to Y+1.
        
    *   **Examples:**
        
        *   To show the **first 3 items** (hide the 4th, 5th, etc.): Use n+4 (as in the example code).
            
        *   To show the **first 5 items** (hide the 6th, 7th, etc.): Use n+6.
            
        *   To show the **first 1 item** (hide the 2nd, 3rd, etc.): Use n+2.
            
3.  **Set the Breakpoint:**
    
    *   max-width: 991px: This value defines the upper limit of the breakpoint. The styles inside this media query will apply to any screen width **up to and including 991px**.
        
    *   Adjust this value to match your desired Webflow breakpoint or custom breakpoint. Common Webflow breakpoints are:
        
        *   Tablet: 991px
            
        *   Mobile Landscape: 767px
            
        *   Mobile Portrait: 479px
            
    *   The code will affect all screen widths _below and including_ the specified max-width.
        
4.  **Placement (Webflow):**
    
    *   You'll need to wrap the CSS code in  tags:</div></li></ul></li></ol><p class="slate-paragraph"></p></x-turndown>
```css
    <style>
  /* Mobile Landscape and Smaller: Show only first 3 items in specific collection */
  @media screen and (max-width: 991px) {
    .your-collection-list-wrapper .your-collection-item:nth-child(n+4) {
      display: none;
    }
  }
</style>
```

1.  Paste this entire ... block into one of the following locations in Webflow:
    
    *   **For a specific page:** Go to Pages panel > Click the Cog icon next to the page name > Scroll down to "Custom Code" > Paste into the "Inside  tag" field.
        
    *   **For sitewide application (if using consistent classes):** Go to Project Settings > Custom Code > Paste into the "Head Code" field.
        

Example Scenario
----------------

Let's say you have a product grid with the CSS class .product-grid for the wrapper and .product-card for each individual product item. You want to display only the first **2 products** on screens **767px wide or less** (Mobile Landscape and smaller).

Your CSS (to be placed inside  tags in Webflow) would be:</p><p class="slate-paragraph"></p></x-turndown>

```css
/* Mobile Landscape and Smaller: Show only first 2 products */
@media screen and (max-width: 767px) {
  .product-grid .product-card:nth-child(n+3) { /* Show 2 items, so hide from (2+1)=3rd item onwards */
    display: none;
  }
}
```

