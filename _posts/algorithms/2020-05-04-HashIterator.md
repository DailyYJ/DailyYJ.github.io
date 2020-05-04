---
title: "Hash Iterator 값 구하기"
date: 2020-05-04 
categories: Algorithm
tags: Hash 
---

## Hash Iterator

> <b>첫번째 방법</b>

```java
Iterator keys = map.keySet().iterator();
	while(keys.hasNext()){
		String key = key.next();
		System.out.println(key, map.get(key));
	}
```

> <b>두번째 방법</b>

```java
for(String key : map.keySet()){
		System.out.println(key, map.get(key);
		}
```