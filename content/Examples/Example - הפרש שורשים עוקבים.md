# דוגמה: הפרש שורשים עוקבים

## תרגיל

תנו דוגמא לסדרה $\{a_n\}_{n=1}^{\infty}$ אשר מקיימת:
$$\lim_{n \to \infty}(a_{n+1} - a_n) = 0$$
אך לא קיים גבול סופי ל-$a_n$.

## פתרון

**נטען כי** $a_n = \sqrt{n}$ מקיימת זאת.

### חלק 1: הסדרה לא חסומה

$\sqrt{n}$ לא חסומה (מכיוון שלכל $k \in \mathbb{N}$ ניתן לקחת את $n = k^2 \in \mathbb{N}$, ואז $a_n = k$).

### חלק 2: הפרש שואף לאפס

נטען כי:
$$\lim_{n \to \infty} \sqrt{n+1} - \sqrt{n} = 0$$

**הוכחה:** יהי $\varepsilon > 0$. נעריך את הביטוי על ידי כפל בצמוד:

$$\left|\sqrt{n+1} - \sqrt{n} - 0\right| = \left|\frac{(\sqrt{n+1} - \sqrt{n})(\sqrt{n+1} + \sqrt{n})}{\sqrt{n+1} + \sqrt{n}}\right|$$
$$= \left|\frac{(n+1) - n}{\sqrt{n+1} + \sqrt{n}}\right| = \left|\frac{1}{\sqrt{n+1} + \sqrt{n}}\right| \leq \frac{1}{\sqrt{n}}$$

נבדוק מתי מתקיים:
$$\frac{1}{\sqrt{n}} < \varepsilon \quad \Leftrightarrow \quad \frac{1}{\varepsilon^2} < n$$

אז נבחר את $N := \left\lfloor \frac{1}{\varepsilon^2} \right\rfloor + 1$ ואז לכל $n > N$ מתקיים:
$$\left|\sqrt{n+1} - \sqrt{n} - 0\right| < \varepsilon$$

ו-$0$ הוא אכן הגבול.

## מסקנה

> [!warning] שימו לב
> העובדה ש-$a_{n+1} - a_n \to 0$ **אינה מבטיחה** שהסדרה מתכנסת!

זו דוגמה נגדית חשובה שמראה שתנאי זה הוא **הכרחי** אבל **לא מספיק** להתכנסות.

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Def - סדרה מתכנסת]], [[Def - סדרה חסומה]], [[Method - הוכחת גבול מההגדרה]]
**משמש ב:** [[Thm - סדרה מתכנסת היא חסומה]]
