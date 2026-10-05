# PROVEN Plugins Marketplace

GitHub-backed marketplace containing the PROVEN Onboarding plugin.

## Repository layout

```text
.
├── .agents/
│   └── plugins/
│       └── marketplace.json
└── plugins/
    └── proven-onboarding/
        ├── plugin.json
        ├── README.md
        └── skills/
            └── proven-onboarding/
                └── SKILL.md
```

## Import into the PROVEN ChatGPT workspace

1. Push this repository to GitHub.
2. In ChatGPT, open Workspace settings → Plugins.
3. Select Add → Import marketplace.
4. Use the repository URL only. Leave Path empty if `.agents/plugins/marketplace.json` is at the repository root.
5. Authorize GitHub and import.
6. Review the import result and configure the plugin's workspace installation policy.

The marketplace entry includes the existing workspace plugin ID so GitHub can become the management source for the already-created PROVEN Onboarding plugin rather than creating a separate plugin.

If this repository is reused in a different ChatGPT workspace, remove the `pluginId` field from `.agents/plugins/marketplace.json` before importing there.

## Plugin

`proven-onboarding` is a skills-only plugin. It does not include an MCP server and does not claim access to PROVEN's production formulation engine, product catalog, customer database, approved claims service, or checkout systems.
