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
