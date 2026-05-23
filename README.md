# Linear Models Final Project

This repository is organized for collaborative work on the building energy dataset in `ENB2012_data 2.xlsx`.

## Project Focus

- Predict `Y1` (Heating Load) from `X1` to `X8`
- Predict `Y2` (Cooling Load) from `X1` to `X8`
- Compare linear-model approaches, diagnostics, and stronger alternatives where appropriate

## Dataset Snapshot

- File: `ENB2012_data 2.xlsx`
- Rows: 1,296 observations plus 1 header row
- Columns: 10
- Features: `X1` to `X8`
- Targets: `Y1`, `Y2`

## Branch Strategy

- `main`: protected, frozen branch for final archival only
- `development`: integration branch for all active work
- Every working branch must be created from `development`

Recommended branch naming:

- `feature/LM-02-data-dictionary`
- `feature/LM-04-heating-model`
- `fix/LM-05-residual-checks`
- `docs/LM-08-report-draft`

## Rules

- Do not push directly to `main`
- Do not merge feature branches into `main`
- Open pull requests into `development`
- Pull latest `development` before starting a new branch
- Keep commits small and clearly named

## Suggested Repo Layout

- `data/`: raw and cleaned project data
- `analysis/`: notebooks or scripts for EDA and modeling
- `docs/`: report notes, meeting notes, and working documents
- `slides/`: presentation materials

See `WORKING_GUIDE.md` for team roles, Git rules, and the task assignment pattern.
