# VendOps — Vending Machine Operator App

A mobile-first concept for vending machine operators managing multiple machines across a city: track inventory, catch repairs early, and dispatch delivery help — without spreadsheets or site visits.

## What's here

`index.html` — a self-contained, static prototype of the **Fleet Analytics** screen: the operator's single view of inventory health, restock/repair activity, revenue, and delivery dispatch across their whole route.

Open it directly in a browser, or serve it:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

### Analytics screen includes

- **Priority queue** — machines needing restock or repair, ranked by urgency, with one-tap dispatch
- **Inventory grid** — a coil-style heatmap of every location × product category, tap any cell for detail, with a table view for accessibility
- **Restock & repair activity** and **revenue trend** — interactive charts with hover tooltips and a Today / 7 Days / 30 Days range switch
- **Top-selling categories** and **machine health/uptime**, worst first
- **Delivery dispatch** — nearby couriers with one-tap notify
- **Auto-generated optimization tips** — reroute, rebalance stock, and maintenance suggestions

Supports light and dark mode (follows system preference).

## Roadmap

This screen is one part of the full app concept, which also includes:

- A draggable city map homepage with vending machine pins (color-coded by stock status)
- An illustrated per-machine detail view
- Push alerts for restock/repair
- Location-based onboarding
