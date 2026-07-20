# SIGGRAPH 2026 Personal Schedule Planner

A single-file web app for planning your [SIGGRAPH 2026](https://s2026.siggraph.org/) (Los Angeles, July 19–23) conference schedule.

**Live app:** https://zhehaoli1999.github.io/SIGGRAPH26-planner/

## Features

- Full conference schedule — 487 sessions across all five days, browsable by day, program type, and free-text search
- Paper-level detail for all 58 Technical Papers sessions (406 papers: titles, full author lists, presenters, per-paper times, session chairs) pulled from the official schedule — search any author's name to find their talk; matching papers expand and highlight automatically
- Pin sessions (★) to build a personal agenda; pins persist in your browser via localStorage
- Automatic conflict detection between overlapping pinned sessions
- Export pinned sessions as an `.ics` file (with configurable reminders) for import into Google Calendar / Apple Calendar — phone notifications come free; Technical Papers events include the full paper lineup in the description
- Per-session "Add to Google Calendar" links
- Mobile friendly; works offline once loaded

## Files

- `index.html` — the app (fully self-contained: data, CSS and JS inlined)
- `siggraph2026_my_picks.ics` — ready-to-import calendar of the initially pinned sessions (15-min reminders, `America/Los_Angeles` timezone)
- `data/sessions.json` — the extracted schedule data

## Notes

Session data was transcribed from the official Full Schedule (s2026.conference-schedule.org) as of July 2026; Technical Papers session details (papers, authors, presenters, chairs, times, rooms) were extracted directly from the official schedule data on July 20, 2026 and cross-validated against the transcription. Rooms and times can change — double-check must-attend sessions against the official schedule.
