---
layout: post
title: كسور مستمرة (جذر 5)
tag: جبر
---

## بين أن

$$
\sqrt{5}=2+\cfrac{1}{4+\cfrac{1}{4+\cfrac{1}{4+\cdots}}}
$$


## برهان

<br>

لدينا

<br>

$$
\begin{split}
(\sqrt{5}-2)(\sqrt{5}+2)&=\sqrt{5}^2-2^2\\
&=5-4\\
&=1
\end{split}
$$

<br>

 و عليه
<br>

$$
\sqrt{5}-2=\frac{1}{2+\sqrt{5}}
$$

<br>

و هذا ينتج

<br>

$$
\color{blue}{\sqrt{5}=2+\frac{1}{2+\sqrt{5}}}
$$

<br>

وبإستعمال هذه النتيجة بالتكرار، نجد

$$
\begin{split}
\sqrt{5}&=2+\cfrac{1}{2+\color{blue}{\sqrt{5}}}\\
&=2+\cfrac{1}{2+\color{blue}{2+\cfrac{1}{2+\sqrt{5}}}}\\
&=2+\cfrac{1}{4+\cfrac{1}{2+\color{blue}{\sqrt{5}}}}\\
&=2+\cfrac{1}{4+\cfrac{1}{2+\color{blue}{2+\cfrac{1}{2+\sqrt{5}}}}}\\
&=2+\cfrac{1}{4+\cfrac{1}{4+\cfrac{1}{2+\color{blue}{\sqrt{5}}}}}\\
&=2+\cfrac{1}{4+\cfrac{1}{4+\cfrac{1}{4+\cdots}}}
\end{split}
$$

<br>

على سبيل المثال

$$
\begin{split}
2+\cfrac{1}{4+\cfrac{1}{4+\cfrac{1}{4+1}}}&=\cfrac{199}{89}\\ \\
2+\cfrac{1}{4+\cfrac{1}{4+\cfrac{1}{4+1}}}&\approx 2.236\approx \sqrt{5}
\end{split}
$$

تعد هذه الطريقة إحدى طرق الحساب التقريبي






