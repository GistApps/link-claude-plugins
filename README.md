# Gist plugins for Claude

Plugin bundles for the [Claude directory](https://claude.ai/directory), one per
Gist app. Each plugin pairs that app's MCP connector with skills
that teach Claude the app's common workflows.

| Plugin | Connector URL | Skills |
| --- | --- | --- |
| `gist-calendar` | `https://mcp.gist.link/calendar/mcp` | daily-agenda, schedule-meeting |
| `gist-crm` | `https://mcp.gist.link/crm/mcp` | account-brief, log-interaction |
| `gist-drive` | `https://mcp.gist.link/drive/mcp` | find-file, organize-files |
| `gist-mail` | `https://mcp.gist.link/mail/mcp` | triage-inbox, draft-reply |
| `gist-sheets` | `https://mcp.gist.link/sheets/mcp` | analyze-sheet, update-tracker |
| `gist-support` | `https://mcp.gist.link/support/mcp` | triage-queue, draft-ticket-reply |
| `gist-teams` | `https://mcp.gist.link/teams/mcp` | catch-up, create-task |

The connectors are served by the GistLink MCP server at `mcp.gist.link`.
Sign-in is OAuth through `auth.api.gist.link`, and each connection only reaches
its own app with the signed-in user's permissions. Connector documentation:
https://developers.gist.link/mcp/connectors/.

## Install in Claude Code

```sh
/plugin marketplace add <github-owner>/claude-plugins
/plugin install gist-sheets@gistlink
```

## Layout

```
.claude-plugin/marketplace.json   marketplace listing all plugins
plugins/gist-<app>/
  .claude-plugin/plugin.json      manifest (name, displayName, version, license)
  .mcp.json                       the app's remote MCP connector
  skills/<skill>/SKILL.md         workflows
  README.md                       directory listing text (40+ words)
```

## Rules

- Keep each plugin's skills in sync with its connector's tool names (listed in
  the connector documentation).
- Raise `version` in `plugin.json` with every release; never rename a plugin.
- No secrets, symlinks, submodules, LFS files, binaries other than images, or
  `.DS_Store` files; keep every file under 256 KiB.
- Validate before pushing: `claude plugin validate ./plugins/gist-<app>`.
- Each plugin folder is submitted separately in the Claude developer portal
  (Plugin bundle → this repository → plugin path `plugins/gist-<app>`), and
  paired with the matching MCP connector listing.

## Privacy

See https://gist.link/privacy.
