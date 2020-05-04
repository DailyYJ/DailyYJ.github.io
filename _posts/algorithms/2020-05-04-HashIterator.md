---
title: "Hash Iterator 값 구하기"
date: 2020-05-04 
categories: Algorithm
tags: Hash 

---

<code>
	Iterator<String> keys = map.keySet().iterator();
	while(keys.hasNext()){
		String key = key.next();
		System.out.println(key, map.get(key));
	}
</code>

<code>
	for(String key : map.keySet()){
		System.out.println(key, map.get(key);
		}
</code>