# The Monthly Claude Challenge

Public home for the challenge boards. Soul-Forged Founders.

**Live at:** https://sunnysink.github.io/monthly-claude-challenge/

## The months

| Month | Theme | Board | Sparks |
|---|---|---|---|
| August 2026 | Made Visible | [`august-made-visible/`](august-made-visible/) | 01 [`tracker/`](august-made-visible/tracker/) |

## How to add next month

**A folder in git is just a path.** You don't create one on its own. You put a
file at `some-folder/index.html` and the folder exists because the file does.
Empty folders can't be committed at all, which is the thing that trips everyone.

Three steps:

1. **Copy** `august-made-visible/index.html` to `<new-month>/index.html`.
   Name the folder `month-theme`, all lowercase, hyphens instead of spaces.
   So September's "Deep Work" month would be `september-deep-work/`.
2. **Edit the new file.** Everything that changes for a new month lives in two
   places: the `:root` colour block at the top (marked THE MONTHLY SKIN) and the
   `SQUARES` array in the script. Change those and the layout stays put.
   Also update `KEY` and `END` near the top of the script, or the new board will
   load last month's saved progress.
3. **Copy the Sparks too, if you're carrying one forward.** The tracker at
   `august-made-visible/tracker/index.html` re-skins the same way: the `:root`
   block at the top and the `MONTH` block in the script, nothing else.
   ⚠️ **Its `key` must change with the month as well**, and it must stay
   different from the board's `KEY`, or the two overwrite each other on the
   member's device.
4. **Edit `index.html` at the root.** Copy the `<a class="month">` block, point
   it at the new folder, and move the old month down under a "Past months"
   heading with its `Live` tag removed.

Then commit and push. GitHub Pages redeploys on its own, usually inside a minute.

## What's in a board

- 25 squares, one prompt each. The centre square is free.
- Progress and post links save to the member's own device, not to a server.
- **Sparks** are the four free things that open weekly through the month. August's
  land on Saturdays: Aug 8, 15, 22, 29. Each one lives in its own folder inside
  the month.
  - **Spark 01 · The Visibility Tracker** — `august-made-visible/tracker/`.
    31-day strip: what you did on the top band, what came back on the bottom, so
    the lag between them is readable. Weekly targets you set yourself, lead
    sources, and a month recap that feeds square 24.
- **The Ember Keeper** is the crown for whoever ends the month top of the
  community leaderboard.

Nothing here collects any data or talks to any server. Every board is one
self-contained HTML file.
