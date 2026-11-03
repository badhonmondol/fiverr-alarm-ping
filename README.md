# GigAlert — Ping

GitHub Actions workflow that keeps the Render server alive.

## How it works

`.github/workflows/ping.yml` runs every 10 minutes via cron.
Each run loops for 9 minutes, pinging `/health` every 1 minute.
This ensures the Render free-tier server never sleeps.

## Secret Required

`fiverr-alarm` repo → Settings → Secrets → Actions:

| Name | Value |
|---|---|
| `HEALTH_URL` | `https://fiverr-alarm-hiff.onrender.com/health` |

## Note

GitHub cron may delay up to 15-30 minutes during busy periods.
The server also self-pings every 4 minutes via `RENDER_EXTERNAL_URL`.
