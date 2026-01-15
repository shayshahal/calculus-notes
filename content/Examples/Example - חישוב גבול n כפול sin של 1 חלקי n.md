# דוגמה: חישוב גבול $n \cdot \sin\left(\frac{1}{n}\right)$

## הבעיה

חשב את גבול הסדרה:
$$\lim_{n \to \infty} n \cdot \sin\left(\frac{1}{n}\right)$$

## הפתרון

### שלב 1: שינוי צורה
נשים לב כי:
$$n \cdot \sin\left(\frac{1}{n}\right) = \frac{\sin\left(\frac{1}{n}\right)}{\frac{1}{n}}$$

### שלב 2: הגדרת פונקציה
נסמן $f(x) = \frac{\sin(x)}{x}$.

ראינו כי מתקיים הגבול הידוע:
$$\frac{\sin(x)}{x} \xrightarrow{x \to 0} 1$$

### שלב 3: שימוש בהגדרת היינה
הסדרה $\frac{1}{n}$ שואפת ל-$0$, ואיבריה שונים מ-$0$.

לכן לפי [[Def - גבול של פונקציה|הגדרת הגבול של היינה]] מתקיים:
$$f\left(\frac{1}{n}\right) = \frac{\sin\left(\frac{1}{n}\right)}{\frac{1}{n}} \xrightarrow{n \to \infty} 1$$

## התשובה

$$\lim_{n \to \infty} n \cdot \sin\left(\frac{1}{n}\right) = 1$$

## הערה

זוהי דוגמה קלאסית לשימוש בהגדרת היינה לגבול פונקציה: אם יש לנו סדרה $x_n \to a$ וידוע ש-$\lim_{x \to a} f(x) = L$, אז $f(x_n) \to L$.

## תלויות

**דורש:** [[Def - גבול של פונקציה]], [[Tool - גבול sin(x) חלקי x]]
**משמש ב:** [[Method - חישוב גבולות באמצעות היינה]]
