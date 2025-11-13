# BudgetBuddy

Manage income and expenses with simple summaries.

---

## Features

- Add income/expense entries
- Category tagging
- Simple balance summary
- Reset demo

## Tech stack

- Frontend: React (Vite)
- Backend: Node.js + Express
- Storage: `lowdb` (JSON file `db.json`) — zero database setup

## Quick start (development)

Requirements: Node 18+ recommended

1. Start backend
```bash
cd backend
npm install
npm run dev
```
Backend runs on port `4000` by default.

2. Start frontend (in a new terminal)
```bash
cd frontend
npm install
npm run dev
```
Frontend runs on port `5173` by default and talks to the backend at `http://localhost:4000/api`.

## API (overview)

- **GET /api/transactions** — List transactions
- **POST /api/transactions** — Add transaction
- **PUT /api/transactions/:id** — Update transaction
- **DELETE /api/transactions/:id** — Delete transaction
- **POST /api/reset** — Reset demo transactions

## Folder structure

```
BudgetBuddy/
├─ backend/        # Express API, db.json, package.json
├─ frontend/       # Vite + React app (src/, styles.css, vite.config.js)
├─ README.md
├─ .gitignore
```

## Example demo data

The backend seeds a small demo dataset on first run. Use **POST /api/reset** to restore demo content.

## Project preview

![screenshot](screenshot.png)

> Replace `screenshot.png` with a real screenshot if you like — the placeholder is there so GitHub renders it nicely.

## Future improvements

- Charts (monthly breakdown)
- CSV export
- Recurring transactions

---

## Notes

This project is intentionally small and self-contained so you can fork it to experiment quickly. If you'd like Docker support, CI, or additional features (auth, persistent DB), tell me which project(s) and I will add them.