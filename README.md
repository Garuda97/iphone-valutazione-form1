# iPhone Valutazione Form

This repository contains a simple valuation and appointment booking form.

## Booking Availability

`availability.json` still defines the overall booking window but the form now
loads daily hours from `schedule.json`. The current day is automatically set as
the first selectable date and the earliest time defaults to one hour from the
moment of booking.

### availability.json

```
{
  "start_date": "2025-07-25",
  "end_date": "2025-12-31",
  "start_time": "09:00",
  "end_time": "18:00"
}
```

### schedule.json

```
{
  "weekly_hours": {
    "Monday": ["09:00", "18:00"],
    "Tuesday": ["09:00", "18:00"],
    "Wednesday": ["09:00", "18:00"],
    "Thursday": ["09:00", "18:00"],
    "Friday": ["09:00", "18:00"],
    "Saturday": ["10:00", "14:00"],
    "Sunday": null
  },
  "exceptions": {
    "2025-08-15": null,
    "2025-12-24": ["09:00", "13:00"]
  }
}
```

Days without hours (e.g. Sundays or dates listed as `null` in `exceptions`) are
not bookable.
