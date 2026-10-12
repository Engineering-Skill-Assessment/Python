# Task API — Python Coding Test

A small Python Task API used as a **10-minute live coding exercise** for backend candidates.

## Quick start

```bash
python server.py
```

Server runs at `http://localhost:3000`.

## Candidate brief

Give the candidate [`TODO.md`](./TODO.md). It contains the full task description, rules, and evaluation criteria.

## What’s already implemented

- In-memory task store with mock data
- `GET /tasks` returns tasks (filter not wired yet)
- `PATCH /tasks/:id/toggle` toggles completion
- `GET /health` health check
- CORS headers for local testing

## API

| Method | Path | Description |
| ------ | ---- | ----------- |
| `GET` | `/tasks?status=all\|active\|completed` | List tasks (candidate implements filtering) |
| `PATCH` | `/tasks/:id/toggle` | Toggle task completion |
| `GET` | `/health` | Health check |

## Stack

- Python 3.10+
- Standard library `http.server` (no Flask/FastAPI)

## Project structure

```text
data.py      # mock tasks
tasks.py     # store + filter_tasks stub
server.py    # HTTP server
```

## Interviewer notes

- Time box: **10 minutes**
- Core task: implement `filter_tasks` in `tasks.py` for **all / active / completed**
- Optional bonus: include a `count` in the list response
- Do not share a solution with the candidate before or during the exercise
