
## Breadcrumb Structure for Digital Resource Subjects

For `Digital Resource Subjects`, the breadcrumb pattern is updated to reflect the hierarchy and navigation flow using the `<nav>` structure. The pattern follows this structure:

`Home` > `Digital Resource Subjects` > `All Digital Resources`

### Components
- **Home**: The first part of the breadcrumb, linking to the site's home page.
- **Digital Resource Subjects**: The second part, representing the category or subject area of digital resources. It links to `/digital/subjects`.
- **All Digital Resources**: The final part, indicating the current page or section the user is viewing.

### HTML Implementation
To implement this breadcrumb pattern, use the following HTML structure:

For the All Digital Resources page:

```html
<nav aria-label="Breadcrumbs" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">All Digital Resources</li>
    <li class="breadcrumb-item"><a href="/digital/subjects">Subjects</a></li>
  </ol>
</nav>
```

For other Digital Resources Subject pages:

```html
<nav aria-label="Breadcrumbs" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/digital/all">All Digital Resources</a></li>
    <li class="breadcrumb-item"><a href="/digital/subjects">Subjects</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ name }}</li>
  </ol>
</nav>
```

In these structures, `{{ name }}` should be dynamically replaced with the title of the current digital resource or section being viewed.


## Implementation Notes
- Ensure that the breadcrumb and title are prominently displayed near the top of each page within the Digital Resources section.
- Test all links in the breadcrumb to confirm correct navigation.
