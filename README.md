# Port of NY & NJ — Dispatch & Reporting demo

**Live demo:** https://black-marlin-labs.github.io/port-reporting-demo/

A public, static copy of an AI-assisted GIS work-management app for port operations. A dispatcher asks
questions in plain language; the agent works the map and the work-activity data, and builds report cards next
to the map.

## What to try

- **Chat (recorded session):** pick the suggested questions in order. The agent:
  - shows the port facilities and zooms to them;
  - colors the airports and marine terminals;
  - measures the distance from Port Newark to JFK;
  - finds the outfalls nearest a terminal;
  - charts overdue work and the workload by person;
  - compares capital project spending;
  - runs a saved report and exports it as a PDF and CSVs.
- **Reports tab:** run any report in the library, set its filters, and download the PDF / CSV. You can also
  check *Recent files* and compare report *Versions*.
- **History:** two earlier chats; reopen one to get its messages and cards back.
- **Map tools** (left edge): search, layers, legend, select (click / box / lasso), measure and basemaps.
- **Cards:** hover for values, click a bar to drill into its activities (table, timeline, on the map), resize
  them on the Reports board, and open an activity record.

## How this copy works

The live app runs the agent against map and database tools (MCP servers) through a small bridge service. This
public copy has **no backend**:

- the chat replays a recorded session of the real agent;
- report runs and PDF / CSV files were made by the live report service when the snapshot was taken (the
  library includes every report with no filter, each filter on its own and a few pairs);
- the work data comes from a snapshot, so edits stay in your browser and a reload resets them;
- schedules, drafts and publishing are read-only here.

## Data

The map layers are public data: NYC Parks Forever Wild, NYC citywide outfalls and the demo port facilities.
The work activities, people and capital projects are fictional sample data.

## Built with

ArcGIS Maps SDK for JavaScript 5 (map components) · React · Vite · Chart.js · Claude (Anthropic) with MCP tool
servers · SQL Server · headless Chromium for the PDF reports.

© Black Marlin Labs
