# Working Guide

## Team & Rituals

| Person | Role | Primary Focus |
|---|---|---|
| Emmanuel Bett | Repo Maintainer | Protect branches, manage pull requests, keep `development` clean |
| David Mauti | QA and Review Lead | Review model logic, check assumptions, coordinate final technical reviews |
| Mike Mbumbu | Modeling Lead | Lead regression strategy for `Y1` and `Y2`, choose strongest model candidates |
| Angela Omweri | EDA Lead | Inspect data quality, summarize patterns, propose feature transformations |
| Emmy Cheruiyot | Presentation Lead | Turn analysis into clear visuals and presentation flow |
| Daniel Vaati  | Documentation Lead | Maintain report drafts, interpretations, and meeting notes |
| Kelvin Ngigi | Validation and Visualization Lead | Compare metrics, generate plots, support model validation |



## Team Rituals

- Short check-in: 10 to 15 minutes before each major work session
- Daily sync when active: each member posts what they started, blocked on, and finished
- Pull request rule: at least one reviewer before merging into `development`
- Freeze window: no major code changes in the final 24 hours before submission without team approval

## Git Rules

- `main` stays protected and untouched during normal work
- `development` is the only shared integration branch
- All new branches must start from `development`
- No direct commits to `development` unless the team agrees it is an emergency fix
- Rebase or merge from `development` before opening a pull request if your branch is behind
- Commit message pattern:
  - `feat: add baseline heating-load model`
  - `fix: correct residual plot labels`
  - `docs: add model comparison summary`
- Pull request title pattern:
  - `LM-04 Baseline models for heating and cooling`

## Task Assignment Pattern

| Task ID | Task | Assigned To | Acceptance Criteria | Depends On |
|---|---|---|---|---|
| LM-01 | Repository setup and branch rules | Emmanuel Bett | Repo created, `main` and `development` exist, guide committed | None |
| LM-02 | Data dictionary and import check | Angela Omweri | Variables documented, row and column counts confirmed, missing-value check written down | LM-01 |
| LM-03 | Exploratory data analysis | Angela Omweri | Summary stats, pairwise patterns, target distributions, initial insights shared | LM-02 |
| LM-04 | Baseline linear regression models for `Y1` and `Y2` | Mike Mbumbu | Baseline models fitted, coefficients interpreted, train and validation metrics recorded | LM-03 |
| LM-05 | Assumption checks and diagnostics | David Mauti | Residual analysis, multicollinearity review, influential-point checks documented | LM-04 |
| LM-06 | Improved model candidates | Mike Mbumbu | At least two stronger alternatives compared against baseline | LM-05 |
| LM-07 | Visualizations and model comparison tables | Kelvin Ngigi | Clean plots and comparison tables ready for report and slides | LM-05 |
| LM-08 | Report drafting and interpretation | Daniel Vaati | Written project narrative covers methods, results, and recommendations | LM-04 |
| LM-09 | Slide deck and speaking plan | Emmy Cheruiyot | Slide deck prepared, speaking order assigned, rehearsal notes captured | LM-07, LM-08 |
| LM-10 | Integration and final readiness review | Emmanuel Bett | Final `development` branch is clean, artifacts are organized, final checklist completed | LM-06, LM-08, LM-09 |

## Working Flow

1. Pull `development`
2. Create a branch from `development`
3. Do one task only or one closely related task group
4. Push branch and open a pull request into `development`
5. Ask the assigned reviewer to check the work
6. Merge into `development` after approval

## Final Note on `main`

Per your team rule, nobody should push directly to `main` and no feature branch should merge into `main`. If the team later wants a final submission branch, only the repo maintainer should handle that after full team sign-off.
