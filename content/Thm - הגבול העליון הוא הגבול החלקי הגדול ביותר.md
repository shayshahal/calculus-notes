# משפט: הגבול העליון הוא הגבול החלקי הגדול ביותר

## ניסוח

תהי $(a_n)$ [[Def - סדרה|סדרה]]. אז:

1. $\limsup_{n \to \infty} a_n$ הוא [[Def - גבול חלקי|גבול חלקי]] של $(a_n)$
2. $\limsup_{n \to \infty} a_n$ הוא **הגבול החלקי הגדול ביותר** של $(a_n)$

באופן דומה:
1. $\liminf_{n \to \infty} a_n$ הוא גבול חלקי של $(a_n)$
2. $\liminf_{n \to \infty} a_n$ הוא **הגבול החלקי הקטן ביותר** של $(a_n)$

## הוכחה עבור limsup

נסמן $L = \limsup_{n \to \infty} a_n$.

### מקרה 1: $L = +\infty$

אם $L = +\infty$ אז $(a_n)$ לא חסומה מלמעלה. במקרה זה $+\infty$ הוא גבול חלקי, והוא בוודאי הגדול ביותר.

### מקרה 2: $L = -\infty$

אם $L = -\infty$ אז $a_n \xrightarrow{n \to \infty} -\infty$. במקרה זה $-\infty$ הוא הגבול החלקי היחיד, ובפרט הגדול ביותר.

### מקרה 3: $L \in \mathbb{R}$

**נראה ש-$L$ גבול חלקי:**

צריך להראות:
$$\forall (\varepsilon > 0) \forall (N_0 \in \mathbb{N}) \exists (n \geq N_0) [|a_n - L| < \varepsilon]$$

יהיו $\varepsilon > 0$ ו-$N_0 \in \mathbb{N}$.

לפי [[Thm - אפיון גבול עליון|תנאי 1 מהאפיון]]:
$$\exists (N_1 \in \mathbb{N}) \forall (n \geq N_1) [a_n < L + \varepsilon]$$

בנוסף, לפי תנאי 2 מהאפיון, יש $n \geq \max\{N_0, N_1\}$ המקיים $a_n > L - \varepsilon$.

אז $n$ אינדקס המקיים $n \geq N_0$ וגם:
$$L - \varepsilon < a_n \underset{\text{כי } n \geq N_1}{<} L + \varepsilon$$

כלומר $|a_n - L| < \varepsilon$.

**נראה ש-$L$ הגדול ביותר:**

יהי $L' > L$. נראה ש-$L'$ **אינו** גבול חלקי.

נבחר $\varepsilon > 0$ מספיק קטן עבורו $L + \varepsilon < L'$.

לפי תנאי 1 מהאפיון:
$$\exists (N_0 \in \mathbb{N}) \forall (n \geq N_0) [a_n < L + \varepsilon]$$

לכן לכל $n \geq N_0$ מתקיים $a_n < L + \varepsilon < L'$.

מכאן, לכל גבול חלקי $\ell$ מתקיים $\ell \leq L + \varepsilon < L'$, ובפרט $L'$ אינו גבול חלקי.

$\blacksquare$

## הערות

1. המשפט נותן הוכחה נוספת ל[[Thm - בולצאנו-ויירשטראס|משפט בולצאנו-ויירשטראס]]: אם $(a_n)$ חסומה אז $\limsup a_n \in \mathbb{R}$ והוא גבול חלקי, כלומר קיימת תת-סדרה מתכנסת.

2. לכל סדרה יש limsup ו-liminf (במובן הרחב).

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול תחתון]], [[Def - גבול חלקי]], [[Thm - אפיון גבול עליון]]
**משמש ב:** [[Thm - שקילות התכנסות וגבול חלקי יחיד]], [[Thm - בולצאנו-ויירשטראס]]
