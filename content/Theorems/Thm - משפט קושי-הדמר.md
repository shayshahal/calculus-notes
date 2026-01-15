# משפט: משפט קושי-הדמר

## ניסוח

רדיוס ההתכנסות של טור החזקות $\sum_{n=0}^{\infty} a_n x^n$ נתון ע"י הנוסחה:

$$R = \frac{1}{\limsup_{k \to \infty} |a_k|^{1/k}}$$

## מקרי קצה

- אם $\limsup_{k \to \infty} |a_k|^{1/k} = 0$, נאמר ש-$R = \infty$
- אם $\limsup_{k \to \infty} |a_k|^{1/k} = \infty$, נאמר ש-$R = 0$

## הסבר

המשפט נותן נוסחה מפורשת לחישוב רדיוס ההתכנסות של טור חזקות על סמך מקדמי הטור בלבד.

## דוגמאות

### דוגמה 1
$\sum_{n=1}^{\infty} \frac{(x-2)^n}{n^{1/n}}$

פתרון:
$$\limsup_{n \to \infty} \left(\frac{1}{n^{1/n}}\right)^{1/n} = \limsup_{n \to \infty} \frac{1}{n^{1/n^2}} = 1$$
לכן $R = 1$.

### דוגמה 2
$\sum_{n=0}^{\infty} \frac{(n+1) \cdot x^{3n}}{2^n}$

פתרון: נשים לב שלא תמיד ברור מהו $a_n$, לכן חשוב שהחזקה תתאים לאינדקס של האיבר בסדרה:
$$a_n = \begin{cases} \frac{k+1}{2^k} & n = 3k \\ 0 & \text{otherwise} \end{cases}$$

כעת:
$$\limsup_{n \to \infty} (a_n)^{1/n} = \limsup_{k \to \infty} \left(\frac{k+1}{2^k}\right)^{1/3k} = \frac{1}{2^{1/3}}$$
לכן $R = \sqrt[3]{2}$.

### דוגמה 3
$\sum_{n=1}^{\infty} \frac{n^2 (x+1)^n}{\pi^n + e^n}$

פתרון:
$$\limsup_{n \to \infty} \left(\frac{n^2}{\pi^n + e^n}\right)^{1/n} = \limsup_{n \to \infty} \frac{1}{\pi} \left(\frac{n^{2/n}}{(1 + (e/\pi)^n)^{1/n}}\right) = \frac{1}{\pi}$$
לכן $R = \pi$.

## תלויות

**דורש:** [[Def - טור חזקות]], [[Def - רדיוס התכנסות]], [[Def - lim sup]]
**משמש ב:** חישוב רדיוס התכנסות, פיתוח פונקציות לטורים
