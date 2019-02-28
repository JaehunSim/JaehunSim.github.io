---

layout: post
title: "간략한 노트"
date: 2019-02-23 10:36:00
sitemap: 
  changefreq: daily
  priority: 1.0
comments: true

---

# 공부하는 것들 짤막한 노트

## matrix multiplication

Naive: n^3  
Strassen: log7 / log2, n^2.807  
제일 실용적인 알고리즘  
Coppersmith-Winograd: n^2.372 [link](https://en.wikipedia.org/wiki/Coppersmith%E2%80%93Winograd_algorithm)  
그러나 이 알고리즘은 구현이 복잡하고 n이 무지 클때만 속도차이가 난다. 전혀 실용적이지 못하다...

## 검증 알고리즘 - A * B = C 인것을 검증

Freivald's algorithm: [link](https://www.geeksforgeeks.org/freivalds-algorithm/)  
> O(kn2) time the algorithm can verify a matrix product with probability of failure less than 2-k  
Monte Carlo randomized algorithm의 일종이다.
