# iPhone Valutazione Form

This repository contains a simple valuation and appointment booking form.

## Booking Availability

The `availability.json` file controls which dates and times can be selected.
It supports the following keys:

- `start_date` (optional): first selectable day. If omitted, today's date is used.
- `end_date`: last selectable day.
- `start_time` (optional): default opening time used when no day specific hours are provided.
- `end_time`: default closing time.
- `days` (optional): object mapping weekday numbers (`0` = Sunday .. `6` = Saturday)
  to objects containing `start_time` and/or `end_time` that override the defaults.
- `closed_dates` (optional): array of ISO dates that cannot be booked.

`start_date` and `end_date` always limit the selectable range. When a date falls
into `closed_dates` the time field is disabled. For other dates, the hours
specified for that weekday in `days` take precedence; otherwise the `start_time`
and `end_time` values are used.
