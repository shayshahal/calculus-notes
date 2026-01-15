# משפט: אפיון קבוצה צפופה

## ניסוח

תהי $A \subseteq \mathbb{R}$. התנאים הבאים שקולים:

1. $A$ צפופה
2. $\forall(x \in \mathbb{R})\forall(\epsilon > 0)\exists(a \in A)[|x - a| < \epsilon]$
3. לכל $x \in \mathbb{R}$ קיימת סדרה $(a_n)_{n=1}^{\infty}$ של איברים ב-$A$ השואפת ל-$x$

## הוכחה

**הוכחת $1 \Leftarrow 2$:**

יהיו $x \in \mathbb{R}$, $\epsilon > 0$.

$A$ צפופה ולכן יש $a \in A$ המקיים:
$$x < a < x + \epsilon$$

$a$ זה מקיים $|x - a| < \epsilon$. $\blacksquare$

**הוכחת $2 \Leftarrow 3$:**

יהי $x \in \mathbb{R}$. לפי תנאי 2, לכל $n \in \mathbb{N}$:
$$\exists(a_n \in A)\left[|x - a_n| < \frac{1}{n}\right]$$

קיבלנו סדרה $(a_n)$ של איברים ב-$A$. לכל $n$ מתקיים:
$$x - \frac{1}{n} < a_n < x + \frac{1}{n}$$

וממשפט הסנדוויץ' $a_n \to x$. $\blacksquare$

**הוכחת $3 \Leftarrow 1$:**

יהיו $x, y \in \mathbb{R}$ המקיימים $y > x$.

יהי $z \in \mathbb{R}$ המקיים $y > z > x$, למשל $z = \frac{x+y}{2}$.

לפי תנאי 3, קיימת סדרה $(a_n)$ של איברים ב-$A$ השואפת ל-$z$.

מתקיים $y > z > x$ וכפי שראינו בעבר, זה גורר:
$$\exists(n \in \mathbb{N})\forall(n \geq n_0)[x < a_n < y]$$

אז $a_{n_0}$ הוא איבר ב-$A$ המקיים $y > a_{n_0} > x$. $\blacksquare$

## מסקנה

לכל מספר ממשי יש סדרה של רציונליים השואפת אליו וסדרה של אי-רציונליים השואפת אליו.

## תלויות

**דורש:** [[Def - קבוצה צפופה]], [[Thm - משפט הסנדוויץ']], [[Def - גבול של סדרה]]

**משמש ב:** [[Thm - צפיפות הרציונליים]], [[Thm - צפיפות האי-רציונליים]]
