# משפט: התכנסות שורש n של a

## ניסוח

לכל $a > 0$ מתקיים:
$$\sqrt[n]{a} \xrightarrow{n \to \infty} 1$$

## תנאים

- $a > 0$

## הוכחה

**מקרה טריוויאלי:** $a = 1$

זו הסדרה הקבועה $1$ ולכן שואפת ל-$1$.

**מקרה כללי:** יהי $\epsilon > 0$. צריך למצוא $n_0$ כך שלכל $n \geq n_0$:
$$1 - \epsilon < \sqrt[n]{a} < 1 + \epsilon$$

באופן שקול (עבור $\epsilon < 1$):
$$(1-\epsilon)^n < a < (1+\epsilon)^n$$

**מקרה 1:** $a > 1$

במקרה זה $(1-\epsilon)^n < a$ נכון לכל $n$.

נשאר להראות שהחל ממקום מסוים $(1+\epsilon)^n > a$.

לפי [[Thm - אי-שוויון ברנולי]]:
$$(1+\epsilon)^n \geq 1 + n\epsilon$$

נבדוק מתי $1 + n\epsilon > a$. זה קורה אם ורק אם $n > \frac{1}{\epsilon}(a-1)$.

אז נבחר:
$$n_0 = \left\lfloor\frac{1}{\epsilon}(a-1)\right\rfloor + 1$$

לכל $n \geq n_0$:
$$(1-\epsilon)^n < a < 1 + n\epsilon \leq (1+\epsilon)^n$$

**מקרה 2:** $0 < a < 1$

אז $(1+\epsilon)^n > a$ מתקיים לכל $n$.

נשאר להראות שהחל ממקום מסוים $(1-\epsilon)^n < a$.

מתקיים $(1-\epsilon) \in (0,1)$. ולכן לפי [[Thm - התכנסות חזקה של מספר בין 0 ל-1]]:
$$(1-\epsilon)^n \xrightarrow{n \to \infty} 0$$

לכן (לוקחים $\epsilon = a$):
$$\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[|(1-\epsilon)^n - 0| < a\right]$$

ואז לכל $n \geq n_0$ מתקיים:
$$(1-\epsilon)^n < a < (1+\epsilon)^n$$

## מסקנות

$$\lim_{n \to \infty} \sqrt[n]{n} = 1$$

(הוכחה בתרגול)

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Thm - אי-שוויון ברנולי]], [[Thm - התכנסות חזקה של מספר בין 0 ל-1]]
**משמש ב:** [[Thm - מבחן השורש]], [[Tool - גבולות בסיסיים של סדרות]]
