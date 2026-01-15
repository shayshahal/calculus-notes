# משפט: התכנסות חזקה של מספר בין 0 ל-1

## ניסוח

יהי $c \in (0,1)$. אז:
$$c^n \xrightarrow{n \to \infty} 0$$

## תנאים

- $0 < c < 1$

## הוכחה

יהי $\epsilon > 0$. קיים $d > 0$ עבורו $c = \frac{1}{1+d}$ (במפורש $d = \frac{1}{c} - 1$).

לכל $n \in \mathbb{N}$ מתקיים:
$$|c^n - 0| = \left|\left(\frac{1}{1+d}\right)^n - 0\right| = \frac{1}{(1+d)^n} \leq \frac{1}{1+nd}$$

הצעד האחרון נובע מ[[Thm - אי-שוויון ברנולי]].

מתקיים $\frac{1}{1+nd} < \epsilon$ אם ורק אם $1 + nd > \frac{1}{\epsilon}$, אם ורק אם $n > \frac{1}{d}\left(\frac{1}{\epsilon} - 1\right)$.

נדרוש $\epsilon < 1$ וניקח:
$$n_0 = \left\lfloor\frac{1}{d}\left(\frac{1}{\epsilon} - 1\right)\right\rfloor + 1$$

אז לכל $n \geq n_0$:
$$|c^n - 0| \leq \frac{1}{1+nd} < \epsilon$$

## דוגמה

$$\left(\frac{1}{2}\right)^n \xrightarrow{n \to \infty} 0$$

## הערות

- המשפט נכון גם עבור $c = 0$ (סדרה קבועה 0)
- עבור $|c| < 1$ (כולל שליליים), ראו [[Thm - התכנסות חזקה של מספר בערך מוחלט קטן מ-1]]

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Thm - אי-שוויון ברנולי]]
**משמש ב:** [[Thm - התכנסות שורש n של a]], [[Thm - גבול ערך מוחלט אפס]]
