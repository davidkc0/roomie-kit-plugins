# Roomie Kit Plugins

Roomie Kit plugins bring Roomie Kit Cloud setup tools into Claude Code and Codex.

Use them to sign in, bootstrap a Roomie Kit project, customize branding, run setup checks, look up docs, and verify a deployment without leaving your coding assistant.

## Requirements

- Node.js 20 or newer
- An active Roomie Kit Cloud account
- Claude Code or Codex installed locally

The plugins start the Roomie Kit MCP server through the published npm package:

~~~bash
npx -y roomie-kit-host mcp
~~~

## Claude Code

Add this marketplace and install the plugin:

~~~txt
/plugin marketplace add davidkc0/roomie-kit-plugins
/plugin install roomie-kit@roomie-kit
/reload-plugins
~~~

Then ask Claude Code:

~~~txt
Use Roomie Kit to start login.
~~~

## Codex

Add this marketplace:

~~~bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
~~~

Then enable **Roomie Kit** from the Codex Plugins UI.

## Sign In

You can start browser login from the plugin, or run it directly:

~~~bash
npx roomie-kit-host login
~~~

Login opens a Roomie Kit activation page and stores local auth in `.roomie-host/auth.local.json`.

## Tools

The plugin exposes:

- `roomie_login_start`
- `roomie_whoami`
- `roomie_bootstrap_project`
- `roomie_customize_app`
- `roomie_doctor`
- `roomie_health_check`
- `roomie_docs_lookup`

For now, production deploy execution remains a CLI command:

~~~bash
npx roomie-kit-host deploy --execute --resume
~~~

## Security

Installing the plugin is public. Managed tools require Roomie Kit Cloud login.

Customer Supabase, Vercel, Agora, and asset secrets stay local. They are not sent to Roomie Kit Cloud.

## Support

Email support@roomiekit.io or visit https://docs.roomiekit.io.
