---
layout: post
title: "النسبة الذهبية (Golden Ratio)"
description: "استكشاف الخصائص الرياضية والجمالية للنسبة الأكثر شهرة في الرياضيات والفن"
tag: تحليل
author: Bachir
---

<br>

## مقدمة تاريخية
النسبة الذهبية، والمعروفة أيضاً بالقسم الذهبي أو النسبة الإلهية، هي واحدة من أشهر الثوابت الرياضية في التاريخ. عُرفت هذه النسبة منذ العصور القديمة، حيث استخدمها الإغريق في بناء البارثينون، ودرسها إقليدس في كتابه "الأسس" حوالي 300 قبل الميلاد تحت اسم "القسم المتطرف والمتوسط".

أُطلق عليها اسم "النسبة الذهبية" لأول مرة في القرن التاسع عشر، وأصبحت ترمز بالحرف اليوناني φ (فاي) تيمناً بالنحات اليوناني فيدياس (Phidias).

## التعريف الرياضي
النسبة الذهبية φ تُعرّف كالتالي: إذا قُسم خط مستقيم إلى جزأين بحيث تكون نسبة الخط الكامل إلى الجزء الأكبر مساوية لنسبة الجزء الأكبر إلى الجزء الأصغر، فإن هذه النسبة هي النسبة الذهبية.

رياضياً، إذا كان لدينا خط طوله $a + b$ مقسوم إلى جزأين بأطوال $a$ و $b$ حيث $a > b$، فإن:

$$\frac{a + b}{a} = \frac{a}{b} = \phi$$

### التمثيل الهندسي

<div style="width: 100%; max-width: 600px; margin: 20px auto; overflow: hidden;">
  <svg width="100%" height="auto" viewBox="0 0 600 250" xmlns="http://www.w3.org/2000/svg" style="display: block;">
  <!-- Background -->
  <rect width="600" height="250" fill="#ffffff"/>
  
  <!-- Main line -->
  <line x1="50" y1="125" x2="500" y2="125" stroke="#2c3e50" stroke-width="4"/>
  
  <!-- Golden ratio division point -->
  <line x1="328" y1="105" x2="328" y2="145" stroke="#e74c3c" stroke-width="3"/>
  <circle cx="328" cy="125" r="4" fill="#e74c3c"/>
  
  <!-- Segment a (larger) -->
  <line x1="50" y1="95" x2="328" y2="95" stroke="#27ae60" stroke-width="6"/>
  <text x="189" y="85" text-anchor="middle" font-family="Arial, sans-serif" font-size="20" font-weight="bold" fill="#27ae60">a</text>
  
  <!-- Segment b (smaller) -->
  <line x1="328" y1="155" x2="500" y2="155" stroke="#f39c12" stroke-width="6"/>
  <text x="414" y="175" text-anchor="middle" font-family="Arial, sans-serif" font-size="20" font-weight="bold" fill="#f39c12">b</text>
  
  <!-- Total length indicator -->
  <path d="M 50 190 Q 275 210 500 190" stroke="#3498db" stroke-width="2" fill="none"/>
  <text x="275" y="230" text-anchor="middle" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#3498db">a + b</text>
  
  <!-- Formula -->
  <text x="300" y="40" text-anchor="middle" font-family="Arial, sans-serif" font-size="24" font-weight="bold" fill="#2c3e50" direction="ltr" unicode-bidi="embed">
    <tspan fill="#3498db">(a + b)</tspan><tspan fill="#2c3e50">/</tspan><tspan fill="#27ae60">a</tspan><tspan fill="#2c3e50"> = </tspan><tspan fill="#27ae60">a</tspan><tspan fill="#2c3e50">/</tspan><tspan fill="#f39c12">b</tspan><tspan fill="#2c3e50"> = φ</tspan>
  </text>
  </svg>
</div>


## اشتقاق القيمة
من التعريف أعلاه، نحصل على المعادلة:

