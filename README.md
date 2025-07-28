# iPhone Valutazione Form

This repository contains a simple valuation and appointment booking form.

## Booking Availability

The `availability.json` file defines the date and time range that users can
select when booking an appointment. It contains four fields:

- `start_date`: first selectable day (ISO `YYYY-MM-DD`)
- `end_date`: last selectable day (ISO `YYYY-MM-DD`)
- `start_time`: earliest selectable time (24h `HH:MM`)
- `end_time`: latest selectable time (24h `HH:MM`)

Update these values to adjust the booking window shown in the form.
