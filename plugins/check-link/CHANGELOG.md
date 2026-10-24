# Check Link: version log · سجل الإصدارات

All notable changes to Check Link. Format based on [Keep a Changelog](https://keepachangelog.com/). Versions: **major.minor.patch** (new features raise the middle number, fixes raise the last).

**Check Link has two parts.**
- **Skill** (this plugin): instructions your AI follows. From 1.6.0 it also makes the **visual report** (score, stars, risk matrix, red flags, checklist and prompt) from a template included in the plugin.
- **Page**: the online version by SNRGX (a Claude artifact): paste a link or upload a .zip and watch the check run, with buttons to convert, translate and download. It isn't installed with the plugin; it's linked from the README.

Each entry below says which part it applies to. Every version was built on 23–24 Oct 2026. **1.5.0 is the first public release.**

---

## [1.6.0] · 2026-10-24 · Any link, not just AI skills

**Added**
- Skill: the **visual report** now comes with the plugin. After each check, the AI fills in `assets/report-template.html` (the same design as the page) and gives you the visual report: in the Claude app as a page in the chat, in Claude Code as an HTML file. The template only draws the report: no network requests, nothing run.
- Docs: a link to try the online page without installing.
- Skill and page: **link types** (AI package, code project, website, document, short link, download link, program, compressed file, media). Each kind is checked its own way and named at the top of the report.
- Skill and page: **websites and documents**: look-alike brand addresses (including Kuwaiti banks, telecoms and delivery services), no https, hidden destinations, pages that ask for passwords, codes, card or ID details, pressure, prize bait, download pushes, macros, and hidden instructions aimed at AI assistants. Scores and "what it can do" fit each kind.
- Skill and page: a **Before you open** checklist and a **safe reading prompt** for any AI assistant.
- Skill and page: programs, compressed files and **download links** (release downloads, "export=download", "dl=1"…) are never opened, so nothing is downloaded: only the address is checked, with a clear "this isn't an antivirus" caution.
- Skill and page: **short links ask first** before being followed ("short link → final address"), and warn if they led to a file the browser may have saved.
- Skill and page: in Arabic reports, red flags are written in Arabic and each English quote gets a line saying what it means.
- Page only: a button to translate a finished report into the other language without running the check again.
- Page only: reads PDFs through Google's document viewer when the browser shows no text, and says so in the report.

**Changed**
- Skill and page: new golden rule: on a page, only read. Never log in, type, click, enable macros or download.
- Skill and page: scores use the full scale. Only a perfect 10 is capped, at 9.5 (before, everything was capped at 9, which pulled good scores down).
- Skill and page: mentions are not requests. A bank's help page that mentions "civil ID", or a security article quoting scam phrases, isn't flagged as asking for them.
- Skill and page: install and safe-reading prompts are always in English with exact technical details (paths, full commit, commands), even in Arabic reports, so AI assistants follow them precisely.
- Skill: clones go into a temporary folder outside your project, are never run, and are deleted afterwards.
- Docs: how to stay on a reviewed version (install from a fixed release instead of the newest files).

**Fixed**
- Docs: the security policy pointed to a version log that didn't exist at the top of the library.
- Docs: this log now says which part (skill or page) each change belongs to. Earlier entries described page features as if they came with the plugin.
- Docs: the weekly OWASP check is a review by the author, approved before any update; it isn't part of the skill's files.
- Docs: tools are checked by their author before release; that is not an independent audit.

## [1.5.0] · 2026-10-23 · First public release

**Added**
- Published as **Check Link** in the **SNRGX AI Library** (github.com/snrgx/AI-Library), with the SNRGX logo, a bilingual README, a security policy and the MIT license.
- Skill and page: every automatic-scan match is reviewed and labelled **confirmed** or **false alarm**, with a one-line reason.

**Changed**
- Renamed from "Skill Trust Check" to **Check Link**.
- Page only: the red warning bar only appears for critical matches the review didn't explain.

**Fixed**
- Skill: the reference guide quoted attack examples, so scanners (ours and the Claude directory's) mistook the guide for the threat. Risks are now described in plain words only; all 7 directory checks pass.

## [1.4.0] · 2026-10-23 · Works with other AI tools, safe install

**Added**
- Skill and page: **Works with**: Claude, Claude Code, ChatGPT, OpenAI Codex, Gemini CLI, Cursor and GitHub Copilot, each marked works / needs adapting / no.
- Skill: on request, rewrites a checked skill in another tool's format, leaving out risky parts. Page: the same as a "Make the version for your tool" button with a .zip download.
- Skill and page: a **Before you install** checklist and a ready **safe-install prompt** (show the command and wait, no `-y`, no `-g`, pinned versions, no scripts, hooks or MCP servers without asking, list added files). Page only: tick the items you want and the prompt updates.

## [1.3.0] · 2026-10-23 · Risk profile and OWASP

**Added**
- Skill and page: likelihood × impact rating for each red flag and overall. Page only: drawn as a **risk matrix** with each flag plotted.
- Skill and page: **what it can do** (reads private data, reads outside content, sends data out, runs code, runs by itself), plus the **data-theft combo** warning.
- Skill and page: check against the **OWASP Agentic Skills Top 10** (v1.0, 2026).

**Changed**
- Skill and page: never says "safe": only **Low / Medium / High risk**.

## [1.2.0] · 2026-10-23 · Scores and bilingual

**Added**
- Skill and page: **score out of 10** with stars and a colour scale (green, yellow, orange, red).
- Skill and page: **English and Arabic**.
- Page only: red-flag counter, details by criteria, black-and-white design with colour only for risk, full right-to-left layout.

## [1.1.0] · 2026-10-23 · Visual page

**Added**
- Page only: one-page tool. Paste a link or upload a .zip, watch the steps, read the report, approve and download.

## [1.0.0] · 2026-10-23 · First skill

**Added**
- Skill: read-only review of AI skills, plugins, MCP servers and marketplace links, with a plain-language report and a risk verdict.

---

<div dir="rtl">

## ملخص بالعربية

لأداة Check Link جزءان، والأول فقط موجود في هذا المستودع: **المهارة** (تعليمات نصية تكتب التقرير نصاً)، و**الصفحة** (أداة مرئية منفصلة من SNRGX فيها الرسوم والأزرار، وليست ضمن هذه الإضافة).

- **1.6.0:** المهارة والصفحة: فحص أي رابط وليس المهارات فقط (المواقع والمستندات والروابط المختصرة وروابط التحميل والبرامج والملفات المضغوطة)، وكشف العناوين المقلّدة والصفحات التي تطلب كلمات المرور أو البطاقات والتعليمات المخفية للذكاء الاصطناعي، مع قائمة «قبل الفتح» وأمر قراءة آمن، وعلامات خطر بالعربية. الصفحة فقط: زر ترجمة التقرير.
- **1.5.0 (أول إصدار عام):** الاسم الجديد Check Link ضمن مكتبة SNRGX، وشرح كل تطابق في الفحص التلقائي (مؤكد أو إنذار كاذب).
- **1.4.0:** المهارة والصفحة: «يعمل مع» 7 أدوات ذكاء اصطناعي، وقائمة «قبل التثبيت» مع أمر تثبيت آمن. الصفحة فقط: زر التحويل وتحديد عناصر القائمة.
- **1.3.0:** المهارة والصفحة: تقييم الاحتمال والأثر، «ما الذي تستطيع فعله»، ومقارنة مع قائمة OWASP. الصفحة فقط: رسم مصفوفة المخاطر.
- **1.2.0:** المهارة والصفحة: تقييم من 10 مع نجوم، والعربية والإنجليزية. الصفحة فقط: التصميم المرئي.
- **1.1.0:** الصفحة فقط: أداة من صفحة واحدة.
- **1.0.0:** المهارة: أول مراجعة للقراءة فقط مع تقرير بلغة بسيطة.

</div>
