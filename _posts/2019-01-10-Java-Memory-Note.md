---

layout: post
title: "Java 메모리 정리"
date: 2019-01-10 14:00:00
sitemap: 
  changefreq: daily
  priority: 1.0
comments: true

---

# 자바 메모리 구조

자바는 메모리를 크게 Java Heap Space, Java Stack Memory 두가지로 구분해서 생각하면 좋다.  
파이썬을 하다보면 메모리 에러가 가끔 뜨는데

1. 너무 큰 파일을 불러올 때 Out of memory error
2. Recursion 함수를 쓸 때 Stack overflow error  

이 두가지가 있다. 각 에러가 Heap, Stack memory와 관련 있는 것 같다.  

https://www.journaldev.com/4098/java-heap-space-vs-stack-memory  

여기서 정확한 정보를 얻을 수 있다.  

`` 7. When stack memory is full, Java runtime throws java.lang.StackOverFlowError whereas if heap memory is full, it throws java.lang.OutOfMemoryError: Java Heap Space error. ``

다음은 Sample 코드와 그에 대한 메모리 그림이다. Reference는 위의 링크에서!  
Stack Memory를 이해하기 좋은 예시 같다.

~~~ Java

package com.journaldev.test;

public class Memory {

	public static void main(String[] args) { // Line 1
		int i=1; // Line 2
		Object obj = new Object(); // Line 3
		Memory mem = new Memory(); // Line 4
		mem.foo(obj); // Line 5
	} // Line 9

	private void foo(Object param) { // Line 6
		String str = param.toString(); //// Line 7
		System.out.println(str);
	} // Line 8

}

~~~

![](https://cdn.journaldev.com/wp-content/uploads/2014/08/Java-Heap-Stack-Memory.png)

다음으로 Java Heap Space를 좀 더 알아보자. 이것을 이해해야 Java Garbage Collection을 잘 이해할 수 있다.  

https://www.journaldev.com/2856/java-jvm-memory-model-memory-management-in-java

![](https://cdn.journaldev.com/wp-content/uploads/2014/05/Java-Memory-Model.png)

이 그림은 힙 메모리의 구조를 보여준다. Perm은 힙 메모리에 포함 안 된다.  
크게 Young Generation, Old Generation으로 나눌 수 있다.  
힙 메모리의 각 구조 크기를 runtime 때 조절할 수 있다. 

