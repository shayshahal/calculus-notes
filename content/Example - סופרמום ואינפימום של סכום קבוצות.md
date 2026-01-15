# דוגמה: סופרמום ואינפימום של סכום קבוצות

## הבעיה

יהיו $A, B \subseteq \mathbb{R}$ קבוצות לא ריקות וחסומות מלעיל. הוכיחו כי $A + B$ חסומה מלעיל ומתקיים:

$$\sup(A + B) = \sup A + \sup B$$

---

## פתרון

**נשתמש בסימונים:**
- $\alpha = \sup A$
- $\beta = \sup B$
- $\gamma = \sup(A + B)$

**נוכיח:** $\gamma = \alpha + \beta$.

---

### שלב 1: הוכחה ש-$\gamma$ קיים (חסימות)

יהי $c \in A + B$. אז $c = a + b$ עבור $a \in A, b \in B$ מתאימים.

מהגדרת הסופרמום ומתקיים $a \leq \alpha$ ו-$b \leq \beta$.

לכן:
$$c = a + b \leq \alpha + \beta$$

לכן $\alpha + \beta$ חסם מלעיל של $A + B$, ובפרט $A + B$ חסומה מלעיל.

מאקסיומת השלמות, קיים $\gamma = \sup(A + B)$.

---

### שלב 2: הוכחה ש-$\gamma \leq \alpha + \beta$

מהשלב הקודם, $\alpha + \beta$ הוא חסם מלעיל של $A + B$.

לפי הגדרת הסופרמום (החסם המלעיל המינימלי), מתקיים $\gamma \leq \alpha + \beta$.

---

### שלב 3: הוכחה ש-$\gamma \geq \alpha + \beta$

**נשתמש בהגדרה השקולה עם אפסילון:**

עלינו להראות כי לכל $\varepsilon > 0$ קיים $c \in A + B$ כך ש-$c > \gamma - \varepsilon$.

אכן, עבור $\varepsilon > 0$ כלשהו, קיימים:
- $a \in A$ כך ש-$a > \alpha - \frac{\varepsilon}{2}$ (מהגדרת $\sup A$)
- $b \in B$ כך ש-$b > \beta - \frac{\varepsilon}{2}$ (מהגדרת $\sup B$)

נסמן $c = a + b \in A + B$.

מהאי-שוויונים לעיל מתקיים:

$$c = a + b > \alpha - \frac{\varepsilon}{2} + \beta - \frac{\varepsilon}{2} = \alpha + \beta - \varepsilon$$

**טריק:** רצינו להראות ש-$c > \gamma - \varepsilon$, והראנו ש-$c > \alpha + \beta - \varepsilon$.

זה מוכיח שאם $\gamma < \alpha + \beta$ אז $\gamma$ אינו חסם מלעיל מינימלי. לכן $\gamma \geq \alpha + \beta$.

---

### מסקנה

קיבלנו $\gamma \leq \alpha + \beta$ וגם $\gamma \geq \alpha + \beta$, לכן:

$$\sup(A + B) = \sup A + \sup B$$

כנדרש.

---

## טכניקה חשובה: חלוקת $\varepsilon$

שימו לב שחילקנו את $\varepsilon$ ל-$\frac{\varepsilon}{2}$ עבור כל אחד מהסופרמומים. זוהי טכניקה סטנדרטית:

- עבור סכום של 2 איברים: חלק ל-$\frac{\varepsilon}{2}$
- עבור סכום של $n$ איברים: חלק ל-$\frac{\varepsilon}{n}$

---

## תרגיל נוסף

**מצאו $\sup S$ ו-$\inf S$ עבור:**

$$S = \left\{\frac{1}{n} - \frac{1}{m} : n, m \in \mathbb{N} \setminus \{0\}\right\}$$

**פתרון:**

נגדיר:
$$N = \left\{\frac{1}{n} : n \in \mathbb{N} \setminus \{0\}\right\}, \quad M = \left\{\frac{1}{m} : m \in \mathbb{N} \setminus \{0\}\right\}$$

אז:
$$S = N + (-M)$$

מתרגיל קודם: $\sup N = 1, \inf N = 0, \sup M = 1, \inf M = 0$.

לכן:
$$\sup(-M) = -\inf M = 0$$
$$\inf(-M) = -\sup M = -1$$

ולכן:
$$\sup S = \sup N + \sup(-M) = 1 + 0 = 1$$
$$\inf S = \inf N + \inf(-M) = 0 + (-1) = -1$$

---

## תלויות

**דורש:** [[Tool - חיבור קבוצות]], [[Method - הוכחת שוויון באמצעות חסמים]], [[Def - חסם עליון (סופרמום)]], [[Thm - אקסיומת השלמות]]
**משמש ב:** הוכחות על סכומי סדרות, אי-שוויונות מתקדמות
