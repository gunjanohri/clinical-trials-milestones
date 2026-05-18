# Clinical Trials Milestones 2026

Static dashboard for current industry-sponsored interventional studies on ClinicalTrials.gov whose phase list contains `PHASE3` and whose `Primary Completion Date` falls in `2026`.

The live site now also overlays a conservative results-signal screen for trials already due by the current cutoff date.

## What is included

- `site/index.html`: the published dashboard
- `site/dashboard.css`: shared dashboard styling
- `site/phase3_completion_2026_dashboard_trials.csv`: trial-level table data, including press-release signal fields
- `site/phase3_completion_2026_month_counts.csv`: month-by-month counts
- `site/phase3_completion_2026_dashboard_summary.json`: summary metadata
- `site/phase3_results_press_release_check_2026.csv`: raw trial-level results/press-release screening output
- `site/phase3_results_press_release_check_2026_summary.json`: screening summary metadata
- `render.yaml`: Render static-site blueprint

## Snapshot

- ClinicalTrials.gov source data timestamp: `2026-05-15T09:00:05`
- Trials in the dashboard: `949`
- Unique lead sponsors: `500`
- Peak month by primary completions: `December` with `192` trials
- Live results check cutoff: `2026-05-17`
- Due trials checked live: `252`
- Likely press releases found: `5`
- Results-coverage-only matches: `61`
- No qualifying live match: `186`
- Future-dated trials not yet due: `697`

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

Direct deploy link:

- [Deploy this repo on Render](https://render.com/deploy?repo=https://github.com/gunjanohri/clinical-trials-milestones)

## Notes

- Drug / therapy labels are derived from the intervention names exported from ClinicalTrials.gov.
- Control-like labels such as placebo are de-emphasized when a more specific therapy label is available.
- The results overlay is a conservative headline-level screen for triage and not a final adjudication of whether a given item is the definitive primary-endpoint readout for that trial.
