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


و هذا ينتج ما يلي

<br>

$$
\begin{split}
x+i y &=\gamma(\cos \theta+i \sin \theta)=\gamma e^{i \theta} \\
z &=x+i y \\
&=\gamma(\sin \theta+i \sin \theta) \\
&\left.=\gamma e^{i \theta} 
\end{split}
$$
