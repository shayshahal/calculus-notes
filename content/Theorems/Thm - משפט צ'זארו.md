# משפט: משפט צ'זארו (התכנסות ממוצע חשבוני)

## ניסוח

תהי $(a_n)$ סדרה השואפת לגבול $a$, סופי או לא. אזי גם:

$$\lim_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{n} = a$$

## תנאים

- $(a_n)$ מתכנסת לגבול $a$ (סופי או $\pm\infty$)

## הוכחה

נפריד למקרים $a \in \mathbb{R}$ ו-$a = \pm\infty$.

### מקרה 1: $a \in \mathbb{R}$ (גבול סופי)

נניח בה"כ כי $a = 0$ (אחרת ניקח את הסדרה $a_n - a$, שגבולה $0$).

יהי $\varepsilon > 0$. אז קיים $N_1 \in \mathbb{N}$ כך שלכל $n \geq N_1$:

$$|a_n| < \frac{\varepsilon}{2}$$

כעת, נבחר $N_2 \in \mathbb{N}$ כך שלכל $n \geq N_2$:

$$\frac{|a_1 + \cdots + a_{N_1}|}{n} < \frac{\varepsilon}{2}$$

(קיים כזה כי $|a_1 + \cdots + a_{N_1}|$ קבוע ו-$\frac{1}{n} \to 0$).

נסמן $N = \max\{N_1, N_2\}$. לכל $n \geq N$:

$$\frac{|a_1 + a_2 + \cdots + a_n|}{n} \leq \frac{|a_1 + \cdots + a_{N_1}|}{n} + \frac{|a_{N_1+1}| + \cdots + |a_n|}{n} \leq \frac{\varepsilon}{2} + \frac{n - N_1}{n} \cdot \frac{\varepsilon}{2} < \varepsilon$$

לכן $\frac{a_1 + \cdots + a_n}{n} \to 0$.

### מקרה 2: $a = \infty$

מכיוון ש-$a_n \to \infty$, הסדרה $(a_n)$ חסומה מלרע. לכן נוכל להניח בה"כ כי $a_n \geq 0$ לכל $n$.

יהי $M > 0$. קיים $N_1 \in \mathbb{N}$ כך שלכל $n \geq N_1$: $a_n \geq 2M$.

נסמן $N = 2N_1$. לכל $n \geq N$:

$$\frac{a_1 + \cdots + a_n}{n} \geq \frac{a_{N_1+1} + \cdots + a_n}{n} \geq \frac{n - N_1}{n} \cdot 2M = \left(1 - \frac{N_1}{n}\right) \cdot 2M \geq \left(1 - \frac{N_1}{2N_1}\right) \cdot 2M = M$$

לכן $\frac{a_1 + \cdots + a_n}{n} \to \infty$.

(המקרה $a = -\infty$ זהה.)

## הערות

> [!warning] ההיפך אינו נכון!
> ממוצע מתכנס לא מבטיח שהסדרה המקורית מתכנסת.

**דוגמה נגדית:** הסדרה $a_n = (-1)^n$ לא מתכנסת, אבל הממוצע שלה $\frac{a_1 + \cdots + a_n}{n}$ מתכנס ל-$0$.

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Def - סדרה מתכנסת]], [[Thm - אריתמטיקת גבולות]]
**משמש ב:** [[Thm - התכנסות ממוצע הנדסי]]
