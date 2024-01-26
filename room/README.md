
## Breadcrumb Structures for Rooms

### Meeting Rooms
For `Meeting Rooms` available for reservation at branch locations, the breadcrumb pattern is as follows:

`Home` > `Rooms` > `Meeting Rooms Reservation` > `Calendar`

#### Components
- **Home**: Links to the site's home page.
- **Rooms**: Points to the main rooms listing, linked to `/meeting-rooms`.
- **Meeting Rooms Reservation**: Indicates the reservation request page, linked to `/meeting-rooms/request`.
- **Calendar**: Represents the calendar page for meeting rooms, linked to `/meeting-rooms/calendar`.

#### HTML Implementation
```html
<nav aria-label="Breadcrumb" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/meeting-rooms">Rooms</a></li>
    <li class="breadcrumb-item"><a href="/meeting-rooms/request">Meeting Rooms Reservation</a></li>
    <li class="breadcrumb-item active" aria-current="page">Calendar</li>
  </ol>
</nav>
```

### Shared Learning Rooms
For `Shared Learning Rooms` at the Central Library, the breadcrumb pattern is as follows:

`Home` > `Rooms` > `Shared Learning Room Reservation` > `Calendar`

#### Components
- **Home**: Links to the site's home page.
- **Rooms**: Points to the main rooms listing, linked to `/meeting-rooms`.
- **Shared Learning Room Reservation**: Indicates the reservation request page, linked to `/slr/request`.
- **Calendar**: Represents the calendar page for shared learning rooms, linked to `/slr/calendar`.

#### HTML Implementation
```html
<nav aria-label="Breadcrumb" class="nav--breadcrumbs">
  <ol class="breadcrumbs">
    <li class="breadcrumb-item"><a href="/">Home</a></li>
    <li class="breadcrumb-item"><a href="/meeting-rooms">Rooms</a></li>
    <li class="breadcrumb-item active" aria-current="page">Shared Learning Room Reservation</li>
    <li class="breadcrumb-item"><a href="/slr/calendar">Calendar</li>
  </ol>
</nav>
```

## Implementation Notes
- Ensure that these breadcrumb structures are clearly displayed at the top of their respective pages.
- Regular testing of all links within these breadcrumbs is recommended for maintaining accurate navigation.
