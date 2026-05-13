# Roomie Kit Plugins

Public plugin marketplace for Roomie Kit Cloud customers.

These wrappers are intentionally thin. They start the shared Roomie Kit MCP server through the published npm package:

~~~bash
npx -y roomie-kit-host mcp
~~~

Installing the plugins is public. Managed tools require Roomie Kit Cloud browser login, and customer Supabase, Vercel, Agora, and asset secrets stay local.

## Claude Code

~~~txt
/plugin marketplace add davidkc0/roomie-kit-plugins
/plugin install roomie-kit@roomie-kit
/reload-plugins
~~~

Then log in:

~~~bash
npx roomie-kit-host login
~~~

## Codex

~~~bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
~~~

Then enable or install **Roomie Kit** from the Codex Plugins UI and log in:

~~~bash
npx roomie-kit-host login
~~~

## Tools

- `roomie_login_start`
- `roomie_whoami`
- `roomie_bootstrap_project`
- `roomie_customize_app`
- `roomie_doctor`
- `roomie_health_check`
- `roomie_docs_lookup`

Deploy execution remains available through the CLI while plugin deploy tooling matures:

~~~bash
npx roomie-kit-host deploy --execute --resume
~~~

## Support

Email support@roomiekit.io or visit https://docs.roomiekit.io.
