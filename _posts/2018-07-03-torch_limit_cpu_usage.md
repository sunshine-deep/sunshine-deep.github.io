---
layout: post
current: post
cover: assets/images/cpu.jpg
navigation: True
title: pytorch limit cpu usage (cpu 사용량 제한)
date: 2018-07-03 16:10:00
tags: [pytorch]
class: post-template
subclass: 'post'
author: sunshine

---

pytorch training 시 아무런 option을 주지 않으면 cpu usage가 2900% 등등 말도 안 되게 올라가는 경우가 있다.

이를 예방하기 위해서는 소스 윗 부분에 

__torch.set_num_threads(2)__ 와 같은 code를 add해주면 된다.

2로 세팅한다고 usage가 200%가 되고 4로 세팅한다고 400%가 되지는 않더라...

내 서버 환경상 아래와 같이 usage limit가 걸렸음. 참고...

torch.set_num_threads(2) : 300%
torch.set_num_threads(4) : 700%