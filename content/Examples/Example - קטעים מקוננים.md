# דוגמה: קטעים מקוננים

## הבעיה

לכל $n \in \mathbb{N}$ יהיו $a_n, b_n \in \mathbb{R}$ כך ש:
- $a_n < b_n$
- $a_n \leq a_{n+1}$ (סדרת הקצוות השמאליים עולה)
- $b_{n+1} \leq b_n$ (סדרת הקצוות הימניים יורדת)

נביט באוסף הקטעים $I_n = [a_n, b_n] \subseteq \mathbb{R}$.

**הוכיחו:**

א. קיימים $\alpha = \sup\{a_n : n \in \mathbb{N}\}$ ו-$\beta = \inf\{b_n : n \in \mathbb{N}\}$ וכן הוכיחו שמתקיים:

$$\bigcap_{n \in \mathbb{N}} I_n = [\alpha, \beta]$$

---

## פתרון

### שלב 1: קיום $\alpha$ ו-$\beta$

**קיום $\alpha$:**

ראשית, נשים לב שהקבוצה $\{a_n : n \in \mathbb{N}\}$ אכן חסומה מלעיל, למשל על ידי $b_1$.

**הוכחה:** לכל $n \in \mathbb{N}$, מכיוון ש-$a_n \leq a_{n+1} \leq \cdots$ וכן $a_n < b_n$, נקבל (באינדוקציה) כי לכל $k \geq n$ מתקיים $a_k \leq b_n$.

בפרט, עבור $n = 1$: לכל $n$ מתקיים $a_n \leq b_1$.

לכן לפי אקסיומת השלמות, קיים:
$$\alpha = \sup\{a_n : n \in \mathbb{N}\}$$

**קיום $\beta$:**

באופן דומה, $\{b_n : n \in \mathbb{N}\}$ חסומה מלרע, למשל על ידי $a_1$.

לכן קיים:
$$\beta = \inf\{b_n : n \in \mathbb{N}\}$$

---

### שלב 2: הוכחה ש-$\alpha \leq \beta$

נניח בשלילה כי $\alpha > \beta$.

אז בפרט קיים $k \in \mathbb{N}$ כך ש-$a_k > \beta$. (אם לא, אז $\beta$ חסם מלעיל ל-$\{a_n\}$ סתירה להגדרת $\alpha$).

ובאותו אופן קיים $m \in \mathbb{N}$ כך ש-$b_m < \alpha$.

**מקרה 1:** $m = k$. אז $a_k > \beta \geq b_k$ (כי $\beta$ חסם מלרע), בסתירה לכך ש-$a_k < b_k$.

**מקרה 2:** $m < k$. אז:
$$b_m \geq b_{m+1} \geq \cdots \geq b_k > a_k$$

(המעבר האחרון מכך ש-$a_k < b_k$).

אבל קיבלנו $b_m < \alpha$ ומצד שני $b_m > a_k$, כלומר $a_k < b_m < \alpha$.

אבל $\alpha = \sup\{a_n\}$ ולכן $a_k \leq \alpha$, ואם $b_m < \alpha$ אז $b_m$ לא יכול להיות גדול מ-$a_k$ ועדיין קטן מ-$\alpha$. סתירה!

**מקרה 3:** $m > k$ דומה.

**מסקנה:** $\alpha \leq \beta$.

---

### שלב 3: הוכחה ש-$[\alpha, \beta] \subseteq \bigcap_{n \in \mathbb{N}} I_n$

יהי $x \in [\alpha, \beta]$, כלומר $\alpha \leq x \leq \beta$.

לכל $n \in \mathbb{N}$ נקבל $a_n \leq \alpha$ ו-$\beta \leq b_n$ (מהגדרת sup ו-inf).

לכן:
$$a_n \leq \alpha \leq x \leq \beta \leq b_n$$

כלומר $x \in [a_n, b_n] = I_n$ לכל $n \in \mathbb{N}$.

לכן $x \in \bigcap_{n \in \mathbb{N}} I_n$.

---

### שלב 4: הוכחה ש-$\bigcap_{n \in \mathbb{N}} I_n \subseteq [\alpha, \beta]$

יהי $x \in \bigcap_{n \in \mathbb{N}} I_n$.

אז לכל $n \in \mathbb{N}$ נקבל ש-$x \in [a_n, b_n]$, ובפרט $a_n \leq x \leq b_n$.

כלומר $x$ חסם מלעיל של $\{a_n : n \in \mathbb{N}\}$ ו-$x$ חסם מלרע של $\{b_n : n \in \mathbb{N}\}$.

לכן:
$$\alpha = \sup\{a_n\} \leq x$$
$$\beta = \inf\{b_n\} \geq x$$

כלומר $\alpha \leq x \leq \beta$, ולכן $x \in [\alpha, \beta]$.

---

### מסקנה

קיבלנו את השוויון:
$$\bigcap_{n \in \mathbb{N}} I_n = [\alpha, \beta]$$

כרצוי.

---

## משמעות: למת קנטור (Cantor's Intersection Theorem)

משפט זה הוא בסיס ל**למת הקטעים המקוננים של קנטור**, ומראה ששדה הממשיים "שלם" - חיתוך של קטעים מקוננים אינו ריק!

**הערה:** עבור קטעים **פתוחים** זה לא נכון! למשל:
$$\bigcap_{n=1}^{\infty} \left(0, \frac{1}{n}\right) = \emptyset$$

---

## תלויות

**דורש:** [[Def - חסם עליון (סופרמום)]], [[Def - חסם תחתון (אינפימום)]], [[Thm - אקסיומת השלמות]], [[Method - מציאת חסם עליון ותחתון]]
**משמש ב:** [[Lemma - קנטור על קטעים מקוננים]], הוכחות על רציפות, [[Thm - בולצאנו-ויירשטראס]]
