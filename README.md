# CAFE Lab Fermentation Monitor

The fermentation kiosk app for the CAFE Lab: six Spike fermenters and two Sennos tanks, with live probe readings, run history and run comparison.

It is a single page (`index.html`) served by GitHub Pages. Live data comes from the lab's Google Sheet through its Apps Script link; until that link is set in `CONFIG` at the top of the script, the page shows made-up demo data.

## Two layers: Live tanks and Learn

The **Live tanks** / **Learn** switch in the header flips between the dashboard and the **Fermentation Explorer**, a touch exhibit for the hallway screen and for CHEM 337 (Beer Chemistry) and CHEM 339. It opens on a start screen, offers a 1-minute guided tour, then lets visitors pick topics: the live tanks explained (pH, temperature, oxygen and sugar in plain language, with each batch's time to reach pH 4.6), microbes, flavor molecules with their structures, a virtual fermentation lab with challenges, pH / oxygen / sulfite safety, a quiz (one question built from the live readings) and a flavor-matching game. Finishing topics earns badges.

- Add `?home=learn` to the address on the hallway screen (`https://cafelabflc.github.io/cafe-fermentation/?home=learn`). The screen then opens on the Learn start screen and returns there after 90 seconds without a touch, from either layer, clearing badges for the next visitor.
- Without it (the lab kiosk), the app opens on the dashboard and an idle Learn layer goes back to the dashboard.
- `#learn` at the end of the address opens the Learn layer once.
- `learnIdleSeconds` and `courseUrl` (a course page shown as a QR code) are in `CONFIG`.

Thank you to the Innovation Center for its ongoing support of the CAFE Lab.
