# Coda MCP Codex Plugin

This bundle installs a local Codex plugin named `coda-mcp`.

The plugin connects Codex to Coda's remote MCP endpoint:

```text
https://coda.io/apis/mcp
```

## Install

From this bundle directory, run:

```bash
./install.sh
```

The installer will:

- Copy the plugin to `~/plugins/coda-mcp`.
- Create or update `~/.agents/plugins/marketplace.json`.
- Register the plugin with `authentication: "ON_INSTALL"` so Codex can discover Coda's MCP tools after authentication.

Then restart Codex.

## Enable And Test

After restarting Codex:

1. Open the local marketplace in Codex.
2. Install or enable **Coda MCP** if it is not already enabled.
3. Complete the browser-based Coda login flow if prompted.
4. Start a fresh chat and ask:

```text
Are you connected to the Coda MCP?
```

Expected result: Codex reports that Coda MCP is connected and authenticated as your Coda account.

## Security Notes

The default plugin registration uses browser OAuth through Coda's remote MCP endpoint. No Coda token is included in this bundle.

The plugin still includes a manual fallback launcher for local stdio testing. Use that only if browser OAuth is unavailable. Do not paste Coda tokens into chat, commit them to files, or store them in `.env` files inside the plugin.

## Uninstall

To remove the plugin files and marketplace entry, run:

```bash
./uninstall.sh
```

Then restart Codex.
# codex_coda_MCP
A Coda.io Codex compatible plugin
