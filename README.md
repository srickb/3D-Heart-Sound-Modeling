# 3D Heart Modeling

## Daily Research Log Automation

This repository includes a lightweight research logging system.

- `scripts/generate_daily_log.py` collects today's Git activity, optional notes, and optional experiment metadata.
- The script writes `daily_logs/YYYY-MM-DD.md` and `daily_logs/structured/YYYY-MM-DD.json` only when the day looks meaningful.
- `project_context.json` stores stable project context and should be updated manually as the project evolves.
- `.github/workflows/daily_research_log.yml` runs the generator on push and at 23:00 Asia/Seoul time, then commits generated logs only when files changed.
- `DAILY_LOG_USAGE.md` explains how to prepare input files and how to read and use the generated markdown log.

Optional input files:

- `notes/daily_raw/YYYY-MM-DD.md`
- `experiments/YYYY-MM-DD.json`
