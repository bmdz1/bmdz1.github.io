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

<iframe src="https://www.geogebra.org/classic/pjbkr9yx?embed" width="600" height="450" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>
