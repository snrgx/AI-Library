# Check Link: version log · سجل الإصدارات

All notable changes to Check Link. Format based on [Keep a Changelog](https://keepachangelog.com/). Versions: **major.minor.patch** (new features raise the middle number, fixes raise the last).

Every version below was built on 23 Oct 2026. **1.5.0 is the first public release.**

---

## [1.5.0] · 2026-10-23 · First public release

**Added**
- Published as **Check Link** in the **SNRGX AI Library** (github.com/snrgx/AI-Library), with the SNRGX logo, a bilingual README, a security policy and the MIT license.
- Every automatic-scan match is reviewed and labelled **confirmed** or **false alarm**, with a one-line reason.

**Changed**
- Renamed from "Skill Trust Check" to **Check Link**.
- The red warning bar only appears for critical matches the review didn't explain.

**Fixed**
- The reference guide quoted attack examples, so scanners (ours and the Claude directory's) mistook the guide for the threat. Risks are now described in plain words only; all 7 directory checks pass.

## [1.4.0] · 2026-10-23 · Works with other AI tools, safe install

**Added**
- **Works with:** Claude, Claude Code, ChatGPT, OpenAI Codex, Gemini CLI, Cursor and GitHub Copilot, each marked works / needs adapting / no, with the format files found.
- **Make the version for your tool:** converts the skill to another tool's format, leaving out risky parts.
- **Before you install** checklist that turns into a ready **safe-install prompt** (show the command and wait, no `-y`, no `-g`, pinned versions, no scripts, hooks or MCP servers without asking, list added files).

## [1.3.0] · 2026-10-23 · Risk profile and OWASP

**Added**
- **Risk matrix** (likelihood × impact) with each red flag plotted.
- **What it can do:** reads private data, reads outside content, sends data out, runs code, runs by itself, plus the **data-theft combo** warning.
- Check against the **OWASP Agentic Skills Top 10** (v1.0, 2026), with a weekly check for list updates.

**Changed**
- Never says "safe": only **Low / Medium / High risk**.

## [1.2.0] · 2026-10-23 · Visual report and bilingual

**Added**
- **Score out of 10** (highest 9: nothing is risk-free) with stars and a colour scale (green, yellow, orange, red).
- Red-flag counter, details by criteria, black-and-white design with colour only for risk.
- **English and Arabic**, with a full right-to-left layout.

## [1.1.0] · 2026-10-23 · Visual tool

**Added**
- One-page tool: paste a link or upload a .zip, watch the steps, read the report, approve and download.

## [1.0.0] · 2026-10-23 · First skill

**Added**
- Read-only review of AI skills, plugins, MCP servers and marketplace links, with a plain-language report and a risk verdict.

---

<div dir="rtl">

## ملخص بالعربية

- **1.5.0 (أول إصدار عام):** الاسم الجديد Check Link ضمن مكتبة SNRGX للذكاء الاصطناعي، شرح كل تطابق في الفحص التلقائي (مؤكد أو إنذار كاذب)، وإصلاح الدليل حتى لا تعتبره أدوات الفحص خطراً.
- **1.4.0:** «يعمل مع» 7 أدوات ذكاء اصطناعي مع التحويل لكل أداة، وقائمة «قبل التثبيت» مع أمر تثبيت آمن جاهز.
- **1.3.0:** مصفوفة المخاطر، «ما الذي تستطيع فعله»، ومقارنة مع قائمة OWASP. لا نقول «آمن» أبداً.
- **1.2.0:** تقييم من 10 مع نجوم، وتصميم مرئي، والعربية والإنجليزية.
- **1.1.0:** صفحة واحدة: الصق الرابط واقرأ التقرير وقرّر.
- **1.0.0:** أول مهارة: مراجعة للقراءة فقط مع تقرير بلغة بسيطة.

</div>
