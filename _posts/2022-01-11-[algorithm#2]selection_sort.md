---
layout: post
title:  "선택 정렬(selection sort)"
summary: "선택 정렬은 현재 위치에 들어갈 알맞은 값을 찾는 정렬 알고리즘이다."
author: aheunkim
date: '2022-01-11 17:11:00 +0900'
category: algorithm
thumbnail: /assets/img/posts/algorithm/thumbnail.jpg
keywords: sort algorithm, selection sort
permalink: /blog/algorithm/selection_sort/
usemathjax: true
---

## 선택 정렬이란?
선택 정렬은 이름에 맞게 현재 위치에 들어갈 값을 찾아 정렬하는 배열 알고리즘이다.  
* 최소 선택 정렬 : 오름차순
* 최대 선택 정렬 : 내림차순  
<br/>
  
오름차순으로 정렬할 때, **가장 작은 숫자의 인덱스를 기억했다가 비교가 끝나면 마지막에 swap**
1. 정렬되지 않은 인덱스의 맨 앞부터 최솟값을 찾는다.
2. 최솟값을 찾으면, 그 값을 현재 인덱스의 값과 바꿔준다. (swap)
3. 다음 인덱스에서 위 과정을 반복해준다.  
<br/>
  
시간복잡도 : n-1, n-2, ···, 1개씩 비교를 반복하므로 **O(n^2)**  
공간복잡도 : 하나의 배열에서만 진행하므로 **O(n)**  
![](/assets/img/posts/algorithm/[2]selection_sort.gif)  
<br/>
<br/>

### 💎코드
```c++
/* selection sort */
#include <bits/stdc++.h>
using namespace std;
 
void SelectionSort(int arr[], int length)
{
    for(int i=0; i<length; i++)
    {
        int idx = i;    //arr[i~length-1]사이의 최솟값 인덱스 저장
        for(int j=i+1; j<length; j++)
            if(arr[idx] > arr[j])
                idx = j;
 
        swap(arr[i], arr[j]);
    }
}
 
int main()
{
    int arr[10] = {5, 6, 10, 4, 3, 8, 7, 1, 2, 9};
 
    SelectionSort(arr, 10);
 
    //확인
    for(int i=0; i<10; i++)
        cout << arr[i] << " ";
 
    return 0;
}
```
내림차순으로 하려면, 11번째 줄의 부등호를 반대로 해주면 된다.
<br/>

---
##### reference
* 기본 정렬 알고리즘(Sorting Algoritm) 요약 정리 (선택, 삽입, 버블, 합병, 퀵) v1.1 ―https://hsp1116.tistory.com/33