# משפט: מבחן המנה לסדרות

## ניסוח

נתונה [[Def - סדרה|סדרה]] חיובית $(a_n)_{n=1}^{\infty}$ כך שמתקיים:

$$L = \lim_{n \to \infty} \frac{a_{n+1}}{a_n}$$

אזי:

1. אם $L < 1$, הסדרה **שואפת לאפס**: $\lim_{n \to \infty} a_n = 0$
2. אם $L > 1$, הסדרה **מתבדרת ל-$+\infty$**: $\lim_{n \to \infty} a_n = +\infty$

## הוכחה

### מקרה 1: $L < 1$

נבחר $\varepsilon > 0$ כך ש-$L + \varepsilon < 1$.

מכיוון ש-$\frac{a_{n+1}}{a_n} \to L$, קיים $N_0 \in \mathbb{N}$ כך שלכל $n \geq N_0$:

$$\left|\frac{a_{n+1}}{a_n} - L\right| < \varepsilon$$

ובפרט:

$$\frac{a_{n+1}}{a_n} < L + \varepsilon$$

כלומר $a_{n+1} < a_n(L + \varepsilon)$.

לכן באינדוקציה, לכל $k \in \mathbb{N}$:

$$0 \leq a_{N_0+k} < a_{N_0}(L + \varepsilon)^k$$

מכיוון ש-$L + \varepsilon < 1$, הסדרה $(L + \varepsilon)^k \to 0$.

מ[[Thm - משפט הסנדוויץ'|משפט הסנדוויץ']]:

$$\lim_{n \to \infty} a_n = \lim_{k \to \infty} a_{N_0+k} = 0$$

### מקרה 2: $L > 1$

נבחר $\delta > 0$ כך ש-$L - \delta > 1 + \delta$.

מהגדרת הגבול, קיים $N_0$ כך שלכל $n \geq N_0$:

$$\frac{a_{n+1}}{a_n} > L - \delta > 1 + \delta$$

יהי $M > 0$. נבחר $k \in \mathbb{N}$ כך ש:

$$a_{N_0}(1 + \delta)^k > M$$

(אפשרי כי $(1 + \delta)^k \to \infty$).

לכל $n > N_0 + k$ מתקיים:

$$a_n = a_{N_0} \prod_{j=1}^{n-N_0} \frac{a_{N_0+j}}{a_{N_0+j-1}} > a_{N_0}(1 + \delta)^{n-N_0} > a_{N_0}(1 + \delta)^k > M$$

לכן $a_n \to +\infty$.

## הערות

> [!warning] המקרה $L = 1$ אינו מכריע
> כאשר $L = 1$, כל האפשרויות יתכנות.

**דוגמאות:**
- $a_n = 1$: מנה $\to 1$, סדרה $\to 1$
- $a_n = \frac{1}{n}$: מנה $\to 1$, סדרה $\to 0$
- $a_n = n$: מנה $\to 1$, סדרה $\to \infty$
- $a_n = \left(1 + \frac{1}{n}\right)^n$: מנה $\to 1$, סדרה $\to e$

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Thm - משפט הסנדוויץ']]
**משמש ב:** [[Thm - מבחן המנה]]
