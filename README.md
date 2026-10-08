# Plushcap for Antigravity

Research developer and AI trends and compare competitor content with Plushcap.
This plugin combines the hosted Plushcap MCP connection with a research skill
for company discovery, competitive analysis, leaderboards, and developer trends.
Its read-only tools query indexed engineering blog posts, YouTube videos, X
posts, LinkedIn activity, Hacker News attention, and historical trend metrics.
Coverage can be incomplete or delayed; check source dates and metric calculation
timestamps when interpreting results.

## Install and connect

Extract the distribution ZIP into a folder, or use the plugin source folder.
Install it with the Antigravity CLI:

```bash
agy plugin validate /path/to/plushcap
agy plugin install /path/to/plushcap
```

In Antigravity CLI, use `/plugin` to inspect the installed plugin and `/mcp` to
inspect its Plushcap connection. In Antigravity 2.0, open **Settings >
Customizations** and authenticate the Plushcap MCP server when prompted.
Follow Antigravity's browser sign-in flow, sign in to Plushcap, review the
requested access and return hostname, and authorize the connection. Complete
any authorization-code handoff only in Antigravity's dedicated authentication
interface, never in chat or configuration files.

A Plushcap account is required; available data, history, and usage limits depend
on your plan. Antigravity manages OAuth credentials and token refresh. This
plugin uses dynamic client registration and connects to
`https://mcp.plushcap.com/mcp` through the `serverUrl` field in `mcp_config.json`.
No API key, client secret, or token is included in the bundle or required in its
configuration.

## Try it

- "Use the Plushcap consumer skill to get Cloudflare's company profile and recent engineering posts."
- "Use Plushcap to compare Cloudflare and Vercel's content activity over the last three months. Cite sources and state the time window."
- "Use Plushcap to research AI agent trends. Show the periods and calculation dates behind the metrics."

The `plushcap-consumer` skill can be selected automatically for relevant
research requests. Mention it by name to explicitly request its workflow.

## Package and release

The plugin includes `plugin.json`, `mcp_config.json`,
`skills/plushcap-consumer/SKILL.md`, this README, `LICENSE`, `VERSION`, and the
icon and rights notice in `assets/`.

The release version is recorded in `VERSION` because Antigravity's documented
plugin manifest supports `name` and `description`, without release-version or
listing-link fields. Keep the manifest at the root when copying the bundle to a
standalone repository. Installing this bundle does not publish a marketplace
listing.

## Data handling

The skill sends research requests through the declared Plushcap MCP connection.
Tools retrieve indexed research data and do not publish content or start
collection jobs. Results may include public author names and professional
profiles. Plushcap stores account-linked authorization and usage records as
described in its privacy policy; read-only research access does not mean that
authentication and usage data are never stored.

## License and support

The configuration, skill, and documentation are licensed under the
[MIT License](LICENSE). The Plushcap icon and trademarks are excluded; see
[the asset notice](assets/NOTICE). This package license does not grant rights to
Plushcap's service or retrieved data, which remain subject to
[Plushcap's terms](https://www.plushcap.com/terms-of-service) and applicable
third-party rights.

- [Plushcap](https://www.plushcap.com)
- [Setup documentation](https://www.plushcap.com/docs/mcp)
- [Support](https://www.plushcap.com/support)
- [Privacy policy](https://www.plushcap.com/privacy-policy)
- [Antigravity plugin format](https://antigravity.google/docs/plugins)
- [Antigravity MCP and OAuth](https://antigravity.google/docs/mcp)
