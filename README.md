# mx-dispatch

Scheduled HTTPS dispatcher. Public repository on purpose: GitHub Actions
standard-runner minutes are **free and unmetered for public repositories**,
so the high-frequency polling channel keeps running on the free plan.

- Contains only the dispatch workflow (`.github/workflows/dispatch.yml`).
- All target endpoints require Bearer authentication; the token lives in
  GitHub Secrets (`CRON_SECRET`) and never appears in code or logs.
- The former private scheduler (`mingxin-marketing-cron`) keeps only
  manual-dispatch workflows and the daily CRM sync.
