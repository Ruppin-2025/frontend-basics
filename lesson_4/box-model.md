# 📌 היכרות עם Box-Model

## 1️⃣ מהו ה-Box Model ב-CSS?

מודל ה-Box ב-CSS מגדיר כיצד אלמנטים מוצגים בדף:

- טבעת 1 - **Content** – התוכן של האלמנט (טקסט, תמונות וכו').
- טבעת 2 - **Padding** – הריפוד הפנימי בין התוכן למסגרת
- טבעת 3 - **Border** –  המסגרת המקיפה את האלמנט.
- טבעת 4 - **Margin** – מרווח חיצוני בין האלמנט לסביבתו.
  
### 📌 דוגמה לקוד:

```css
.box {
  width: 200px;
  height: 100px;
  padding: 10px;
  border: 5px solid black;
  margin: 20px;
  box-sizing: border-box; /* שומר על הגודל הכולל */
}
```

### לסיכום

🔹התכונה `box-sizing: border-box;` מבטיח שהרוחב והגובה יכללו גם את ה-padding וה-border ולא יגדילו את האלמנט מעבר למה שהוגדר.
