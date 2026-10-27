# Templates

`plugin-starter/` is the starting shape for every new tool in the SNRGX AI Library. It is not a plugin and isn't listed in the library catalog, so nobody can install it.

To start a new tool:
1. Copy `plugin-starter/` to `plugins/<tool-name>/` (lowercase, hyphens).
2. Rename `skills/my-tool/` to `skills/<tool-name>/`, rename `SKILL.md.template` to `SKILL.md` (it is named `.template` here so installers don't offer the starter as a real skill), and replace `my-tool` / `My Tool` everywhere (plugin.json, SKILL.md, README.md).
3. Fill in SKILL.md, README.md (English and Arabic) and CHANGELOG.md. If the SKILL.md `description` contains a colon, write it as `description: >-` with the text on the next line, indented: other installers (skills.sh, Gemini, Codex) skip a skill whose header isn't valid YAML. Put any visual template in `skills/<tool-name>/assets/`.
   Add a square icon at `.claude-plugin/icon.png` (PNG, 512–2048 px, under 2 MB). Choose carefully: the Claude directory locks the icon the first time the plugin is submitted.
4. Add one entry to `.claude-plugin/marketplace.json`:
   `{ "name": "<tool-name>", "source": "./plugins/<tool-name>", "description": "…" }`
5. Add one row to the Tools table in the main README.
6. Check it with Check Link and with `claude plugin validate ./plugins/<tool-name>`, then `claude plugin validate .`.
7. After it's on `main`, create a release tagged `<tool-name>-v1.0.0`.
