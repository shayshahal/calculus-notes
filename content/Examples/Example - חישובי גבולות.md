# דוגמה: חישובי גבולות

## תרגיל 1: פונקציה רציונלית

חשבו: $\lim_{n \to \infty} \frac{n^7 - n^5 + 4}{3n^7 - 20n + 2}$

**פתרון:** נחלק מונה ומכנה ב-$n^7$ (החזקה הגבוהה ביותר):

$$\lim_{n \to \infty} \frac{n^7 - n^5 + 4}{3n^7 - 20n + 2} = \lim_{n \to \infty} \frac{1 - \frac{1}{n^2} + \frac{4}{n^7}}{3 - \frac{20}{n^6} + \frac{2}{n^7}} = \frac{1 - 0 + 0}{3 - 0 + 0} = \frac{1}{3}$$

## תרגיל 2: סדרה אפסית כפול חסומה

חשבו: $\lim_{n \to \infty} \frac{2^n \sin(\pi\sqrt{n})}{3^n}$

**פתרון:**

$$\frac{2^n \sin(\pi\sqrt{n})}{3^n} = \underbrace{\left(\frac{2}{3}\right)^n}_{\to 0 \text{ (גבול בסיסי)}} \cdot \underbrace{\sin(\pi\sqrt{n})}_{\text{חסומה}}$$

לפי [[Thm - מכפלת סדרה אפסית בחסומה|משפט מכפלת סדרה אפסית בחסומה]], הגבול הוא $0$.

## תרגיל 3: שורשים וחזקות

חשבו: $\lim_{n \to \infty} \sqrt[n]{4^{2n+3}n^5}$

**פתרון:**

$$\sqrt[n]{4^{2n+3}n^5} = 4^{\frac{2n+3}{n}} \cdot n^{\frac{5}{n}} = 4^2 \cdot (\sqrt[n]{4})^3 \cdot (\sqrt[n]{n})^5$$

לפי [[Tool - גבולות בסיסיים של סדרות|גבולות בסיסיים]]:
- $\sqrt[n]{4} \to 1$
- $\sqrt[n]{n} \to 1$

לכן:
$$\sqrt[n]{4^{2n+3}n^5} \to 4^2 \cdot 1^3 \cdot 1^5 = 16$$

## תרגיל 4: הפרש שורשים (כפל בצמוד)

חשבו: $\lim_{n \to \infty} \sqrt{n^2 + 5n + 2} - \sqrt{n^2 + n + 1}$

**פתרון:** נכפיל ונחלק בצמוד:

$$\sqrt{n^2 + 5n + 2} - \sqrt{n^2 + n + 1} = \frac{(n^2 + 5n + 2) - (n^2 + n + 1)}{\sqrt{n^2 + 5n + 2} + \sqrt{n^2 + n + 1}}$$
$$= \frac{4n + 1}{\sqrt{n^2 + 5n + 2} + \sqrt{n^2 + n + 1}}$$

נחלק מונה ומכנה ב-$n$:

$$= \frac{4 + \frac{1}{n}}{\sqrt{1 + \frac{5}{n} + \frac{2}{n^2}} + \sqrt{1 + \frac{1}{n} + \frac{1}{n^2}}} \to \frac{4}{1 + 1} = 2$$

## תרגיל 5: סדרה עם ריצפה

חשבו: $\lim_{n \to \infty} \sqrt{\left\lfloor 1 - \frac{1}{n} \right\rfloor}$

**פתרון:**

> [!warning] זהירות!
> **לא ניתן** "להחליף" גבול עם פונקציות באופן אוטומטי!

גישה "נאיבית" (שגויה):
$$\lim_{n \to \infty} \sqrt{\left\lfloor 1 - \frac{1}{n} \right\rfloor} = \sqrt{\lfloor 1 \rfloor} = 1$$

**הפתרון הנכון:** נבחן את איברי הסדרה.

לכל $n \in \mathbb{N}$ מתקיים $1 - \frac{1}{n} < 1$, ולכן:
$$\left\lfloor 1 - \frac{1}{n} \right\rfloor = 0$$

כלומר זו הסדרה הקבועה $0$, ולכן:
$$\lim_{n \to \infty} \sqrt{\left\lfloor 1 - \frac{1}{n} \right\rfloor} = \lim_{n \to \infty} 0 = 0$$

## תלויות

**דורש:** [[Thm - אריתמטיקת גבולות]], [[Tool - גבולות בסיסיים של סדרות]], [[Thm - מכפלת סדרה אפסית בחסומה]]
**משמש ב:** [[Method - הוכחת גבול מההגדרה]]
