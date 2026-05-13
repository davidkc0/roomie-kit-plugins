# Roomie Kit Codex Plugin

Use Roomie Kit from Codex to bootstrap, customize, and diagnose Roomie Kit apps.

The plugin starts the shared Roomie Kit MCP server through:

~~~bash
npx -y roomie-kit-host mcp
~~~

## Requirements

- Node.js 20 or newer
- Codex with plugin support
- An active Roomie Kit Cloud account

## Install

Add the public marketplace:

~~~bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
~~~

Then enable **Roomie Kit** from the Codex Plugins UI.

## Sign In

~~~bash
npx roomie-kit-host login
~~~

You can also ask Codex:

~~~txt
Use Roomie Kit to start login.
~~~

Login opens a browser activation page and stores auth locally in `.roomie-host/auth.local.json`.

## Common Prompts

- `Use Roomie Kit to check who I am.`
- `Use Roomie Kit to bootstrap this project. Use app name Acme Live.`
- `Use Roomie Kit to customize this app with the stream-dark theme.`
- `Use Roomie Kit to run doctor on this project.`
- `Use Roomie Kit to look up the livestreaming docs.`

## Security

Installing the plugin is public. Managed tools require Roomie Kit Cloud login.

Customer Supabase, Vercel, Agora, and asset secrets stay local. They are not sent to Roomie Kit Cloud.
