# Damage Monitoring and Tracking

Your main page is `frontend/DamageMonitoringPage.jsx`.

It contains the farmer-facing **My Damage Reports** screen, where a farmer can:

- monitor pending, reviewing, resolved, and rejected reports;
- search and filter report records;
- inspect evidence photos, incident details, MAO feedback, and review history;
- export a CSV report list; and
- print or save an individual damage report as a PDF.

## Add it to the team project

1. Copy `DamageMonitoringPage.jsx` to `client/src/pages/`.
2. In `client/src/App.jsx`, import `MyReportsPage` from `./pages/DamageMonitoringPage.jsx`.
3. Keep the existing route: `#my-reports` renders `<MyReportsPage />`.

The page uses the project’s existing shared `AppShell`, `PageHeader`, `StatusBadge`, API helper, realtime hook, and `GET /api/reports/mine` endpoint. The current backend files that provide the tracking data are:

- `server/src/api/routes/reportRoutes.js`
- `server/src/api/controllers/reportController.js`
- `server/src/api/models/reportModel.js`
- `server/db/migrations/013_report_scan_review_history.sql`
