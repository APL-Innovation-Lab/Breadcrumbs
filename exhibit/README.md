
## Breadcrumb Structure for the Exhibits Page

For the `Exhibits Page` on a Drupal-based website, a specific breadcrumb pattern is designed to showcase the navigation flow. The structure is as follows:

`Home` > `Events` > `Exhibits`

### Components
- **Home**: This is the starting point in the breadcrumb, linking back to the site's home page.
- **Events**: The second element, pointing to the general events section. It links to `/events`.
- **Exhibits**: The final element, representing the current page dedicated to exhibits.

### HTML Implementation
To implement this breadcrumb pattern for the Exhibits Page, use the following HTML code:

```html
<nav aria-label="Breadcrumb" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/events">Events</a></li>
    <li class="breadcrumb-item active" aria-current="page">Exhibits</li>
  </ol>
</nav>
```

## Implementation Notes
- It's crucial to ensure the breadcrumb is prominently displayed at the top of the Exhibits page.
- Regular testing of the breadcrumb links is recommended to ensure they navigate correctly.

## Breadcrumb Structure for Individual Exhibits

For individual `Exhibits`, the breadcrumb pattern is similar but includes the specific exhibit title at the end. The structure is as follows:

`Home` > `Events` > `Exhibits` > `{{ title }}`

### Components
- **Home**: The starting element, linking to the site's home page.
- **Events**: Points to the main events section, linking to `/events`.
- **Exhibits**: Links to the overall exhibits page.
- **{{ title }}**: The final element, dynamically representing the specific exhibit being viewed.

### HTML Implementation
For individual Exhibits pages, use this HTML structure:

```html
<nav aria-label="Breadcrumb" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/events">Events</a></li>
    <li class="breadcrumb-item"><a href="/events/exhibits">Exhibits</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
```

## Implementation Notes
- Ensure that the breadcrumb for individual exhibits is prominently displayed at the top of each exhibit page.
- Regularly test all breadcrumb links to confirm proper navigation.
