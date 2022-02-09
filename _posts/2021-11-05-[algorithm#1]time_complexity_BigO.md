---
layout: post
title:  "시간 복잡도 빅오(Big-O) 표기법"
summary: "시간 복잡도 중에서도 많이 쓰이는 빅오 표기법"
author: aheunkim
date: '2021-11-05 13:11:00 +0900'
category: algorithm
thumbnail: /assets/img/posts/algorithm/thumbnail.jpg
keywords: time complexity, Big-O
permalink: /blog/algorithm/time_complexity_Big-O/
usemathjax: true
---

코딩을 할 때 효율적으로 코드를 작성할 필요가 있다.  
이를 위해서 공간 복잡도와 시간 복잡도를 고려할 필요가 있는데,  
시간 복잡도 중에서도 가장 많이 쓰이는 빅오 표기법만 정리해두려고 한다.
<br/>
  
시간 복잡도의 점근 표기법에는 3가지가 있다.
* 최상의 경우 : 오메가 표기법 (Big-Ω Notation)
* 평균의 경우 : 세타 표기법 (Big-θ Notation)
* 최악의 경우 : 빅오 표기법 (Big-O Notation)
<br/>
  
### 빅오(Big-O) 표기법
빅오 표기법은 불필요한 연산을 제거하여 알고리즘 분석을 쉽게 할 목적으로 사용된다.  
|수식|Big-O|
|---|-----|
|1|O(1)|
|n, 2n, 999n, 2n+3|O(n)|
|nlogn|O(nlogn)|
|$$n^2, 3n^2, 3n^2+3$$|O($$n^2$$)|
|n!|O(n!)|
<br/>

수식의 계수는 상관없다. 차수가 중요하다!  
로그의 밑 역시 중요하지 않다.
<br/>

알고리즘에서 가장 흔하게 등장하는 빅오 식은 다음과 같다.  
O($$1$$) < O($$logn$$) < O($$n$$) < O($$nlogn$$) < O($$n^2$$) < O($$n^3$$) < O($$2^n$$) < O($$n!$$) ...  
![](/assets/img/posts/algorithm/[1]time_complexity.png)
<br/>
<br/>

### 정렬 알고리즘 비교
|Sorting Algorithms|공간복잡도|시간복잡도|||
|:--:|--|--|--|--|
||최악|최선|평균|최악|
|Bubble Sort|O(1)|O(n)|O(n^2)|O(n^2)|
|Insertion Sort|O(1)|O(n)|O(n^2)|O(n^2)|
|Heap Sort|O(1)|O(nlogn)|O(nlogn)|O(nlogn)|
|Merge Sort|O(n)|O(nlogn)|O(nlogn)|O(nlogn)|
|Quick Sort|O(logn)|O(nlogn)|O(nlogn)|O(n^2)|
<br/>

---
#### reference
https://blog.naver.com/kks227/220769859177  
https://blog.chulgil.me/algorithm/
