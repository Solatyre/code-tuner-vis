# Code Tuner Viz

A full-stack dashboard for visualising software complexity metrics, so you can see at a glance where a codebase is getting harder to maintain.

![Code Tuner Viz screenshot](docs/screenshot.png)
<!-- Add a screenshot at docs/screenshot.png -->

## Features

- **Overview** – high-level project metrics in one view
- **Histogram** – distribution of complexity across fixed buckets
- **Class sizes** – lines of code per class, with the raw data table
- **Trend** – how complexity changes over time
- **Benchmarks** – compare repositories side by side

## Tech stack

| Layer    | Tools                                  |
|----------|----------------------------------------|
| Frontend | React, Vite, TypeScript, Recharts      |
| Backend  | Node.js, Express, TypeScript           |
| Database | PostgreSQL with Prisma ORM             |

## Getting started

**Prerequisites:** Node.js 18+ and a PostgreSQL database.

1. Copy the environment file and add your database URL:

   ```bash
   cp .env.example .env
   ```

2. Start the backend (terminal 1):

   ```bash
   cd code-tuner-viz-backend
   npm install
   npx prisma generate
   npm run dev
   ```

3. Start the frontend (terminal 2):

   ```bash
   cd code-tuner-viz-frontend
   npm install
   npm run dev
   ```

4. Open the URL Vite prints (usually http://localhost:5173).

## Project structure

```
code-tuner-viz-backend/    Express API + Prisma schema
code-tuner-viz-frontend/   React app (pages, charts, API clients)
```
