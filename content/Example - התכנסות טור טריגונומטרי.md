# דוגמה: התכנסות טור טריגונומטרי

## הבעיה

תהי $a_n \to 0$ מונוטונית ויהי $x \in (0, \pi)$. הוכיחו כי הטור $\sum a_n \sin(nx)$ מתכנס.

## פתרון

נרצה להשתמש ב[[Thm - מבחן דיריכלה]]. לשם כך צריך להראות שסדרת הסכומים החלקיים:

$$B_N(x) := \sum_{n=1}^{N} \sin(nx)$$

חסומה.

**שלב 1: שימוש בזהות טריגונומטרית**

נכפיל ב-$\sin\left(\frac{x}{2}\right)$ ונשתמש בזהות:

$$\sin(\alpha)\sin(\beta) = \frac{1}{2}[\cos(\alpha - \beta) - \cos(\alpha + \beta)]$$

$$B_N(x) \sin\left(\frac{x}{2}\right) = \sum_{n=1}^{N} \sin(nx) \sin\left(\frac{x}{2}\right)$$

$$= \frac{1}{2} \sum_{n=1}^{N} \left[ \cos\left(nx - \frac{x}{2}\right) - \cos\left(nx + \frac{x}{2}\right) \right]$$

$$= \frac{1}{2} \sum_{n=1}^{N} \left[ \cos\left(\frac{2n-1}{2}x\right) - \cos\left(\frac{2n+1}{2}x\right) \right]$$

**שלב 2: טור טלסקופי**

זהו [[Def - טור טלסקופי|טור טלסקופי]]:

$$= \frac{1}{2} \left[ \cos\left(\frac{x}{2}\right) - \cos\left(\frac{2N+1}{2}x\right) \right]$$

**שלב 3: חסימת $B_N(x)$**

$$|B_N(x)| = \frac{\left| \cos\left(\frac{x}{2}\right) - \cos\left(\frac{2N+1}{2}x\right) \right|}{2\sin\left(\frac{x}{2}\right)}$$

משימוש בזהות $\cos\alpha - \cos\beta = -2\sin\left(\frac{\alpha+\beta}{2}\right)\sin\left(\frac{\alpha-\beta}{2}\right)$:

$$= \frac{\left| \sin\left(\frac{N+1}{2}x\right) \sin\left(\frac{N}{2}x\right) \right|}{\sin\left(\frac{x}{2}\right)} \leq \frac{1}{\sin\left(\frac{x}{2}\right)}$$

**שלב 4: סיום**

מכיוון ש-$x \in (0, \pi)$, מתקיים $\sin\left(\frac{x}{2}\right) > 0$ ולכן $B_N(x)$ אכן חסום.

לפי [[Thm - מבחן דיריכלה]], הטור $\sum a_n \sin(nx)$ מתכנס.

## הערות

1. התוצאה נכונה גם עבור $\sum a_n \cos(nx)$ (בהוכחה דומה)
2. עבור $x = 0$ או $x = \pi$ הטור מתנהג אחרת
3. לא ניתן לומר משהו כללי על התכנסות בהחלט - זה תלוי בסדרה $a_n$

## תלויות

**דורש:** [[Thm - מבחן דיריכלה]], [[Def - טור טלסקופי]], [[Tool - זהויות טריגונומטריות]]
**משמש ב:** טורי פורייה, אנליזה הרמונית
