# משפט: השוואת מכפלות גבולות עליונים ותחתונים

## ניסוח

אם $(a_n), (b_n)$ סדרות של מספרים **אי-שליליים**, אזי:

$$a \cdot b \leq \liminf_{n \to \infty}(a_n \cdot b_n) \leq a \cdot B \leq \limsup_{n \to \infty}(a_n \cdot b_n) \leq A \cdot B$$

כאשר:
- $a = \liminf_{n \to \infty} a_n$
- $A = \limsup_{n \to \infty} a_n$
- $b = \liminf_{n \to \infty} b_n$
- $B = \limsup_{n \to \infty} b_n$

## תנאים

הסדרות חייבות להיות **אי-שליליות** ($a_n, b_n \geq 0$ לכל $n$).

## הוכחה (עבור סדרות חסומות)

### אי-שוויון (i): $a \cdot b \leq \liminf(a_n \cdot b_n)$

תהי $(a_{n_k} \cdot b_{n_k})$ תת-סדרה של $(a_n \cdot b_n)$ המתכנסת ל-$\liminf$.

תהי $(a_{n_{k_l}})$ תת-סדרה מתכנסת של $(a_{n_k})$ לגבול $a'$.

תהי $(b_{n_{k_{l_j}}})$ תת-סדרה מתכנסת של $(b_{n_{k_l}})$ לגבול $b'$.

אז:
$$a \cdot b \leq a' \cdot b' = \lim_{j \to \infty} a_{n_{k_{l_j}}} \cdot b_{n_{k_{l_j}}} = \liminf_{n \to \infty}(a_n \cdot b_n)$$

### אי-שוויון (ii): $\liminf(a_n \cdot b_n) \leq a \cdot B$

תהי $(a_{n_k})$ ששואפת ל-$a$.

תהי $(b_{n_{k_l}})$ תת-סדרה של $(b_{n_k})$ המתכנסת לגבול $b'$.

אז $(a_{n_{k_l}} \cdot b_{n_{k_l}})$ שואפת ל-$a \cdot b'$, ומתקיים:
$$\liminf_{n \to \infty}(a_n \cdot b_n) \leq a \cdot b' \leq a \cdot B$$

### אי-שוויונות (iii) ו-(iv)

ההוכחות דומות ל-(ii) ו-(i) בהתאמה.

## הוכחה חלופית (עם אפסילונים) לאי-שוויון (i)

המקרה בו $a = 0$ או $b = 0$ מושאר כתרגיל. אחרת:

יהי $\varepsilon \in (0, 2ab)$. קיים $N \in \mathbb{N}$ כך שלכל $n > N$ מתקיים:
$$a_n \geq a - \frac{\varepsilon}{2b} > 0 \quad \text{וגם} \quad b_n \geq b - \frac{\varepsilon}{2a} > 0$$

לכן לכל $n > N$:
$$a_n b_n \geq \left(a - \frac{\varepsilon}{2b}\right)\left(b - \frac{\varepsilon}{2a}\right) = ab - \varepsilon + \frac{\varepsilon^2}{4ab} > ab - \varepsilon$$

כלומר $\liminf(a_n \cdot b_n) \geq ab - \varepsilon$ לכל $\varepsilon > 0$, ולכן $\liminf(a_n \cdot b_n) \geq ab$.

## הערה חשובה

> [!warning] התנאי הכרחי
> התנאי שהסדרות הן אי-שליליות הוא **הכרחי**.
>
> דוגמה נגדית: $a_n = -3, -1, -3, -1, \ldots$ ו-$b_n = 1, 5, 1, 5, \ldots$
>
> אז $a = -3, A = -1, b = 1, B = 5$, אבל:
> - $a_n \cdot b_n = -3, -5, -3, -5, \ldots$
> - $\limsup(a_n \cdot b_n) = -3 \not\leq A \cdot B = -5$

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול תחתון]], [[Thm - בולצאנו-ויירשטראס]]
**משמש ב:** [[Thm - מבחן המנה לסדרות]]
