# תוכנית ההדרכה – Tizon Health

אתר סטטי של תוכנית ההדרכה לשותפים המייסדים: תפריט ראשי ומפגשים לפי הסדר.

## מבנה
```
index.html              תפריט ראשי
meetings/meeting-1.html מפגש ראשון – מפגש השותפים המייסדים (19.10.2026)
meetings/meeting-2.html מפגש שני – הדרכת שותפים (26.10.2026)
assets/                 לוגו עם רקע שקוף (גרסה לרקע בהיר ולרקע כהה)
netlify.toml            פריסה ל-Netlify ללא שלב בנייה
```

## הוספת מפגש חדש
1. שמרו את הקובץ בשם `meetings/meeting-N.html`.
2. בקובץ `index.html` הפכו את שורת המפגש מ-`<div class="m soon">` ל-`<a class="m" href="meetings/meeting-N.html">`, והחליפו את `בהכנה` ב-`לפתיחה`.

## פריסה
Netlify ← Add new site ← Import from Git ← בחירת הריפו. אין פקודת בנייה; תיקיית הפרסום היא השורש.
