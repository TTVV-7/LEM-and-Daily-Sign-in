# LEM Hours Check

A single-page tool for the daily Workforce Report (sign-in sheet) and LEM Report.

## Fill in the day
- Enter the crew once: name, ID, position, LEM tab (staff or trades), shift, time in/out, activity, CWP and cost code, plus equipment.
- **Start from a saved day** copies a previous day (people, times, equipment) so you only change what's different.
- **Drop a scanned sign-in** (a phone photo or a PDF from the scanner) to take today's times from the signed paper sheet. Claude reads the handwriting. If the crew is already on screen, only the times change: people on the scan get their times, new names are added, and anyone not on the scan has their times cleared. Lines with no signature, or that were hard to read, are listed so you can check them against the paper.
- **Drop yesterday's sign-in and LEM** to fill the form from those files. The files are kept as templates, so downloads keep your own layout, logos and formulas. Workers' signatures on the sign-in are removed.
- Download the sign-in and LEM. Both come from the same entries, so the hours always match.
- Trades hours are split into straight time, overtime and double time with the rules under "Hours rules" (default: 8 ST, OT to 11, DT after).

Days are saved in the claude.ai artifact's database. Opened as a plain file or on another host, they're saved in the browser.

## Check sign-in vs LEM
Drop the sign-in and the LEM to compare every person's hours. The sign-in can be the Excel file or a scan of the signed sheet (photo or PDF). Problems are shown row by row on copies of the sheets, with cell references (line numbers for a scan). A scan is shown next to what was read from it, with missing signatures and hard-to-read entries listed.

Everything runs in the browser using SheetJS, ExcelJS and (for PDF scans) PDF.js from cdnjs. Scans are sent to Claude on the viewer's own claude.ai account, so reading them only works when the page is open in claude.ai. The artifact has to declare the capabilities `db`, `downloads` and `sample` with `images: true`.
