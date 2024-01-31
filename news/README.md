
# Breadcrumbs Documentation for News Content Type

This document outlines the implementation of breadcrumbs for the News content type on the library.austintexas.gov website.

## HTML Structure

The breadcrumbs are implemented within a `<nav>` element with an `aria-label` for accessibility, and are contained within a class that aligns them in a grid layout. The breadcrumbs themselves are an ordered list (`<ol>`) with each item (`<li>`) representing a level in the breadcrumb trail.

### Code Snippet

```html
<nav aria-label="Breadcrumbs" class="nav--breadcrumbs grid-col-10 grid-offset-1">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/news">News</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
<h1 class="grid-col-10 grid-offset-1">{{ title }}</h1>
```

## Explanation

- The `<nav>` element helps in semantic grouping and is labeled as "Breadcrumbs" for screen readers.
- `grid-col-10 grid-offset-1` are custom classes that define the grid layout and positioning.
- The `<ol>` element, with the class `breadcrumbs`, represents the breadcrumb trail.
- Each `<li>` element within the list is a step in the breadcrumb trail. The active page is marked with the class `active` and `aria-current="page"` for better accessibility.
- The `{{ title }}` placeholders are used to dynamically insert the title of the current news page.
