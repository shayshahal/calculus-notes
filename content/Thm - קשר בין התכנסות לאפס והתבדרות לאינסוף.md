# משפט: קשר בין התכנסות לאפס והתבדרות לאינסוף

## ניסוח

תהי $(a_n)_{n=1}^{\infty}$ [[Def - סדרה|סדרה]] של מספרים חיוביים. אז:

$$a_n \to 0 \quad \Longleftrightarrow \quad \frac{1}{a_n} \to \infty$$

## תנאים

הסדרה חייבת להיות של **מספרים חיוביים** ($a_n > 0$ לכל $n$).

## הוכחה

### כיוון 1: אם $a_n \to 0$ אז $\frac{1}{a_n} \to \infty$

נניח $a_n \to 0$ ונראה כי $\frac{1}{a_n} \to \infty$.

יהי $M > 0$. נסמן $\varepsilon = \frac{1}{M}$.

מכיוון ש-$a_n \to 0$, קיים $n_0 \in \mathbb{N}$ כך שלכל $n \geq n_0$:

$$a_n = |a_n - 0| < \varepsilon = \frac{1}{M}$$

ואז לכל $n \geq n_0$ מתקיים:

$$\frac{1}{a_n} > \frac{1}{\varepsilon} = M$$

לכן $\frac{1}{a_n} \to \infty$.

### כיוון 2: אם $\frac{1}{a_n} \to \infty$ אז $a_n \to 0$

נניח $\frac{1}{a_n} \to \infty$ ונראה כי $a_n \to 0$.

יהי $\varepsilon > 0$. נסמן $M = \frac{1}{\varepsilon}$.

מכיוון ש-$\frac{1}{a_n} \to \infty$, קיים $n_0 \in \mathbb{N}$ כך שלכל $n \geq n_0$:

$$\frac{1}{a_n} > M = \frac{1}{\varepsilon}$$

ואז לכל $n \geq n_0$ מתקיים:

$$a_n < \varepsilon$$

ומכיוון ש-$a_n > 0$:

$$|a_n - 0| = a_n < \varepsilon$$

לכן $a_n \to 0$.

## הערה חשובה

> [!warning] התנאי $a_n > 0$ הכרחי
> המשפט **לא בהכרח נכון** אם לא מניחים ש-$(a_n)$ סדרה של מספרים חיוביים.
>
> **דוגמה נגדית:**
> $$a_n = \frac{(-1)^n}{n}$$
> הסדרה שואפת ל-$0$, אבל:
> $$\frac{1}{a_n} = \frac{n}{(-1)^n} = (-1)^n \cdot n$$
> שאין לה גבול במובן הרחב (מתנדנדת בין $\pm\infty$).

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Def - התבדרות לאינסוף]]
**משמש ב:** [[Example - צורות אי-קביעות]], [[Method - חישוב גבולות בעזרת הצבה]]
