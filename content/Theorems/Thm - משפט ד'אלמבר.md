# משפט: משפט ד'אלמבר

## ניסוח

תהי $(x_n)$ [[Def - סדרה|סדרה]] חיובית כך ש:

$$\lim_{n \to \infty} \frac{x_{n+1}}{x_n} = c$$

כאשר $c$ גבול סופי או $+\infty$.

אז מתקיים:

$$\lim_{n \to \infty} \sqrt[n]{x_n} = c$$

## הוכחה

נגדיר סדרה $(y_n)$ באופן הבא:

$$y_1 = x_1, \quad y_n = \frac{x_n}{x_{n-1}}, \quad n > 1$$

אז $y_n \to c$.

נשים לב ש-$y_1 \cdot y_2 \cdots y_n = x_n$, ולכן:

$$\sqrt[n]{x_n} = \sqrt[n]{y_1 \cdot y_2 \cdots y_n}$$

מ[[Thm - התכנסות ממוצע הנדסי|התכנסות ממוצע הנדסי]]:

$$\lim_{n \to \infty} \sqrt[n]{y_1 \cdots y_n} = c$$

לכן $\lim_{n \to \infty} \sqrt[n]{x_n} = c$.

## הערות

> [!warning] ההיפך אינו נכון!
> ייתכן שהשורש מתכנס אבל המנה לא.

**דוגמה נגדית:** הסדרה $x_n = n^{(-1)^n}$ מקיימת:

$$\sqrt[n]{x_n} = \begin{cases} \sqrt[n]{n}, & n \text{ זוגי} \\ \frac{1}{\sqrt[n]{n}}, & n \text{ אי-זוגי} \end{cases} \to 1$$

אבל הגבול $\lim_{n \to \infty} \frac{x_{n+1}}{x_n}$ **לא קיים**.

## יישום: חישוב $\lim_{n \to \infty} \sqrt[n]{\binom{2n}{n}}$

נסמן $a_n = \binom{2n}{n}$. לפי משפט ד'אלמבר, אם קיים הגבול $\lim_{n \to \infty} \frac{a_{n+1}}{a_n}$ אזי ערכו שווה לגבול המבוקש.

$$\frac{a_{n+1}}{a_n} = \frac{\binom{2(n+1)}{n+1}}{\binom{2n}{n}} = \frac{\frac{(2n+2)!}{(n+1)!(n+1)!}}{\frac{(2n)!}{n!n!}} = \frac{(2n+2)(2n+1)}{(n+1)^2} = \frac{4n^2 + 6n + 2}{n^2 + 2n + 1} \to 4$$

לכן הגבול הוא $4$.

## תלויות

**דורש:** [[Thm - התכנסות ממוצע הנדסי]], [[Def - גבול של סדרה]]
**משמש ב:** [[Thm - מבחן המנה לסדרות]], [[Thm - מבחן השורש]]
