
# Breadcrumb and JSON-LD Implementation for AHC Page

This document explains the implementation of breadcrumb navigation and JSON-LD structured data for the `ahc_page` content type on the site. 

## Overview
The implementation involves iterating the default Drupal View used for displaying AHC Pages. The View has been updated to include a `<nav>` section for breadcrumbs above the markup for the title field. The configuration of this View is stored in `views.view.ahc_page.yml` in this repository.

## Breadcrumb Structure
The breadcrumb pattern for `ahc_page` follows a clear and concise navigation path:

`[AHC Home](/ahc)` > `[node:title]`

### Components
- **[AHC Home](/ahc)**: The anchor to the Austin History Center (AHC) main page.
- **[node:title]**: The title of the current page, indicating the user's current location.

### HTML Markup
The breadcrumb HTML structure is as follows:

```html
<nav aria-label="Breadcrumb" class="grid-offset-1 grid-col-10">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/ahc">AHC Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
```

### Twig Template Override
A Twig template override (`block--views-block--ahc-page-block-1.html.twig`) was created, based on `block.html.twig`, and placed in `aplpa/templates/block`.

## JSON-LD Structured Data
We have added JSON-LD structured data to support schema.org breadcrumbs. This addition is  for improving search engine results and providing richer breadcrumbs in those results.

### Implementation
The JSON-LD is specifically tailored for AHC Page content and meets schema.org's breadcrumb guidelines. This structured data is implemented in the `block--views-block--ahc-page-block-1.html.twig` file.

### Preprocess Function
A preprocess function added to `aplpa.theme` makes the page title available for the JSON-LD structured data in the Twig template.

## Implementation Notes
- Ensure the breadcrumb and title are prominently displayed at the top of the page.
- Test the breadcrumb link for correct navigation.
- Apply this pattern consistently across all `ahc_page` content types for uniform user experience.
- The JSON-LD structured data is for enhancing the page's SEO.
