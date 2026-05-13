---
description: Use Roomie Kit Cloud tools to set up, customize, diagnose, and prepare Roomie Kit apps for paid customers.
---

# Roomie Kit

Use the Roomie Kit MCP tools when the user asks to set up, customize, diagnose, or prepare a Roomie Kit app.

Start with `roomie_login_start` if local auth is missing, then use `roomie_whoami` to confirm the account. For new apps, use `roomie_bootstrap_project`, `roomie_customize_app`, `roomie_doctor`, and `roomie_health_check` in that order.

Deploy execution is still handled by the CLI:

```bash
npx roomie-kit-host deploy --execute --resume
```

Security note: installing this plugin is public. Managed tools require Roomie Kit Cloud login. Customer Supabase, Vercel, Agora, and asset secrets stay local and are not sent to Roomie Kit Cloud.
