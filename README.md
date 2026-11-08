# forgecycle-reports

Anonymized improvement reports from [ForgeCycle](https://github.com/forgecycle/forgecycle-releases) runs.
Each issue is one report, created by `forgecycle report --submit`.

## What a report contains

Counters and enums only: the ForgeCycle version, OS and architecture; the configured adapters,
models, and efforts; run states, turn counts, stop kinds, and durations; command exit codes;
per-candidate validity, repair, and quota figures; and which handoff fields failed validation.

It never contains prompts, handoff or feedback text, file paths, or the names of your repository,
branches, tasks, runs, or candidates. Runs and candidates appear as `r1`, `m1`, and `c1`.

## Sending one

```
forgecycle report --out report.json     # read it first
forgecycle report --submit --repo forgecycle/forgecycle-reports
```

`--submit` shows the exact issue body and asks before sending. You need `gh` logged in to GitHub.
Issues here are public, so check the report before you send it. To remove a report you sent,
delete its issue.
