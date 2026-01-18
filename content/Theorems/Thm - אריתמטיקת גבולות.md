# משפט: אריתמטיקת גבולות

## ניסוח

תהיינה $(a_n)$, $(b_n)$ סדרות כך ש-$a_n \to a$ ו-$b_n \to b$ (כאשר $a, b \neq \pm\infty$). אז:

1. **חיבור/חיסור:** $(a_n \pm b_n) \to a \pm b$

2. **כפל:** $(a_n \cdot b_n) \to a \cdot b$

3. **חילוק:** אם $b \neq 0$ ו-$b_n \neq 0$ אז $\frac{a_n}{b_n} \to \frac{a}{b}$

## תנאים

- שתי הסדרות מתכנסות לגבולות סופיים
- לחילוק: הגבול $b$ אינו אפס, והאיברים $b_n$ אינם אפס

## הוכחה

### 1. חיבור: $(a_n + b_n) \to A + B$

יהי $\varepsilon > 0$. לכל $n$:

$$|(a_n + b_n) - (A + B)| = |(a_n - A) + (b_n - B)| \underset{\text{אי-שוויון המשולש}}{\leq} |a_n - A| + |b_n - B|$$

$a_n \to A$ ולכן:
$$\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[|a_n - A| < \frac{\varepsilon}{2}\right]$$

$b_n \to B$ ולכן:
$$\exists(n_1 \in \mathbb{N})\forall(n \geq n_1)\left[|b_n - B| < \frac{\varepsilon}{2}\right]$$

נסמן $n_2 = \max\{n_0, n_1\}$. לכל $n \geq n_2$:

$$|(a_n + b_n) - (A + B)| \leq |a_n - A| + |b_n - B| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon$$

$\blacksquare$

### 2. כפל: $(a_n \cdot b_n) \to A \cdot B$

יהי $\varepsilon > 0$. לכל $n$:

$$|a_n b_n - AB| = |a_n b_n - a_n B + a_n B - AB| = |a_n(b_n - B) + B(a_n - A)|$$
$$\underset{\text{אי-שוויון המשולש}}{\leq} |a_n| \cdot |b_n - B| + |B| \cdot |a_n - A|$$

$a_n$ מתכנסת, ולכן [[Thm - סדרה מתכנסת היא חסומה|חסומה]]:
$$\exists(M > 0)\forall(n \in \mathbb{N})[|a_n| \leq M]$$

נסמן $M_0 = \max\{M, |B|\}$.

$a_n \to A$ ולכן:
$$\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[|a_n - A| < \frac{\varepsilon}{2M_0}\right]$$

$b_n \to B$ ולכן:
$$\exists(n_1 \in \mathbb{N})\forall(n \geq n_1)\left[|b_n - B| < \frac{\varepsilon}{2M_0}\right]$$

נסמן $n_2 = \max\{n_0, n_1\}$. לכל $n \geq n_2$:

$$|a_n b_n - AB| \leq \underbrace{|a_n|}_{\leq M \leq M_0} \cdot |b_n - B| + \underbrace{|B|}_{\leq M_0} \cdot |a_n - A| \leq M_0|b_n - B| + M_0|a_n - A| < \frac{M_0 \varepsilon}{2M_0} + \frac{M_0 \varepsilon}{2M_0} = \varepsilon$$

$\blacksquare$

### 3. חילוק: $\frac{a_n}{b_n} \to \frac{A}{B}$ (כאשר $B \neq 0$)

מספיק להוכיח כי $\frac{1}{b_n} \to \frac{1}{B}$, ואז נקבל:
$$\frac{a_n}{b_n} = a_n \cdot \frac{1}{b_n} \underset{\text{לפי סעיף 2}}{\longrightarrow} A \cdot \frac{1}{B} = \frac{A}{B}$$

**נוכיח $\frac{1}{b_n} \to \frac{1}{B}$:**

יהי $\varepsilon > 0$. לכל $n$:
$$\left|\frac{1}{b_n} - \frac{1}{B}\right| = \left|\frac{B - b_n}{b_n B}\right| = \frac{|b_n - B|}{|b_n||B|}$$

**מציאת חסם תחתון ל-$|b_n|$:**

מכיוון ש-$|B| > 0$ ו-$b_n \to B$, גם $|b_n| \to |B|$. לכן:
$$\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[||b_n| - |B|| < \frac{|B|}{2}\right]$$

ואז לכל $n \geq n_0$ מתקיים:
$$\frac{|B|}{2} = |B| - \frac{|B|}{2} < |b_n| < |B| + \frac{|B|}{2}$$

ואז לכל $n \geq n_0$:
$$\left|\frac{1}{b_n} - \frac{1}{B}\right| = \frac{|b_n - B|}{|b_n||B|} \leq \frac{|b_n - B|}{\frac{|B|}{2}|B|} = |b_n - B| \cdot \frac{2}{|B|^2}$$

$b_n \to B$ ולכן:
$$\exists(n_1 \in \mathbb{N})\forall(n \geq n_1)\left[|b_n - B| < \varepsilon \cdot \frac{|B|^2}{2}\right]$$

נסמן $n_2 = \max\{n_0, n_1\}$. לכל $n \geq n_2$:
$$\left|\frac{1}{b_n} - \frac{1}{B}\right| \underset{n \geq n_0}{\leq} |b_n - B| \cdot \frac{2}{|B|^2} \leq \varepsilon \cdot \frac{|B|^2}{2} \cdot \frac{2}{|B|^2} = \varepsilon$$

$\blacksquare$

## הערות

ניתן לנסח טענה דומה עבור גבולות אינסופיים (אם כי לא לכל המקרים).

למשל:
- אם $a_n \to \infty$ ו-$b_n \to L > 0$ אז $a_n \cdot b_n \to \infty$
- אם $a_n \to \infty$ ו-$b_n \to \infty$ אז $a_n + b_n \to \infty$

**מקרים לא מוגדרים** (ביטויים אי-קבועים):
- $\infty - \infty$
- $0 \cdot \infty$
- $\frac{\infty}{\infty}$
- $\frac{0}{0}$

## שימושים

המשפט מאפשר לחשב גבולות של ביטויים מורכבים על ידי פירוק לחלקים פשוטים יותר.

## דוגמה

$$\lim_{n \to \infty} \frac{n^7 - n^5 + 4}{3n^7 - 20n + 2} = \lim_{n \to \infty} \frac{1 - \frac{1}{n^2} + \frac{4}{n^7}}{3 - \frac{20}{n^6} + \frac{2}{n^7}} = \frac{1 - 0 + 0}{3 - 0 + 0} = \frac{1}{3}$$

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Def - סדרה מתכנסת]], [[Thm - סדרה מתכנסת היא חסומה]]
**משמש ב:** [[Tool - גבולות בסיסיים של סדרות]], [[Thm - משפט צ'זארו]], [[Thm - התכנסות ממוצע הנדסי]]
