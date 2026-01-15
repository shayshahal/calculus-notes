# פונקציה גזירה עם נגזרת לא רציפה

## הפונקציה

$$f(x) = \begin{cases} x^2 \cdot \sin\left(\frac{1}{x}\right), & x \neq 0 \\ 0, & x = 0 \end{cases}$$

## גזירה ב-$x \neq 0$

לכל $x \neq 0$ ניתן לגזור בנקודה $x$ לפי כללי גזירה:

$$(f(x))' = 2x \cdot \sin\left(\frac{1}{x}\right) + x^2 \cos\left(\frac{1}{x}\right) \cdot \left(-\frac{1}{x^2}\right) = 2x \cdot \sin\left(\frac{1}{x}\right) - \cos\left(\frac{1}{x}\right)$$

## גזירה ב-$x = 0$

בנקודה $0$ נגזור לפי ההגדרה. לכל $h \neq 0$:

$$\frac{f(0 + h) - f(0)}{h} = \frac{h^2 \sin\left(\frac{1}{h}\right)}{h} = h \sin\left(\frac{1}{h}\right) \xrightarrow[h \to 0]{\text{אפסה כפול חסומה}} 0$$

## סיכום

סה"כ $f$ גזירה בכל $\mathbb{R}$:

$$f'(x) = \begin{cases} 2x \cdot \sin\left(\frac{1}{x}\right) - \cos\left(\frac{1}{x}\right), & x \neq 0 \\ 0, & x = 0 \end{cases}$$

$f'$ **לא רציפה ב-$0$**. (הגבול $\lim_{x \to 0} f'(x)$ לא קיים)

## תרגיל

הראו כי $f(x) = x^2 D(x)$ גזירה בנקודה $0$, ולא גזירה באף נקודה אחרת (כאשר $D(x)$ היא פונקציית דיריכלה).

## תלויות
**דורש:** [[Def - נגזרת]], [[Tool - נגזרות של פונקציות יסודיות]]
**משמש ב:** —
