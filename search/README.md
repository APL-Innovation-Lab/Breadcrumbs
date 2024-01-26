
# Breadcrumb Pattern for Search Results Page

The breadcrumb pattern for the search results page is designed to enhance user experience by offering a clear and concise navigation path. The pattern follows this structure:

`Home` > `Website Search Results`

### Components
- **Home**: This is the first part of the breadcrumb and serves as the anchor to the main page. It is a clickable link that directs users to the home page.
- **Website Search Results**: This represents the search results page. It is the second and final part of the breadcrumb trail, indicating the current location of the user within the site.

### Example
Consider a user performing a search on the site. The breadcrumb for the search results page will be displayed as:

`Home` > `Website Search Results`

Where "Home" is a hyperlink to the main page, and "Website Search Results" indicates the current page.

### HTML Code Example
The HTML structure for the breadcrumb navigation might look like this:

```html
<div class="apl breadcrumbs"><a href="/">Home</a> &gt; Website Search Results</div>
```

## Implementation Notes
- The breadcrumb pattern should be consistently implemented on the search results page.
- Ensure that the breadcrumb is prominently displayed near the top of the page, allowing easy navigation for users.
- The link in the breadcrumb should be tested to confirm that it navigates correctly back to the main page.
