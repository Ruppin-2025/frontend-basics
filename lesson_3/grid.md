# הנחיות על Grid Layout ב-CSS

ב-CSS, `Grid Layout` הוא מודל מיקום שמאפשר למעצבים למקם אלמנטים בתוך מערכת טבלה גמישה. השיטה מאפשרת שליטה מלאה על המיקומים של רכיבים בתוך גריד בעמודה ושורה, ומספקת גמישות רבה בתכנון פריסות עמודים.

## יצירת Grid Layout

כדי ליצור גריד, יש להחיל את תכונת ה- `display` עם ערך `grid` על אלמנט ההורה (container):

```css
.container {
  display: grid;
}
```

### הגדרת שורות ועמודות

לאחר שמוגדר ה- `display: grid`, אפשר להגדיר את השורות והעמודות עם `grid-template-rows` ו- `grid-template-columns`.

#### דוגמה:

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* 3 עמודות */
  grid-template-rows: 100px auto 200px; /* 3 שורות */
}
```

במקרה זה:

- יש 3 עמודות, עם יחסים של 1:2:1 בין רוחבן.
- יש 3 שורות, שורה אחת בגובה קבוע של 100px, השנייה בגובה אוטומטי, והשלישית בגובה קבוע של 200px.

## מיקום פריטים בתוך הגריד

כאשר המיכלים (items) בתוכה, כל אלמנט יכול להתמקם בתוך הגריד לפי אינדקסים של שורות ועמודות.

### הגדרת מיקום של רכיב

- `grid-column`: מגדיר את המיקום של רכיב בעמודה.
- `grid-row`: מגדיר את המיקום של רכיב בשורה.

#### דוגמה:

```css
.item1 {
  grid-column: 1 / 3; /* מתחיל בעמודה 1 ומסתיים בעמודה 3 */
  grid-row: 1 / 2; /* מתחיל בשורה 1 ומסתיים בשורה 2 */
}
```

## תכונות נוספות

### מרווחים בין רכיבים

- `gap`: קובע את המרווח בין שורות ועמודות בתוך הגריד.
- `row-gap`: קובע את המרווח בין השורות.
- `column-gap`: קובע את המרווח בין העמודות.

#### דוגמה:

```css
.container {
  display: grid;
  gap: 20px; /* רווח של 20px בין כל רכיב */
}
```

### `auto-fill` ו- `auto-fit`

- `auto-fill`: משלים את השורות והעמודות בכמה שיותר תאים, כך שהרכיבים יתאימו לגודל.
- `auto-fit`: כמו `auto-fill`, אבל הוא משאיר את התא ריק אם אין מקום להכניס אליו רכיב.

#### דוגמה:

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
}
```

במקרה זה, העמודות יתמלאו אוטומטית עם רכיבים בגודל מינימלי של 100px ויתפשטו לכדי גודל גמיש.

## דוגמה מלאה

```css
.container {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  grid-template-rows: 100px auto 100px;
  gap: 10px;
}

.header {
  grid-column: 1 / 4;
  grid-row: 1;
}

.sidebar {
  grid-column: 1;
  grid-row: 2;
}

.main {
  grid-column: 2;
  grid-row: 2;
}

.footer {
  grid-column: 1 / 4;
  grid-row: 3;
}
```

במקרה זה:

- ישנן 3 עמודות ושורות, עם אלמנטים הממוקמים לפי הגדרות שורה ועמודה.
- ה- `.header` וה- `.footer` תופסים את כל העמודות.

## סיכום

- `Grid Layout` מאפשר יצירת פריסות דינמיות וגמישות.
- באמצעות תכונות כמו `grid-template-columns`, `grid-template-rows` ו- `gap`, ניתן לשלוט באופן מדויק על העיצוב של עמודים.
- מיקום רכיבים בתוך הגריד מתבצע באמצעות `grid-column` ו- `grid-row`.

למידע נוסף, ניתן לעיין בתיעוד הרשמי של [MDN CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout).
