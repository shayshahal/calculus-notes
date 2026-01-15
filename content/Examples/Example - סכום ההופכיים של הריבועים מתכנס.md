# דוגמה: סכום ההופכיים של הריבועים מתכנס

## הסדרה

$$a_n = 1 + \frac{1}{2^2} + \frac{1}{3^2} + \cdots + \frac{1}{n^2} = \sum_{k=1}^{n} \frac{1}{k^2}$$

## הטענה

הסדרה $(a_n)$ היא [[Def - סדרת קושי|סדרת קושי]], ולכן מתכנסת.

## הוכחה

יהי $\varepsilon > 0$. לכל $n, p \in \mathbb{N}$ מתקיים:

$$|a_{n+p} - a_n| = \left| \left(1 + \frac{1}{2^2} + \cdots + \frac{1}{n^2} + \cdots + \frac{1}{(n+p)^2}\right) - \left(1 + \frac{1}{2^2} + \cdots + \frac{1}{n^2}\right) \right|$$

$$= \left| \frac{1}{(n+1)^2} + \frac{1}{(n+2)^2} + \cdots + \frac{1}{(n+p)^2} \right|$$

$$= \frac{1}{(n+1)^2} + \frac{1}{(n+2)^2} + \cdots + \frac{1}{(n+p)^2}$$

### אומדן באמצעות שברים חלקיים

נשתמש באי-שוויון:
$$\frac{1}{k^2} \leq \frac{1}{k(k-1)} = \frac{1}{k-1} - \frac{1}{k}$$

(זהות טלסקופית: $\frac{1}{k(k-1)} = \frac{1}{k-1} - \frac{1}{k}$)

לכן:
$$|a_{n+p} - a_n| \leq \frac{1}{n(n+1)} + \frac{1}{(n+1)(n+2)} + \cdots + \frac{1}{(n+p-1)(n+p)}$$

$$= \left(\frac{1}{n} - \frac{1}{n+1}\right) + \left(\frac{1}{n+1} - \frac{1}{n+2}\right) + \cdots + \left(\frac{1}{n+p-1} - \frac{1}{n+p}\right)$$

זהו **טור טלסקופי**, ולכן:
$$|a_{n+p} - a_n| \leq \frac{1}{n} - \frac{1}{n+p} < \frac{1}{n}$$

### בחירת $N$

נרצה $\frac{1}{n} < \varepsilon$, כלומר $n > \frac{1}{\varepsilon}$.

נבחר $N_0 = \left\lfloor \frac{1}{\varepsilon} \right\rfloor + 1$.

לכל $n \geq N_0$ ולכל $p \in \mathbb{N}$:
$$|a_{n+p} - a_n| < \frac{1}{n} \underset{n \geq N_0 > \frac{1}{\varepsilon}}{\leq} \varepsilon$$

$\blacksquare$

## מסקנה

הסדרה היא סדרת קושי, ולפי [[Thm - סדרה מתכנסת היא סדרת קושי|קריטריון קושי]] היא מתכנסת.

## הערה

הגבול הוא $\frac{\pi^2}{6}$ (תוצאה של אוילר), אך אין צורך לדעת זאת כדי להוכיח התכנסות!

## תלויות

**דורש:** [[Def - סדרת קושי]], [[Thm - סדרה מתכנסת היא סדרת קושי]], [[Def - טור טלסקופי]]
**משמש ב:** [[Thm - התכנסות טור הריבועים ההופכיים]]
