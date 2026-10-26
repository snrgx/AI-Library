<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/snrgx-logo-dark.svg">
    <img src="assets/snrgx-logo-light.svg" alt="SNRGX" height="64">
  </picture>
  &nbsp;&nbsp;<b>AI Library</b> · مكتبة الذكاء الاصطناعي
</p>

# SNRGX AI Library

Infusing AI into process engineering: visual, bilingual (EN/AR) skills, plugins and MCP tools for founders and creators, with a friendly UI/UX, so anyone can use them.

Built by **SNRGX**. Every tool is checked with Check Link by its author before release. That is our own review, not an independent audit: outside reviews are welcome (see [SECURITY.md](SECURITY.md)).

## Tools

| Tool | What it does | Status |
|---|---|---|
| 🛡️ [**Check Link**](plugins/check-link) | Paste any link and get a **visual** trust check before you install or open it ([try it online](https://claude.ai/artifact/EkkUzsiWypeoe5tpH7XfFy)). AI skills, plugins and MCP servers: score out of 10, likelihood × impact risk rating, OWASP Agentic Skills Top 10, red flags and a safe-install prompt. Websites, documents and short links: look-alike addresses, requests for passwords or cards, hidden AI instructions | [v1.6.0](plugins/check-link/CHANGELOG.md) |

More tools are on the way.

## How to install and use Check Link

### 1. Try it online, no install
Open the [Check Link page](https://claude.ai/artifact/EkkUzsiWypeoe5tpH7XfFy), paste a link and press **Check it**. Checking links needs the Claude desktop app; uploading a skill's .zip works anywhere in Claude.

### 2. Claude Code
```
/plugin marketplace add snrgx/AI-Library
/plugin install check-link@snrgx
```
Then check any link:
```
/check-link:check-link https://github.com/owner/repo
```
or just ask: *"Check this link before I install it: …"*. You get a short summary in the chat and a visual report saved as `check-link-report-<name>.html`. Open it in your browser.

### 3. Claude app (web, desktop)
1. Turn on **Settings → Capabilities → Code execution and file creation**.
2. Download this repo (**Code → Download ZIP**, or a release from [Releases](https://github.com/snrgx/AI-Library/releases)) and unzip it.
3. Zip only the folder `plugins/check-link/skills/check-link`.
4. In Claude: **Customize → Skills → + → Upload a skill**, and choose that zip.
5. In a new chat, paste a link and ask *"Check this link"*. The visual report arrives as a file in the chat.

### What you get
A visual report in **English and Arabic** (switch at the top): score out of 10 with stars, risk level (low, medium, high: never "safe"), red flags with the exact file and line, risk matrix, what it can do, OWASP Agentic Skills Top 10, which AI tools it works with, a **Before you install** checklist and a ready prompt for your AI assistant. Websites, documents and short links get a **Before you open** checklist instead. Nothing you check is ever installed, run or downloaded.

**Stay on a reviewed version:** the commands above follow the newest files. For a fixed version, use a release from [Releases](https://github.com/snrgx/AI-Library/releases) (for example `check-link-v1.6.0`).

Every new tool added to this library appears in the same place. Each tool's own README has more detail.

## Library structure

Each tool has its own folder with all its files. Only the library's shared files sit at the top.

```
AI-Library/
├── .claude-plugin/marketplace.json   the catalog: every tool in the library
├── README.md                         this page: all tools and how to install them
├── LICENSE · SECURITY.md             rules for the whole library
├── assets/                           SNRGX logos, shared by all tools
├── templates/plugin-starter/         the starting shape for a new tool (not installable)
└── plugins/
    └── check-link/                   everything for Check Link
        ├── .claude-plugin/plugin.json   name, version, icon
        ├── README.md · CHANGELOG.md · LICENSE · SECURITY.md
        └── skills/check-link/        SKILL.md · references/ · assets/report-template.html
```

**For users:** add the library once (`/plugin marketplace add snrgx/AI-Library`), then install only the tools you want, each by name: `/plugin install <tool>@snrgx`. Every tool has its own version, version log and release tag (for example `check-link-v1.6.0`), so updating one never changes another.

**For new tools:** see [templates/README.md](templates/README.md).

## Safety

Every tool in this library is reviewed by its author with **Check Link** before release. This is not an independent audit and not a guarantee. Found a problem? See [SECURITY.md](SECURITY.md).

---

<div dir="rtl">

## مكتبة SNRGX للذكاء الاصطناعي

مهارات وإضافات وأدوات MCP من **SNRGX** لروّاد الأعمال وصنّاع المحتوى والفرق، بالعربية والإنجليزية، بلغة بسيطة، وتُفحص كل أداة قبل نشرها.

**الأدوات:** 🛡️ [**Check Link**](plugins/check-link): الصق أي رابط (مهارة أو إضافة أو خادم MCP، أو موقع إلكتروني، أو مستند) واحصل على تقرير موثوقية مرئي قبل التثبيت أو الفتح.

### طريقة التثبيت والاستخدام

**1. جرّبها على الإنترنت دون تثبيت:** افتح [صفحة Check Link](https://claude.ai/artifact/EkkUzsiWypeoe5tpH7XfFy)، والصق الرابط، واضغط «افحص الآن». فحص الروابط يحتاج تطبيق Claude لسطح المكتب، ورفع ملف ‎.zip‎ يعمل في أي مكان في Claude.

**2. في Claude Code:** اكتب الأمرين:
```
/plugin marketplace add snrgx/AI-Library
/plugin install check-link@snrgx
```
ثم افحص أي رابط بالأمر ‎`/check-link:check-link`‎ متبوعاً بالرابط، أو اطلب ببساطة: «افحص هذا الرابط قبل أن أثبّته». ستحصل على ملخص في المحادثة وتقرير مرئي محفوظ كملف HTML تفتحه في المتصفح.

**3. في تطبيق Claude:**
1. فعّل «تنفيذ الأكواد وإنشاء الملفات» من الإعدادات ← الإمكانات.
2. حمّل هذا المستودع (Code ← Download ZIP) وفك ضغطه.
3. اضغط المجلد ‎`plugins/check-link/skills/check-link`‎ وحده في ملف ‎.zip‎.
4. في Claude: تخصيص ← المهارات ← + ← رفع مهارة، واختر الملف.
5. في محادثة جديدة، الصق الرابط واكتب «افحص هذا الرابط». سيصلك التقرير المرئي كملف في المحادثة.

**هيكل المكتبة:** لكل أداة مجلد خاص بها داخل ‎`plugins/`‎ يضم كل ملفاتها، وفي الأعلى فقط ملفات المكتبة المشتركة (الفهرس والصفحة الرئيسية والترخيص والشعارات). تضيف المكتبة مرة واحدة، ثم تثبّت الأدوات التي تريدها فقط، كل أداة باسمها، ولكل أداة إصدارها وسجلها الخاص.

**ما تحصل عليه:** تقرير مرئي **بالعربية والإنجليزية** مع زر للتبديل: تقييم من 10 مع نجوم، ومستوى المخاطر (منخفضة، متوسطة، عالية، ولا نقول «آمن» أبداً)، وعلامات الخطر مع الملف والسطر، ومصفوفة المخاطر، وقائمة OWASP، والأدوات التي يعمل معها، وقائمة «قبل التثبيت» مع أمر جاهز لمساعدك الذكي. لا يتم تثبيت أو تشغيل أو تحميل أي شيء تفحصه.

</div>

---

Created by **Hamidah Rahimi** ([@hamidahrk](https://github.com/hamidahrk)) · **SNRGX** ([@snrgx](https://github.com/snrgx)). License: MIT (see [LICENSE](LICENSE); each tool also carries its own license file).
