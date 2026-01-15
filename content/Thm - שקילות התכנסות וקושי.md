# משפט: שקילות התכנסות וקושי

## ניסוח

סדרה מתכנסת אם ורק אם היא סדרת קושי.

## תנאים

- הסדרה מעל $\mathbb{R}$ (הממשיים)

## הוכחה

### כיוון 1: מתכנסת $\Rightarrow$ קושי

נניח $a_n \xrightarrow{n \to \infty} L$. נראה שהיא סדרת קושי.

יהי $\epsilon > 0$. לפי הגדרת הגבול:

$$\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[|a_n - L| < \frac{\epsilon}{2}\right]$$

ואז לכל $m,n \geq n_0$ מתקיים:

$$|a_m - a_n| = |(a_m - L) + (L - a_n)| \underset{\text{אי-שוויון המשולש}}{\leq} |a_m - L| + |a_n - L| \underset{m,n \geq n_0}{<} \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

$\blacksquare$

### כיוון 2: קושי $\Rightarrow$ מתכנסת

נניח $(a_n)$ סדרת קושי. נראה כי מתכנסת.

לפי [[Lemma - סדרת קושי חסומה|הלמה]] $a_n$ חסומה. לפי [[Thm - בולצאנו-ויירשטראס|משפט בולצאנו-ויירשטראס]] יש ל-$a_n$ תת-סדרה מתכנסת $(a_{n_k})_{k=1}^{\infty}$. נסמן:

$$L = \lim_{k \to \infty} a_{n_k}$$

ומשום שלסדרה מתכנסת יש גבול חלקי יחיד, אז בהכרח אם $a_n$ מתכנסת היא מתכנסת ל-$L$.

נוכיח כי $a_n \to L$.

יהי $\epsilon > 0$.

מכיוון ש-$a_{n_k} \xrightarrow{k \to \infty} L$:

$$\exists(k_0 \in \mathbb{N})\forall(k \geq k_0)\left[|a_{n_k} - L| < \frac{\epsilon}{2}\right]$$

בנוסף $(a_n)$ סדרת קושי, ולכן:

$$\exists(n_0 \in \mathbb{N})\forall(m,n > n_0)\left[|a_m - a_n| < \frac{\epsilon}{2}\right]$$

נראה שלכל $n \geq n_0$ מתקיים $|a_n - L| < \epsilon$.

אכן, יהי $n \geq n_0$.

$n_k \xrightarrow{k \to \infty} \infty$ ולכן ניתן לבחור $k \geq k_0$ המקיים $n_k \geq n_0$.

עבור $k$ זה:

$$|a_n - L| = |a_n - a_{n_k} + a_{n_k} - L| \underset{\text{אי-שוויון המשולש}}{\leq} \underbrace{|a_n - a_{n_k}|}_{n,n_k \geq n_0 \text{ ולכן קטן מ-} \frac{\epsilon}{2}} + \underbrace{|a_{n_k} - L|}_{k \geq k_0 \text{ ולכן קטן מ-} \frac{\epsilon}{2}} \leq \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

$\blacksquare$

## הערות

- זהו מאפיין של שלמות הממשיים - לא מתקיים ברציונליים
- המשפט מאפשר להוכיח התכנסות בלי לדעת את הגבול

## תלויות

**דורש:** [[Def - סדרת קושי]], [[Def - סדרה מתכנסת]], [[Lemma - סדרת קושי חסומה]], [[Thm - בולצאנו-ויירשטראס]], [[Thm - אי-שוויון המשולש]]
**משמש ב:** [[Thm - קריטריון קושי לטורים]], [[Example - סכום ריבועים הופכיים מתכנס]]
