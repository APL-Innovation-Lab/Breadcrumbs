
# Breadcrumb Pattern for Search Results Page

This document outlines the updated breadcrumb navigation pattern for the `search_results` content type on the site, incorporating the latest HTML and CSS standards.

## Breadcrumb Structure
The updated breadcrumb pattern for `search_results` enhances user navigation by providing a clear path back to the homepage:

`[Home](/)` > `Website Search Results`

### Components
- **[Home](/)**: This is the first part of the breadcrumb, linking back to the site's homepage.
- **Website Search Results**: This represents the title of the current page, indicating that the user is viewing search results.

### HTML Markup
Implement the breadcrumb using the following HTML structure:

```html
<nav aria-label="Breadcrumbs" class="grid-offset-1 grid-col-10">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Website Search Results</li>
  </ol>
</nav>
```

### CSS
Apply the following CSS to style the breadcrumbs:

```css
ol.breadcrumbs {
    list-style: none;
    padding: 0;
    display: flex;
    align-items: center;
}

ol.breadcrumbs li {
    margin-right: 10px; /* Spacing between breadcrumb items */
}

ol.breadcrumbs li::after {
    content: url('/library/ii/breadcrumb_arrow.svg'); /* Arrow image */
    margin-left: 10px;
}

ol.breadcrumbs li:last-child::after {
    content: none; /* No arrow after the last item */
}

nav.grid-offset-1.grid-col-10 {
    padding-top: 2px;
}
```

### Twig Template
Update the Twig template for the Search Results page:

```twig
<nav aria-label="Breadcrumb" class="grid-offset-1 grid-col-10">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Website Search Results</li>
  </ol>
</nav>
<div class="search-results-title grid-offset-1 grid-col-10">
  <h1>{{ title }}</h1>
</div>
```

## Implementation Notes
- Ensure that the breadcrumb and title are displayed prominently at the top of the Search Results page.
- Test the breadcrumb link to confirm correct navigation back to the homepage.
- Apply this updated pattern consistently across the Search Results content type for a uniform user experience.
