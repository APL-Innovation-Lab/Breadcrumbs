
# Breadcrumb and JSON-LD Implementation for Individual Digital Resources


The breadcrumb pattern for individual `Digital Resources` pages is updated to reflect the hierarchy and navigation flow using the `<nav>` structure. The pattern follows this structure:

`Home` > `All Digital Resources` > `Subjects` > `title`

### Components
- **Home**: The first part of the breadcrumb, linking to the site's home page.
- **All Digital Resources**: The second part, linking to the comprehensive list of digital resources. It links to `/digital/all`.
- **Subjects**: The third part, representing the category or subject area of digital resources. It links to `/digital/subjects`.
- **title**: The final part, dynamically representing the title of the current digital resource or section being viewed.

### HTML Markup
The breadcrumb HTML structure is as follows:

```html
<nav aria-label="Breadcrumbs" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/digital/all">All Digital Resources</a></li>
    <li class="breadcrumb-item"><a href="/digital/subjects">Subjects</a></li>
    <li class="breadcrumb-item active" aria-current="page">{{ title }}</li>
  </ol>
</nav>
```
In this structure, `{{ title }}` should be dynamically replaced with the title of the current digital resource or section being viewed.

### Twig Template Override
A Twig template override (`block--views-block--digital-resource-block-4.html.twig`) was created, based on `block.html.twig`, and placed in `aplpa/templates/block`.

## JSON-LD Structured Data
We have added JSON-LD structured data to support schema.org breadcrumbs. This addition is for improving search engine results and providing richer breadcrumbs in those results.

### Implementation
The JSON-LD is specifically tailored for Digital Resource content and meets schema.org's breadcrumb guidelines. This structured data is implemented in the `block--views-block--digital-resource-block-4.html.twig` file:

```
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@id": "https://library.austintexas.gov",
        "name": "Home"
      }
    },
    {
      "@type": "ListItem",
      "position": 2,
      "item": {
        "@id": "https://library.austintexas.gov/digital/all",
        "name": "All Digital Resources"
      }
    },
    {
      "@type": "ListItem",
      "position": 3,
      "item": {
        "@id": "https://library.austintexas.gov/digital/subjects",
        "name": "Subjects"
      }
    },
    {
      "@type": "ListItem",
      "position": 4,
      "item": {
        "@id": "{{ url('<current>') }}", 
        "name": "{{ page_title }}"
      }
    }
  ]
}
</script>
```

### Preprocess Function
A preprocess function added to `aplpa.theme` makes the page title available for the JSON-LD structured data in the Twig template.

## Implementation Notes
- Ensure the breadcrumb and title are prominently displayed at the top of the page.
- Test the breadcrumb link for correct navigation.
- Apply this pattern consistently across all Digital Resource content nodes for uniform user experience.
- The JSON-LD structured data is for enhancing the page's SEO.
