---
layout: post
title: تكامل ريمان
tag: التكاملات
---


لتكن \\(f\\) دالة معرفة على مجال \\([a,b]\\)، و لنعتبر التجزأة  التالية للمجال
\begin{equation}
x_0 = a < x_1 < \cdots < x_N = b
\end{equation}
 نسمي المجموع التالي
 
\begin{equation}
\sum_{i=1}^N f(x_i^ * ) (x_i - x_{i-1}) \ \ , \ x_i^* \in [x_{i-1},x_i]
\end{equation}

 بمجموع ريمان ل \\(f\\)


<div class="sage">
  <script type="text/x-sage">
f(x) = sqrt(x) ### The function.
a = 1 ### The lower bound.
b = 9 ### The upper bound.
m = 4
t = 0 ### 0 for a left Riemann sum, 1 for a right one, 0.5 for a middle one.
@interact
def midpoint(n = slider(1,40,1,m)):
###############################################################################################
   I = integral(f(x), x, a, b).n(digits=5)
   delta = (b-a)/n; tdelta = t*delta; xk = a; L = []; S = 0
   for k in range(n):
      L = L + [(xk, 0)]
      y = f(xk+tdelta)
      S = S + y
      L = L + [(xk,y)]
      xk = xk + delta
      L = L + [(xk, y)]
   S = delta*S.n(digits=5)
   pretty_print('Integral = %s'%I)
   pretty_print('Riemann sums = %s'%S)
   L = L + [(xk,0)]
   G = plot(f(x), (x, a-1, b+1), color = 'red', thickness = 1)
   G = G + plot(f(x), (x, a, b), color = 'green', thickness = 1, fill = true, fillcolor = 'blue')
   G = G + polygon(L, edgecolor = 'black', rgbcolor = (t,t^2,1-t))
   G.show(aspect_ratio = 'automatic')

   
  </script>
</div>




<div class="sage">
  <script type="text/x-sage">
f(x) = sqrt(x) ### The function.
a = 1 ### The lower bound.
b = 9 ### The upper bound.
G = plot(f(x), (x, a-1, b+1), color = 'red', thickness = 1)
G = G + plot(f(x), (x, a, b), color = 'green', thickness = 1, fill = true, fillcolor = 'grey')
G.show(aspect_ratio = 'automatic')
  </script>
</div>



details {
  padding: 10px;
  background-color: #e4eaef;
  border-radius: 5px;
}
