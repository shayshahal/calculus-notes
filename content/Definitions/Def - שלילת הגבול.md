# הגדרה: שלילת הגבול

## הגדרה פורמלית

סדרה $(a_n)$ **לא שואפת** ל-$L$ אם:
$$\exists(\epsilon > 0)\forall(n_0 \in \mathbb{N})\exists(n \geq n_0)\left[|a_n - L| \geq \epsilon\right]$$

## הסבר

זוהי השלילה הלוגית של [[Def - גבול של סדרה|הגדרת הגבול]]:
$$\lim_{n \to \infty} a_n = L \iff \forall(\epsilon > 0)\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[|a_n - L| < \epsilon\right]$$

השלילה מתקבלת על ידי:
- $\forall \to \exists$
- $\exists \to \forall$
- $< \to \geq$

## שימוש

כדי להוכיח שסדרה **לא** מתכנסת ל-$L$, צריך:
1. למצוא $\epsilon > 0$ קונקרטי
2. להראות שלכל $n_0 \in \mathbb{N}$ קיים $n \geq n_0$ כך ש-$|a_n - L| \geq \epsilon$

## דוגמה

נוכיח ש-$a_n = (-1)^n$ לא שואפת לשום $L \in \mathbb{R}$.

**הוכחה:** נניח בשלילה שקיים גבול $L \in \mathbb{R}$.

נבחר $\epsilon = \frac{1}{2}$.

לפי הגדרת הגבול:
$$\exists(n_0 \in \mathbb{N})\forall(n \geq n_0)\left[|a_n - L| < \frac{1}{2}\right]$$

אם כך, לכל $n \geq n_0$ מתקיים $a_n - \frac{1}{2} < L < a_n + \frac{1}{2}$.

ובפרט:
$$L > a_{2n_0} - \frac{1}{2} = 1 - \frac{1}{2} = \frac{1}{2}$$
$$L < a_{2n_0+1} + \frac{1}{2} = -1 + \frac{1}{2} = -\frac{1}{2}$$

הגענו כי $L > \frac{1}{2}$ וגם $L < -\frac{1}{2}$, סתירה.

## תלויות

**דורש:** [[Def - גבול של סדרה]], [[Tool - סימונים לוגיים וכמתים]]
**משמש ב:** [[Method - הוכחת אי-קיום גבול]], [[Example - התבדרות סדרה מתחלפת]]
