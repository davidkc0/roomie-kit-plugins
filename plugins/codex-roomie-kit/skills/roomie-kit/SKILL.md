---
description: Use Roomie Kit Cloud tools to set up, customize, diagnose, and prepare Roomie Kit apps for paid customers.
---

# Roomie Kit

Use the Roomie Kit MCP tools when the user asks to set up, customize, diagnose, or prepare a Roomie Kit app.

## Workflow

1. If local auth is missing, call `roomie_login_start` and guide the user through browser activation.
2. Call `roomie_whoami` to confirm the paid Roomie Kit Cloud account.
3. For a new app, call `roomie_bootstrap_project` with the intended app name and target path.
4. Call `roomie_customize_app` for app name, theme template, brand colors, and local override folders.
5. Call `roomie_doctor` before deployment work.
6. Call `roomie_health_check` after the user has a deployed URL.
7. Use `roomie_docs_lookup` whenever a docs link would help.

Deploy execution is still handled by the CLI:

```bash
npx roomie-kit-host deploy --execute --resume
```

Security note: installing this plugin is public. Managed tools require Roomie Kit Cloud login. Customer Supabase, Vercel, Agora, and asset secrets stay local and are not sent to Roomie Kit Cloud.
