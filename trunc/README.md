
# JavaScript Text Truncation

This document outlines the implementation of text truncation using JavaScript to ensure that text breaks at the end of a word. This method is particularly useful for managing the display of lengthy text elements like breadcrumbs, ensuring they remain concise and user-friendly, especially in responsive designs.

## Files Included
- `trunc.js`: Contains the JavaScript function for truncation.
- `style.css`: Contains the basic styling needed for the truncated text.

## JavaScript Function (trunc.js)
The JavaScript file `trunc.js` includes a function to truncate text at the nearest word boundary within a character limit. Here's the content of `trunc.js`:

```javascript
function trunc(selector, maxLength) {
  var elements = document.querySelectorAll(selector);
  elements.forEach(function(element) {
    for (let child of element.childNodes) {
      if (child.nodeType === Node.TEXT_NODE || child.nodeType === Node.ELEMENT_NODE) {
        var textContent = child.textContent || child.innerText;
        if (textContent.length > maxLength) {
          var truncated = textContent.substr(0, maxLength);
          truncated = truncated.substr(0, Math.min(truncated.length, truncated.lastIndexOf(" "))) + '...';
          if (child.nodeType === Node.TEXT_NODE) {
            child.textContent = truncated;
          } else {
            child.innerText = truncated;
          }
        }
      }
    }
  });
}


// Usage example: trunc('.breadcrumbs', 20);
```

## CSS Styling (style.css)
The `style.css` file provides basic styling for the truncated text elements. Here's the content of `style.css`:

```css
.breadcrumbs {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

## Implementation Guide
1. **Include the Files**: Add `trunc.js` and `style.css` to your project.
2. **Link the CSS**: In your HTML, link to `style.css` within the `<head>` tag.
3. **Use the JavaScript Function**:
   - Call `trunc(selector, maxLength)` on document ready.
   - Replace `breadcrumbs` with the CSS selector for the elements you want to truncate.
   - Set `maxLength` to the maximum number of characters allowed before truncation.

### Example Usage
In your HTML, add a class to the elements you want to truncate. For instance:

```html
<div class="breadcrumbs">Some very long breadcrumb text goes here</div>
```

Then, in your JavaScript file or script tag:

```javascript
document.addEventListener('DOMContentLoaded', function() {
  truncate('.breadcrumbs', 20);
});
```

## Conclusion
This JavaScript approach to text truncation offers a dynamic way to manage text length, ensuring readability and consistency across different display sizes. It's especially useful for elements like breadcrumbs where space is limited and content varies.