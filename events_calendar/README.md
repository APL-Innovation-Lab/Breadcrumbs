
# Breadcrumbs for Events Calendar Page on library.austintexas.gov

The breadcrumb trail for the Events Calendar page is as follows:

- Home > Events > Events Calendar
  - **Home**: Links to the main homepage of the website.
  - **Events**: Links to the main events listing page ("/events").
  - **Events Calendar**: Represents the current page.

## Managing the Events Calendar Page

### 1. Accessing the Page

- Navigate to the Events Calendar page directly via [Events Calendar](https://library.austintexas.gov/events/calendar).

### 2. Updating Breadcrumbs

- Ensure that the breadcrumb navigation is correctly displayed at the top of the Events Calendar page.
- The HTML structure for the breadcrumb should be as follows:

```html
<nav aria-label="Breadcrumbs" class="grid-offset-1 grid-col-10">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/events">Events</a></li>
    <li class="breadcrumb-item active" aria-current="page">Events Calendar</li>
  </ol>
</nav>
```

- Verify that the 'Home' and 'Events' links in the breadcrumbs are functioning correctly.
  - **Home Link**: Should redirect to the homepage of the library.austintexas.gov website.
  - **Events Link**: Should redirect to the main events listing page at "/events".

- Apply the following CSS to style the breadcrumbs:

```css
ol.breadcrumbs {
    list-style: none;
    padding: 0;
    display: flex;
    align-items: center;
}

ol.breadcrumbs li {
    margin-right: 10px; /* Spacing between breadcrumb items */
}

ol.breadcrumbs li::after {
    content: url('/library/ii/breadcrumb_arrow.svg'); /* Arrow image */
    margin-left: 10px;
}

ol.breadcrumbs li:last-child::after {
    content: none; /* No arrow after the last item */
}

nav.grid-offset-1.grid-col-10 {
    padding-top: 2px;
}
```

### 3. Content and Layout

- Review and update the content and layout of the Events Calendar page as needed.
- Ensure that the page is user-friendly and the calendar is easy to navigate.
