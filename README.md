# VendOps — Vending Machine Operator App

A mobile-first concept for vending machine operators managing multiple machines across a city: track inventory, catch repairs early, and dispatch delivery help — without spreadsheets or site visits.

## What's here

`index.html` — a self-contained, interactive prototype of the **home/map** screen: the operator's single view of every machine on their route, with restock and repair dispatch built in.

Open it directly in a browser, or serve it:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

### What's interactive

- **Map home** — every machine plotted as a pin, color-coded by status (stocked / low / needs repair). Filter chips and an alert pill narrow the map to what needs attention.
- **Machine drawer** — tap a pin to open a bottom card with status, uptime, and last-serviced date. Drag the handle (or tap "View inventory details") to expand into the full per-item stock levels.
- **Restock flow** — tap Restock to see nearby distributors with ratings and live availability ("Available now" / "in 25 min" / "Tomorrow 9 AM"); one tap dispatches.
- **Repair flow** — same pattern with a list of technicians and their specialties.
- **Toast notifications** — dispatch confirmations and live status alerts surface as toasts at the bottom of the screen. They auto-dismiss after a few seconds, or swipe one left to dismiss immediately. A few seconds after load, a simulated incoming fault alert demonstrates an unprompted update arriving.
- Dispatching simulates completion a few seconds later (inventory refills / fault clears), with a follow-up toast — a stand-in for a real backend push.

Supports light and dark mode (follows system preference).

## Roadmap

Out of scope for this iteration, but natural next screens:

- A machine list / history view as an alternate to the map
- Push notifications when the app isn't open
- Location-based onboarding and route optimization
