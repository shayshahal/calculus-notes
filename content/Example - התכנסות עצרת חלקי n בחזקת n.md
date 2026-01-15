# דוגמה: התכנסות עצרת חלקי n בחזקת n

## הטור

$$\sum_{n=1}^{\infty} \frac{n!}{n^n}$$

## פתרון

### שלב 1: זיהוי שזה טור חיובי

לכל $n \geq 1$ מתקיים $\frac{n!}{n^n} > 0$, לכן זה [[Def - טור חיובי|טור חיובי]].

### שלב 2: מציאת חסם עליון

נפרק את האיבר הכללי:

$$\frac{n!}{n^n} = \frac{1 \cdot 2 \cdot 3 \cdot 4 \cdots n}{n \cdot n \cdot n \cdot n \cdots n} = \frac{2}{n^2} \cdot \underbrace{\frac{3}{n} \cdot \frac{4}{n} \cdot \frac{5}{n} \cdots \frac{n}{n}}_{\text{כל גורם } \leq 1}$$

כל גורם מהצורה $\frac{k}{n}$ (עבור $k \leq n$) קטן או שווה ל-1, לכן:

$$\frac{n!}{n^n} \leq \frac{2}{n^2}$$

### שלב 3: מבחן ההשוואה

הטור $\sum_{n=1}^{\infty} \frac{2}{n^2}$ מתכנס (כי $\sum \frac{1}{n^2}$ מתכנס והקבוע 2 לא משפיע).

לפי [[Thm - מבחן ההשוואה הרגיל|מבחן ההשוואה הראשון]]:

$$\frac{n!}{n^n} \leq \frac{2}{n^2} \quad \text{וגם} \quad \sum \frac{2}{n^2} < \infty$$

לכן:

$$\sum_{n=1}^{\infty} \frac{n!}{n^n} < \infty$$

## הערה

ניתן גם להשתמש ב[[Thm - מבחן המנה|מבחן המנה]]:

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)!}{(n+1)^{n+1}} \cdot \frac{n^n}{n!} = \frac{n^n}{(n+1)^n} = \left(\frac{n}{n+1}\right)^n \to \frac{1}{e} < 1$$

לכן הטור מתכנס לפי מבחן המנה הגבולי.

## תלויות

**דורש:** [[Def - טור חיובי]], [[Thm - מבחן ההשוואה הרגיל]], [[Thm - מבחן המנה]], [[Def - עצרת]]
**משמש ב:** [[Example - התכנסות טור עם פרמטר a]]
