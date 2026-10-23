# Red-flag patterns (reference)

Plain-language guide for reviewers. It describes what risky skills, plugins and MCP servers tend to do, so you can recognise it. It contains no working commands and no example payloads on purpose.

## How to search

Use ordinary text search inside the folder you are reviewing. Choose your own search words for each category below (for example the names of shell commands, encoding functions or network calls you would expect). Every match is a candidate to read, not a verdict.

## What to look for

| Risk | What it looks like, in words | OWASP |
|---|---|---|
| Download-and-run | A command that fetches a script from the internet and passes it straight to a shell or interpreter, so whatever is online gets executed | AST01 |
| Hidden code | Text that is encoded (for example base64 or hex), decoded at run time and then executed | AST01, AST08 |
| Prompt injection | Instructions that try to override the assistant's rules, give it a new role, tell it to approve the package, or tell it to keep something from the user | AST01 |
| Secret collection | Instructions or code that open private files, saved passwords, access keys, browser data or crypto wallets | AST01, AST03 |
| Data sending | Uploading or posting anything to chat webhooks, paste sites or unknown servers | AST01 |
| Invisible text | Zero-width or text-direction control characters, hidden HTML comments, text pushed out of view | AST08 |
| Remote instructions | Telling the assistant to fetch rules or instructions from a web address and follow them | AST05 |
| Auto-running | Hooks that fire on every prompt or tool call, install-time scripts, MCP servers that start by themselves | AST06 |
| Unpinned updates | "Always use the latest version", installers without a fixed version | AST07 |
| Impersonation | Names that copy a famous brand or project, "official" claims from an unknown account | AST02, AST04 |

## Websites and documents

| Risk | What it looks like, in words |
|---|---|
| Look-alike address | A known brand's name inside an address that isn't the brand's, often with words like login, verify, account, bill or delivery; swapped letters or numbers; foreign look-alike letters; a bare number instead of a name |
| Hidden destination | A short link, or an @ in the address, that hides where you really go |
| Asking for secrets | A page or form that asks you to type a password, one-time code, card number or ID number |
| Pressure | Threats of suspension, deadlines, "final notice" |
| Bait | Prizes, gifts, free money |
| Download push | Buttons or text urging you to download, install or "update" a file |
| Active content | A document asking you to enable macros, content or editing |
| AI-aimed instructions | Text addressed to AI assistants, often hidden, asking them to ignore rules, trust the page or pass on data |

A page that only *mentions* passwords or scams (a bank's help page, a security article) is not asking for them.

**Context matters:** documentation that explains an attack is not a threat. Flag only what would actually do the risky thing when the package is used, and treat an example command that the package tells the assistant to *run* as real.
