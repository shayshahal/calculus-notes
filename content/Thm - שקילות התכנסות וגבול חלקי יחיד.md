# משפט: שקילות התכנסות וגבול חלקי יחיד

## ניסוח

תהי $(a_n)$ [[Def - סדרה|סדרה]]. אז התנאים הבאים **שקולים**:

1. $(a_n)$ מתכנסת במובן הרחב
2. ל-$(a_n)$ יש [[Def - גבול חלקי|גבול חלקי]] יחיד
3. $\limsup_{n \to \infty} a_n = \liminf_{n \to \infty} a_n$

## הערה מקדימה

תמיד מתקיים:
$$\liminf_{n \to \infty} a_n \leq \limsup_{n \to \infty} a_n$$

## הוכחה

### $(1) \Rightarrow (2)$: התכנסות גוררת גבול חלקי יחיד

אם $a_n \xrightarrow{n \to \infty} L$ במובן רחב, אז כל [[Def - תת-סדרה|תת-סדרה]] שואפת ל-$L$.

בפרט, $L$ הוא הגבול החלקי היחיד.

### $(2) \Rightarrow (3)$: גבול חלקי יחיד גורר שוויון limsup ו-liminf

$\limsup a_n$ ו-$\liminf a_n$ הם שניהם גבולות חלקיים (לפי [[Thm - הגבול העליון הוא הגבול החלקי הגדול ביותר|המשפט הקודם]]).

לכן אם יש גבול חלקי יחיד, הם שווים.

### $(3) \Rightarrow (1)$: שוויון limsup ו-liminf גורר התכנסות

נסמן $L = \limsup_{n \to \infty} a_n = \liminf_{n \to \infty} a_n$.

**מקרה $L = -\infty$:**

בפרט $\limsup_{n \to \infty} a_n = -\infty$.

ראינו שזה גורר $a_n \xrightarrow{n \to \infty} -\infty$.

**מקרה $L = +\infty$:**

בפרט $\liminf_{n \to \infty} a_n = +\infty$.

ראינו שזה גורר $a_n \xrightarrow{n \to \infty} +\infty$.

**מקרה $L \in \mathbb{R}$:**

נראה כי $a_n \xrightarrow{n \to \infty} L$.

יהי $\varepsilon > 0$.

מכיוון ש-$\limsup_{n \to \infty} a_n = L$, לפי [[Thm - אפיון גבול עליון|תנאי 1 מהאפיון]]:
$$\exists (N_0 \in \mathbb{N}) \forall (n \geq N_0) [a_n < L + \varepsilon]$$

בנוסף, מכיוון ש-$\liminf_{n \to \infty} a_n = L$, לפי התנאי המקביל ל-liminf:
$$\exists (N_1 \in \mathbb{N}) \forall (n \geq N_1) [a_n > L - \varepsilon]$$

ואז לכל $n \geq \max\{N_0, N_1\}$ מתקיים:
$$L - \varepsilon < a_n < L + \varepsilon$$

כלומר $|a_n - L| < \varepsilon$.

$\blacksquare$

## דוגמאות

### דוגמה 1: סדרה מתכנסת

עבור $a_n = \frac{1}{n}$:
- $\limsup_{n \to \infty} a_n = \liminf_{n \to \infty} a_n = 0$
- גבול חלקי יחיד: $0$
- הסדרה מתכנסת ל-$0$

### דוגמה 2: סדרה לא מתכנסת

עבור $a_n = (-1)^n$:
- $\limsup_{n \to \infty} a_n = 1$
- $\liminf_{n \to \infty} a_n = -1$
- שני גבולות חלקיים: $1$ ו-$(-1)$
- הסדרה אינה מתכנסת

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול תחתון]], [[Def - גבול חלקי]], [[Thm - אפיון גבול עליון]], [[Thm - הגבול העליון הוא הגבול החלקי הגדול ביותר]]
**משמש ב:** [[Def - סדרה מתכנסת]]
