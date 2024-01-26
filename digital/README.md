
## Breadcrumb Structure for Individual Digital Resources

The breadcrumb pattern for individual `Digital Resources` pages is updated to reflect the hierarchy and navigation flow using the `<nav>` structure. The pattern follows this structure:

`Home` > `All Digital Resources` > `Subjects` > `title`

### Components
- **Home**: The first part of the breadcrumb, linking to the site's home page.
- **All Digital Resources**: The second part, linking to the comprehensive list of digital resources. It links to `/digital/all`.
- **Subjects**: The third part, representing the category or subject area of digital resources. It links to `/digital/subjects`.
- **title**: The final part, dynamically representing the title of the current digital resource or section being viewed.

### HTML Implementation

For individual Digital Resources pages:

```html
<nav aria-label="Breadcrumb" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/digital/all">All Digital Resources</a></li>
    <li class="breadcrumb-item"><a href="/digital/subjects">Subjects</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
```

In this structure, `{{ title }}` should be dynamically replaced with the title of the current digital resource or section being viewed.

## Implementation Notes
- Ensure that the breadcrumb and title are prominently displayed near the top of each individual Digital Resources page.
- Test all links in the breadcrumb to confirm correct navigation.
