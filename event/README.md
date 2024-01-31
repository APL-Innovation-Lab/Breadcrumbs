
## Breadcrumb Structure for Individual Event Pages

The breadcrumb pattern for individual `Event` pages is designed to provide users with a clear navigation path. The pattern follows this structure:

`Home` > `Events` > `title`

### Components
- **Home**: The first part of the breadcrumb, linking to the site's home page.
- **Events**: The second part, linking to the main events listing page. It links to `/events`.
- **title**: The final part, dynamically representing the title of the current event being viewed.

### HTML Implementation

For individual Event pages:

```html
<nav aria-label="Breadcrumbs" class="nav--breadcrumbs grid-col-10 grid-offset-1">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/events">Events</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
```

In this structure, `{{ title }}` should be dynamically replaced with the title of the current event.

## Implementation Notes
- Ensure that the breadcrumb and title are prominently displayed near the top of each individual Event page.
- Test all links in the breadcrumb to confirm correct navigation.
