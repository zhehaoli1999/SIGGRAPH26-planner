# SIGGRAPH 2026 Personal Schedule Planner

A single-file web app for planning your [SIGGRAPH 2026](https://s2026.siggraph.org/) (Los Angeles, July 19–23) conference schedule.

**Live app:** https://zhehaoli1999.github.io/SIGGRAPH26-planner/

## Features

- Full conference schedule — 487 sessions across all five days, browsable by day, program type, and typo-tolerant fuzzy search (word-order independent, accent-insensitive, ~1–2 character edits forgiven: "gaussain splatting", "ruizen hu" and "layots procedural" all find what you meant)
- Paper-level detail for all 58 Technical Papers sessions (406 papers: titles, full author lists, presenters, per-paper times, thumbnails, session chairs) pulled from the official schedule — search any author's name to find their talk; matching papers expand and highlight automatically
- Keyword filter chips (official taxonomy: Geometry, AI/ML, Animation, Fabrication, …) — narrow all 406 papers by topic; matching papers highlight and their sessions auto-expand, with keyword tags shown on every paper
- Start-time and end-time range sliders (8:00am–8:00pm, half-hour steps) — hide sessions starting or ending outside your windows ("free 2pm onward, must leave by 5"); the extremes are unbounded so the default full ranges hide nothing, and the Overview columns respect them too
- Overview tab — Keenan-Crane-style per-day columns summarizing any program category (default: Technical Papers); pin from the list (★) or tap a session to jump to its full card
- Session and paper titles link (↗) to their page on the official schedule site — 422 sessions and all 406 papers carry official ids (the few unlinked entries are aggregates like grouped poster listings with no single official page)
- Pin sessions (★) to build a personal agenda; pins persist in your browser via localStorage
- Automatic conflict detection between overlapping pinned sessions
- Export pinned sessions as an `.ics` file (with configurable reminders) for import into Google Calendar / Apple Calendar — phone notifications come free; Technical Papers events include the full paper lineup in the description
- Per-session "Add to Google Calendar" links
- Mobile friendly; works offline once loaded

## Files

- `index.html` — the app (data, CSS and JS inlined; paper thumbnails lazy-load from `data/thumbs/`)
- `data/sessions.json` — the extracted schedule data
- `data/thumbs/` — paper representative images (resized to 200 px thumbnails)

## Notes

Session data was transcribed from the official Full Schedule (s2026.conference-schedule.org) as of July 2026; Technical Papers session details (papers, authors, presenters, chairs, times, rooms) were extracted directly from the official schedule data on July 20, 2026 and cross-validated against the transcription. Rooms and times can change — double-check must-attend sessions against the official schedule.
