# הגדרה: תת-קבוצה

## הגדרה פורמלית

$$A \subseteq B \iff (\forall a \in A \Rightarrow a \in B)$$

נכתוב כי $A \subseteq B$ (קוראים: "$A$ תת-קבוצה של $B$", "$B$ מכילה את $A$", "$A$ מוכלת ב-$B$") אם לכל $a \in A$ מתקיים כי גם $a \in B$.

## סוגים

### שוויון קבוצות
$$A = B \iff (A \subseteq B \text{ וגם } B \subseteq A)$$

### הכלה ממש
$$A \subsetneq B \iff (A \subseteq B \text{ אבל } A \neq B)$$

## דוגמאות

- $\{1, 2, 3\} \subseteq \{1, 2, 3, -10\}$
- $\{1, 2, 3\} \subsetneq \{1, 2, 3, -10\}$ (הכלה ממש)
- $\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$ (הכלות ממש)
- $\emptyset \subseteq A$ לכל קבוצה $A$

## קישורים

- [[Def - קבוצה]]
- [[Def - שייכות לקבוצה]]
- [[Def - הקבוצה הריקה]]
