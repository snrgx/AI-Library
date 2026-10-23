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
- **Risk matrix** (likelihood × impact) and **what it can do** (reads private data, sends data out, runs code…)
- Checked against the **OWASP Agentic Skills Top 10** (OWASP: Open Worldwide Application Security Project)
- **Works with:** Claude, Claude Code, ChatGPT, OpenAI Codex, Gemini CLI, Cursor, GitHub Copilot
- **Before you install:** a checklist plus a ready **safe-install prompt** for your AI assistant (no `-y`, no `-g`, pinned versions, no scripts or hooks without asking)
- **Any other link (new in 1.6):** websites, documents (PDF, Word, Excel), short links and download links. It spots look-alike brand addresses (including Kuwaiti banks and delivery services), pages that ask for passwords, codes or card details, pressure and prize bait, download pushes, macros, and hidden instructions aimed at your AI. You get a **Before you open** checklist and a **safe reading prompt**. Programs, compressed files and download links are never opened, so nothing is downloaded: only their address is checked. Short links are followed only after you agree.
- English and Arabic

## Install

**Claude Code** (as a plugin):
```
/plugin marketplace add snrgx/AI-Library
/plugin install check-link@snrgx
```

**Claude app** (claude.ai, desktop): download this repo as a .zip, take the `plugins/check-link/skills/check-link` folder, zip it, then go to **Customize → Skills → + → Create skill → Upload a skill**.

**Other tools that support Agent Skills:** add `skills/check-link/SKILL.md` the way your tool loads skills.

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

Current version: **1.6.0**. See what changed in each version: [CHANGELOG.md](CHANGELOG.md) · [سجل الإصدارات](CHANGELOG.md#ملخص-بالعربية)

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
- **مصفوفة المخاطر** (الاحتمال × الأثر) و**ما الذي تستطيع فعله** (قراءة بياناتك الخاصة، إرسال بيانات للخارج، تشغيل أكواد…)
- مقارنة مع قائمة **OWASP Agentic Skills Top 10** (مشروع أمن التطبيقات المفتوح عالمياً)
- **يعمل مع:** Claude وClaude Code وChatGPT وOpenAI Codex وGemini CLI وCursor وGitHub Copilot
- **قبل التثبيت:** قائمة تحقق وأمر **تثبيت آمن** جاهز لمساعدك الذكي (بدون ‎-y‎ وبدون ‎-g‎، بإصدارات ثابتة، ولا سكربتات أو خطافات دون استئذان)
- **أي رابط آخر (جديد في 1.6):** المواقع والمستندات (PDF وWord وExcel) والروابط المختصرة وروابط التحميل. يكشف العناوين التي تقلّد العلامات المعروفة (ومنها البنوك وشركات التوصيل في الكويت)، والصفحات التي تطلب كلمات المرور أو رموز التحقق أو بيانات البطاقة، والضغط والجوائز الوهمية، ودفعك للتحميل، ووحدات الماكرو، والتعليمات المخفية الموجهة لمساعدك الذكي. وتحصل على قائمة **قبل الفتح** و**أمر قراءة آمن**. البرامج والملفات المضغوطة وروابط التحميل لا يتم فتحها أبداً، فلا يُحمَّل أي شيء: يُفحص عنوانها فقط. والروابط المختصرة لا تتم متابعتها إلا بموافقتك.
- بالعربية والإنجليزية

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
