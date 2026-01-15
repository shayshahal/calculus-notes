# דוגמה: מבחן מנה עם פרמטר

## הטור

$$\sum_{n=1}^{\infty} \frac{n! \cdot a^n}{n^n}$$

כאשר $a > 0$ פרמטר.

## פתרון

זה [[Def - טור חיובי|טור חיובי]].

נסמן $a_n = \frac{n! \cdot a^n}{n^n}$.

### חישוב יחס האיברים העוקבים

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)! \cdot a^{n+1}}{(n+1)^{n+1}} \cdot \frac{n^n}{n! \cdot a^n}$$

$$= \frac{(n+1) \cdot a \cdot n^n}{(n+1)^{n+1}} = a \cdot \frac{n^n}{(n+1)^n}$$

$$= a \cdot \left(\frac{n}{n+1}\right)^n = a \cdot \left(\frac{n+1-1}{n+1}\right)^n = a \cdot \left(1 - \frac{1}{n+1}\right)^n$$

### חישוב הגבול

$$\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = a \cdot \lim_{n \to \infty} \left(1 - \frac{1}{n+1}\right)^n = a \cdot \frac{1}{e} = \frac{a}{e}$$

### מסקנות לפי [[Thm - מבחן המנה|מבחן המנה הגבולי]]

1. **אם $a < e$:** הגבול $\frac{a}{e} < 1$, לכן הטור **מתכנס**

2. **אם $a > e$:** הגבול $\frac{a}{e} > 1$, לכן הטור **מתבדר**

3. **אם $a = e$:** הגבול שווה 1, מבחן המנה הגבולי נכשל

### המקרה $a = e$

נשים לב שמתקיים:

$$\frac{a_n}{a_{n+1}} = \frac{1}{a} \cdot \left(\frac{n+1}{n}\right)^n = \frac{1}{a} \cdot \left(1 + \frac{1}{n}\right)^n$$

הסדרה $\left(1 + \frac{1}{n}\right)^n$ **מונוטונית עולה** וחסומה על ידי $e$.

לכן כאשר $a = e$:

$$\frac{a_n}{a_{n+1}} = \frac{1}{e} \cdot \left(1 + \frac{1}{n}\right)^n \leq \frac{e}{e} = 1$$

כלומר:

$$\frac{a_{n+1}}{a_n} \geq 1$$

לפי [[Thm - מבחן המנה|מבחן המנה הרגיל]] (חלק 2), הטור **מתבדר** כאשר $a = e$.

## סיכום

$$\sum_{n=1}^{\infty} \frac{n! \cdot a^n}{n^n} \begin{cases} \text{מתכנס} & a < e \\ \text{מתבדר} & a \geq e \end{cases}$$

## הערה

זו דוגמה קלאסית שמראה את החשיבות של בדיקת המקרה הגבולי ($a = e$) בנפרד כאשר מבחן המנה הגבולי נכשל.

## תלויות

**דורש:** [[Thm - מבחן המנה]], [[Def - טור חיובי]], [[Def - הקבוע e]]
**משמש ב:** בעיות פרמטריות, [[Def - רדיוס התכנסות]]
