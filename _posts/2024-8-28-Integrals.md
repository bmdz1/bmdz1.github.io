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
  <script type="text/x-python">

import numpy as np
import matplotlib.pyplot as plt

f = lambda x : 1/(1+x**2)
a = 0; b = 8; N = 8
n = 10 # Use n*N+1 points to plot the function smoothly

x = np.linspace(a,b,N+1)
y = f(x)

X = np.linspace(a,b,n*N+1)
Y = f(X)

plt.figure(figsize=(9,5))

plt.plot(X,Y,'b')
x_left = x[:-1] # Left endpoints
y_left = y[:-1]
plt.plot(x_left,y_left,'b.',markersize=10)
plt.bar(x_left,y_left,width=(b-a)/N,alpha=0.2,align='edge',edgecolor='b')
plt.title('Left Riemann Sum, N = {}'.format(N))
plt.show()
   
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
        rects = rects + line([[xm,0],[xm,ym],[xm,ym],[xm,0]], rgbcolor = (1,0,0)) + point((xm,ym), rgbcolor = (1,0,0))
    min_y = min(0, find_local_minimum(func,a,b)[0])
    max_y = max(0, find_local_maximum(func,a,b)[0])
    pretty_print(html('<h3>Numerical integrals with the midpoint rule</h3>'))
    pretty_print(html(r'$\int_{a}^{b}{f(x) dx} {\approx} \sum_i{f(x_i) \Delta x}$'))
    print("\n\nSage numerical answer: " + str(integral_numerical(func,a,b,max_points = 200)[0]))
    print("Midpoint estimated answer: " + str(RDF(dx*sum([midys[q] for q in range(n)]))))
    show(plot(func,a,b) + rects, xmin = a, xmax = b, ymin = min_y, ymax = max_y)

 </script>
</div>
