# LEM Hours Check

A single-page tool that compares the Daily Workforce Report (sign-in sheet) against the daily LEM Report and shows, per person, whether the hours line up.

Open `index.html` in a browser (or host it on GitHub Pages) and drop both `.xlsx` files on it. Everything runs in the browser; files are never uploaded.

- Sign-in hours = Time Out − Time In (overnight shifts wrap past midnight), minus an optional unpaid break.
- LEM hours = the "Hours" / "Total" column on every labour tab, summed per person.
- Names are matched as "Last, First", tolerating small spelling differences and short first names; those are flagged so the spelling can be fixed.
