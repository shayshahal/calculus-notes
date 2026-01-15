# משפט: אי-רציונליות של סכום עצרות

## ניסוח

נתונה סדרה של מספרים $\epsilon_n$ כך שמתקיים $\epsilon_n \in \{-1, 1\}$.

המספר $\displaystyle\sum_{n=1}^{\infty} \frac{\epsilon_n}{n!}$ הוא אי-רציונלי.

## הוכחה

קל לראות שהטור מתכנס בהחלט לכל סדרה כנ"ל לפי מבחן המנה.

נניח בשלילה כי הסכום הוא מספר רציונלי, לכן ניתן לרשום ($p \in \mathbb{Z}, q \in \mathbb{N}$):

$$\sum_{n=1}^{\infty} \frac{\epsilon_n}{n!} = \frac{p}{q}$$

$$\Rightarrow (q-1)! \cdot p = \sum_{n=1}^{q} \epsilon_n \cdot \frac{q!}{n!} + \sum_{n=q+1}^{\infty} \epsilon_n \cdot \frac{q!}{n!}$$

נשים לב שאגף שמאל, והאיבר הראשון באגף ימין הם מספרים שלמים, לכן גם $\sum_{n=q+1}^{\infty} \epsilon_n \cdot \frac{q!}{n!}$ הוא מספר שלם.

מצד שני:

$$\left|\sum_{n=q+1}^{\infty} \epsilon_n \cdot \frac{q!}{n!}\right| \overset{(*)}{\leq} \sum_{n=q+1}^{\infty} \frac{q!}{n!} = \sum_{n=q+1}^{\infty} \frac{1}{(q+1)(q+2) \cdots n}$$

$$< \sum_{n=q+1}^{\infty} \frac{1}{(q+1)^{n-q}} = \frac{1}{q} \leq 1$$

ולכן הסכום יכול להיות שווה רק ל-$0$.

כלומר נוכל להגיע לסתירה ע"י כך שנראה שלא מתקיים $\sum_{n=q+1}^{\infty} \epsilon_n \cdot \frac{q!}{n!} = 0$.

נשים לב כי:

$$\left|\sum_{n=q+1}^{\infty} \epsilon_n \cdot \frac{q!}{n!}\right| \geq \left|\frac{1}{q+1}\right| - \left|\sum_{n=q+2}^{\infty} \epsilon_n \frac{q!}{n!}\right|$$

$$\geq \frac{1}{q+1} - \sum_{n=q+2}^{\infty} \frac{q!}{n!} > \frac{1}{q+1} - \sum_{n=q+2}^{\infty} \frac{1}{(q+1)^{n-q}}$$

$$= \frac{1}{q+1} - \frac{1}{q(q+1)} = \frac{q-1}{q(q+1)} \geq 0$$

## הערה

ב-$(*)$ השתמשנו באי-שוויון המשולש עבור טורים.

## תלויות

**דורש:** [[Def - טור]], [[Thm - אי-שוויון המשולש לטורים]], [[Def - מספרים רציונליים]]
**משמש ב:** דוגמאות למספרים אי-רציונליים
