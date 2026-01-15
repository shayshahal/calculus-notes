# דוגמה: חישובי גבולות פונקציות

## דוגמה 1: גבול של פונקציה רציונלית

$$\lim_{x \to a} \frac{x^2 - 3x + 2}{x^2 - 5x + 6}$$

### (א) $a = 2$: מחשבון גבולות

$$\frac{x^2 - 3x + 2}{x^2 - 5x + 6} = \frac{(x-1)(x-2)}{(x-2)(x-3)} = \frac{x-1}{x-3} \to \frac{1}{-1} = -1$$

### (ב) $a = \infty$: מחשבון גבולות

$$\frac{x^2 - 3x + 2}{x^2 - 5x + 6} = \frac{1 - \frac{3}{x} + \frac{2}{x^2}}{1 - \frac{5}{x} + \frac{6}{x^2}} \to 1$$

## דוגמה 2: כפל בצמוד

$$\lim_{x \to a} \frac{x}{\sqrt{x+1} - 1}$$

### (א) $a = 0$: כפל בצמוד

$$\lim_{x \to 0} \frac{x}{\sqrt{x+1} - 1} = \lim_{x \to 0} \frac{x(\sqrt{x+1} + 1)}{x+1-1} = \lim_{x \to 0} (\sqrt{x+1} + 1) = 2$$

### (ב) $a = \infty$: מוציאים $\sqrt{x}$

$$\lim_{x \to \infty} \frac{x}{\sqrt{x+1} - 1} = \lim_{x \to \infty} \sqrt{x} \cdot \frac{1}{\sqrt{1 + \frac{1}{x}} - \frac{1}{\sqrt{x}}} = \infty$$

על ידי אריתמטיקה מוכללת ($\infty \cdot 1 = \infty$).

## דוגמה 3: גבול טריגונומטרי

$$\lim_{x \to 0} \frac{\tan x}{x}$$

$$\lim_{x \to 0} \frac{\tan x}{x} = \lim_{x \to 0} \frac{\sin x}{x} \cdot \frac{1}{\cos x} \stackrel{(*)}{=} \lim_{x \to 0} \frac{\sin x}{x} \cdot \lim_{x \to 0} \frac{1}{\cos x} = 1$$

המעבר $(*)$ מוצדק משום שהגבולות מימינו קיימים.

## דוגמה 4: כלל הסנדוויץ'

$$\lim_{x \to 0} x \cos\left(\frac{1}{x}\right)$$

נעזרים בכלל הסנדוויץ'/השוואה: $\left|x \cos\left(\frac{1}{x}\right)\right| \leq |x|$ ו-$\lim_{x \to 0} |x| = 0$.

ולכן הגבול הוא $0$.

## דוגמה 5: גבול לוגריתמי

$$\lim_{x \to 0} \frac{\log(\cos x)}{x^2}$$

רושמים מחדש:
$$\lim_{x \to 0} \frac{\log(\cos x)}{x^2} = \lim_{x \to 0} \frac{\log(1 + \cos x - 1)}{\cos x - 1} \cdot \frac{\cos x - 1}{x^2}$$

הגבול הראשון (הצבה $t = \cos(x) - 1$):
$$\lim_{x \to 0} \frac{\log(1 + \cos(x) - 1)}{\cos(x) - 1} = \lim_{t \to 0} \frac{\log(1+t)}{t} = 1$$

הגבול השני (זהות טריגונומטרית):
$$\lim_{x \to 0} \frac{\cos(x) - 1}{x^2} = \lim_{x \to 0} \frac{-2\sin^2\left(\frac{x}{2}\right)}{x^2} = -\frac{1}{2}$$

לכן הגבול המקורי הוא $-\frac{1}{2}$.

## דוגמה 6: גבול מהצורה $1^\infty$

$$\lim_{x \to 0} (1 + \tan x)^{1/x}$$

$$\lim_{x \to 0} (1 + \tan x)^{1/x} = \lim_{x \to 0} (1 + \tan x)^{\frac{1}{\tan x} \cdot \frac{\tan x}{x}}$$

לפי כלל ההצבה: $(1 + \tan x)^{1/\tan x} \to e$

ולכן: $(1 + \tan x)^{\frac{1}{\tan x} \cdot \frac{\tan x}{x}} \to e^1 = e$

## דוגמה 7: גבול מהצורה $0^0$

$$\lim_{x \to 0^+} x^x$$

נשתמש בכלל ההצבה ובאלמנטריות של $e^x$:
$$\lim_{x \to 0^+} x^x = \lim_{x \to 0^+} e^{x \ln x} = \ldots$$

$$\lim_{x \to 0^+} x \ln x = \lim_{t \to \infty} \frac{1}{t} \ln\frac{1}{t} = \lim_{t \to \infty} \left(-\frac{\ln t}{t}\right) = 0$$

$$\ldots = \lim_{y \to 0} e^y = e^0 = 1$$

## דוגמה 8: פונקציית המדרגות

$$\lim_{x \to 0^+} x \cdot \left\lfloor\frac{1}{x}\right\rfloor$$

נשים לב כי מתקיים: $\frac{1}{x} - 1 \leq \left\lfloor\frac{1}{x}\right\rfloor \leq \frac{1}{x}$

$$\lim_{x \to 0^+} x \cdot \left(\frac{1}{x} - 1\right) = \lim_{x \to 0^+} x \cdot \frac{1}{x} = 1$$

ולכן לפי כלל הסנדוויץ' הגבול הוא $1$.

## תלויות

**דורש:** [[Tool - גבולות ידועים של פונקציות]], [[Thm - אריתמטיקת גבולות פונקציות]], [[Method - חישוב גבולות בעזרת הצבה]], [[Thm - כלל הסנדוויץ' לפונקציות]]
**משמש ב:** [[Method - חישוב גבולות פונקציות]], [[Example - מיון נקודות אי-רציפות]]
