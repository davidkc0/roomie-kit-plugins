# Roomie Kit Codex Plugin

This plugin connects Codex to the shared Roomie Kit MCP server.

## Install

The public marketplace repo is `davidkc0/roomie-kit-plugins`.

~~~bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
~~~

Then enable or install **Roomie Kit** from the Codex Plugins UI.

## Login

~~~bash
npx roomie-kit-host login
~~~

The login opens a browser activation page and stores local auth for the CLI and plugin tools.

## MCP Server

The plugin launches:

~~~bash
npx -y roomie-kit-host mcp
~~~

Security note: installing the plugin is public. Managed tools require Roomie Kit Cloud login. Customer Supabase, Vercel, Agora, and asset secrets stay local and are not sent to Roomie Kit Cloud.
