---
layout: post
title: برهان متطابقة أويلر
tag: جبر
---

![Euler identity.png](/images/Euler identity.png){: style="float: center; 
height: 85%; width: 85%; margin-left: 1em; margin-top: 2em;"}{:class="img-responsive"}

<br>

أولا نذكر بنشر الدالة الأسية (نشر تايلور)

<br>

\begin{equation}
e^{z}=1+\frac{z}{1 !}+\frac{z^{2}}{2 !}+\ldots+\frac{z^{n}}{n !}+\cdots
\end{equation}

<br>

بجعل \\(z=x+iy\\) و \\(x=0\\)، نجد \\(z=iy\\)، و عليه
<br>

$$
\begin{split}
e^{i y} &=1+\frac{i y}{1 !}+\frac{(i y)^{2}}{2 !}+\frac{(i y)^{3}}{3 !}+\frac{(i y)^{4}}{4 !}+\cdots  \\
&=\left(1-\frac{y^{2}}{2 !}+\frac{y^{4}}{4 !}-\cdots\right)+i\left(y-\frac{y^{3}}{3 !}+\frac{y^{5}}{5 !}-\cdots\right) \\
&=\cos y+i \sin y
\end{split}
$$

<br>


بأخذ  \\(y=\pi\\) ،  فإن

<br>

$$
\begin{split}
e^{i\pi} &= (\cos\pi +i \sin\pi) \\
&= 1 (-1 + i\, 0) \\
&= -1
\end{split}
$$

<br>

و هذا يعطي

<br>


\begin{equation}
e^{i\pi}+1=0
\end{equation}


