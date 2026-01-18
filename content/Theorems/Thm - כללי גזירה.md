# משפט: כללי גזירה

## ניסוח

אם $f$ ו-$g$ גזירות ב-$x$, אז:

### 1. ליניאריות הנגזרת

הפונקציה $f + g$ גזירה ב-$x$, ולכל $c \in \mathbb{R}$ הפונקציה $cf$ גזירה ב-$x$:

$$(f + g)'(x) = f'(x) + g'(x)$$
$$(cf)'(x) = c \cdot f'(x)$$

### 2. כלל לייבניץ (כלל המכפלה)

הפונקציה $f \cdot g$ גזירה ב-$x$:

$$(f \cdot g)'(x) = f'(x) \cdot g(x) + f(x) \cdot g'(x)$$

### 3. נגזרת של מנה

אם $g(x) \neq 0$, אז $\frac{f}{g}$ גזירה ב-$x$:

$$\left(\frac{f}{g}\right)'(x) = \frac{f'(x) \cdot g(x) - f(x) \cdot g'(x)}{g^2(x)}$$

## הוכחות

### 1. חיבור: $(f + g)'(x) = f'(x) + g'(x)$

$$\lim_{h \to 0} \frac{(f+g)(x+h) - (f+g)(x)}{h} = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} + \lim_{h \to 0} \frac{g(x+h) - g(x)}{h} = f'(x) + g'(x)$$

$\blacksquare$

### 2. כפל בסקלר: $(cf)'(x) = c \cdot f'(x)$

$$\lim_{h \to 0} \frac{cf(x+h) - cf(x)}{h} = c \cdot \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} = c \cdot f'(x)$$

$\blacksquare$

### 3. כלל לייבניץ (מכפלה): $(f \cdot g)'(x) = f'(x)g(x) + f(x)g'(x)$

$$\frac{f(x+h)g(x+h) - f(x)g(x)}{h} = \frac{f(x+h)g(x+h) - f(x)g(x+h) + f(x)g(x+h) - f(x)g(x)}{h}$$

$$= \frac{f(x+h) - f(x)}{h} \cdot g(x+h) + f(x) \cdot \frac{g(x+h) - g(x)}{h}$$

כאשר $h \to 0$:
- $\frac{f(x+h) - f(x)}{h} \to f'(x)$
- $g(x+h) \to g(x)$ (כי $g$ גזירה ולכן רציפה)
- $\frac{g(x+h) - g(x)}{h} \to g'(x)$

לכן:
$$(f \cdot g)'(x) = f'(x) \cdot g(x) + f(x) \cdot g'(x)$$

$\blacksquare$

### 4. נגזרת של מנה: $\left(\frac{f}{g}\right)'(x) = \frac{f'g - fg'}{g^2}$

נוכיח תחילה ש-$\left(\frac{1}{g}\right)'(x) = -\frac{g'(x)}{g^2(x)}$:

$$\frac{\frac{1}{g(x+h)} - \frac{1}{g(x)}}{h} = \frac{g(x) - g(x+h)}{h \cdot g(x+h) \cdot g(x)} = -\frac{1}{g(x+h) \cdot g(x)} \cdot \frac{g(x+h) - g(x)}{h}$$

כאשר $h \to 0$: $g(x+h) \to g(x)$ ו-$\frac{g(x+h) - g(x)}{h} \to g'(x)$.

לכן:
$$\left(\frac{1}{g}\right)'(x) = -\frac{g'(x)}{g^2(x)}$$

עכשיו, $\frac{f}{g} = f \cdot \frac{1}{g}$, ולפי כלל לייבניץ:

$$\left(\frac{f}{g}\right)' = f' \cdot \frac{1}{g} + f \cdot \left(-\frac{g'}{g^2}\right) = \frac{f'}{g} - \frac{fg'}{g^2} = \frac{f'g - fg'}{g^2}$$

$\blacksquare$

## הסבר

- **ליניאריות:** הנגזרת היא אופרטור לינארי
- **כלל לייבניץ:** שם על שם גוטפריד לייבניץ
- **כלל המנה:** מתקבל מכלל לייבניץ + נגזרת של הפוכי

## תלויות

**דורש:** [[Def - נגזרת]]

**משמש ב:** [[Thm - כלל השרשרת]], [[Example - נגזרת של sin בחזקת cos]]
