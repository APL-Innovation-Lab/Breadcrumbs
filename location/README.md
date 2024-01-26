
## Breadcrumb Structure for Library Locations

For `Library Locations` pages, a breadcrumb pattern is established to navigate through different library locations. The structure is outlined as follows:

`Home` > `Locations` > `{{ title }}`

### Components
- **Home**: The initial element in the breadcrumb, linking to the website's main page.
- **Locations**: The middle element, pointing to the main library locations listing. It links to `/locations`.
- **{{ title }}**: The final element, dynamically representing the specific library location being viewed.

### HTML Implementation
To apply this breadcrumb pattern for individual Library Location pages, utilize the following HTML code:

```html
<nav aria-label="Breadcrumb" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/locations">Locations</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
```

In this structure, `{{ title }}` should be dynamically replaced with the name of the specific library location.

## Implementation Notes
- Ensure that the breadcrumb is clearly visible at the top of each Library Location page.
- Regularly test the breadcrumb links to maintain accurate and functional navigation.
