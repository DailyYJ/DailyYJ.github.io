---
title: "프로그래머스 가장 큰 수"
date: 2020-05-01 
categories: -Algorithms
			-Programmers
tags: programmers
---
<pre>
<code>
'''java
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
'''
</code>
</pre>
