# LEM Hours Check

A single-page tool for the daily Workforce Report (sign-in sheet) and LEM Report.

## Fill in the day
- The date starts on yesterday, since most LEMs are for the day before. Yesterday / Today buttons sit next to the date.
- Enter the crew once: name, ID, position, LEM tab (staff or trades), shift, time in/out, activity, CWP and cost code, plus equipment.
- **Start from a saved day** copies a previous day (people, times, equipment) so you only change what's different.
- **Drop yesterday's sign-in and LEM** to fill the form from those files. The files are kept as templates, so downloads keep your own layout, logos and formulas. If the crew already has people, dropping a file only adds the workers (and equipment) that aren't on it yet, placed after the last person with the same position. Everyone already listed is left as is, and Undo takes the new ones back off. When the sign-in times and the LEM hours for someone don't agree, the LEM's hours are used (time out is moved to match) and the message lists who was changed. Everything drawn on the sign-in is kept, including workers' pen/ink signatures, sign-offs, logos and header/footer pictures. The crew stays in the file's order (by role), so each signature stays beside the same person. Signatures on the LEM (pictures, pen/ink signatures, shapes, header and footer pictures) are kept exactly as they were in the file you dropped.
- Each person has − / + buttons beside their hours to take off or add an hour (time out moves, time in stays), and a 0 button to set them to zero hours.
- Download the sign-in and LEM. Both come from the same entries, so the hours always match.
- Trades hours are split into straight time, overtime and double time with the rules under "Hours rules":
  - Weekdays: 8 ST, OT to 11, DT after.
  - Saturdays: OT up to 11, DT after (a 12-hour day is 11 OT + 1 DT).
  - Sundays and stat holidays: all DT. Tick "Stat holiday" beside the date for a stat.
- Trades get the cost code "Maintenance" as soon as they have hours (you can type a different code). Taking someone's hours away (0, − down to zero, Clear times) also clears their cost code and activity ID.
- The date you're making LEMs for is shown in large text under the date, with the rates that apply that day.

Days are saved in the claude.ai artifact's database. Opened as a plain file or on another host, they're saved in the browser.

## Check two files
Drop a finished sign-in and LEM to compare every person's hours. Problems are shown row by row on copies of the sheets, with cell references.

Everything runs in the browser using SheetJS, ExcelJS and JSZip from cdnjs.
