# Roomie Kit Plugin Setup

Use this guide when a user installs the Roomie Kit Claude Code plugin.

1. Confirm Node.js 20 or newer is available.
2. Ask the user to run `npx roomie-kit-host login`, or call the `roomie_login_start` MCP tool if available.
3. Have the user approve the browser activation code at roomiekit.io.
4. Run `roomie_whoami` to confirm their paid Roomie Kit Cloud account.
5. For a new app, use `roomie_bootstrap_project`, then `roomie_customize_app`, then `roomie_doctor`.
6. For deploy execution, tell the user to run `npx roomie-kit-host deploy --execute --resume` until plugin deploy execution ships.

Security note: installing the plugin is public. Managed tools require Roomie Kit Cloud login. Customer Supabase, Vercel, Agora, and asset secrets stay local and are not sent to Roomie Kit Cloud.
