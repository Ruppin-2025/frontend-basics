## מדריך מקוצר ל-Flexbox ב-CSS

### מה זה Flexbox?

<p dir="rtl">
Flexbox (Flexible Box Layout) הוא מודל פריסה מתקדם ב-CSS המאפשר</strong> חלוקה דינמית של מרחב<strong> בין אלמנטים בתוך מיכל גמיש.</p>

### ההבדלים בין Flex Container לעומת Flex Item

<ul dir="rtl">
  <li><strong>Flex Container</strong> – אלמנט הורה שמוגדר עם `display: flex`, קובע את סידור הפריטים הפנימיים.</li>
  <li><strong>Flex Item</strong> – אלמנטים בתוך ה-Flex Container שהעיצוב שלהם מושפע מהגדרות המיכל.</li>
</ul>

### תכונות עיקריות של Flex Container

```css
.container {
  display: flex;
  flex-direction: row; /* ברירת מחדל: אופקי */
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
```

### תכונות עיקריות של Flex Items

```css
.item {
  flex-grow: 1; /* מאפשר לאלמנט לגדול */
  flex-shrink: 2; /* קובע כמה האלמנט יתכווץ */
  flex-basis: 200px; /* קובע רוחב התחלתי */
  align-self: center; /* יישור עצמאי בתוך הקונטיינר */
}
```

<p dir="rtl">
Flexbox מאפשר יצירת <strong>פריסות רספונסיביות וגמישות</strong> בקלות, תוך התאמה לתוכן ולמסכים שונים.
</p>
