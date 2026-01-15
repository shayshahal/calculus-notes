# משפט: רציפות במידה שווה בקטע אינסופי

## ניסוח

תהי $f: [a, \infty) \to \mathbb{R}$ פונקציה רציפה.

אם $\lim_{x \to \infty} f(x)$ קיים וסופי, אז $f$ רציפה במידה שווה ב-$[a, \infty)$.

## תנאים

- $f$ רציפה ב-$[a, \infty)$
- הגבול באינסוף קיים וסופי

## הוכחה

נסמן $L = \lim_{x \to \infty} f(x)$. יהי $\epsilon > 0$.

לפי הגדרת הגבול:
$$\exists(M > a)\forall(x \geq M)\left[|f(x) - L| < \frac{\epsilon}{4}\right]$$

מכאן נובע שלכל $x, y \geq M$ מתקיים:
$$|f(x) - f(y)| = |f(x) - L + L - f(y)| \leq |f(x) - L| + |f(y) - L| < \frac{\epsilon}{4} + \frac{\epsilon}{4} = \frac{\epsilon}{2}$$

בנוסף, לפי [[Thm - משפט קנטור]], $f$ רציפה במ"ש ב-$[a, M]$ ולכן:
$$\exists(\delta > 0)\forall(x, y \in [a,M]: |x - y| < \delta)\left[|f(x) - f(y)| < \frac{\epsilon}{2}\right]$$

נראה כי $\delta$ זה עובד בכל הקטע $[a, \infty)$.

יהיו $x, y \in [a, \infty)$ המקיימים $|x - y| < \delta$. נפריד למקרים:

1. **$x, y \in [a, M]$**: לפי הגדרת $\delta$ מתקיים $|f(x) - f(y)| < \frac{\epsilon}{2} < \epsilon$

2. **$x, y \in [M, \infty)$**: כפי שראינו $|f(x) - f(y)| < \frac{\epsilon}{2} < \epsilon$

3. **$x \in [a, M], y \in [M, \infty)$** (ללא הגבלת הכלליות):
   - $|x - M| = M - x \leq y - x = |y - x| < \delta$
   - לכן $x, M$ שתי נקודות ב-$[a,M]$ עם $|x - M| < \delta$, כך ש-$|f(x) - f(M)| < \frac{\epsilon}{2}$
   - באופן דומה $|M - y| < \delta$, ו-$M, y \in [M, \infty)$ כך ש-$|f(M) - f(y)| < \frac{\epsilon}{2}$
   - סה"כ: $|f(x) - f(y)| \leq |f(x) - f(M)| + |f(M) - f(y)| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$

$\blacksquare$

## הערות

- **ההפך לא נכון**: $f(x) = \sin(x)$ ו-$f(x) = x$ רציפות במ"ש ב-$[0, \infty)$ למרות שאין להן גבול סופי באינסוף
- באופן דומה, אם $f: (-\infty, b] \to \mathbb{R}$ רציפה והגבול $\lim_{x \to -\infty} f(x)$ קיים וסופי, אז $f$ רציפה במ"ש

## דוגמה

$f(x) = \frac{\sin(x)}{x}$ רציפה במ"ש ב-$(0, \infty)$ כי:
- היא רציפה
- $\lim_{x \to 0^+} \frac{\sin(x)}{x} = 1$
- $\lim_{x \to \infty} \frac{\sin(x)}{x} = 0$ (חסומה כפול שואפת ל-0)

## תלויות

**דורש:** [[Def - רציפות במידה שווה]], [[Def - גבול פונקציה באינסוף]], [[Thm - משפט קנטור]], [[Thm - אי-שוויון המשולש]]

**משמש ב:** [[Lemma - הדבקת קטעים]]
