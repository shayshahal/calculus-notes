# דוגמה: $\log x$ רציפה במ"ש ב-$(1, \infty)$

## טענה

הפונקציה $f(x) = \log x$ רציפה במידה שווה בקטע $(1, \infty)$.

## הוכחה

יהי $\varepsilon > 0$. צריך למצוא $\delta > 0$ כך שאם $|x - y| < \delta$ אז $|\log x - \log y| < \varepsilon$ לכל $x, y \in (1, \infty)$.

יהיו $x, y \in [1, \infty)$ עם $|x - y| < \delta$ (נקבע את $\delta$ בהמשך). נניח בה"כ $y > x$.

אז:
$$|\log x - \log y| = \log\frac{y}{x} = \log\frac{y - x + x}{x} = \log\left(1 + \frac{y - x}{x}\right)$$

**אפשרות 1:** שימוש באי-שוויון $\log(1+t) \leq t$ לכל $t > -1$:

$$\log\left(1 + \frac{y-x}{x}\right) \leq \frac{y-x}{x} \leq |y-x| < \delta$$

לכן מספיק לבחור $\delta = \varepsilon$.

**אפשרות 2:** שימוש בגבול המוכר $\lim_{t \to 0^+} \frac{\log(1+t)}{t} = 1$:

מהגדרת הגבול, קיים $\delta_1 > 0$ כך שלכל $0 < t < \delta_1$:
$$\left|\frac{\log(1+t)}{t} - 1\right| < 1 \implies \log(1+t) < 2t$$

לכן אם $\delta \leq \delta_1$:
$$\log\left(1 + \frac{y-x}{x}\right) < 2 \cdot \frac{y-x}{x} \leq 2|x-y| < 2\delta \leq \varepsilon$$

נבחר $\delta = \min\left\{\delta_1, \frac{\varepsilon}{2}\right\}$.

## תלויות

**דורש:** [[Def - רציפות במידה שווה]], [[Tool - גבולות ידועים של פונקציות]]

**משמש ב:** —
