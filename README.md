# CAFE Lab Fermentation Monitor

The fermentation kiosk app for the CAFE Lab: six Spike fermenters and two Sennos tanks, with live probe readings, run history and run comparison.

It is a single page (`index.html`) served by GitHub Pages. Live data comes from the lab's Google Sheet through its Apps Script link; until that link is set in `CONFIG` at the top of the script, the page shows made-up demo data.

## Two layers: Live tanks and Learn

The **Live tanks** / **Learn** switch in the header flips between the dashboard and the **Chemistry And Fermentation Experience**, a touch exhibit for the hallway screen and for CHEM 337 (Beer Chemistry) and CHEM 339.

Its main screen is **Design your Fermentation**: pick a microbe (14, from ale yeast to koji mold, natto bacteria or a wild ferment), up to 6 of 48 ingredients, and the temperature, dissolved oxygen and salt, then press **Start fermentation**. A Spike-style conical fermenter fills and comes alive while the pH and oxygen change, the main reactions turn reactants into products (with drawn structures), and pleasant and unpleasant flavor molecules build up. It ends with what you made and whether it reached pH 4.6 safely. It is a simplified teaching model: the directions are right, the numbers are made up. Quick-start buttons load beer, wine, sauerkraut, yogurt, kombucha, miso, natto and vinegar.

**More to explore** opens the earlier topics: the live tanks explained, microbes, flavor molecules, a lab with challenges, pH / oxygen / sulfite safety, a quiz and a flavor-matching game, with badges.

- Add `?home=learn` to the address on the hallway screen (`https://cafelabflc.github.io/cafe-fermentation/?home=learn`). The screen then opens on Design your Fermentation and starts over after 90 seconds without a touch, from either layer.
- Without it (the lab kiosk), the app opens on the dashboard and an idle Learn layer goes back to the dashboard.
- `#learn` at the end of the address opens the Learn layer once.
- `learnIdleSeconds` and `courseUrl` (a course page shown as a QR code) are in `CONFIG`.

Thank you to the Innovation Center for its ongoing support of the CAFE Lab.
