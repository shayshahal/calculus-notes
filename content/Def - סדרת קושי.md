# הגדרה: סדרת קושי

## הגדרה פורמלית

סדרה $\{a_n\}$ נקראת **סדרת קושי** אם:

$$\forall \varepsilon > 0 \; \exists N : \forall n, m \geq N, \; |a_n - a_m| < \varepsilon$$

## ניסוח שקול

$$\forall \varepsilon > 0 \; \exists N : \forall n \geq N, \; k \in \mathbb{N}, \; |a_{n+k} - a_n| < \varepsilon$$

## סדרה אינה סדרת קושי אם

$$\exists \varepsilon > 0 \; \forall n \; \exists m > n : |a_m - a_n| > \varepsilon$$

בניסוח אחר:

$$\exists \varepsilon > 0 \; \forall n \; \exists k \in \mathbb{N} : |a_{n+k} - a_n| > \varepsilon$$

## הסבר

סדרת קושי היא סדרה שהאיברים שלה "מתקרבים זה לזה" ככל שמתקדמים.

היתרון בהגדרה זו הוא שאין צורך לדעת מהו הגבול כדי לבדוק התכנסות.

## רעיון

לפעמים קשה לחשב גבול וקל להראות שסדרה היא סדרת קושי.

## דוגמה - סדרה שהיא סדרת קושי

הסדרה $a_n = 1 + \frac{1}{4} + \frac{2^2}{4^2} + \ldots + \frac{n^2}{4^n}$ היא סדרת קושי.

**פתרון:** מתקיים $n^4 < 4^n$ לכל $n \geq 5$. לכן (ניתן להניח כי $n \geq 5$):

$$|a_{n+k} - a_n| = \sum_{j=n+1}^{n+k} \frac{j^2}{4^j} < \sum_{j=n+1}^{n+k} \frac{1}{j^2} \leq \sum_{j=n+1}^{n+k} \frac{1}{j(j-1)}$$

נשים לב כי $\frac{1}{j(j-1)} = \frac{1}{j-1} - \frac{1}{j}$ (טלסקופי), ולכן:

$$|a_{n+k} - a_n| < \frac{1}{n} - \frac{1}{n+k} < \frac{1}{n}$$

לכן בהינתן $\varepsilon > 0$ נבחר $N \in \mathbb{N}$ כך ש-$N > \frac{1}{\varepsilon}$. אז לכל $n > N$ ולכל $k \in \mathbb{N}$ מתקיים $|a_{n+k} - a_n| < \frac{1}{n} < \varepsilon$.

## דוגמה - סדרה שאינה סדרת קושי

הסדרה $a_n = \sum_{k=1}^{n} \frac{1}{\sqrt{k}}$ אינה סדרת קושי.

**פתרון:** נגדיר $\varepsilon_0 = \frac{1}{\sqrt{2}}$, יהי $N \in \mathbb{N}$, ונסמן $m = 2N$. אז מתקיים:

$$|a_n - a_m| = \left|\sum_{k=1}^{n} \frac{1}{\sqrt{k}} - \sum_{k=1}^{m} \frac{1}{\sqrt{k}}\right| = \sum_{k=N+1}^{2N} \frac{1}{\sqrt{k}} \geq \sum_{k=N+1}^{2N} \frac{1}{\sqrt{2N}} = \frac{N}{\sqrt{2N}} = \frac{\sqrt{N}}{\sqrt{2}} \geq \frac{1}{\sqrt{2}} = \varepsilon_0$$

## תלויות

**דורש:** [[Def - סדרה]], [[Def - ערך מוחלט]]
**משמש ב:** [[Thm - סדרה מתכנסת היא סדרת קושי]], [[Thm - סדרת קושי מתכנסת]]
