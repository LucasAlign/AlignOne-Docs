---
status: ready
primary: frontend
---

# Build a Reports & Impact report

**Who this is for:** Program staff (Admins and Coordinators).
**When to use it:** When you want to see your program's numbers, build a custom dashboard, or produce a shareable impact report (CSV, PDF, or print).
**Before you start:** You're signed in with staff access.

!!! info "Screenshots coming"
    These steps are described in words for now; annotated screenshots land once the screens are final.

## Open Reports & Impact

1. From the top navigation, open **Reports & Impact**.
2. The page opens with a set of **metric tiles** (counters like *Kids Served*, *Families Served*) and **charts** (like *Families Served Over Time*), all reflecting live data.

Admins see figures across every county. Coordinators start filtered to their own county and can switch to another county or *All Counties* from the filters.

## Filter the report

A row of filters at the top controls every metric at once:

1. **Date range** — choose *Last 30 days*, *Last 3 months*, *Last 6 months*, or *Year to date*.
2. **County** — *All Counties* or a specific county. (Coordinators start on their own county.)
3. **Church** — *All Churches* or a specific church.

**County** and **church** apply to every metric. Every tile and chart updates to match.

### When the date range doesn't apply

The **date range** applies only to metrics that count something that happened on a date — *New Families*, *Needs Fulfilled*, *Families Served Over Time*, and *Monthly Support Activity Totals*.

Some metrics describe **how things stand right now** (for example *Families Served* and the status breakdowns) or count **people without a recorded date** (the volunteer metrics, and *Kids Served*). A date range can't be applied to those, so instead of quietly ignoring it, the metric shows a small **"Date range N/A"** badge in its corner. That's your cue that the number reflects current totals (filtered by county and church), not the selected time window.

!!! note "Why current-status metrics ignore the date range"
    We don't keep a history of when a family's status changed, so we can't say how many were "active" *during* a past period — only how many are active *now*. See [Statuses explained](../../reference/statuses.md).

## Customize your report

Select **Customize** in the top-right to start editing. (Select **Done** when finished.) While customizing you can:

### Add a metric

1. Select **Add metric**.
2. Pick a counter or chart from the list. It's added to the bottom of the report.

Most metrics can be added once; the flexible **Needs Fulfilled** counter can be added **several times** so you can track different need types side by side.

### Move and resize

- **Drag** a panel by the handle at its top edge to reposition it.
- **Resize** by dragging the corner at its bottom-right. Panels never overlap — they stay where you place them.

### Change a metric's options

Some metrics can be tuned. A panel with options shows a **gear (⚙)** while customizing.

1. Select the **gear (⚙)** on the panel.
2. Adjust its settings, for example:
    - **Needs Fulfilled** — pick which need **types** to count (e.g. Meals, Transportation) and a custom label.
    - **Families by County** — group by county, church, or status, and show the percentage of the total.
    - **Families by Church / Training by Church** — set how many to show (top 5, 10, all).
    - **New Families** — follow the date-range filter and show the change versus the previous period.

The tile updates as you change its settings.

### Remove a metric

Select the **✕** on a panel to take it off the report.

### Start over

Select **Reset** to restore the default report with every metric in its standard place.

## Your layout is saved automatically

Your customized report is remembered **in this browser**, so it's still there when you come back. (It isn't shared between devices or teammates — to share a layout, use export/import below.)

## Share a report layout

To give a teammate the same arrangement of metrics:

1. While customizing, select **Export** and either **Download** the layout file or **Copy** its code.
2. Have your teammate select **Import**, then paste the code or upload the file. Their report switches to your layout.

## Export and print

You can turn the current report — its metrics, order, options, and filters — into a shareable document.

1. Choose a **page size** (A4, Letter, Legal, or A3) from the selector next to the export buttons. This applies to PDF and print.
2. Then choose:
    - **Export CSV** — downloads the report's data as a spreadsheet, one section per metric.
    - **Export PDF** — downloads a formatted PDF at your chosen page size.
    - **Print** — opens your browser's print dialog (where you can also save as PDF).

!!! tip "Metrics are never split across a page"
    When exporting to PDF or printing, each metric stays whole — a tile or chart is moved to the next page rather than being cut in half.

## What you'll see

A dashboard that matches the metrics, layout, and filters you chose — and CSV/PDF/print output that mirrors it exactly.

!!! note "Impact Summary"
    The **Impact Summary** block currently shows a "coming soon" message. Narrative impact summaries will appear here in a later release.

## Related

- [Oversight](oversight.md)
- [Statuses explained](../../reference/statuses.md)
- [Roles & permissions matrix](../../reference/permissions-matrix.md)
