# למה: אי-שוויון sin ו-tan

## ניסוח

לכל $x \in \left(0, \frac{\pi}{2}\right)$ מתקיים:

$$\sin(x) < x < \tan(x)$$

## מסקנה

לכל $x \neq 0$, $x \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ מתקיים:

$$|\sin(x)| < |x| < |\tan(x)|$$

## הוכחה (לא פורמלית)

נשתמש בהשוואת שטחים על מעגל היחידה.

עבור $x \in \left(0, \frac{\pi}{2}\right)$:

**שטח משולש $ABO$ (מוכל בגזרה):**
$$S_{\triangle ABO} = \frac{1 \cdot \sin(x)}{2} = \frac{\sin(x)}{2}$$

**שטח הגזרה:**
$$S_{ABO} = \pi \cdot \frac{x}{2\pi} = \frac{x}{2}$$

**שטח משולש $ACO$ (מכיל את הגזרה):**
$$S_{\triangle ACO} = \frac{1 \cdot \tan(x)}{2} = \frac{\tan(x)}{2}$$

המשולש $ABO$ מוכל בגזרה, והגזרה מוכלת במשולש $ACO$. לכן:

$$\frac{\sin(x)}{2} < \frac{x}{2} < \frac{\tan(x)}{2}$$

$$\sin(x) < x < \tan(x)$$

## הוכחת המסקנה

עבור $x \in \left(0, \frac{\pi}{2}\right)$ הראינו את זה.

אם $x \in \left(-\frac{\pi}{2}, 0\right)$ אז $-x \in \left(0, \frac{\pi}{2}\right)$ ולפי הלמה:

$$\sin(-x) < -x < \tan(-x)$$
$$-\sin(x) < -x < -\tan(x)$$

כאשר $\sin(x), x, \tan(x)$ כולם שליליים, נקבל:

$$|\sin(x)| < |x| < |\tan(x)|$$

## תלויות

**דורש:** [[Def - רדיאנים]], [[Tool - זהויות טריגונומטריות]]
**משמש ב:** [[Thm - גבול sin(x) חלקי x]], [[Thm - גבול cos(x) ב-0]]
