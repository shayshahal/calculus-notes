# דוגמה: נגזרת של $(\sin x)^{\cos x}$

## הפונקציה

$$f(x) = (\sin x)^{\cos x}, \quad x \in (0, \pi)$$

## רעיון

בתחום $(0, \pi)$ מתקיים $\sin x > 0$.

נשתמש בזהות $a^b = e^{b \ln a}$ לכל $a > 0$:

$$(\sin x)^{\cos x} = \exp(\cos x \cdot \ln(\sin x))$$

## חישוב הנגזרת

נגזור לפי כלל השרשרת:

$$\left((\sin x)^{\cos x}\right)' = \exp(\cos x \cdot \ln(\sin x)) \cdot (\cos x \cdot \ln(\sin x))'$$

נחשב את הנגזרת הפנימית:
$$(\cos x \cdot \ln(\sin x))' = -\sin x \cdot \ln(\sin x) + \cos x \cdot \frac{\cos x}{\sin x}$$

$$= -\sin x \cdot \ln(\sin x) + \frac{\cos^2 x}{\sin x}$$

## התוצאה

$$f'(x) = (\sin x)^{\cos x} \cdot \left(-\sin x \cdot \ln(\sin x) + \frac{\cos^2 x}{\sin x}\right)$$

## הערה

זו דוגמה ל**גזירה לוגריתמית** - כאשר יש חזקה שתלויה ב-$x$ גם בבסיס וגם במעריך, נוח לכתוב את הפונקציה בצורת אקספוננט ואז לגזור.

## תלויות

**דורש:** [[Thm - כלל השרשרת]], [[Thm - כללי גזירה]], [[Tool - נגזרות של פונקציות יסודיות]]

**משמש ב:** —
