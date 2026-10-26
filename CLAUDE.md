# תוכנית ההדרכה – Tizon Health

אתר סטטי (HTML בלבד, בלי שלב בנייה) של תוכנית ההדרכה ל"שותפים המייסדים" של Tizon Health.
הבעלים: ד״ר צחי זילבר, Ph.D (המייסד). כל התוכן בעברית, RTL. סיכומים ודוחות אליו – תמיד בעברית.

## מבנה
- `index.html` – תפריט ראשי. כל מפגש הוא שורה ברשימה `<ol class="menu">`.
  מפגש מוכן: `<a class="m" href="meetings/meeting-N.html">` עם `<span class="go">לפתיחה</span>`.
  מפגש עתידי: `<div class="m soon">` עם `<span class="pill">בהכנה</span>`.
- `meetings/meeting-N.html` – סדר יום של כל מפגש. בראש כל אחד קישור "→ חזרה לתפריט".
- `assets/logo-light.png`, `assets/logo-dark.png` – לוגו עם רקע שקוף. גרסת dark מבהירה את הכיתוב
  "The Architecture of Vitality" כדי שיהיה קריא על רקע כהה. בעמודים עצמם הלוגו מוטמע כ-data URI
  בשתי תמונות (`.lg-dark`, `.lg-light`) שמתחלפות לפי ערכת הצבעים.
- `netlify.toml` – publish = "." (אין build).

## עיצוב (לשמור עקביות בכל מפגש חדש)
- רקע כהה כברירת מחדל (#0f1712), זהב (#c9a46a) וירוק (#7cb342), עם ערכה בהירה דרך prefers-color-scheme / data-theme.
- גופנים: Frank Ruhl Libre לכותרות, Assistant לטקסט.
- לכותרת: תאריך לועזי + עברי (pyluach: `dates.GregorianDate(y,m,d).to_heb().hebrew_date_string()`).
- זמני כל סעיף מוצגים בקטן ובעמעום (`.dur`) – לעיניו של צחי, לא בולטים לשותפים.

## המפגשים
1. 19.10.2026 (ח׳ בחשוון תשפ״ז) – מפגש השותפים המייסדים: חזון, סיפור Tizon, שבעת המוצרים, מסלול המטפל, צוות ותמיכה.
2. 26.10.2026 20:00 (ט״ו בחשוון) – הדרכת שותפים: חזרה על החזון, חלוקה לצוותים (שמות חסרים עדיין), ארבעת שלבי השותף, הדרכת CRM.
3. 29.10.2026 10:00 (י״ח בחשוון) – הדרכה. בהכנה.
4. 9.11.2026 (כ״ט בחשוון) – מפגש שותפים מלא, הצגת המודל העסקי. בהכנה.
הדרכות קבועות: ימי שני 20:00, ימי חמישי 10:00.

## פריסה
פרויקט Netlify בשם `tizon-training` (צוות zilberz) נוצר: https://tizon-training.netlify.app
עדיין לא מחובר לריפו – יש לחבר אותו ב-Netlify (Link repository → GitHub → zilberz-hue/tizon-training, branch main, ללא פקודת build).
