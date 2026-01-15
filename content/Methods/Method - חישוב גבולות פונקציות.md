# שיטה: חישוב גבולות פונקציות

## מתי להשתמש

כאשר צריך לחשב $\lim_{x \to a} f(x)$ לפונקציה כלשהי.

## הכלים העיקריים

### 1. אריתמטיקה של גבולות

אם הגבולות הפנימיים קיימים:
- חיבור/חיסור/כפל/חילוק (אם מוגדר)
- [[Thm - אריתמטיקת גבולות פונקציות|אריתמטיקה מוכללת]]: $x + \infty = \infty$, $\infty + \infty = \infty$, $\infty \cdot \infty = \infty$, $\frac{x}{\infty} = 0$

### 2. גבולות לא מוגדרים

לא ניתן לתת כלל אצבע ל:
$$\frac{0}{0}, \quad \frac{\infty}{\infty}, \quad 0 \cdot \infty, \quad \infty - \infty, \quad 1^\infty, \quad 0^0$$

### 3. הרכבה

אם $\lim_{x \to x_0} f(x) = y_0$ ו-$\lim_{y \to y_0} g(y) = L$ ובנוסף $f(x) \neq y_0$ בסביבת $x_0$:
$$\lim_{x \to x_0} g(f(x)) = L$$

### 4. פונקציות אלמנטריות

עבור [[Tool - פונקציות אלמנטריות|פונקציות אלמנטריות]] מתקיים:
$$\lim_{x \to a} f(x) = f(a)$$
לכל $a$ בתחום ההגדרה.

### 5. גבולות ידועים

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$
$$\lim_{x \to \infty} \left(1 + \frac{1}{x}\right)^x = e$$
$$\lim_{x \to 0} \frac{\log(1+x)}{x} = 1$$

## טכניקות נפוצות

### כפל בצמוד

עבור ביטויים עם שורשים:
$$\lim_{x \to 0} \frac{x}{\sqrt{x+1} - 1} = \lim_{x \to 0} \frac{x(\sqrt{x+1} + 1)}{x+1-1} = \lim_{x \to 0} (\sqrt{x+1} + 1) = 2$$

### הצבה

אם $t = f(x)$ ו-$f(x) \to y_0$ כאשר $x \to x_0$:
$$\lim_{x \to x_0} g(f(x)) = \lim_{t \to y_0} g(t)$$

**דוגמה:** חשבו $\lim_{x \to 1} \frac{x^{1/n} - 1}{x^{1/m} - 1}$.

נעזר בהצבה $t = x^{1/(mn)}$, אז $t \to 1$ כאשר $x \to 1$:
$$\lim_{x \to 1} \frac{x^{1/n} - 1}{x^{1/m} - 1} = \lim_{t \to 1} \frac{t^m - 1}{t^n - 1} = \lim_{t \to 1} \frac{(t-1)(1 + \ldots + t^{m-1})}{(t-1)(1 + \ldots + t^{n-1})} = \frac{m}{n}$$

### כלל הסנדוויץ'

אם $g(x) \leq f(x) \leq h(x)$ ו-$\lim g(x) = \lim h(x) = l$, אז $\lim f(x) = l$.

### רישום מחדש של הביטוי

לעיתים יש לפרק את הביטוי למכפלה/מנה של גבולות ידועים:
$$\lim_{x \to 0} \frac{\tan x}{x} = \lim_{x \to 0} \frac{\sin x}{x} \cdot \frac{1}{\cos x} = 1 \cdot 1 = 1$$

### שימוש באקספוננט

עבור $\lim_{x \to 0^+} x^x$:
$$\lim_{x \to 0^+} x^x = \lim_{x \to 0^+} e^{x \ln x} = e^{\lim_{x \to 0^+} x \ln x}$$

וכעת $\lim_{x \to 0^+} x \ln x = \lim_{t \to \infty} \frac{1}{t} \ln \frac{1}{t} = \lim_{t \to \infty} \left(-\frac{\ln t}{t}\right) = 0$.

ולכן $\lim_{x \to 0^+} x^x = e^0 = 1$.

## תלויות

**דורש:** [[Thm - אריתמטיקת גבולות פונקציות]], [[Thm - הרכבת פונקציות וגבולות]], [[Tool - גבולות ידועים של פונקציות]]
**משמש ב:** [[Example - חישובי גבולות פונקציות]]
