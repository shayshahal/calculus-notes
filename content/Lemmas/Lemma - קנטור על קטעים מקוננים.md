# למה: קנטור על קטעים מקוננים

## ניסוח

יהיו $(a_n)_{n=1}^{\infty}$, $(b_n)_{n=1}^{\infty}$ סדרות, כך שלכל $n$ מתקיים $a_n \leq b_n$.

נניח כי מתקיים:
$$[a_1, b_1] \supseteq [a_2, b_2] \supseteq [a_3, b_3] \supseteq \cdots$$

ובאופן כללי:
$$[a_{n+1}, b_{n+1}] \subseteq [a_n, b_n]$$

בנוסף, נניח $b_n - a_n \xrightarrow{n \to \infty} 0$.

**אז:** קיימת ויחידה נקודה $c \in \mathbb{R}$ השייכת לכל הקטעים $[a_n, b_n]$.

יתר על כן מתקיים:
$$c = \lim_{n \to \infty} a_n = \lim_{n \to \infty} b_n$$

## הוכחה

**שלב 1: מונוטוניות**

נטען כי $(a_n)$ עולה ו-$(b_n)$ יורדת.

אכן, יהי $n \in \mathbb{N}$. מתקיים:
$$[a_{n+1}, b_{n+1}] \subseteq [a_n, b_n]$$

ובפרט $a_{n+1}, b_{n+1} \in [a_n, b_n]$.

מכאן $a_{n+1} \geq a_n$ ו-$b_{n+1} \leq b_n$.

**שלב 2: חסימות**

בנוסף, לכל $n \in \mathbb{N}$ מתקיים:
$$a_n \leq b_n \underset{b_n \text{ יורדת}}{\leq} b_1$$

אז $(a_n)$ חסומה מלמעלה ע"י $b_1$.

באופן דומה, לכל $n$:
$$\underset{a_n \text{ עולה}}{\geq} a_1 \leq a_n \leq b_n$$

ולכן $(b_n)$ חסומה מלמטה ע"י $a_1$.

**שלב 3: התכנסות**

קיבלנו כי $a_n$ עולה וחסומה מלמעלה, $b_n$ יורדת וחסומה מלמטה, ולכן הן מתכנסות.

נסמן $c = \lim_{n \to \infty} a_n$. נראה שגם $b_n \xrightarrow{n \to \infty} c$. ואכן:
$$b_n = a_n + (b_n - a_n) \xrightarrow{n \to \infty} c + 0 = c$$

**שלב 4: שייכות לכל הקטעים**

נראה שהנקודה $c$ היא הנקודה שחיפשנו, כלומר נראה שהיא שייכת לכל הקטעים.

יהי $k \in \mathbb{N}$ ונראה כי $c \in [a_k, b_k]$. מתקיים:
$$c = \lim_{n \to \infty} a_n \underset{a_n \text{ עולה}}{=} \sup_{n \in \mathbb{N}}(a_n) \geq a_k$$
$$c = \lim_{n \to \infty} b_n \underset{b_n \text{ יורדת}}{=} \inf_{n \in \mathbb{N}}(b_n) \leq b_k$$

קיבלנו כי:
$$a_k \leq c \leq b_k$$

כלומר $c \in [a_k, b_k]$. וזה נכון לכל $k$.

**שלב 5: יחידות**

תהי $d \in \mathbb{R}$ נקודה השייכת לכל הקטעים.

לכל $n \in \mathbb{N}$ מתקיים $d \in [a_n, b_n]$, כלומר לכל $n$: $a_n \leq d \leq b_n$.

אז $d$ בפרט חסם מלמעלה של $(a_n)$ ולכן:
$$c = \sup_{n \in \mathbb{N}}(a_n) \leq d$$

באופן דומה, $d$ חסם מלמטה של $(b_n)$, ולכן:
$$d \leq \inf_{n \in \mathbb{N}}(b_n) = c$$

אז $c \leq d$ וגם $d \leq c$. אז סה"כ $d = c$. $\blacksquare$

## הערה

הלמה לא נכונה אם נחליף את הקטעים הסגורים בקטעים פתוחים.

למשל, אין אף נקודה השייכת לכל הקטעים:
$$(0,1) \supseteq \left(0, \frac{1}{2}\right) \supseteq \left(0, \frac{1}{3}\right) \supseteq \cdots$$

אין אף $x$ עבורה:
$$\forall(n \in \mathbb{N}) \quad 0 < x < \frac{1}{n}$$

## תלויות

**דורש:** [[Def - סדרה מונוטונית]], [[Thm - סדרה מונוטונית וחסומה מתכנסת]], [[Def - חסם עליון (סופרמום)]], [[Def - חסם תחתון (אינפימום)]], [[Thm - אריתמטיקת גבולות]]

**משמש ב:** [[Thm - בולצאנו-ויירשטראס]], [[Example - קטעים מקוננים]]
