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

The form automatically sets the minimum selectable date to today and the
minimum time to one hour from when the form is opened. Time limits adjust
based on the schedule defined in `days` and `closed_dates`.
