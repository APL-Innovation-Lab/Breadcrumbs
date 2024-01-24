
## Breadcrumb Structure
For `Digital Resources`, the breadcrumb pattern is structured to reflect the hierarchy and navigation flow. The pattern follows this structure:

`Home` > `Digital Resource Subjects` > `All Digital Resources`

### Components
- **Home**: The first part of the breadcrumb, linking to the site's home page.
- **Digital Resource Subjects**: The second part, representing the category or subject area of digital resources. It links to `/digital/subjects`.
- **All Digital Resources**: The final part, indicating the current page or section the user is viewing.

### HTML Implementation
To implement this breadcrumb pattern, use the following HTML structure:

```html
<div class="apl breadcrumbs">
  <a href="/">Home</a> > 
  <a href="/digital/subjects">Digital Resource Subjects</a> > 
  {{ name }}
</div>
```

In this structure, `{{ name }}` should be dynamically replaced with the title of the current digital resource or section being viewed.

### Example
An example of this breadcrumb in action would be:

`Home` > `Digital Resource Subjects` > `All Digital Resources`

Represented in HTML as:

```html
<div class="apl breadcrumbs">
  <a href="/">Home</a> > 
  <a href="/digital/subjects">Digital Resource Subjects</a> > 
  All Digital Resources
</div>
```

## Implementation Notes
- Ensure that the breadcrumb is consistently implemented across all relevant pages within the Digital Resources section.
- Verify that all links in the breadcrumb are functioning correctly and lead to the appropriate pages.