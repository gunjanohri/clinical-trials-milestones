# Clinical Trials Milestones 2026

Static dashboard for current industry-sponsored interventional studies on ClinicalTrials.gov whose phase list contains `PHASE3` and whose `Primary Completion Date` falls in `2026`.

## What is included

- `site/index.html`: the published dashboard
- `site/dashboard.css`: shared dashboard styling
- `site/phase3_completion_2026_dashboard_trials.csv`: trial-level table data
- `site/phase3_completion_2026_month_counts.csv`: month-by-month counts
- `site/phase3_completion_2026_dashboard_summary.json`: summary metadata
- `render.yaml`: Render static-site blueprint

## Snapshot

- ClinicalTrials.gov source data timestamp: `2026-05-15T09:00:05`
- Trials in the dashboard: `949`
- Unique lead sponsors: `500`
- Peak month by primary completions: `December` with `192` trials

## Scope

This project reflects the current-status filter used in the source export:

- `NOT_YET_RECRUITING`
- `RECRUITING`
- `ENROLLING_BY_INVITATION`
- `ACTIVE_NOT_RECRUITING`
- `SUSPENDED`

The dashboard uses the broader set where the study phase list contains `PHASE3`, which means some rows may also include mixed phase labels such as `PHASE2|PHASE3`.

## Local preview

Open [site/index.html](./site/index.html) in a browser.

## Render deploy

This repo is set up for a Render `Static Site`.

- Service type: `Static Site`
- Build command: `echo "Static site ready"`
- Publish directory: `site`

If you use the included Blueprint, Render can read [render.yaml](./render.yaml) directly.

## Notes

- Drug / therapy labels are derived from the intervention names exported from ClinicalTrials.gov.
- Control-like labels such as placebo are de-emphasized when a more specific therapy label is available.
