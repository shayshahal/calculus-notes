# דוגמה: סופרמום של סדרה חיובית

## תרגיל

נניח כי $(a_n)$ סדרה חיובית. נגדיר את הסדרה $b_n$ על ידי:

$$b_n = \sqrt[n]{a_1^n + a_2^n + \ldots + a_n^n}$$

הוכיחו כי:
$$\lim_{n \to \infty} b_n = a := \sup\{a_n : n \in \mathbb{N}\}$$

התייחסו גם למקרה שבו הקבוצה $\{a_n : n \in \mathbb{N}\}$ אינה חסומה, שבו נגדיר $a = \infty$.

## פתרון

### מקרה 1: $a = \infty$

כלומר לכל $M > 0$ קיים $N$ כך ש-$a_N > M$.

לכל $n \geq N$ מתקיים:
$$b_n = \sqrt[n]{a_1^n + a_2^n + \ldots + a_n^n} \geq \sqrt[n]{a_N^n} = a_N > M$$

ולכן $\lim_{n \to \infty} b_n = \infty$.

### מקרה 2: $a$ סופי

נשים לב כי לכל $a_n$ מתקיים $a_n \leq a$ ולכן:

**חסם עליון:**
$$b_n = \sqrt[n]{a_1^n + a_2^n + \ldots + a_n^n} \leq \sqrt[n]{a^n + \ldots + a^n} = \sqrt[n]{n \cdot a^n} = \sqrt[n]{n} \cdot a$$

ידוע כי $\sqrt[n]{n} \to 1$ ולכן לכל $\varepsilon > 0$ קיים $N_1$ כך שלכל $n > N_1$ מתקיים $\sqrt[n]{n} < 1 + \frac{\varepsilon}{a}$, כלומר:
$$b_n \leq \left(1 + \frac{\varepsilon}{a}\right) \cdot a = a + \varepsilon$$

**חסם תחתון:**
מהגדרת $\sup$ נובע כי לכל $\varepsilon > 0$ קיים $N_2$ כך ש-$a_{N_2} > a - \varepsilon$, כלומר לכל $n > N_2$:
$$b_n \geq \sqrt[n]{a_{N_2}^n} = a_{N_2} > a - \varepsilon$$

**סיכום:**
אם נבחר $N = \max\{N_1, N_2\}$, נקבל מהנ"ל כי לכל $n > N$ מתקיים:
$$b_n \in (a - \varepsilon, a + \varepsilon)$$

כלומר $b_n \to a$.

## הערות

תרגיל זה משלב:
- [[Def - חסם עליון (סופרמום)|הגדרת סופרמום]]
- [[Tool - גבולות בסיסיים של סדרות|הגבול $\sqrt[n]{n} \to 1$]]
- [[Thm - משפט הסנדוויץ'|משפט הסנדוויץ']]

## תלויות

**דורש:** [[Def - חסם עליון (סופרמום)]], [[Tool - גבולות בסיסיים של סדרות]], [[Thm - משפט הסנדוויץ']]
**משמש ב:** [[Thm - התכנסות ממוצע הנדסי]]
