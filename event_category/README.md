
## Breadcrumb Structure for Event Categories

For `Event Categories`, the breadcrumb pattern is tailored to display the navigation flow for events. This structure is defined as follows:

`Home` > `Events` > `{{ name }}`

### Components
- **Home**: This is the first element in the breadcrumb, linking to the website's main page.
- **Events**: The second element, representing the general events section. It links to `/events`.
- **{{ name }}**: The last element, dynamically representing the specific event category being viewed.

### HTML Implementation
To realize this breadcrumb structure for specific Event Category pages, use the following HTML code:

```html
<nav aria-label="Breadcrumbs" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/events">Events</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ name }}</li>
  </ol>
</nav>
```

In this structure, `{{ name }}` should be dynamically replaced with the name of the specific event category.

## Implementation Notes
- It is important to ensure that the breadcrumb is prominently displayed at the top of each event category page.
- Regular testing of the breadcrumb links is advised to maintain correct and efficient navigation.
