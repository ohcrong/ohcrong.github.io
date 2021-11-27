---
layout: post
title:  "Java / Array"
subtitle:   "Java / Array"
categories: dev
tags: tdl
comments: true
---

# Java / Array

Array를 지금까지 아무 생각없이 사용했다.

Array도 '객체'라는 것을 다시 깨닫고 많이 부끄러웠다.

(이렇게 무지성 코딩이 무섭다)

```java
int[] a = new int[3];
```

단순하게만 생각해도 변수 선언이 아닌 

new를 붙여 객체 생성을 하고, a 변수를 통해 번지수를 쓰는 것이다.

그렇다면 Array를 왜 사용하는것일까?

같은 DataType에 한하여

보통 개별적인 변수 하나 하나 파라미터를 넘기거나 이동을 시킬 필요가 있을때

배열로 만들어 사용하면 이동이 쉽다.

또 번지수로 접근하기 때문에 기억공간 접근이 쉽다.

```java
public class App {
    public static void main(String[] args) throws Exception {
        //data 개별 이동
        int a = 10;
        int b = 20;
        int c = 30;
        
        sum(a,b,c);

        //data array로 이동
        int[] arr = new int[3];
        arr[0] = 10;
        arr[1] = 20;
        arr[2] = 30;
        
        arraySum(arr);
    }

    public static void sum(int x, int y, int z){
        int sum = 0;
        sum = x + y + z;
        System.out.println(sum); //60
    }
    
    public static void arraySum(int[] temp){
        int sum = 0;
        for(int i=0; i<temp.length; i++) {
            sum+=temp[i];
        }
        System.out.println(sum); //60
    }
}
```

즉, Array는 장바구니라고 생각하면 편하다.

과자를 3개던 10개던 두손으로 계산대까지 이동하는것보다 

'new'를 통해 '객체 생성'을 하여 장바구니를 만들어 놓고 담아 쓰면 더 편하기 때문에 쓰는것이 아닐까

단, 같은 카테고리 품목만 담도록 하자!