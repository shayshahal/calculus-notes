# שיטה: הוכחת שוויון באמצעות חסמים

## מתי להשתמש

כאשר צריך להוכיח שוויונות של הצורה:
- $\sup(A + B) = \sup A + \sup B$
- $\inf(-A) = -\sup A$
- $\sup|A| = \max\{\sup A, -\inf A\}$

## הרעיון הכללי

להוכיח ששני מספרים $s$ ו-$t$ שווים, נראה ש:
1. $s \leq t$
2. $s \geq t$

מכאן נובע $s = t$.

## השלבים

### שלב 1: זיהוי הטענה

נניח שרוצים להוכיח $\sup(A + B) = \sup A + \sup B$.

נסמן:
- $\alpha = \sup A$
- $\beta = \sup B$
- $\gamma = \sup(A + B)$

**טענה:** $\gamma = \alpha + \beta$.

### שלב 2: הוכחה ש-$\gamma \leq \alpha + \beta$

**רעיון:** נראה ש-$\alpha + \beta$ הוא חסם מלעיל של $A + B$.

יהי $c \in A + B$. אז $c = a + b$ עבור $a \in A, b \in B$ מתאימים.

מהגדרת הסופרמום: $a \leq \alpha$ ו-$b \leq \beta$.

לכן: $c = a + b \leq \alpha + \beta$.

מכאן ש-$\alpha + \beta$ חסם מלעיל של $A + B$, ולכן $\gamma \leq \alpha + \beta$ (מהגדרת הסופרמום כחסם מלעיל מינימלי).

### שלב 3: הוכחה ש-$\gamma \geq \alpha + \beta$ (שימוש באפסילון!)

**רעיון:** נשתמש בהגדרה השקולה לסופרמום עם $\varepsilon$.

יהי $\varepsilon > 0$. עלינו להראות שקיים $c \in A + B$ כך ש-$c > \alpha + \beta - \varepsilon$.

לפי הגדרת הסופרמום, קיימים:
- $a \in A$ כך ש-$a > \alpha - \frac{\varepsilon}{2}$
- $b \in B$ כך ש-$b > \beta - \frac{\varepsilon}{2}$

נסמן $c = a + b \in A + B$. מהאי-שוויונים לעיל:

$$c = a + b > \alpha - \frac{\varepsilon}{2} + \beta - \frac{\varepsilon}{2} = \alpha + \beta - \varepsilon$$

כנדרש! לכן $\gamma = \sup(A + B) = \alpha + \beta$.

## טריק חשוב: חלוקת אפסילון

כאשר צריך להוכיח שוויון עבור **סכום** של שני סופרמומים, חלק את $\varepsilon$ ל-$\frac{\varepsilon}{2}$ עבור כל אחד מהם.

באופן כללי, עבור $n$ איברים, חלק ל-$\frac{\varepsilon}{n}$.

## דוגמה נוספת: $\inf(-A) = -\sup A$

**הוכחה:**

נסמן $s = \sup A$ ו-$-s = \inf(-A)$. נראה כי $\inf(-A) = -s$.

1. **חסם מלרע:** יהי $y \in -A$, אז $y = -x$ עבור $x \in A$ כלשהו. מתקיים $x \leq s$ ולכן $y = -x \geq -s$.

2. **מקסימליות:** יהי $\varepsilon > 0$. קיים $x \in A$ כך ש-$x > s - \varepsilon$. אז $-x \in -A$ ומתקיים $-x < -s + \varepsilon$, כנדרש.

## תלויות

**דורש:** [[Def - חסם עליון (סופרמום)]], [[Def - חסם תחתון (אינפימום)]], [[Method - מציאת חסם עליון ותחתון]]
**משמש ב:** [[Tool - חיבור קבוצות]], [[Example - סופרמום ואינפימום של סכום קבוצות]]
