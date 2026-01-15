# משפט: מבחן ההשוואה הגבולי

## ניסוח

נתונות סדרות של מספרים חיוביים $a_n, b_n$.

נניח כי קיים הגבול:
$$\ell = \lim_{n \to \infty} \frac{a_n}{b_n}$$

אז:

1. **אם $\ell \in (0, \infty)$:** הטורים מתכנסים ומתבדרים **יחד**
   $$\sum a_n < \infty \iff \sum b_n < \infty$$

2. **אם $\ell = 0$:**
   $$\sum b_n < \infty \Rightarrow \sum a_n < \infty$$

3. **אם $\ell = \infty$:**
   $$\sum a_n < \infty \Rightarrow \sum b_n < \infty$$

## רעיון ההוכחה (מקרה $\ell \in (0, \infty)$)

לפי הנתון, קיים $\epsilon > 0$ קטן מספיק כך שהמ"מ:
$$0 < \ell - \epsilon < \frac{a_n}{b_n} < \ell + \epsilon$$

כלומר:
$$a_n < (\ell + \epsilon) b_n \quad \text{וגם} \quad b_n < \frac{1}{\ell - \epsilon} a_n$$

לפי [[Thm - מבחן ההשוואה הרגיל|מבחן ההשוואה]], $\sum a_n$ מתכנס אם"ם $\sum b_n$ מתכנס.

## אזהרה

> התוצאה **אינה נכונה** אם $a_n, b_n$ אינם טורים חיוביים!

## דוגמה

בדקו עבור אילו ערכים של $\alpha$ הטור הבא מתכנס:
$$\sum_{n=1}^{\infty} \left(\sqrt{n+1} - \sqrt{n-1}\right)^\alpha$$

**פתרון:**

נסמן $a_n = \left(\sqrt{n+1} - \sqrt{n-1}\right)^\alpha$.

נפשט:
$$a_n = \left(\sqrt{n+1} - \sqrt{n-1}\right)^\alpha \cdot \frac{\left(\sqrt{n+1} + \sqrt{n-1}\right)^\alpha}{\left(\sqrt{n+1} + \sqrt{n-1}\right)^\alpha}$$

$$= \frac{((n+1) - (n-1))^\alpha}{\left(\sqrt{n+1} + \sqrt{n-1}\right)^\alpha} = \frac{2^\alpha}{\left(\sqrt{n+1} + \sqrt{n-1}\right)^\alpha}$$

נשתמש בהשוואה עם $b_n = \frac{1}{n^\beta}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{2^\alpha \cdot n^\beta}{n^{\alpha/2} \cdot \left(\sqrt{1 + \frac{1}{n}} + \sqrt{1 - \frac{1}{n}}\right)^\alpha} = \lim_{n \to \infty} n^{\beta - \alpha/2}$$

הגבול הוא $1$ כאשר $\beta = \alpha/2$.

כלומר, הטור $\sum a_n$ מתכנס אם"ם הטור $\sum \frac{1}{n^{\alpha/2}}$ מתכנס, כלומר כאשר $\alpha > 2$.

## תלויות

**דורש:** [[Def - טור חיובי]], [[Thm - מבחן ההשוואה הרגיל]], [[Def - גבול של סדרה]]
**משמש ב:** [[Thm - מבחן השורש]], [[Thm - מבחן המנה]]
