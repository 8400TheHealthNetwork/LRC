<div id="intro" dir="rtl" markdown="1">

## קהילה - Server

### Patient Resource
בתחילת התהליך ביה"ח מתשאל את הקהילה לקבלת ה-Patient Resource , ובכך הוא גם מקבל את המידע הדרוש ובמקביל מוודא שהמטופל אכן מבוטח באותה הקופה.
מנקודה זו והלאה, ניתן לשייך משאבים למטופל (reference) באופן רלטיבי באמצעות המזהה הלוגי שלו (לדוגמה: Patient/123456).

<span style="font-size:1.2em;"><u> SearchParameters </u></span> 
<br>
לצורך מימוש של פעולת החיפוש אחר ה- Patient, על ה- server לתמוך באפשרות לביצוע חיפוש לפי:

- **identifier** (חובה) – המזהה העסקי של המטופל.

על פי המזהה העסקי, אשר זהה וידוע לשני הארגונים, יבוצעו חיפוש ושליפה של המשאב.

יש לתמוך בשליפה של רשימת מטופלים במסגרת חיפוש אחד.

- **summary\_** (מומלץ) – שליפת תמצית המשאב.
  במידה ולביה"ח אין צורך בכל הפרטים המלאים של המטופל, התישאול יוגדר עם מאפיין summary\_ אשר מורה לשרת להחזיר את הפרטים המצומצמים הכוללים בתוכם את המזהה הלוגי של כל מטופל וכן שדות חובה בלבד.
  לפרטים [לחצו כאן](https://hl7.org/fhir/R4/search.html#summary)


### ServiceRequest Resource 

<span style="font-size:1.2em;"><u> Interactions </u></span>

לצורך מימוש אינטראקציית היצירה של ServiceRequest בקהילה, על הקהילה לתמוך בפעולה הבאה:
-	**POST ServiceRequest** – שמירת פרטי ההפניה באמצעות יצירת משאב ServiceRequest.
יצירת המשאב באופן הזה מתבצעת הן עבור הפניה אטומית/סוללה והן עבור הפניה מאגדת.

</div>