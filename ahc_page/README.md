
# Breadcrumb Pattern for AHC Page

This document describes the updated breadcrumb navigation pattern implemented for the `ahc_page` content type on the site, incorporating the latest HTML and CSS standards used in the library's web pages.

## Breadcrumb Structure
The updated breadcrumb pattern for `ahc_page` is designed to enhance user experience by providing a clear and concise navigation path, following the latest design:

`[AHC Home](/ahc)` > `[node:title]`

### Components
- **[AHC Home](/ahc)**: This is the first part of the breadcrumb and serves as the anchor to the Austin History Center (AHC) main page. It is a clickable link that directs users to `/ahc`.
- **[node:title]**: This represents the title of the current page. It is the second and final part of the breadcrumb trail, indicating the current location of the user within the site.

### HTML Markup
Use the following HTML structure to implement the breadcrumb:

```html
<nav aria-label="Breadcrumb" class="grid-offset-1 grid-col-10">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/ahc">AHC Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
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
Replace the old Twig template with the new version:

```twig
<nav aria-label="Breadcrumb" class="grid-offset-1 grid-col-10">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/ahc">AHC Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
<div class="ahc-title grid-offset-1 grid-col-10">
  <h1>{{ title }}</h1>
</div>
```

## Implementation Notes
- Ensure that the breadcrumb and title are prominently displayed near the top of the page.
- Test the breadcrumb link to confirm correct navigation.
- Implement this pattern consistently across all `ahc_page` content types for uniform user experience.
