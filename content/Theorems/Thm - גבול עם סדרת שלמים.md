# משפט: גבול עם סדרת שלמים

## ניסוח

תהי $(m_n)$ סדרה של מספרים **שלמים** כך ש-$m_n \to \infty$. אז:

$$\lim_{n \to \infty} \left(1 + \frac{1}{m_n}\right)^{m_n} = e$$

## הכללה

**משפט:** תהי $(a_n)$ סדרה כך ש-$a_n \to \infty$. אז:

$$\lim_{n \to \infty} \left(1 + \frac{1}{a_n}\right)^{a_n} = e$$

## הוכחה (עבור סדרת שלמים)

נסמן $b_n = \left(1 + \frac{1}{m_n}\right)^{m_n}$.

יהי $\varepsilon > 0$. מכיוון ש-$\left(1 + \frac{1}{k}\right)^k \to e$, קיים $K \in \mathbb{N}$ כך שלכל $k \geq K$:
$$\left|\left(1 + \frac{1}{k}\right)^k - e\right| < \varepsilon$$

מכיוון ש-$m_n \to \infty$, קיים $N \in \mathbb{N}$ כך שלכל $n \geq N$ מתקיים $m_n \geq K$.

לכן לכל $n \geq N$:
$$|b_n - e| = \left|\left(1 + \frac{1}{m_n}\right)^{m_n} - e\right| < \varepsilon$$

כנדרש.

## הערה

נשאר נכון גם כאשר $(m_n)$ אינה סדרה של מספרים שלמים, כל עוד $m_n \to \infty$ (תרגיל בית).

## יישום: חישוב גבולות

חשבו את גבול הסדרה $\left(1 + \frac{2}{n}\right)^n$.

**פתרון:**

$$\lim_{n \to \infty} \left(1 + \frac{2}{n}\right)^n = \lim_{n \to \infty} \left[\left(1 + \frac{2}{n}\right)^{\frac{n}{2}}\right]^2 = \left[\lim_{n \to \infty} \left(1 + \frac{1}{\frac{n}{2}}\right)^{\frac{n}{2}}\right]^2 = e^2$$

## תלויות

**דורש:** [[Def - הקבוע e]], [[Def - גבול של סדרה]]
**משמש ב:** [[Tool - גבולות בסיסיים של סדרות]], [[Method - חישוב גבולות פונקציות]]
