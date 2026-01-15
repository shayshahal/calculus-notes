# דוגמה: טור טלסקופי מוכלל

## הבעיה

חשבו את סכום הטור:

$$\sum_{n=1}^{\infty} \frac{1}{n(n+2)}$$

## פתרון

**שלב 1: פירוק לשברים חלקיים**

$$\frac{1}{n(n+2)} = \frac{1}{2} \left( \frac{1}{n} - \frac{1}{n+2} \right)$$

זה לא בדיוק [[Def - טור טלסקופי|טור טלסקופי]] רגיל (כי ההפרש הוא בין $n$ ל-$n+2$ ולא $n+1$).

**שלב 2: חישוב הסכום החלקי**

$$S_n = \sum_{k=1}^{n} \frac{1}{k(k+2)} = \frac{1}{2} \sum_{k=1}^{n} \left( \frac{1}{k} - \frac{1}{k+2} \right)$$

נפתח:
$$= \frac{1}{2} \left( \sum_{k=1}^{n} \frac{1}{k} - \sum_{k=1}^{n} \frac{1}{k+2} \right) = \frac{1}{2} \left( \sum_{k=1}^{n} \frac{1}{k} - \sum_{k=3}^{n+2} \frac{1}{k} \right)$$

**שלב 3: צמצום טלסקופי**

$$= \frac{1}{2} \left( \frac{1}{1} + \frac{1}{2} - \frac{1}{n+1} - \frac{1}{n+2} \right)$$

$$= \frac{1}{2} \left( 1 + \frac{1}{2} - \frac{1}{n+1} - \frac{1}{n+2} \right)$$

**שלב 4: חישוב הגבול**

$$\lim_{n \to \infty} S_n = \frac{1}{2} \cdot \frac{3}{2} = \frac{3}{4}$$

## התשובה

$$\sum_{n=1}^{\infty} \frac{1}{n(n+2)} = \frac{3}{4}$$

## הכללה

באופן כללי, עבור $\frac{1}{n(n+k)}$:

$$\frac{1}{n(n+k)} = \frac{1}{k} \left( \frac{1}{n} - \frac{1}{n+k} \right)$$

והסכום יהיה:
$$\sum_{n=1}^{\infty} \frac{1}{n(n+k)} = \frac{1}{k} \left( 1 + \frac{1}{2} + \ldots + \frac{1}{k} \right) = \frac{H_k}{k}$$

כאשר $H_k = \sum_{j=1}^{k} \frac{1}{j}$ הוא המספר ההרמוני ה-$k$.

## תלויות

**דורש:** [[Def - טור טלסקופי]], [[Def - גבול של סדרה]]
**משמש ב:** חישוב סכומי טורים
