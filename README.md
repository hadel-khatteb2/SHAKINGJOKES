# 📳 נער אותי! (Shake Me)

אתר סטטי שרץ בפלאפון, קורא את **מד התאוצה** (Accelerometer) ומזהה ניעור.
בכל ניעור הוא מביא תוכן אקראי מ־API חינמי:

| מצב | API | כתובת |
|---|---|---|
| 😂 בדיחה | JokeAPI | `https://v2.jokeapi.dev/joke/Any?safe-mode` |
| 🍝 מתכון | TheMealDB | `https://www.themealdb.com/api/json/v1/1/random.php` |
| 💡 עצה | Advice Slip | `https://api.adviceslip.com/advice` |

אף אחד מה־API לא דורש מפתח (API key).

## חיישנים ו־API של הדפדפן שבשימוש
- `devicemotion` (קריאת `accelerationIncludingGravity` בצירים X/Y/Z). זיהוי ניעור לפי השינוי בתאוצה בין שתי קריאות.
- `DeviceMotionEvent.requestPermission()`: בקשת הרשאה לחיישן, נדרשת באייפון.
- `navigator.vibrate()`: רטט בכל ניעור (אנדרואיד בלבד).
- `fetch()`: קריאה ל־API החיצוניים.

## העלאה ל־GitHub Pages
1. יוצרים repository חדש ב־GitHub (למשל `shake-me`), ציבורי.
2. מעלים את `index.html` (ואת הקובץ הזה): **Add file → Upload files → Commit**.
3. נכנסים ל־**Settings → Pages**.
4. ב־**Source** בוחרים `Deploy from a branch`, ב־Branch בוחרים `main` ו־`/ (root)`, ולוחצים **Save**.
5. אחרי דקה־שתיים האתר זמין בכתובת:
   `https://<שם-המשתמש>.github.io/shake-me/`

> חשוב: חיישני התנועה עובדים רק ב־**HTTPS**, ו־GitHub Pages מספק את זה אוטומטית.

## "הורדה" לפלאפון
פותחים את הכתובת בפלאפון, ואז:
- **אנדרואיד (Chrome):** תפריט ⋮ → **הוסף למסך הבית**
- **אייפון (Safari):** כפתור שיתוף → **הוסף למסך הבית**

## שימוש
1. לוחצים **התחל** (באייפון מאשרים גישה לחיישן).
2. בוחרים בדיחה / מתכון / עצה.
3. מנערים את הפלאפון! 📳
4. אם הניעור לא נקלט, או נקלט בקלות מדי, מזיזים את סליידר **הרגישות**.
