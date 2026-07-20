# St. Andrew's Calendars

Public subscription calendars for St. Andrew's athletics, theatre, and other school activities.

## Current calendars

- Football 5/6 — Fall 2026
- Football JV — Fall 2026

The public landing page is intended to be served with GitHub Pages from the `main` branch and repository root.

## Updating a schedule

1. Edit the appropriate YAML file under `data/`.
2. Run `python3 scripts/generate_calendars.py`.
3. Commit both the YAML source and regenerated `.ics` files.
4. Keep each event's `id` unchanged when changing its time, place, title, or status. The ID produces a stable calendar UID so subscribers receive an update instead of a duplicate.
5. Increase `sequence` for an edited event. Set `status: cancelled` rather than deleting a cancelled event.

Stable subscription files live under `calendars/<category>/latest/`. Archived season files live under `calendars/<category>/<year>/`.

## Adding another activity

Create another YAML schedule using the existing files as examples. The generator supports athletics, plays, rehearsals, competitions, performances, meetings, and other timed or all-day events.