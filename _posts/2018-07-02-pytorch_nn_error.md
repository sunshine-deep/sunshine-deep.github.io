---
layout: post
current: post
cover: assets/images/waves.jpg
navigation: True
title: NameError: name 'nn' is not defined
date: 2018-07-02 15:40:00
tags: [pytorch]
class: post-template
subclass: 'post'
author: sunshine

---

NameError: name 'nn' is not defined

pytorch 사용시 위와 같은 에러가 난다면 조치 방법은 간단하다
아래 한 줄을 추가해주며 된다.

**import torch.nn as nn**

import torch 만 코드에 기입되어 있어 발생되는 문제이다.