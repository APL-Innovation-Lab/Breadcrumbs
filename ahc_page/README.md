
# Breadcrumb Pattern for AHC Page

This document describes the breadcrumb navigation pattern implemented for the `ahc_page` content type on site. Breadcrumbs are an essential part of the site's navigation strategy, providing users with a way to trace the path back to their starting point.

## Breadcrumb Structure
The breadcrumb pattern for `ahc_page` is designed to enhance user experience by providing a clear and concise navigation path. The pattern follows this structure:

`[AHC Home](/ahc)` > `[node:title]`

### Components
- **[AHC Home](/ahc)**: This is the first part of the breadcrumb and serves as the anchor to the Austin History Center (AHC) main page. It is a clickable link that directs users to `/ahc`.
- **[node:title]**: This represents the title of the current page. It is the second and final part of the breadcrumb trail, indicating the current location of the user within the site.

### Example
Consider the following URL: `https://library.austintexas.gov/ahc/research`. The breadcrumb for this page will be displayed as:

`[AHC Home](/ahc)` > `Research`

Where "AHC Home" is a hyperlink to `/ahc`, and "Research" is the title of the current page.

## Implementation Notes
- The breadcrumb pattern should be implemented consistently across all `ahc_page` content types.
- Ensure that the breadcrumb is prominently displayed near the top of the page, allowing easy navigation for users.
- The link in the breadcrumb should be tested to confirm that it correctly navigates back to the AHC main page.

## Conclusion
The breadcrumb pattern for `ahc_page` is a simple yet effective navigation tool that aids users in understanding their location within the site and allows for easy backtracking to the AHC main page.