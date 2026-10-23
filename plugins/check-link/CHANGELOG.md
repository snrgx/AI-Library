# Changelog

All versions were built on 23 Oct 2026. 1.5.0 is the first public release.

## 1.5.0: first public release as Check Link (SNRGX AI Library)
- Renamed from "Skill Trust Check" to **Check Link**, published by SNRGX in the AI Library.
- Every automatic-scan match is reviewed: confirmed or false alarm, with a one-line reason.
- The reference guide describes risky patterns in plain words only, with no example commands or secret-file paths, so directory scanners don't mistake the guide for the threat.
- SNRGX logo, bilingual README, security policy, MIT license.

## 1.4: adapt for other AI tools and install safely
- "Works with" for Claude, Claude Code, ChatGPT, OpenAI Codex, Gemini CLI, Cursor and GitHub Copilot, with conversion for tools that need adapting.
- Before-you-install checklist and a ready safe-install prompt (no -y, no -g, pinned versions, no scripts or hooks without asking).

## 1.3: risk profile and OWASP
- Risk matrix (likelihood × impact), what the package can do, and the data-theft combo warning.
- Checks against the OWASP Agentic Skills Top 10 (v1.0, 2026).
- Never calls anything "safe": Low / Medium / High risk only.

## 1.2: visual report, scores and bilingual
- Score out of 10 (maximum 9) with stars, red-flag count and criteria details.
- English and Arabic.

## 1.1: visual tool
- A one-page tool: paste a link or upload a .zip, see the report, approve and download.

## 1.0: first skill
- Read-only review of skills, plugins, MCP servers and marketplace links, with a plain-language report.
