---
title:  "C++ stl 비트셋(bitset)"
date: 2021-01-19 21:00:00
categories: 
- STL
tags:
---



[https://en.cppreference.com/w/](https://en.cppreference.com/w/) 를 참고했습니다.



## 선언 방법

```c++
#include <bitset> 
std::bitset<8> b1;
std::bitset<8> b2(42);
std::bitset<8> b3(std::string("110010"));
```

**bitset\<크기\> 변수명 (정수 or string)**



## 지원 연산

**~** : Bitwise NOT

**&** / **&=** : Bitwise AND

**\|** / **\|=** : Bitwise OR

**^** / **^=** : Bitwise XOR

**\<<** / **\<<=** / **\>>** / **\>>=** : Bitwise shift

**==** / **!=** : Equal to / Not equal to

**b[]** 로 접근이 가능하다



## 함수

**b.set()** : 모든 비트를 킨다.

**b.set($i$, [true, false])** : $i$번째 비트를 키거나 끈다.

**b.reset()** : 모든 비트를 끈다.

**b.reset($i$)** : $i$번째 비트를 끈다.

**b.flip()** : 모든 비트를 반전시킨다.

**b.flip($i$)** : $i$번째 비트를 반전시킨다.

<br/>

**b.count()** : 켜져있는 비트의 개수를 리턴한다.

**b.size()** : bitset의 크기를 리턴한다.

**b.test($i$)** : $i$번째 비트가 켜져있으면 true, 꺼져있으면 false를 리턴한다.

**b.any()**  : 비트가 하나라도 켜져있으면 true, 모두 꺼져있으면 false를 리턴한다.

**b.none()** : 비트가 모두 꺼져있으면 true, 하나라도 켜져있으면 false를 리턴한다.

**b.all()** : 비트가 모두 켜져있으면 true, 하나라도 꺼져있으면 false를 리턴한다.

<br/>

**b.to_string()** / **b.to_ulong()** / **b.to_ullong()** : 전체 비트를 string / unsigned long / unsigned long long 형으로 변환하여 리턴한다.
