---
title: "프로그래머스 가장 큰 수"
date: 2020-05-01 
categories: Algorithm
tags: programmers
---
## 프로그래머스 가장 큰 수

## Problems
0 또는 양의 정수가 주어졌을 때, 정수를 이어 붙여 만들 수 있는 가장 큰 수를 알아내 주세요.

예를 들어, 주어진 정수가 [6, 10, 2]라면 [6102, 6210, 1062, 1026, 2610, 2106]를 만들 수 있고, 이중 가장 큰 수는 6210입니다.

0 또는 양의 정수가 담긴 배열 numbers가 매개변수로 주어질 때, 순서를 재배치하여 만들 수 있는 가장 큰 수를 문자열로 바꾸어 return 하도록 solution 함수를 작성해주세요.

## 제한사항
-numbers의 길이는 1 이상 100,000 이하입니다.</b>
-numbers의 원소는 0 이상 1,000 이하입니다.</b>
-정답이 너무 클 수 있으니 문자열로 바꾸어 return 합니다.</b>

## 입출력 예

numbers|returns
--------------|---------|
[6, 10, 2]|"6120"|
[3, 30, 34, 5, 9]|"9534330"|

```java
import java.util.*;
class Solution {
    public String solution(int[] numbers) {
        String answer = "";
        String[] st = new String[numbers.length];
        for(int i = 0; i < numbers.length; i++){
            st[i] = Integer.toString(numbers[i]);
        }
        Arrays.sort(st, new Comparator<String>(){
           @Override
            public int compare(String a, String b){
                if(a.charAt(0) == b.charAt(0)){
                    int ab = Integer.parseInt(a+b);
                    int ba = Integer.parseInt(b+a);
                    return ba - ab;
                }else{
                    return b.charAt(0)-a.charAt(0);
                } 
            }
        });
        StringBuilder sb = new StringBuilder();
        for(String i: st){
            sb.append(i);
        }
        return sb.toString();
    }
}
```

