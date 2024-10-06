---
layout: post
title: كسور مستمرة (جذر 2)
tag: جبر
---




## بين أن

$$
\sqrt{2}=1+\cfrac{1}{2+\cfrac{1}{2+\cfrac{1}{2+\cdots}}}
$$


## برهان



<br>

لدينا

$$
\begin{split}
(\sqrt{2}-1)(\sqrt{2}+1)&=\sqrt{2}^2-1^2\\
&=2-1\\
&=1
\end{split}
$$
 و عليه
<br>

$$
\sqrt{2}-1=\frac{1}{1+\sqrt{2}}
$$

<br>

و هذا ينتج

<br>

$$
\color{blue}{\sqrt{2}=1+\frac{1}{1+\sqrt{2}}}
$$

<br>

وبإستعمال هذه النتيجة بالتكرار، نجد

$$
\begin{split}
\sqrt{2}&=1+\cfrac{1}{1+\color{blue}{\sqrt{2}}}\\
&=1+\cfrac{1}{1+\color{blue}{1+\cfrac{1}{1+\sqrt{2}}}}\\
&=1+\cfrac{1}{2+\cfrac{1}{1+\color{blue}{\sqrt{2}}}}\\
&=1+\cfrac{1}{2+\cfrac{1}{1+\color{blue}{1+\cfrac{1}{1+\sqrt{2}}}}}\\
&=1+\cfrac{1}{2+\cfrac{1}{2+\cfrac{1}{1+\color{blue}{\sqrt{2}}}}}\\
\sqrt{2}&=1+\cfrac{1}{2+\cfrac{1}{2+\cfrac{1}{2+\cdots}}}
\end{split}
$$

<br>

على سبيل المثال

$$
\begin{split}
1+\cfrac{1}{2+\cfrac{1}{2+\cfrac{1}{2+1}}}&=\cfrac{24}{17}\\ \\
1+\cfrac{1}{2+\cfrac{1}{2+\cfrac{1}{2+1}}}&\approx 1.41..\approx \sqrt{2}
\end{split}
$$

تعد هذه الطريقة إحدى طرق الحساب التقريبي






