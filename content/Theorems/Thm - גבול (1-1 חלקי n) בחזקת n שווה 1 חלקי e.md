# משפט: גבול $(1-\frac{1}{n})^n$ שווה $\frac{1}{e}$

## ניסוח

$$\lim_{n \to \infty} \left(1 - \frac{1}{n}\right)^n = \frac{1}{e}$$

## הוכחה

נתחיל מהביטוי:

$$\left(1 - \frac{1}{n}\right)^n = \left(\frac{n-1}{n}\right)^n$$

לכל $n \geq 2$:

$$= \frac{1}{\left(\frac{n}{n-1}\right)^n} = \frac{1}{\left(\frac{n-1+1}{n-1}\right)^n} = \frac{1}{\left(1 + \frac{1}{n-1}\right)^n}$$

נפרק את החזקה:

$$= \frac{1}{\left(1 + \frac{1}{n-1}\right)^{n-1} \cdot \left(1 + \frac{1}{n-1}\right)}$$

$$= \frac{1}{\underbrace{\left(1 + \frac{1}{n-1}\right)^{n-1}}_{\to e} \cdot \underbrace{\left(1 + \frac{1}{n-1}\right)}_{\to 1}}$$

כאשר $n \to \infty$:

$$\xrightarrow{n \to \infty} \frac{1}{e \cdot 1} = \frac{1}{e}$$

## הכללה

**משפט:** אם $a_n \to \infty$ אז:

$$\left(1 - \frac{1}{a_n}\right)^{a_n} \to \frac{1}{e}$$

ההוכחה דומה להוכחה של [[Def - הקבוע e|ההכללה עבור $(1+\frac{1}{a_n})^{a_n}$]].

## קשר להגדרת $e$

משפט זה הוא "התאום" של הגדרת $e$:

| גבול | ערך |
|------|-----|
| $\lim\limits_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$ | $e$ |
| $\lim\limits_{n \to \infty} \left(1 - \frac{1}{n}\right)^n$ | $\frac{1}{e}$ |

## תלויות

**דורש:** [[Def - הקבוע e]], [[Thm - אריתמטיקת גבולות]]
**משמש ב:** [[Tool - גבולות בסיסיים של סדרות]], [[Example - צורות אי-קביעות]]