$$\frac{a + b}{a} = \frac{a}{b}$$

بقسمة البسط والمقام في الطرف الأيسر على $a$:

$$1 + \frac{b}{a} = \frac{a}{b}$$

بوضع $x = \frac{a}{b}$، نحصل على:

$$1 + \frac{1}{x} = x$$

وهذا يعطينا المعادلة التربيعية:

$$x^2 - x - 1 = 0$$

حل هذه المعادلة يعطينا:

$$x = \frac{1 \pm \sqrt{5}}{2}$$

بما أن $\phi > 0$، فإن:

$$\phi = \frac{1 + \sqrt{5}}{2} \approx 1.618...$$

## الخصائص الرياضية المذهلة

### الخاصية الأساسية

$$\phi^2 = \phi + 1$$

هذا يعني أن مربع النسبة الذهبية يساوي النسبة الذهبية زائد واحد.

### التمثيل ككسر مستمر

$$\phi = 1 + \cfrac{1}{1 + \cfrac{1}{1 + \cfrac{1}{1 + \cfrac{1}{\ddots}}}}$$

النسبة الذهبية لها أبسط تمثيل ككسر مستمر:

$$\phi = [1; 1, 1, 1, 1, ...]$$


## العلاقة مع متتالية فيبوناتشي
النسبة الذهبية مرتبطة بشكل عميق مع متتالية فيبوناتشي:

$$\lim_{n \to \infty} \frac{F_{n+1}}{F_n} = \phi$$

كما تظهر في صيغة بينيه:

$$F_n = \frac{\phi^n - (1-\phi)^n}{\sqrt{5}}$$



## التطبيقات في الطبيعة والفن

### في الطبيعة
- **الأصداف البحرية**: شكل صدفة الحلزون
- **النباتات**: ترتيب الأوراق والبتلات
- **جسم الإنسان**: نسب الأطراف والوجه
- **الحشرات**: بنية جسم النحل

### في الفن والعمارة
- **اللوحات الفنية**: استخدمها دافينشي في لوحة الموناليزا
- **العمارة**: البارثينون، الأهرامات
- **الموسيقى**: التركيب الموسيقي والأوكتافات
- **التصميم الحديث**: شعارات الشركات والتصميم الجرافيكي

## التطبيقات العملية

### في الرياضيات
- **نظرية الأعداد**: دراسة الكسور المستمرة
- **الهندسة**: بناء الخماسي المنتظم [أنظر هنا](https://www.cut-the-knot.org/do_you_know/GoldenRatioInRegularPentagon.shtml)
- **التحليل**: دراسة الدوال والمتتاليات

- 
### في العلوم التطبيقية
- **خوارزميات البحث**: البحث الذهبي في التحسين
- **التمويل**: تحليل الأسواق المالية
- **التصميم**: نسب الشاشات والواجهات

## خرافات ومفاهيم خاطئة
رغم شهرتها، هناك العديد من المفاهيم الخاطئة حول النسبة الذهبية:
- ليس كل شيء جميل يحتوي على النسبة الذهبية
- لا تظهر في كل أعمال الفن القديم كما يُشاع
- الإدراك الجمالي للنسبة الذهبية قد يكون مبالغاً فيه أحياناً

---
## المراجع
1. Livio, Mario. "The Golden Ratio: The Story of Phi, the World's Most Astonishing Number"
2. Huntley, H.E. "The Divine Proportion: A Study in Mathematical Beauty"
3. Posamentier, Alfred S. and Lehmann, Ingmar. "The Glorious Golden Ratio"
4. Euclid. "Elements, Book VI, Definition 3"

<div id="comments">
  <script src="https://utteranc.es/client.js"
          repo="bachirmath/bachirmath.github.io"
          issue-term="pathname"
          theme="github-dark-orange"
          crossorigin="anonymous"
          async>
  </script>
</div>
