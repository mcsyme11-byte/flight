# Live flight · share page

**[Open the share page →](https://mcsyme11-byte.github.io/flight/)**  
`https://mcsyme11-byte.github.io/flight/`

This repository holds a pilot's **always-on share page**: a small web page that shows their flights in
Microsoft Flight Simulator 2024, for friends and family to open any time, even when the pilot's PC is off. It is made
and kept up to date by **Logbook**, part of the [Flight Deck Suite](https://github.com/mcsyme11-byte/Flight-Suite-Releases).

> Everything on the page comes from a flight simulator. It is not a real aircraft.

## What the page shows

- **The flight in progress**, live, while the pilot is flying: route, position, altitude, speed and phase of flight.
- **The last flight**: airports, aircraft, flight time, distance, and its landing (rate, grade and runway).
- **The last landing**, with its rate, grade, runway and crab angle.
- **The pilot's career**, if they choose to show it: totals, landings, a map of their routes, aircraft, airports,
  records and milestones.
- **Landing videos**, if the pilot chooses to share them.

## How it works

1. **Logbook runs on the pilot's PC** beside the simulator and logs every flight by itself: times, route and the
   landing.
2. **After each flight** (and whenever the pilot changes what the page shows), Logbook uploads the page to this
   repository, with a key that can only change this one repository.
3. **GitHub Pages publishes it** at the address above, so the page works around the clock.
4. **While the pilot is flying with the PC on,** the page also asks the pilot's own computer for the flight as it happens (through Tailscale Funnel), so it follows the aircraft live. When the PC is off, it shows the last snapshot instead.

**Each upload replaces everything here** as one new commit with no history: nothing old is kept, so a video taken off
the page really is gone. For the same reason, **don't edit these files by hand**: the next upload replaces them,
this README included.

## What's in this repository

| File | What it is |
|---|---|
| `index.html` | The share page itself (one file: the page, its look and its code). |
| `data.json` | A small read-only snapshot of what the page shows: the last flight, the last landing, the career if the pilot shows it, and the list of shared landing videos. |
| `land.json` | The outline of the world for the page's map (Natural Earth, public domain). |
| `emblem-96.png`, `icon-180.png`, `icon-192.png` | The page's emblem and its icons (for a phone's home screen). |
| `videos/` | The landing videos the pilot chose to share (`.mp4`), each with a still picture (`.jpg`). |
| `.nojekyll` | Tells GitHub Pages to serve the files exactly as they are. |
| `README.md` | This page, written by Logbook. |

## Privacy and safety

- **The page only shows.** Nothing on it can change the logbook, the simulator or the pilot's PC.
- **Only what the page shows is uploaded.** The pilot's full logbook, settings and files stay on their PC.
- **No tracking.** The page collects nothing about the people who open it: no cookies, no analytics, no accounts.
  Its full Privacy Policy and Terms of Use are on the page itself (*About this page*).
- **Logbook's key** for this repository is kept on the pilot's PC only, encrypted for their Windows account.

## Flight Deck Suite

Logbook is one of the add-on tools of the **Flight Deck Suite** for Microsoft Flight Simulator 2024, flown on VATSIM:

- **Logbook**: automatic flight logging, landing rates, a stats site, and this share page.
- **Playback**: landing replays, flown by the sim, built into Logbook.
- **Hangar**: a read-only finder for the sim's Community add-ons, also in Logbook.
- **Squawk**: a phone remote for vPilot.
- **Ramp**: parked aircraft on empty stands.
- **Vantage**: cameras, sound and feel.

**Downloads and the suite's website:** [mcsyme11-byte/Flight-Suite-Releases](https://github.com/mcsyme11-byte/Flight-Suite-Releases). The source code is
maintained privately.

## Credits

Flight data from the pilot's simulator, through Logbook, and the VATSIM network · landing videos recorded in the
pilot's simulator with OBS Studio · airports from the VATSIM Spy data project and OurAirports · map from Natural
Earth (public domain) · delivered by GitHub Pages and, for the live flight, Tailscale Funnel.

Logbook is an independent project and is not made by, endorsed by or affiliated with VATSIM, the developer of vPilot,
Microsoft, OBS Studio, Tailscale, GitHub or Apple.

---

Made with Logbook 4.9 · Flight Deck Suite · developed by Malcolm Syme · mcsyme11@gmail.com
© 2026 Malcolm Syme. All rights reserved.
