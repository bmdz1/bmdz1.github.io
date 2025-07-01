---
layout: post
title: متوسط المسافة بين نقطتين عشوائيتين في مربع وحدة
tag: احتماليات
---
<br>

مسألة حساب متوسط المسافة بين نقطتين عشوائيتين في مربع وحدة هي من المسائل الكلاسيكية في نظرية الاحتماليات والهندسة التحليلية. هذه المسألة البسيطة في صياغتها تقودنا إلى تكاملات معقدة وتطبيقات واسعة في الرياضيات التطبيقية.

## تعريف المسألة

لنفرض أن لدينا مربعاً وحدة، أي مربع طول ضلعه يساوي 1، ونختار نقطتين عشوائيتين $(x_1, y_1)$ و $(x_2, y_2)$ داخل هذا المربع. المطلوب هو حساب القيمة المتوقعة للمسافة الإقليدية بين هاتين النقطتين:

$$
\mathbb{E}[d] = \mathbb{E}\left[\sqrt{(x_2-x_1)^2 + (y_2-y_1)^2}\right]
$$

حيث $x_1, y_1, x_2, y_2 \sim \text{Uniform}(0,1)$ ومستقلة.

## الحل التحليلي

### الخطوة 1: صياغة التكامل

المتوسط المطلوب يمكن حسابه من خلال التكامل الرباعي:

$$
\mathbb{E}[d] = \int_0^1 \int_0^1 \int_0^1 \int_0^1 \sqrt{(x_2-x_1)^2 + (y_2-y_1)^2} \, dx_1 \, dy_1 \, dx_2 \, dy_2
$$

### الخطوة 2: النتيجة التحليلية

بعد بعض حسابات تكاملية (تغيير متغيرات)، نحصل على القيمة الدقيقة:

$$
\mathbb{E}[d] = \frac{1}{15}\left(2 + \sqrt{2} + 5\ln(1 + \sqrt{2})\right) \approx 0.521405
$$


## الطرق العددية

### محاكاة مونت كارلو
الطريقة الأكثر بساطة وفعالية لتقدير هذا المتوسط:

```python
import random
import math

def monte_carlo_average_distance(n_simulations):
    total_distance = 0
    for _ in range(n_simulations):
        # Generate two random points
        x1, y1 = random.random(), random.random()
        x2, y2 = random.random(), random.random()
        
        # Calculate distance
        distance = math.sqrt((x2-x1)**2 + (y2-y1)**2)
        total_distance += distance
    
    return total_distance / n_simulations
print(monte_carlo_average_distance(1000))
```

### دقة التقدير
مع زيادة عدد المحاكاة $n$، ينخفض الخطأ المعياري بمعدل $O(1/\sqrt{n})$ وفقاً لنظرية الحد المركزي.

## تعميمات المسألة

### أبعاد أخرى
- **الخط الوحدة**: $\mathbb{E}[d] = 1/3$
- **المكعب الوحدة**: $\mathbb{E}[d] \approx 0.661707$
- **الكرة الوحدة**: تحليل أكثر تعقيداً

### أشكال هندسية أخرى
- **المثلث**: متوسط المسافة في مثلث متساوي الأضلاع
- **الدائرة**: حسابات تتضمن الإحداثيات القطبية
- **الأشكال غير المنتظمة**: طرق عددية بحتة

## خلاصة

مسألة متوسط المسافة في المربع الوحدة تُظهر الجمال في تقاطع الهندسة والاحتماليات والتحليل الرياضي. رغم بساطة صياغتها، تقود إلى حسابات عميقة وتطبيقات واسعة في العلوم والهندسة.



---

## مراجع 

1.  Steven R. Dunbar (1997) The Average Distance Between Points in Geometric
Figures, The College Mathematics Journal, 28:3, 187-197
2.  Mathai A. M. An Introduction to Geometrical Probability: Distributional Aspects with Applications. Newark: Gordon and Breach, 1999.

<br>
