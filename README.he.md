<div dir="rtl">

<p align="center">
  <a href="README.md">English</a> | <a href="README.he.md">עברית</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AI-Agent%20Skills-blueviolet?style=for-the-badge&logo=robot&logoColor=white" alt="מיומנויות סוכני AI"/>
  <img src="https://img.shields.io/badge/Skills-210+-green?style=for-the-badge" alt="מספר מיומנויות"/>
  <img src="https://img.shields.io/github/stars/eladjak/ai-agents-skills?style=for-the-badge&logo=github&color=yellow" alt="כוכבי GitHub"/>
  <img src="https://img.shields.io/github/license/eladjak/ai-agents-skills?style=for-the-badge" alt="רישיון"/>
  <img src="https://img.shields.io/github/last-commit/eladjak/ai-agents-skills?style=for-the-badge" alt="עדכון אחרון"/>
</p>

<p align="center">
  <img src="hero-skills.jpg" alt="מיומנויות סוכני AI"/>
</p>

<p align="center">
  <b>אם המאגר הזה שימושי לכם, בבקשה תנו <a href="https://github.com/eladjak/ai-agents-skills">⭐ כוכב</a>!</b>
</p>

# מאגר מיומנויות לסוכני AI

אוסף מיומנויות מתמחות לסוכני קידוד AI (Claude Code, GitHub Copilot, Cursor, Windsurf).

## התחלה מהירה

### באמצעות skill-sync (מומלץ)

```powershell
# הצגת מיומנויות זמינות
powershell -File ~/.claude/skills/skill-sync/sync.ps1 list

# סנכרון כל המיומנויות
powershell -File ~/.claude/skills/skill-sync/sync.ps1 sync

# בדיקת עדכונים
powershell -File ~/.claude/skills/skill-sync/sync.ps1 check
```

### התקנה ידנית

1. שכפלו את המאגר: `gh repo clone eladjak/ai-agents-skills`
2. העתיקו מיומנויות ל-`~/.claude/skills/`

## ספריית מיומנויות ישראלית (92 מיומנויות) - חדש!

