---
layout: post
title: SageMath
tag: SageMath
---

## الجبر في SageMath


لحل المعادلة 

$$ x^2 + x - 2=0. $$

<div class="sage">
  <script type="text/x-sage">
solve(x**2 + x - 2==0,x)
  </script>
</div>


لإيجاد حل المعادلة

$$ax^2+bx+c=0.$$

بالنسبة ل \\(x\\) 

<div class="sage">
  <script type="text/x-sage">
x,a,b,c = var("x,a,b,c") 
solve(a*x**2+b*x+c==0,x)
  </script>
</div>




<script src="https://utteranc.es/client.js"
        repo="bachirmath/bachirmath.github.io"
        issue-term="pathname"
        theme="github-dark-orange"
        crossorigin="anonymous"
        async>
</script>



<iframe scrolling="no" title="Untitled" src="https://www.geogebra.org/material/iframe/id/fje8usvq/width/1466/height/689/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="1466px" height="689px" style="border:0px;"> </iframe>
