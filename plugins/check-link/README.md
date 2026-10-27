<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="../../assets/snrgx-logo-dark.svg">
    <img src="../../assets/snrgx-logo-light.svg" alt="SNRGX" height="64">
  </picture>
  &nbsp;&nbsp;<b>AI Library</b> · مكتبة الذكاء الاصطناعي
</p>

# 🛡️ Check Link

**Trust-check any link *before* you install, open or trust it.** · [العربية ↓](#العربية)

AI skills, plugins and MCP servers are everywhere. Most are helpful. But a skill is a set of instructions your AI follows, and a plugin can run code on your computer. A bad one can hide instructions, read your passwords or keys, or send your data somewhere.

**Check Link** (by SNRGX) teaches your AI to review any skill, plugin, MCP server or marketplace link **without running it**, and gives you a plain-language report:

- **Score out of 10** with stars (never a perfect 10: nothing is risk-free) and a **Low / Medium / High risk** level
- **Red flags** with the exact file and line
- **Risk rating** (likelihood × impact, per red flag and overall) and **what it can do** (reads private data, sends data out, runs code…)
- Checked against the **OWASP Agentic Skills Top 10** (OWASP: Open Worldwide Application Security Project)
- **Works with:** Claude, Claude Code, ChatGPT, OpenAI Codex, Gemini CLI, Cursor, GitHub Copilot
- **Before you install:** a checklist plus a ready **safe-install prompt** for your AI assistant (no `-y`, no `-g`, pinned versions, no scripts or hooks without asking)
- **Any other link (new in 1.6):** websites, documents (PDF, Word, Excel), short links and download links. It spots look-alike brand addresses (including Kuwaiti banks and delivery services), pages that ask for passwords, codes or card details, pressure and prize bait, download pushes, macros, and hidden instructions aimed at your AI. You get a **Before you open** checklist and a **safe reading prompt**. Programs, compressed files and download links are never opened, so nothing is downloaded: only their address is checked. Short links are followed only after you agree.
- English and Arabic

**What you get with this plugin:** the skill **and its visual report**. After each check, your AI fills in Check Link's report design and gives you a visual page: score and stars, red-flag counter, risk matrix, what it can do, OWASP tiles, works with, red flags, and the checklist with a ready prompt to copy. Every report comes in **English and Arabic**, with a switch at the top. In the Claude app it opens in the chat; in Claude Code it's saved as an HTML file you open in your browser. A short text summary comes with it.

**Coming soon:** Check Link online, in your browser with nothing to install.

## Install

**Claude Code:**
```
/plugin marketplace add snrgx/AI-Library
/plugin install check-link@snrgx
```

**Claude app, OpenAI Codex, GitHub Copilot, Gemini CLI, Cursor and other agents:** see the [one-minute setup](../../README.md#install-1-minute-setup) on the library page. Every route is tested and has its own copy-paste lines.

**Prefer a reviewed, fixed version?** Every release is tagged (for example `check-link-v1.6.0`) on the [Releases](https://github.com/snrgx/AI-Library/releases) page.

## Use

Type the command with a link:
```
/check-link https://github.com/owner/repo/tree/main/skills/some-skill
```
(Installed as a Claude Code plugin, the command shows as `/check-link:check-link`.)

Or just ask:
> Check this link before I install it: https://github.com/…

> Is this link OK to open? (paste the link)

> افحص هذه المهارة قبل أن أثبّتها: https://github.com/…

## Version

Current version: **1.6.1**. See what changed in each version: [CHANGELOG.md](CHANGELOG.md) · [سجل الإصدارات](CHANGELOG.md#ملخص-بالعربية)

## Important

This is an AI-assisted review, **not a guarantee**. It catches common risks and explains them in plain language, but it can miss things. Re-check after every update. OWASP does not endorse this project; it checks *against* the OWASP list.

Found a problem? See [SECURITY.md](SECURITY.md).

---

<a id="العربية"></a>
<div dir="rtl">

## 🛡️ Check Link: فحص موثوقية المهارات

**افحص أي رابط *قبل* أن تثبّته أو تفتحه أو تثق به.**

المهارات والإضافات وخوادم MCP منتشرة في كل مكان، ومعظمها مفيد. لكن المهارة هي تعليمات يتبعها مساعدك الذكي، والإضافة قد تشغّل أكواداً على جهازك. والسيئة منها قد تخفي تعليمات، أو تقرأ كلمات مرورك ومفاتيحك، أو ترسل بياناتك إلى جهة ما.

أداة **Check Link** من SNRGX تعلّم مساعدك الذكي مراجعة أي مهارة أو إضافة أو خادم MCP أو رابط متجر **دون تشغيله**، ويعطيك تقريراً بلغة بسيطة:

- **تقييم من 10** مع نجوم (لا يوجد تقييم كامل 10، فلا شيء خالٍ من المخاطر) ومستوى **مخاطر منخفضة / متوسطة / عالية**
- **علامات الخطر** مع اسم الملف والسطر بالضبط
- **تقييم المخاطر** (الاحتمال × الأثر لكل علامة خطر وللحزمة كلها) و**ما الذي تستطيع فعله** (قراءة بياناتك الخاصة، إرسال بيانات للخارج، تشغيل أكواد…)
- مقارنة مع قائمة **OWASP Agentic Skills Top 10** (مشروع أمن التطبيقات المفتوح عالمياً)
- **يعمل مع:** Claude وClaude Code وChatGPT وOpenAI Codex وGemini CLI وCursor وGitHub Copilot
- **قبل التثبيت:** قائمة تحقق وأمر **تثبيت آمن** جاهز لمساعدك الذكي (بدون ‎-y‎ وبدون ‎-g‎، بإصدارات ثابتة، ولا سكربتات أو خطافات دون استئذان)
- **أي رابط آخر (جديد في 1.6):** المواقع والمستندات (PDF وWord وExcel) والروابط المختصرة وروابط التحميل. يكشف العناوين التي تقلّد العلامات المعروفة (ومنها البنوك وشركات التوصيل في الكويت)، والصفحات التي تطلب كلمات المرور أو رموز التحقق أو بيانات البطاقة، والضغط والجوائز الوهمية، ودفعك للتحميل، ووحدات الماكرو، والتعليمات المخفية الموجهة لمساعدك الذكي. وتحصل على قائمة **قبل الفتح** و**أمر قراءة آمن**. البرامج والملفات المضغوطة وروابط التحميل لا يتم فتحها أبداً، فلا يُحمَّل أي شيء: يُفحص عنوانها فقط. والروابط المختصرة لا تتم متابعتها إلا بموافقتك.
- بالعربية والإنجليزية

**ما تحصل عليه مع هذه الإضافة:** المهارة **مع تقريرها المرئي**. بعد كل فحص، يملأ مساعدك الذكي تصميم تقرير Check Link ويعطيك صفحة مرئية: التقييم والنجوم وعدد علامات الخطر ومصفوفة المخاطر وما الذي تستطيع فعله وقائمة OWASP و«يعمل مع» وعلامات الخطر وقائمة التحقق مع أمر جاهز للنسخ. كل تقرير يأتي **بالعربية والإنجليزية** مع زر للتبديل في الأعلى. في تطبيق Claude يظهر في المحادثة، وفي Claude Code يُحفظ كملف HTML تفتحه في المتصفح، ومعه ملخص نصي قصير.

**قريباً:** Check Link على الإنترنت، في متصفحك دون أي تثبيت.

## التثبيت

في Claude Code:
```
/plugin marketplace add snrgx/AI-Library
/plugin install check-link@snrgx
```

لتطبيق Claude وOpenAI Codex وGitHub Copilot وGemini CLI وCursor وغيرها: راجع [التثبيت في دقيقة](../../README.md#arabic) في صفحة المكتبة، ولكل طريقة أوامر جاهزة للنسخ.

## طريقة الاستخدام

اكتب الأمر مع الرابط:
```
/check-link https://github.com/…
```
(عند تثبيتها كإضافة في Claude Code يظهر الأمر بهذا الشكل: ‎`/check-link:check-link`‎)

أو اطلب ببساطة:
> افحص هذا الرابط قبل أن أثبّته: https://github.com/…

## تنبيه مهم

هذا تقييم بمساعدة الذكاء الاصطناعي **وليس ضماناً**. أعد الفحص بعد كل تحديث. هذا المشروع غير معتمد من OWASP، بل يقارن مع قائمتها.

</div>

---

Created by **Hamidah Rahimi** ([@hamidahrk](https://github.com/hamidahrk)) · **SNRGX** ([@snrgx](https://github.com/snrgx))
15 years as a business owner · MBA · Design Thinking (University of Virginia) · 1st place globally, MIT App Inventor 2023 · WRO Kuwait

License: MIT. Free to use, share and adapt; please keep the credit.
