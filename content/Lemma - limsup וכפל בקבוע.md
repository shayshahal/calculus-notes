# למה: limsup וכפל בקבוע

## ניסוח

תהי $(a_n)_{n=1}^{\infty}$ סדרה, ויהי $c \geq 0$. אז:

$$\limsup_{n \to \infty}(c \cdot a_n) = c \cdot \limsup_{n \to \infty}(a_n)$$

## הוכחה

עבור $c = 0$ זה מיידי (שני האגפים שווים $0$).

נניח $c > 0$.

$\limsup a_n$ זה גבול חלקי של $a_n$, ולכן יש תת-סדרה $(a_{n_k})_{k=1}^{\infty}$ השואפת אליו.

מחשבון גבולות:
$$c \cdot a_{n_k} \xrightarrow{k \to \infty} c \cdot \limsup(a_n)$$

הסדרה $c \cdot a_{n_k}$ היא תת-סדרה של $c \cdot a_n$, ולכן קיבלנו כי $c \cdot \limsup(a_n)$ הוא גבול חלקי של $c \cdot a_n$.

מכאן:
$$c \cdot \limsup(a_n) \leq \limsup(c \cdot a_n)$$

להפך, מתקיים:
$$\limsup(c \cdot a_n) = c \cdot \left[\frac{1}{c} \cdot \limsup(c \cdot a_n)\right] \leq c \cdot \limsup\left(\frac{1}{c} \cdot c \cdot a_n\right) = c \cdot \limsup(a_n)$$

כאשר האי-שוויון נובע מהחלק הראשון של ההוכחה (עם $\frac{1}{c}$ במקום $c$).

מכאן:
$$c \cdot \limsup(a_n) \leq \limsup(c \cdot a_n) \leq c \cdot \limsup(a_n)$$

ולכן:
$$\limsup(c \cdot a_n) = c \cdot \limsup(a_n)$$

## הערות

- הלמה משמשת בהוכחת נוסחת קושי-הדמר לרדיוס התכנסות
- שימו לב שהדרישה $c \geq 0$ חיונית - עבור $c < 0$ הכפל הופך limsup ל-liminf

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול חלקי]], [[Def - תת-סדרה]], [[Thm - אריתמטיקת גבולות]]
**משמש ב:** [[Thm - משפט קושי-הדמר]], [[Def - רדיוס התכנסות]]