ספריית מיומנויות מלאה לשוק הישראלי מ-[Skills IL](https://agentskills.co.il). ראו [skills/israeli-skills-library/README.md](skills/israeli-skills-library/README.md) לפרטים מלאים.

קטגוריות: מיסים ופיננסים (23), שירותי ממשלה (16), לוקליזציה (15), כלי פיתוח (13), שיווק וצמיחה (9), תקשורת (7), אבטחה ותאימות (7), שירותי בריאות (5), מזון ומסעדנות (4), טכנולוגיה משפטית (3), חינוך (3).

```bash
# התקנת כל המיומנויות הישראליות
npx skills-il add skills-il/tax-and-finance --all -g
npx skills-il add skills-il/localization --all -g
npx skills-il add skills-il/government-services --all -g
# ... ראו רשימה מלאה ב-israeli-skills-library/README.md
```

## מיומנויות זמינות (210+ סה"כ)

| מיומנות | תיאור |
|---------|-------|
| owasp-security | מימוש נהלי קידוד מאובטח לפי OWASP Top 10 |
| planning-patterns | תבניות תכנון לפיתוח |
| postgres-patterns | תבניות PostgreSQL לאופטימיזציית שאילתות, עיצוב סכמה, אינדקסים ואבטחה |
| nano-banana-pro | יצירת תמונות עם Gemini 3 Pro Image של Google |
| mobile-responsiveness | בניית אפליקציות רספונסיביות mobile-first |
| mongodb | עבודה עם מסדי נתונים MongoDB בהתאם לשיטות מומלצות |
| nano-banana-poster | יצירת תמונות ופוסטרים עם Google Gemini |
| railway | פריסת אפליקציות על פלטפורמת Railway |
| react-best-practices | הנחיות אופטימיזציית ביצועים ל-React ו-Next.js מצוות Vercel |
| react-native-callstack | אופטימיזציית ביצועים ל-React Native - FPS, TTI, גודל חבילה, דליפות זיכרון |
| r3f-best-practices | שיטות מומלצות ל-React Three Fiber (R3F) ואקוסיסטם Poimandres |
| presentation-architect | הפיכת רעיונות למצגות מובנות ב-Markdown |
| project-init | אתחול מהיר של פרויקטים חדשים |
| quick-commands | קיצורי דרך לפעולות נפוצות ב-Claude Code |
| mermaid-diagrams | יצירת דיאגרמות והדמיות בתחביר Mermaid |
| golang-testing | תבניות בדיקות Go כולל table-driven tests, benchmarks, fuzzing |
| honest-agent | הגדרת סוכני AI כנים, אובייקטיביים ולא סיקופנטיים |
| html-to-pdf | המרת HTML ל-PDF עם תמיכה מצוינת בעברית/RTL |
| golang-patterns | תבניות Go אידיומטיות לבניית יישומים חזקים ויעילים |
| github-trending | הצגת מאגרים ומפתחים פופולריים ב-GitHub |
| github-workflows | תבניות GitHub ל-PRs, סקירת קוד, ענפים וניהול מאגרים |
| local-llm-router | ניתוב שאילתות AI למודלי LLM מקומיים ברשתות מבודדות |
| langchain | בניית אפליקציות LLM עם LangChain ו-LangGraph |
| html-to-pptx | המרת HTML ל-PowerPoint עם תמיכה מצוינת בעברית/RTL |
| iterative-retrieval | תבנית לשכלול הדרגתי של אחזור הקשר |
| react-native-skills | שיטות מומלצות ל-React Native ו-Expo |
| ux-design-systems | בניית מערכות עיצוב עקביות עם טוקנים, רכיבים ועיצוב נושא |
| vercel | פריסה והגדרה של אפליקציות על Vercel |
| writing-plans | כתיבת תוכניות עבודה למשימות מרובות שלבים |
| writing-skills | יצירת מיומנויות חדשות ועריכת מיומנויות קיימות |
| whatsapp | אוטומציית WhatsApp באמצעות Green API |
| web-accessibility | בניית אפליקציות web נגישות לפי הנחיות WCAG |
| web-design-guidelines | סקירת קוד UI לתאימות עם Web Interface Guidelines |
| ui-skills | אילוצים לבניית ממשקים טובים יותר עם סוכנים |
| shabbat-times | גישה ללוח השנה היהודי וזמני שבת דרך Hebcal API |
| sage | SAGE - מנוע צמיחה אוטונומי חכם |
| systematic-debugging | ניפוי באגים שיטתי לפני הצעת תיקונים |
| three-best-practices | שיטות מומלצות ואופטימיזציית ביצועים ל-Three.js |
| skill-sync | סנכרון מיומנויות ממאגר ai-agents-skills ב-GitHub |
| speech-generator | יצירת דיבור מטקסט באמצעות ElevenLabs TTS |
| cloudflare | בנייה ופריסה על פלטפורמת Cloudflare |
| clickhouse-io | תבניות ClickHouse לאופטימיזציית שאילתות ו-data engineering |
| bun | בניית אפליקציות מהירות עם Bun JavaScript runtime |
| calendar | אינטגרציית Google Calendar דרך Apps Script API |
| cc10x-router | נקודת כניסה ראשית ל-CC10X לכל משימות פיתוח |
| Convex Agents | בניית סוכני AI עם רכיב Convex Agent |
| Convex Best Practices | הנחיות לבניית אפליקציות Convex לפרודקשן |
| continuous-learning-v2 | מערכת למידה מבוססת אינסטינקטים |
| code-snippets | ספריית קטעי קוד ותבניות שימושיות |
| composition-patterns | תבניות קומפוזיציה ב-React שמתרחבות |
| continuous-learning | חילוץ אוטומטי של תבניות שימושיות מסשנים |
| aviz-skills-installer | התקנת מיומנויות מספריית AVIZ Skills |
| avoid-feature-creep | מניעת feature creep בבניית תוכנה |
| analytics-metrics | בניית דשבורדים לניתוח נתונים והדמיות |
| agent-browser | אוטומציית דפדפן לבדיקות, מילוי טפסים וצילומי מסך |
| better-auth-best-practices | אינטגרציית Better Auth - פריימוורק אימות מקיף ל-TypeScript |
| better-result-adopt | מיגרציה מ-try/catch לטיפול שגיאות עם better-result |
| baseline-ui | אכיפת בסיס UI למניעת ממשקים גרועים מ-AI |
| aws-account-management | ניהול חשבונות AWS, ארגונים, IAM וחיוב |
| aws-agentcore | בניית סוכני AI עם AWS Bedrock AgentCore |
| aws-strands | בניית סוכני AI עם Strands Agents SDK |
| fal-ai | יצירת תמונות, וידאו ואודיו עם fal.ai serverless AI |
| figma | אינטגרציה עם Figma API לאוטומציית עיצוב |
| env-checker | אימות הגדרות סביבת פיתוח ואבחון בעיות |
| eval-harness | מסגרת הערכה רשמית לסשנים ב-Claude Code |
| gh-pages-deploy | פריסת תוכן סטטי ל-GitHub Pages |
| git-helper | עזרה בתהליכי Git נפוצים |
| github-backup | גיבוי מיומנויות Claude והגדרות ל-GitHub |
| design-motion-principles | ביקורת עיצוב תנועה ואינטראקציה |
| copilot-docs | הגדרת GitHub Copilot עם הוראות מותאמות |
| copilot-sdk | בניית אפליקציות עם GitHub Copilot SDK |
| eigent-integration | AI מרובה סוכנים לזרימות עבודה מקומיות עם פרטיות |
| planning-with-files | תכנון מבוסס Markdown למשימות מורכבות |


## מבנה מיומנות

כל מיומנות בנויה כך:

```
skills/
  skill-name/
    SKILL.md      # הגדרת המיומנות
    *.ps1         # סקריפטים אופציונליים
    references/   # חומרי עזר
```

## יצירת מיומנות חדשה

1. צרו תיקייה ב-`skills/` עם שם המיומנות
2. הוסיפו `SKILL.md` עם:

```yaml
---
name: my-skill
description: מה המיומנות עושה. מופעלת על ידי מילה1, מילה2.
---
```

3. הוסיפו הוראות לסוכן

## תרומה

1. צרו Fork למאגר
2. צרו מיומנות חדשה
3. שלחו Pull Request

## רישיון

MIT - נוצר על ידי יובל אבידני

---

*עדכון אחרון: 2026-04-12*

</div>
