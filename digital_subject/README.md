
# Breadcrumb Modification for Drupal Website

This README outlines the steps and code required to modify the breadcrumb trail on a Drupal-based website, focusing on incorporating specific design and functionality elements.

## Overview
The modifications include:
- Adding "All Digital Resources" to the breadcrumb structure.
- Truncating long titles to 20 characters.
- Adding spacing and a custom icon in place of the caret.
- Responsive design adjustments for mobile view.

## CSS Changes
Add the following CSS to your theme's stylesheet to incorporate the spacing, custom icon, and responsive design.

```css
.breadcrumb {
  padding-top: 15px; /* adds padding above the breadcrumb */
}

.breadcrumb > .delimiter {
  margin: 0 5px; /* extra space around the caret */
}

/* Custom icon for the caret */
.breadcrumb > .delimiter:before {
  content: url('path_to_your_custom_icon'); /* replace with your icon path */
}

/* Responsive design for mobile */
@media (max-width: 767px) {
  .breadcrumb {
    /* Adjustments for mobile view */
  }
}
```

## JavaScript for Title Truncation
Add this JavaScript code to handle the truncation of long titles in the breadcrumb. Ensure this script runs after the DOM is fully loaded.

```javascript
document.querySelectorAll('.breadcrumb li').forEach(function(elem) {
  let text = elem.innerText;
  if (text.length > 20) {
    // Truncate and stop at the end of a word
    text = text.split(' ').reduce((acc, word) => {
      if ((acc + word).length <= 20) {
        return acc + ' ' + word;
      }
      return acc;
    }) + '...';
    elem.innerText = text;
  }
});
```

## Implementation Notes
- Adjust the paths and selectors according to your website's structure.
- Test these changes on a staging site before applying to the live site.
- Ensure compatibility across different browsers and devices.
