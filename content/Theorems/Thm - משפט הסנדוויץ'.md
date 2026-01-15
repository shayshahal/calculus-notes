# משפט: משפט הסנדוויץ'

## ניסוח

תהיינה $(a_n)$, $(b_n)$, $(c_n)$ סדרות כך שהחל ממקום מסוים:

$$a_n \leq b_n \leq c_n$$

ובנוסף:

$$\lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L \in \mathbb{R}$$

אז גם $(b_n)$ מתכנסת ומתקיים:

$$\lim_{n \to \infty} b_n = L$$

## תנאים

1. קיים $N_0$ כך שלכל $n \geq N_0$: $a_n \leq b_n \leq c_n$
2. שתי הסדרות "החיצוניות" מתכנסות לאותו גבול $L$

## הוכחה

יהי $\varepsilon > 0$. מכיוון ש-$a_n \to L$ ו-$c_n \to L$:
- קיים $N_1$ כך שלכל $n \geq N_1$: $|a_n - L| < \varepsilon$, כלומר $L - \varepsilon < a_n$
- קיים $N_2$ כך שלכל $n \geq N_2$: $|c_n - L| < \varepsilon$, כלומר $c_n < L + \varepsilon$

נבחר $N = \max\{N_0, N_1, N_2\}$. לכל $n \geq N$:

$$L - \varepsilon < a_n \leq b_n \leq c_n < L + \varepsilon$$

לכן $|b_n - L| < \varepsilon$, ומכאן $b_n \to L$.

## משפט עזר: שימור אי-שוויון חלש

תהיינה $(a_n)$, $(b_n)$ סדרות כך ש-$a_n \to a$, $b_n \to b$, והחל ממקום מסוים $a_n \leq b_n$.

אז $a \leq b$.

> [!warning] אי-שוויון חזק אינו נשמר בגבול!
> למשל, $0 < \frac{1}{n}$ לכל $n$, אבל $\lim_{n \to \infty} \frac{1}{n} = 0$.

## דוגמה

חשבו $\lim_{n \to \infty} \frac{(-1)^n \cdot \cos(2^n) \cdot \sqrt[5]{n^3}}{n+1}$.

**פתרון:** נשתמש בסנדוויץ' על מנת להוכיח ש-$|a_n| \to 0$. מתקיים:

$$0 \leq |a_n| \leq \frac{\sqrt[5]{n^3}}{n + 1} = \frac{\sqrt[5]{n^{-2}}}{1 + \frac{1}{n}} \to 0$$

לכן, מסנדוויץ', $|a_n| \to 0$ ומכאן גם $a_n \to 0$.

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Def - סדרה מתכנסת]]
**משמש ב:** [[Thm - משפט הסנדוויץ' לאינסוף]], [[Tool - גבולות בסיסיים של סדרות]], [[Thm - משפט צ'זארו]], [[Thm - התכנסות ממוצע הנדסי]]
