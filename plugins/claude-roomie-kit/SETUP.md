# Roomie Kit Plugin Setup

Use this guide when helping someone with the Roomie Kit Claude Code plugin.

## Recommended Flow

1. Start with `roomie_login_start` if local auth is missing.
2. Run `roomie_whoami` to confirm the active Roomie Kit Cloud account.
3. For a new app, run `roomie_bootstrap_project`.
4. Run `roomie_customize_app` for app name, theme, colors, and local override folders.
5. Run `roomie_doctor` before deploy work.
6. Run `roomie_health_check` after the user has a deployed URL.

Deploy execution is currently handled by the CLI:

~~~bash
npx roomie-kit-host deploy --execute --resume
~~~

## Notes

- Do not ask users to paste Supabase, Vercel, or Agora secrets into chat.
- Customer provider secrets should stay in `.roomie-host/env.local` or their shell.
- Managed tools require Roomie Kit Cloud login even though the plugin itself is public.
