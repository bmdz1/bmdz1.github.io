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
<div style="border: 2px solid black; padding: 10px;">
إذا تقاربت المتتالية \\( \{x_{n}\} \\) نحو نقطة \\(x^{*}\\)، فإن


$$
\begin{split}
x^{*}&\in I\\
x^{*}&=g(x^{*})
\end{split}
$$
</div>


 
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

نستعمل نظام SageMath لحساب بعض الحدود لهذه المتتالية

<div class="sage">
  <script type="text/x-sage">
import numpy as np
x=0;n=10
for i in range(0, n):
        x=np.cos(x);
        print(f"x_{i+1}= {x}")
error=abs(x-np.cos(x))
print(f"error= {error}")
  </script>
</div>

## الشبكة العنكبوتية (Cobweb)
<br>

يمكن تمثيل عناصر هذه المتتالية بيانيا بما يسمى ب Cobweb (شبكة عنكبوتية، و ذلك لشكلها)، حيث نبدأ بحساب صورة \\(x_{0}\\) بإسقاطها عموديا على بيان الدالة \\(g\\)، في حالتنا \\(g=\cos\\) ،
فتعطينا \\(x_{1}\\).  و لحساب \\(x_{2}\\) نريد جعل\\(x_{1}\\) سابقة، فنسقطها أفقيا على المستقيم \\(y=x\\)، ثم عموديا على بيان الدالة  \\(\cos\\)، و نكرر هذه العملية

<br>

<div class="sage">
  <script type="text/x-sage">
def cobweb(a_function, start, mask = 0, iterations = 20, xmin = 0, xmax = 1.2):
    basic_plot = plot(a_function, xmin = xmin, xmax = xmax,rgbcolor = (0.2,0.9,0.2))
    id_plot = plot(lambda x: x, xmin = xmin, xmax = xmax)
    iter_list = []
    current = start
    for i in range(mask):
        current = a_function(current)
    for i in range(iterations):
        iter_list.append([current,a_function(current)])
        current = a_function(current)
        iter_list.append([current,current])
    cobweb = line(iter_list, rgbcolor = (1,0,0))
    return basic_plot + id_plot + cobweb
var('x')
@interact
def cobwebber(f_text = input_box(default = "cos(x)",label = "function", type=str), start_val = slider(0,1,.05,0,label = 'start value'), its = slider([i+1 for i in range(0,14)],default = 5, label="iterations")):
    def f(x):
        return eval(f_text)
    show(cobweb(f, start_val, iterations = its))
  </script>
</div>
