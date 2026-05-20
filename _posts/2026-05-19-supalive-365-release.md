---
tags: ["2026", "Releases"]
---

## supalive-365

![supalive-365 Banner](/images/supalive-365/banner.png)

I'm excited to announce the release of **supalive-365** — centralized uptime automation for all Supabase projects.

### About the Project

supalive-365 is a GitHub Actions–based keepalive system that prevents Supabase free-tier projects from pausing due to inactivity. It sends daily health pings to every configured project using lightweight, deterministic workflows.

### Features

Daily scheduled pings run at **06:00 UTC**. One repository can target **multiple Supabase projects**, using only **public anon keys** (safe by design). Each run logs **per-project success or failure** in the Actions output. After secrets and config are in place, maintenance is low. The design is also **extensible** for retries, alerts, or Management API usage later.

### How It Works

Supabase pauses free-tier projects after roughly seven days without API activity. supalive-365 issues a daily `GET` request to each project's health endpoint:

`{SUPABASE_URL}/auth/v1/health`

That request counts as valid activity and resets the inactivity clock.

### Resources

- **🔗 GitHub Repository**: [supalive-365 on GitHub](https://github.com/bmoler68/supalive-365)

For questions, support, or feedback, please contact me at bmoler@brianmoler.com.
