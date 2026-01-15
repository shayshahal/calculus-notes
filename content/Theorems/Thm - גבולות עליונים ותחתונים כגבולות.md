# משפט: גבולות עליונים ותחתונים כגבולות

## ניסוח

תהי $\{a_n\}_{n=1}^{\infty}$ [[Def - סדרה חסומה|סדרה חסומה]]. נגדיר:
$$u_n = \sup\{a_k : k \geq n\}$$
$$\ell_n = \inf\{a_k : k \geq n\}$$

אז:
$$\limsup_{n \to \infty} a_n = \lim_{n \to \infty} u_n$$
$$\liminf_{n \to \infty} a_n = \lim_{n \to \infty} \ell_n$$

## הוכחה עבור lim sup

### שלב 1: הסדרה $(u_n)$ יורדת

יהי $n \in \mathbb{N}$. מתקיים:
$$\{a_k : k \geq n+1\} \subseteq \{a_k : k \geq n\}$$

על כן:
$$u_{n+1} = \sup\{a_k : k \geq n+1\} \leq \sup\{a_k : k \geq n\} = u_n$$

### שלב 2: הסדרה $(u_n)$ חסומה מלרע

$(a_n)$ חסומה, לכן חסומה מלרע. יהי $m \in \mathbb{R}$ כך שלכל $n \in \mathbb{N}$ מתקיים $a_n \geq m$.

לכל $k \geq n$ מתקיים $a_k \geq m$, על כן $u_n = \sup\{a_k : k \geq n\} \geq m$.

### שלב 3: קיום הגבול

$(u_n)$ יורדת וחסומה מלרע, על כן מתכנסת. נסמן $L = \lim_{n \to \infty} u_n$.

### שלב 4: הוכחה ש-$L = \limsup a_n$

**(א)** יהי $\varepsilon > 0$.

כיוון ש-$u_n \to L$, קיים $N \in \mathbb{N}$ כך שלכל $n \geq N$ מתקיים $|u_n - L| < \frac{\varepsilon}{2}$, ובפרט $u_N < L + \frac{\varepsilon}{2}$.

לכל $n \geq N$ מתקיים:
$$a_n \leq u_N < L + \frac{\varepsilon}{2} < L + \varepsilon$$

**(ב)** יהי $\varepsilon > 0$ ויהי $N \in \mathbb{N}$.

מתכונת הסופרמום, קיים $k \geq N$ כך ש-$a_k > u_N - \frac{\varepsilon}{2}$.

כמו כן:
$$u_N - L \leq |u_N - L| < \varepsilon$$
ולכן $u_N < L + \varepsilon$, וגם $u_N > L - \frac{\varepsilon}{2}$ (כי $(u_n)$ יורדת ל-$L$).

על כן:
$$a_k > u_N - \frac{\varepsilon}{2} > L - \frac{\varepsilon}{2} - \frac{\varepsilon}{2} = L - \varepsilon$$

לכן לפי [[Thm - אפיון גבול עליון|משפט האפיון]], $L = \limsup_{n \to \infty} a_n$.

## הוכחה עבור lim inf

ההוכחה דומה:
- $({\ell_n})$ עולה (כי מקטינים את קבוצת האיברים)
- $(\ell_n)$ חסומה מלעיל
- לכן מתכנסת לגבול שהוא lim inf

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול תחתון]], [[Def - חסם עליון (סופרמום)]], [[Def - חסם תחתון (אינפימום)]], [[Thm - סדרה מונוטונית וחסומה מתכנסת]]
**משמש ב:** [[Thm - תכונות גבול עליון]], [[Thm - אפיון גבול עליון]]
