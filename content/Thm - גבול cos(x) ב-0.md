# משפט: גבול cos(x) ב-0

## ניסוח

$$\lim_{x \to 0} \cos(x) = 1$$

## הוכחה

ניזכר בזהות: $\cos(2x) = 1 - 2\sin^2(x)$

לכן, לכל $x \neq 0$, $x \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ מתקיים:

$$0 \leq 1 - \cos(x) = 2\sin^2\left(\frac{x}{2}\right) = 2\left|\sin\left(\frac{x}{2}\right)\right|^2$$

לפי [[Lemma - אי-שוויון sin ו-tan]]:

$$\left|\sin\left(\frac{x}{2}\right)\right| < \left|\frac{x}{2}\right|$$

לכן:

$$0 \leq 1 - \cos(x) \leq 2 \cdot \left|\frac{x}{2}\right|^2 = 2 \cdot \frac{x^2}{4} = \frac{x^2}{2} \xrightarrow{x \to 0} 0$$

ועל כן:

$$0 \xleftarrow{x \to 0} 0 \leq 1 - \cos(x) \leq \frac{x^2}{2} \xrightarrow{x \to 0} 0$$

לפי כלל הסנדוויץ' נובע כי:

$$1 - \cos(x) \xrightarrow{x \to 0} 0$$

ומחשבון גבולות:

$$\cos(x) \xrightarrow{x \to 0} 1$$

## הערות

1. אגב ההוכחה קיבלנו גם: $1 - \cos(x) \leq \frac{x^2}{2}$
2. ניתן להשתמש בתוצאה זו להוכחת גבולות טריגונומטריים נוספים

## תלויות

**דורש:** [[Tool - זהויות טריגונומטריות]], [[Lemma - אי-שוויון sin ו-tan]], [[Thm - כלל הסנדוויץ' לפונקציות]]
**משמש ב:** [[Thm - גבול sin(x) חלקי x]], [[Tool - גבולות ידועים של פונקציות]]
