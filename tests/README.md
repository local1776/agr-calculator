# Tests and build notes

Nothing in this folder is loaded by the calculator. The whole tool is `index.html` in the repository root.

- `engine_test.js`: runs the math in Node across seven member profiles and sweeps the data for gaps. `node tests/engine_test.js index.html`
- `lifetime_test.js`: prints the Bottom Line ledger (working years, retirement, all in) for the baseline profiles and checks it against the retirement card.
- `sweep.js`: runs one member through every duty location in the country.
- `ui_test.py`, `print_test.py`, `print_gap.py`: headless Chrome checks of the page and of the Print / Save as PDF output (Playwright).
- `og_card.html`: source for `og.png`, the share-preview image.
- `build-v1.1/`: the six scripts that turned version 1.0 into version 1.1, in order (a to f). Kept as a record of exactly what changed.

Rule: any change to the math or the data is run through `engine_test.js` first. Numbers move only when a change is meant to move them.
