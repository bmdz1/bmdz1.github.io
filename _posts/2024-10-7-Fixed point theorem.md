---
layout: post
title: طريقة التكرار بنقطة ثابتة
tag: تحليل
---

## نقطة ثابتة

ليكن \\(I\\) مجال مغلق من \\(\mathbb{R}\\) و لتكن


$$
\begin{split}
g:I&\longrightarrow I\\
x&\longrightarrow g(x)
\end{split}
$$

 نسمي كل نقطة \\(x^{*}\\) تحقق

$$
x^{*}=g(x^{*})
$$

**<u>بنقطة ثابتة</u>**  ل \\(g\\) (لأن \\(g\\) تحافظ على \\(x^{*}\\))

## التكرار بنقطة ثابتة

نحافظ على نفس الرموز، و لتكن \\(x_{0}\in I\\)، نسمي المتتالية التالية 

$$
\begin{cases}
x_{n+1}=g(x_{n}),\, n\geq 0\\
x_{0}
\end{cases}
$$

 بمتتالية التكرار بالنقطة الثابتة (Fixed Point Iteration )

 
<br>
نفرض أن الدالة \\(g\\) مستمرة، فنجد النظرية التالية

### نظرية:

إذا تقاربت المتتالية \\( \{x_{n}\} \\) نحو نقطة \\(x^{*}\\)، فإن


$$
\begin{split}
x^{*}&\in I\\
x^{*}&=g(x^{*})
\end{split}
$$

 
### برهان:

بما أن \\(\forall  n, x_{n}\in I \\)، و \\(I\\) مغلق، فإن

$$
x^{*}=\lim_{n\to\infty}x_{n}\in I
$$

و بما أن  \\(g\\) مستمرة فإن

$$
\begin{split}
x^{*}&= \lim_{n\to\infty}x_{n+1}=\lim_{n\to\infty} g(x_{n})\\
&=g(\lim_{n\to\infty}  x_{n})\\
x^{*}&=g(x^{*})
\end{split}
$$

يمكن تطبيق هذه الطريقة لحل معادلات من الشكل

$$
x=g(x)
$$

بشرط تقارب متتالية التكرار بنقطة ثابتة


## مثال تطبيقي

لنعتبر المعادلة   

$$
x=\cos(x)
$$

لكي نحل المعادلة في \\(\mathbb{R}\\)، يجب أن نكتب مسألتنا على الشكل الذي إعتبرناه، 

فهنا يمكننا إعتبار الدالة

$$
\begin{split}
g:[0,1]&\longrightarrow [0,1]\\
x&\longrightarrow g(x)=\cos(x)
\end{split}
$$

و يمكن إختيار \\(x_{0}=0\\)، و هكذا يمكننا صناعة 
متتالية من الشكل




$$
\begin{cases}
x_{n+1}=g(x_{n})=\cos(x_{n})\\
x_{0}=0
\end{cases}
$$

<div class="sage">
  <script type="text/x-sage">
import numpy as np
x0=0
for n in range(0, 10):
        x0=np.cos(x0);
        print(x0)

error=abs(x0-np.cos(x0))
error
  </script>
</div>

