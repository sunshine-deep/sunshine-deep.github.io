---
layout: post
current: post
cover: assets/images/2018-0711.jpg
navigation: True
title: Expected object of type torch.FloatTensor but found type torch.cuda.FloatTensor for argument
date: 2018-07-11 16:10:00
tags: [pytorch]
class: post-template
subclass: 'post'
author: sunshine

---
**Expected object of type torch.FloatTensor but found type torch.cuda.FloatTensor for argument**


cuda 를 사용하다 보면 cuda에 올라가 있는 변수와 cpu에 있는 변수가 혼재하는 경우가 있는데

cuda variable 과 cpu variable간의 연산이 발생하면 위와 같은 에러가 발생하게 된다.

해결책은 간단하다

cuda variable에 .cpu() 를 붙이거나 cpu variable에 .cuda()를 붙여서 연산하면 된다.

ex)
>  a : cuda variable  
  b : cpu varriable

 > sol 1) **c = a.cpu() + b**  
 > sol 2) **c = a + b.cuda()**