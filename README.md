# PROVEN Plugins

GitHub marketplace repository for the PROVEN Onboarding plugin.

## Repository layout

- `.agents/plugins/marketplace.json` — workspace marketplace manifest
- `plugins/proven-onboarding/plugin.json` — portable Agent Plugins 1.0 manifest
- `plugins/proven-onboarding/.codex-plugin/plugin.json` — OpenAI/Codex compatibility manifest
- `plugins/proven-onboarding/skills/proven-onboarding/SKILL.md` — onboarding skill

## Import into ChatGPT workspace

1. Push the contents of this directory to the repository root.
2. In Admin / Workspace settings > Plugins, choose Add > Import marketplace.
3. Enter the GitHub repository URL only.
4. Leave Path empty when `.agents/plugins/marketplace.json` is at repository root.
5. After import or sync, open PROVEN Onboarding in Admin > Plugins and set its Installation policy to Available or Installed for the intended roles.
6. If set to Available, install it from the Plugins Directory before testing in a new chat.

The marketplace includes `policy.installation: AVAILABLE`, `policy.authentication: ON_INSTALL`, and `category: Productivity`, following the documented catalog format. Workspace GitHub import does not apply the repository's installation or authentication policy; configure access in Admin > Plugins.

## Update an existing import

Commit these files to the same GitHub repository, then open Admin > Plugins > Marketplaces, select PROVEN Plugins, and choose Sync now. Review the saved sync report after it completes. If the generic import-status banner remains, use the report's specific error to diagnose it; package validation alone does not verify workspace import.

The marketplace retains the existing plugin ID so GitHub continues to manage the same workspace plugin. This ID is workspace-specific.

## Archive contents

This ZIP has no enclosing wrapper directory. Extract its contents into the repository root and include the hidden `.agents/` and plugin `.codex-plugin/` directories. Verify that `.agents/plugins/marketplace.json` is committed; some file pickers hide dot-prefixed directories.

Version: `0.1.4`. The onboarding skill is unchanged from v3.

## Official documentation

- [Plugin packaging and marketplace format](https://developers.openai.com/plugins/build/plugins)
- [Workspace import, access, migration, and sync](https://learn.chatgpt.com/docs/enterprise/plugin-management)
