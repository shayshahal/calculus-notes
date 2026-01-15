# דוגמה: x כפול sin(1 חלקי x) שואף ל-0

## הטענה

$$x \cdot \sin\left(\frac{1}{x}\right) \xrightarrow{x \to 0} 0$$

## הוכחה

נשתמש בעובדה שמכפלת פונקציה חסומה בפונקציה שואפת לאפס שואפת לאפס.

**פירוק:**

- הפונקציה $g(x) = x$ מקיימת $x \xrightarrow{x \to 0} 0$
- הפונקציה $f(x) = \sin\left(\frac{1}{x}\right)$ חסומה: $\left|\sin\left(\frac{1}{x}\right)\right| \leq 1$

**מסקנה:**

$$\left|x \cdot \sin\left(\frac{1}{x}\right)\right| = |x| \cdot \left|\sin\left(\frac{1}{x}\right)\right| \leq |x| \cdot 1 = |x| \xrightarrow{x \to 0} 0$$

לפי כלל הסנדוויץ':

$$-|x| \leq x \cdot \sin\left(\frac{1}{x}\right) \leq |x|$$

ומכיוון ש-$|x| \to 0$ וגם $-|x| \to 0$, נקבל:

$$x \cdot \sin\left(\frac{1}{x}\right) \xrightarrow{x \to 0} 0$$

## השוואה

שימו לב להבדל מ-$\sin\left(\frac{1}{x}\right)$ לבדה, שאין לה גבול ב-$0$ (ראו [[Example - אי-קיום גבול sin(1 חלקי x)]]).

הכפלה ב-$x$ "מרסנת" את ההתנודות של הסינוס.

## תלויות

**דורש:** [[Thm - כלל הסנדוויץ' לפונקציות]], [[Def - פונקציה חסומה]]
**משמש ב:** [[Method - חישוב גבולות פונקציות]]
