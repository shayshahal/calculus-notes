# משפט: אפיון גבול עליון

## ניסוח

מספר $L \in \mathbb{R}$ הינו [[Def - גבול עליון|הגבול העליון]] של [[Def - סדרה|סדרה]] $(a_n)$ אם ורק אם מתקיימים שני התנאים:

1. לכל $\varepsilon > 0$ קיים $N \in \mathbb{N}$ כך שלכל $n \geq N$ מתקיים $a_n < L + \varepsilon$

2. לכל $\varepsilon > 0$ ולכל $N \in \mathbb{N}$ קיים $n \geq N$ כך ש-$a_n > L - \varepsilon$

## הסבר

- **תנאי 1:** מהמקום מסוים, כל האיברים קטנים מ-$L + \varepsilon$ (כלומר, $L$ הוא "כמעט חסם עליון")
- **תנאי 2:** יש אינסוף איברים גדולים מ-$L - \varepsilon$ (כלומר, אי אפשר להקטין את $L$)

## הוכחה

### כיוון ראשון: התנאים מתקיימים $\Rightarrow$ $L$ הוא הגבול העליון

**נוכיח ש-$\limsup_{n \to \infty} a_n \leq L$:**

יהי $\varepsilon > 0$. מתנאי 1 קיים $N \in \mathbb{N}$ כך שלכל $n \geq N$ מתקיים $a_n < L + \varepsilon$.

לכן מ[[Thm - תכונות גבול עליון|תכונות הגבול העליון]] (סעיף 1א): $\limsup_{n \to \infty} a_n \leq L + \varepsilon$.

זה נכון לכל $\varepsilon > 0$, ולכן $\limsup_{n \to \infty} a_n \leq L$.

**נוכיח ש-$L$ הוא [[Def - גבול חלקי|גבול חלקי]] של $(a_n)$:**

יהיו $\varepsilon > 0$ ו-$N_1 \in \mathbb{N}$.

מתנאי 1 קיים $N_2 \in \mathbb{N}$ כך שלכל $n > N_2$ מתקיים $a_n < L + \varepsilon$.

נסמן $N = \max\{N_1, N_2\} + 1$. לפי תנאי 2 קיים $n > N$ כך ש-$a_n > L - \varepsilon$, ולכן $a_n < L + \varepsilon$.

משמע, לכל $\varepsilon > 0$ ו-$N_1 \in \mathbb{N}$ קיים $n > N_1$ כך ש-$|a_n - L| < \varepsilon$, ולכן $L$ גבול חלקי.

מכיוון ש-$L \geq \limsup a_n$ וכפי שראינו $\limsup a_n \leq L$, נקבל $L = \limsup_{n \to \infty} a_n$.

### כיוון שני: $L = \limsup a_n$ $\Rightarrow$ התנאים מתקיימים

**נראה כי תנאי 1 מתקיים:**

נניח בשלילה כי קיים $\varepsilon > 0$ כך שלכל $N \in \mathbb{N}$ קיים $n > N$ המקיים $a_n \geq L + \varepsilon$.

כלומר, יש [[Def - תת-סדרה|תת-סדרה]] $(a_{n_k})$ המקיימת $a_{n_k} \geq L + \varepsilon$.

לפי [[Thm - בולצאנו-ויירשטראס|בולצאנו-ויירשטראס]] קיים לסדרה גבול חלקי $\ell$. משום שאי-שוויון חלש נשמר בגבול: $\ell \geq L + \varepsilon > L$.

אבל $\ell$ גם גבול חלקי של $(a_n)$, בסתירה למקסימליות של $L$.

**נראה כי תנאי 2 מתקיים:**

היות ו-$L$ הוא גבול חלקי, לכל $\varepsilon > 0$ ולכל $N \in \mathbb{N}$ קיים $n > N$ עבורו $|a_n - L| < \varepsilon$.

בפרט $a_n > L - \varepsilon$.

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול חלקי]], [[Thm - תכונות גבול עליון]], [[Thm - בולצאנו-ויירשטראס]]
**משמש ב:** [[Thm - השוואת גבולות עליונים ותחתונים]], [[Method - חישוב גבולות עליונים ותחתונים]]
