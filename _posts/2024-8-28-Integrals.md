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





<div class="sage">
  <script type="text/x-python">

var('x')
@interact
def midpoint(n = slider(1,100,1,4), f = input_box(default = "sqrt(x)", type = str), start = input_box(default = "1", type = str), end = input_box(default = "9", type = str)):
    a = N(start)
    b = N(end)
    func = sage_eval(f, locals={'x':x})
    dx = (b-a)/n
    midxs = [q*dx + a for q in range(n)]
    midys = [func(x=x_val) for x_val in midxs]
    rects = Graphics()
    for q in range(n):
        xm = midxs[q]
        ym = midys[q]
        rects = rects + line([[xm,0],[xm,ym],[xm+dx,ym],[xm+dx,0]], rgbcolor = (1,0,0)) + point((xm,ym), rgbcolor = (1,0,0))
    min_y = min(0, find_local_minimum(func,a,b)[0])
    max_y = max(0, find_local_maximum(func,a,b)[0])
    pretty_print(html('<h3>Numerical integrals with the midpoint rule</h3>'))
    pretty_print(html(r'$\int_{a}^{b}{f(x) dx} {\approx} \sum_i{f(x_i) \Delta x}$'))
    print("\n\nSage numerical answer: " + str(integral_numerical(func,a,b,max_points = 200)[0]))
    print("Midpoint estimated answer: " + str(RDF(dx*sum([midys[q] for q in range(n)]))))
    show(plot(func,a,b) + rects, xmin = a, xmax = b, ymin = min_y, ymax = max_y)

 </script>
</div>
