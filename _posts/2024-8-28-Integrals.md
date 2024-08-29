---
layout: post
title: تكامل ريمان
tag: التكاملات
---


لتكن \\(f\\) دالة معرفة على مجال \\([a,b]\\)، يسمى
\begin{equation}
\sum_{i=1}^N f(x_i^ * ) (x_i - x_{i-1}) \ \ , \ x_i^* \in [x_{i-1},x_i]
\end{equation}
 (في حالة تقارب التكامل)، 
**<u>بتحويل لابلاس</u>**  ل \\(f\\).


<div class="sage">
  <script type="text/x-sage">
f(x) = sqrt(x) ### The function.
a = 1 ### The lower bound.
b = 9 ### The upper bound.
n = 4 ### The number of rectangles.
t = 0 ### 0 for a left Riemann sum, 1 for a right one, 0.5 for a middle one.
###############################################################################################
I = integral(f(x), x, a, b).n()
delta = (b-a)/n; tdelta = t*delta; xk = a; L = []; S = 0
for k in range(n):
    L = L + [(xk, 0)]
    y = f(xk+tdelta)
    S = S + y
    L = L + [(xk,y)]
    xk = xk + delta
    L = L + [(xk, y)]
S = delta*S.n()
pretty_print('Integral = %s'%I)
pretty_print('Riemann Sum = %s'%S)
L = L + [(xk,0)]
G = plot(f(x), (x, a-1, b+1), color = 'yellow', thickness = 1)
G = G + plot(f(x), (x, a, b), color = 'red', thickness = 1, fill = true, fillcolor = 'grey')
G = G + polygon(L, edgecolor = 'black', rgbcolor = (t,t^2,1-t))
G.show(aspect_ratio = 'automatic')
  </script>
</div>






