# משפט: השוואת גבולות עליונים ותחתונים (משפט 7.1)

## ניסוח

תהיינה $a_n, b_n$ סדרות. נסמן:

$$a = \liminf_{n \to \infty} a_n, \quad A = \limsup_{n \to \infty} a_n$$
$$b = \liminf_{n \to \infty} b_n, \quad B = \limsup_{n \to \infty} b_n$$

אז אם החל ממקום מסוים $a_n \leq b_n$, מתקיים:

$$A \leq B \quad \text{וגם} \quad a \leq b$$

## תנאים

- $a_n \leq b_n$ לכל $n \geq N_0$ עבור $N_0$ כלשהו

## הוכחה

**מקרה $B = \infty$:** הטענה ברורה כי $A \leq \infty$.

**מקרה $B = -\infty$:** אז $b_n \to -\infty$ וממשפט הסנדוויץ' נובע כי גם $a_n \to -\infty$, ולכן $A = B = -\infty$.

**מקרה $A, B$ סופיים:** כעת נפנה למקרה שבו $A, B$ סופיים (כלומר הסדרות חסומות מלעיל).

יהי $\varepsilon > 0$. קיים $N_1 \in \mathbb{N}$ כך שלכל $n \geq N_1$ מתקיים $b_n < B + \varepsilon$.

כמו כן, קיים $N_2 \in \mathbb{N}$ כך שלכל $n \geq N_2$ מתקיים $a_n \leq b_n$.

נבחר $N = \max\{N_1, N_2\} + 1$. אז לכל $n \geq N$ מתקיים $a_n < B + \varepsilon$ ולכן מתכונות הגבול העליון $A \leq B + \varepsilon$.

כלומר, לכל $\varepsilon > 0$ מתקיים $A \leq B + \varepsilon$ ולכן $A \leq B$.

ההוכחה עבור $a \leq b$ דומה.

## הערה חשובה

**הערה 8.1:** אי אפשר להסיק ש-$A \leq b$ כי עבור $a_n = b_n$ סדרה לא מתכנסת, בהכרח $A = B > b$.

## תרגיל נלווה

אם $a_n, b_n$ סדרות של מספרים אי-שליליים, אזי מתקיים:

$$a \cdot b \stackrel{(i)}{\leq} \liminf_{n \to \infty}(a_n \cdot b_n) \stackrel{(ii)}{\leq} a \cdot B \stackrel{(iii)}{\leq} \limsup_{n \to \infty}(a_n \cdot b_n) \stackrel{(iv)}{\leq} A \cdot B$$

## תלויות

**דורש:** [[Def - גבול עליון]], [[Def - גבול תחתון]], [[Thm - משפט הסנדוויץ']]
**משמש ב:** [[Method - חישוב גבולות עליונים ותחתונים]]
