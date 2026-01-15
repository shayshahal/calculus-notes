# למה: גבול נמצא בסביבה

## ניסוח

תהי $(a_n)_{n=1}^{\infty}$ סדרה. נניח כי $a_n \xrightarrow{n \to \infty} L$.

יהיו $\alpha, \beta \in \mathbb{R}$ עבורם $\alpha < L < \beta$.

אז:

$$\exists (N_0 \in \mathbb{N}) \forall (n \geq N_0) [\alpha < a_n < \beta]$$

## הסבר

אם סדרה מתכנסת לגבול $L$, אז החל ממקום מסוים כל איברי הסדרה נמצאים בתוך כל סביבה פתוחה של $L$.

בפרט, אם $L$ נמצא בתוך הקטע הפתוח $(\alpha, \beta)$, אז גם איברי הסדרה נמצאים בקטע הזה החל ממקום מסוים.

## הוכחה

ניקח $\varepsilon > 0$ מספיק קטן שעבורו:

$$\alpha < L - \varepsilon < L + \varepsilon < \beta$$

במפורש, צריך לבחור $\varepsilon < \min\{L - \alpha, \beta - L\}$.

נשתמש בהגדרת הגבול עבור $\varepsilon$ זה:

$$\exists (N_0 \in \mathbb{N}) \forall (n \geq N_0) [L - \varepsilon < a_n < L + \varepsilon]$$

ואז לכל $n \geq N_0$:

$$\alpha < L - \varepsilon < a_n < L + \varepsilon < \beta$$

$\blacksquare$

## שימושים

למה זו שימושית להוכחת משפטים על שימור אי-שוויונות בגבולות. במקום להוכיח ישירות, מראים שההנחה ההפוכה מובילה לסתירה באמצעות למה זו.

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Def - סדרה מתכנסת]]
**משמש ב:** [[Thm - משפט הסנדוויץ']], [[Thm - אריתמטיקת גבולות]]
