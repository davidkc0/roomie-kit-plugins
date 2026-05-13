# Roomie Kit Claude Code Plugin

This plugin connects Claude Code to the shared Roomie Kit MCP server.

## Install

~~~txt
/plugin marketplace add davidkc0/roomie-kit-plugins
/plugin install roomie-kit@roomie-kit
/reload-plugins
~~~

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
