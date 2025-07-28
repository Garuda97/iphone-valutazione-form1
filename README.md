# iPhone Valutazione Form

This repository contains a simple valuation and appointment booking form.

## Booking Availability

The `availability.json` file controls which days and times can be selected.
It lets you define opening hours for each weekday and disable specific
holiday dates. The file supports these fields:

- `end_date`: last selectable day (ISO `YYYY-MM-DD`)
- `days`: object with weekday names (`monday`, `tuesday`, ...)
  mapped to `[start, end]` time values (24h `HH:MM`). Use `null` to mark a
  closed day.
- `closed_dates`: list of ISO dates that are not bookable.

The form automatically sets the earliest bookable day to **today** and the
initial time to one hour from when the page is loaded. Limits are then
adjusted based on the weekday schedule defined in `days` and any specific
`closed_dates` you add.

To modify availability simply edit `availability.json`:

1. Update `end_date` to change the last bookable day.
2. In `days`, specify opening hours for each weekday or set the value to
   `null` if the store is closed on that day.
3. Add any holiday closures to `closed_dates` as an array of ISO dates.
