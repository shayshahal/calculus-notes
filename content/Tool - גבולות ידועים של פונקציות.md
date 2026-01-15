# כלי: גבולות ידועים של פונקציות

## גבולות בסיסיים

### לוגריתם מול חזקה

$$\lim_{x \to \infty} \frac{\log x}{x^\alpha} = 0 \quad \text{כאשר } \alpha > 0$$

### חזקה מול אקספוננט

$$\lim_{x \to \infty} \frac{x^b}{a^x} = 0 \quad \text{כאשר } a > 1 \text{ ו-} b \in \mathbb{R}$$

**הוכחה:**
$$\lim_{x \to \infty} \frac{x^b}{a^x} = e^{\lim_{x \to \infty}(b \ln x - x \ln a)} \leq e^{\lim_{x \to \infty} -\frac{x \ln a}{2}} = e^{-\infty} = 0$$

כאשר אי-השוויון נובע מהאבחנה: $b \ln x < \frac{1}{2} x \ln a$ החל ממקום מסוים.

### גבול סינוס

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

### גבול אקספוננטי

$$\lim_{x \to \infty} \left(1 + \frac{1}{x}\right)^x = \lim_{x \to 0} (1 + x)^{1/x} = e$$

**בעזרת כלל ההצבה:** אם $\lim_{x \to x_0} f(x) = \infty$ אזי:
$$\lim_{x \to x_0} \left(1 + \frac{1}{f(x)}\right)^{f(x)} = e$$

### גבול לוגריתמי

$$\lim_{x \to 0} \frac{\log(1+x)}{x} = 1$$

**הוכחה:**
$$\lim_{t \to 0} \frac{\log(1+t)}{t} = \lim_{t \to 0} \log(1+t)^{1/t} = \log\left(\lim_{t \to 0}(1+t)^{1/t}\right) = \log e = 1$$

כאשר במעבר השני השתמשנו באלמנטריות הפונקציה $\log$.

## כלל הסנדוויץ' לפונקציות

אם ידוע כי $\lim_{x \to x_0} h(x) = \lim_{x \to x_0} g(x) = l$ ובנוסף $g(x) \leq f(x) \leq h(x)$ בסביבה של $x_0$, אזי $\lim_{x \to x_0} f(x) = l$.

## כלל ההשוואה

אם ידוע כי $\lim_{x \to x_0} g(x) = \infty$ ובנוסף $f(x) \geq g(x)$ בסביבה של $x_0$, אזי $\lim_{x \to x_0} f(x) = \infty$.

## תלויות

**דורש:** [[Def - גבול של פונקציה]], [[Thm - הרכבת פונקציות וגבולות]], [[Thm - משפט הסנדוויץ']]
**משמש ב:** [[Method - חישוב גבולות פונקציות]], [[Example - חישובי גבולות פונקציות]]
