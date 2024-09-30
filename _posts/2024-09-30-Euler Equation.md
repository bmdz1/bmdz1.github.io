---
layout: post
title: برهان متطابقة أويلر
tag: جبر
---


أولا نذكر بنشر الدالة الأسية (تايلور)

\begin{equation}
e^{z}=1+\frac{z}{1 !}+\frac{z^{2}}{2 !}+\ldots+\frac{z^{n}}{n !}+\cdots
\end{equation}


بجعل \\(z=x+iy\\) و \\(x=0\\)، نجد \\(z=iy\\)، و عليه
<br>

$$
\begin{split}
e^{i y} &=1+\frac{i y}{1 !}+\frac{(i y)^{2}}{2 !}+\frac{(i y)^{3}}{3 !}+\frac{(i y)^{4}}{4 !}+\cdots  \\
&=\left(1-\frac{y^{2}}{2 !}+\frac{y^{4}}{4 !}-\cdots\right)+i\left(y-\frac{y^{3}}{3 !}+\frac{y^{5}}{5 !}-\cdots\right) \\
&=\cos y+i \sin y
\end{split}
$$

و منه نجد

\begin{equation}
e^{z}=e^{x}  e^{i y}=e^{x}(\cos y+i \sin y)
\end{equation}

بأخذ \\(x=0\\) و \\(y=\pi\\) ،  فإن

<br>

$$
\begin{split}
e^{0+i\pi} &= e^{0}(\cos\pi +i \sin\pi) \\
&= 1 (-1 + i 0) \\
&= -1
\end{split}
$$

و هذا يعطي

<br>


\begin{equation}
e^{i\pi}+1=0
\end{equation}


