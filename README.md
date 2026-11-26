# DriveKit — The Road Trip, Planned Before You Turn the Key

A single-file web app that plans a South India road trip end to end: route legs with
hairpin warnings, fuel and toll maths, stops worth pulling over for, pre-drive car
checks, packing, a day-by-day plan and a trip budget — all saved on your device.

**Live:** https://abhiramunni.github.io/drivekit/

## What it does

- **Your trips** — three saved trips (Kovoor → Ooty, Bengaluru → Coorg,
  Bengaluru → Pondicherry). Tap one and every section switches to it.
- **Route atlas** — leg-by-leg breakdown with kilometres, driving time and plain-words
  notes (hairpin counts, forest stretches, where to fuel up). Tap a leg for detail.
- **Fuel & tolls calculator** — mileage slider, editable fuel price, petrol/diesel/CNG,
  one-way or round trip, people splitting the cost. Every number on the page updates.
- **Stops** — viewpoints, food and fuel stops with kilometre marks; mark them visited,
  add your own.
- **Trip budget** — planned vs spent per category (fuel, tolls, stay, food, fun) with a
  progress ring; log spends as you go.
- **Car checks & packing** — 12 pre-drive checks and a 10-item packing list, both
  ticked and saved on-device.
- **Day plan** — a slow, realistic day-by-day plan per trip.
- **Six guides** — ghat driving, night driving, FASTag, fuel economy, breakdowns,
  monsoon driving, in plain words.

## The numbers

Seeded with the real Kovoor → Ooty run: 190 km via Thamarassery, Kalpetta, Sultan
Bathery and Gudalur; 45 hairpin bends; 5 hrs 5 mins driving. At 12 km/l and
₹113.79/litre (November 2026 Karnataka petrol), fuel is about ₹1,802 one way;
the all-in round trip is ₹9,003, or ₹2,251 each for four people. Distances, prices
and tolls are estimates — check the pump price before you leave.

## How it works

- One self-contained `index.html` — no backend, no signup, no account.
- Everything saves in `localStorage` under the key `drivekit_v1`.
- Two photos (`drivekit-hero.webp`, `drivekit-flatlay.webp`) sit in the repo root
  and are referenced by `index.html`.
- Works offline once loaded; the only network use is Google Fonts.

## Files

- `index.html` — the app
- `drivekit-hero.webp`, `drivekit-flatlay.webp` — photos
- `README.md`, `LICENSE` (MIT)

QA: 54/54 headless jsdom assertions, node --check OK, zero uncaught JS errors (26 Nov 2026).
