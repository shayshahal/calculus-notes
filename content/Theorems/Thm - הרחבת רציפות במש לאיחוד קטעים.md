# משפט: הרחבת רציפות במ"ש לאיחוד קטעים

## ניסוח

אם $f$ רציפה במידה שווה בקטעים המוכללים $(a, b]$ ו-$[b, c)$, אזי $f$ רציפה במידה שווה ב-$(a, c)$.

באופן דומה, הטענה נכונה כאשר $a = -\infty$ ו/או $c = \infty$.

## הוכחה

יהי $\varepsilon > 0$. נבחר $\delta = \min\{\delta_1, \delta_2\}$ כאשר:
- $\delta_1$ מתאים לקטע $(a, b]$ עבור $\varepsilon/2$
- $\delta_2$ מתאים לקטע $[b, c)$ עבור $\varepsilon/2$

נראה כי $\delta$ מבטיח רציפות במ"ש ב-$(a, c)$.

יהיו $x < y$ ב-$(a, c)$ עם $|y - x| < \delta$. יש שלושה מקרים:

**מקרה 1:** $x, y \in (a, b]$

מכיוון ש-$|x - y| < \delta \leq \delta_1$, נסיק $|f(x) - f(y)| < \varepsilon/2 < \varepsilon$.

**מקרה 2:** $x, y \in [b, c)$

בדומה, $|f(x) - f(y)| < \varepsilon/2 < \varepsilon$.

**מקרה 3:** $x \in (a, b]$ ו-$y \in [b, c)$

מתקיים:
$$|b - x| = b - x \leq y - x < \delta \leq \delta_1$$
$$|b - y| = y - b \leq y - x < \delta \leq \delta_2$$

לכן מאי-שוויון המשולש:
$$|f(x) - f(y)| \leq |f(x) - f(b)| + |f(b) - f(y)| < \varepsilon/2 + \varepsilon/2 = \varepsilon$$

## תלויות

**דורש:** [[Def - רציפות במידה שווה]], [[Thm - אי-שוויון המשולש]]

**משמש ב:** —
