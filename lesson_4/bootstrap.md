# 📌 היכרות עם Bootstrap

## **1️⃣ מה זה Bootstrap?**
הגדרה: **Bootstrap** הוא Framework מבוסס CSS ו-JavaScript, המאפשר עיצוב מהיר, רספונסיבי ונוח של אתרים. 

- ✅ מאפשר **פיתוח מהיר** עם מחלקות מוכנות מראש.
- ✅ **רספונסיבי** – מתאים את העיצוב לכל המסכים.
- ✅ כולל **Grid System, כפתורים, טפסים, כרטיסים ועוד.**
- ✅ נתמך ע"י כל הדפדפנים המודרניים.

---
📌 יש למקם לינקים לקבצי **CSS** ו-**JS** ב-`<head>`:
```html
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">

<!-- Bootstrap JavaScript Bundle -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```
📌 יש להוסיף **Meta Tags** מתאימים כדי להבטיח רספונסיביות מלאה:
```html
<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>דף Bootstrap</title>
</head>
<body>
  ...
</body>
</html>
```
---

## **3️⃣ חלוקת ה12-עמודות - The 12-Column Grid System**
**מערכת ה-Grid** של Bootstrap מבוססת על **12 עמודות גמישות**, המאפשרות יצירת פריסות דינמיות.

📌 דוגמה בסיסית:
```html
<div class="container">
  <div class="row">
    <div class="col-4">תוכן 1</div>
    <div class="col-4">תוכן 2</div>
    <div class="col-4">תוכן 3</div>
  </div>
</div>
```
🔹 כל `col-4` תופס **4 מתוך 12 עמודות** → יחד הן משלימות **12 עמודות**.

---

## **4️⃣ חלוקת גדלים - Grid Classes Sizes**
📌 מאפשר שליטה בגודל העמודות בהתאמה למסכים שונים:

| **מחלקה**    | **X-Small** | **Small** | **Medium** | **Large** | **X-Large** | **XX-Large** |
|--------------|-------------|-----------|------------|-----------|-------------|--------------|
| `col-`       | תמיד 12     | 576px+    | 768px+     | 992px+    | 1200px+     | 1400px+      |
| `col-sm-`    | 100%        | מחלק את הרוחב | מחלק את הרוחב | מחלק את הרוחב | מחלק את הרוחב | מחלק את הרוחב |
| `col-md-`    |             | 100%      | מחלק את הרוחב | מחלק את הרוחב | מחלק את הרוחב | מחלק את הרוחב |
| `col-lg-`    |             |           | 100%       | מחלק את הרוחב | מחלק את הרוחב | מחלק את הרוחב |
| `col-xl-`    |             |           |            | 100%      | מחלק את הרוחב | מחלק את הרוחב |
| `col-xxl-`   |             |           |            |           | 100%         | מחלק את הרוחב |

📌 **דוגמה: פריסה משתנה בהתאם למסך**
```html
<div class="row">
  <div class="col-md-6 col-lg-4">תוכן 1</div>
  <div class="col-md-6 col-lg-4">תוכן 2</div>
  <div class="col-md-12 col-lg-4">תוכן 3</div>
</div>
```
🔹 בטאבלט **(md)** – שתי עמודות, ובמסכים גדולים **(lg)** – שלוש עמודות.

---

## **5️⃣ חלוקה בהתאמה אישית - Define Grid Division**
ניתן להגדיר **רוחב עמודה בהתאמה אישית**, בלי לספור עמודות:
```html
<div class="row">
  <div class="col">תוכן 1</div>
  <div class="col">תוכן 2</div>
  <div class="col">תוכן 3</div>
</div>
```
🔹 כל עמודה תקבל **רוחב שווה** באופן אוטומטי.

---

## **6️⃣ נושא Implicit Division Values**
כאשר אין ציון מפורש של עמודות, Bootstrap מחלק את הרוחב **באופן שווה** בין כל האלמנטים בתוך `row`.

📌 **דוגמה:**
```html
<div class="row">
  <div class="col">פריט 1</div>
  <div class="col">פריט 2</div>
  <div class="col">פריט 3</div>
</div>
```
🔹 כל פריט יקבל **שליש מהרוחב**.

---

## **7️⃣ הסתרת אלמנטים בדף**
ניתן להסתיר אלמנטים **לפי גודל מסך**:

📌 **דוגמה:**
```html
<p class="d-none d-md-block">טקסט זה יופיע רק במסכים בגודל בינוני ומעלה.</p>
```
- למשל, `d-none` מסתיר את האלמנט תמיד.
- למשל, `d-md-block` מציג את האלמנט רק כאשר המסך בינוני ומעלה (768px+).

---

## **8️⃣ אלמנטים נוספים מומלצים ב-Bootstrap**
📌 **כפתורים מעוצבים:**
```html
<button class="btn btn-primary">כפתור ראשי</button>
<button class="btn btn-outline-danger">כפתור מסגרת</button>
```

📌 **טפסים מעוצבים:**
```html
<form>
  <input type="text" class="form-control" placeholder="הכנס טקסט">
  <button type="submit" class="btn btn-success mt-2">שלח</button>
</form>
```

📌 **כרטיסים (Cards) להצגת תוכן:**
```html
<div class="card" style="width: 18rem;">
  <img src="image.jpg" class="card-img-top" alt="תמונה">
  <div class="card-body">
    <h5 class="card-title">כותרת</h5>
    <p class="card-text">תיאור קצר של התוכן.</p>
  </div>
</div>
```

📌 **סרגל ניווט (Navbar) רספונסיבי:**
```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">לוגו</a>
  <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
    ☰
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item"><a class="nav-link" href="#">בית</a></li>
      <li class="nav-item"><a class="nav-link" href="#">אודות</a></li>
    </ul>
  </div>
</nav>
```

---
