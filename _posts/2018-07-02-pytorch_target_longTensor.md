---
layout: post
current: post
cover: assets/images/speeches.jpg
navigation: True
title: Expected object of type torch.LongTensor but found type torch.FloatTensor for argument &#35;2 'target'
date: 2018-07-02 15:50:00
tags: [pytorch]
class: post-template
subclass: 'post'
author: sunshine

---

RuntimeError: Expected object of type torch.LongTensor but found type torch.FloatTensor for argument #2 'target'

pytorch 에서 cross entory loss 사용 시 target 값은
longTensor를 사용해라는 에러 메세지 이다.
구글링 해 봤을 때 double 등도 사용해도 된다고 적혀 있긴 했는데...

어쨋든 target 값을 아래와 같이 long type으로 바꿔주면 된다.

**logitoutput_teacher = logitoutput_teacher.long()**