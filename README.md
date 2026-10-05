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

Repository policy fields are intentionally omitted because workspace GitHub import does not apply installation/authentication policy from the marketplace file.
