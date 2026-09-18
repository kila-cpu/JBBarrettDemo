# J.B. Barrett Tractors — Sales App Demo

Interactive prototype of the sales rep mobile app. Everything in it works:
what you create, edit and convert persists for the session.

**Live:** deployed on Railway from this repo.

## What's in it

| Area | What works |
|---|---|
| **Quotes** | Search and status filters, live price total (unit × qty, trade-in, VAT toggle), pull a machine in from stock, duplicate, email |
| **Quote → Sales Order** | Convert pre-fills the order from the quote, raises an order number, flips the quote to *Converted* and marks the stock line *Allocated* |
| **Sales Leads** | Search and status filters, priority sorting, notes timeline, status changes logged as notes, create a quote straight off a lead |
| **Site Visits** | Three fields only. A revisit date feeds the notifications badge |
| **Stock** | Brand and new/used filters, age-in-stock colour coding, allocate / release, quote off a stock line |
| **Notifications** | Driven by real follow-up and revisit dates in the data |

Dates are anchored to **25 June 2026** so the "due soon / overdue" logic reads
sensibly against the seeded data.

## Running it locally

```bash
npm start
```

Then open http://localhost:3000. No dependencies — `server.js` is a plain Node
static host. You can also just open `public/index.html` in a browser; the page
is a single self-contained file with no external requests.

## Notes

- State is kept in `localStorage`, so a refresh keeps your work.
  **Account → Reset demo data** puts it back to the seeded set.
- On a desktop the app renders inside a drawn handset, scaled to fit the window.
  On a real phone the frame drops away and it runs full-bleed.
- Brand colours (navy `#1B1A4E`, green `#5CB947`) were matched by eye from the
  logo artwork. Swap the two CSS custom properties at the top of the file if the
  brand guide says otherwise.

---

Prepared by DMC Consultancy Ltd.
