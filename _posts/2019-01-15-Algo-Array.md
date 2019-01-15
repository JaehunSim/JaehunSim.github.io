---

layout: post
title: "알고리즘 - Array"
date: 2019-01-15 09:30:30
sitemap:
  changefreq: daily
comments: true

---

# [#1210 SW Expert Academy](https://www.swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV14ABYKADACFAYh)

사다리를 Array로 표현하고 골인지점이 어디인지를 찾는 문제이다.

![](https://raw.githubusercontent.com/JaehunSim/JaehunSim.github.io/master/assets/images/SWAcademy/ladder.png)

일단 10 by 10 사다리 문제부터 풀고 100 by 100으로 확장하는게 이해하는데 좋다.
문제를 풀때의 방법으로 두가지 방법이 있다.
1. 맨윗줄 사다리부터 출발해서 모든 경우에 대해 사다리를 내려가본 후
목표 지점에 도착하는 시작점 index를 반환해줄 수 있다.
2. 맨 아랫줄 목표지점부터 시작해서 목표지점이 거꾸로 사다리를 올라가 어느 시작점으로부터 시작하는지 index를 구해본다.

둘 다 방법은 똑같지만 시간 소요 면에서 2번이 좀 더 효율적이다. 2번방법으로 문제를 풀어보자.

일단 빈 2차 배열을 만들어 준다.
만들어진 빈 2차 배열에 사다리 입력값을 넣어준다.
그 다음 마지막줄에서 2를 찾는다.(목표지점이다)

2를 찾았으면 
1. #up 
2. #left or #right
을 어떻게 시행할건지 고민해보고 알고리즘을 짜본다.
2를 임의로 지정해서 어느 지점에서 시작하든 시작점을 찾을 수 있게끔 알고리즘을 짜야한다.

사다리를 올라가는 경우 옆에 길이 있으면 옆으로 빠져야만 한다.
좌측이나 우측에 사다리가 있는지 계속 체크하면서 올라가면 이를 해결할 수 있다.
이 때 어느 방향인지 direction 값에 저장한다.

사다리를 왼쪽이나 오른쪽으로 타는 경우
한칸씩 이동 후 위에 길이 있다면 멈춰야 한다.

up이나 left,right 코드를 짯다면 
이를 일반화 할 수 있어야 한다.
index, height와 같은 키워드를 이용해 추상화를 잘 한다면 코드를 이해하기 쉽게 잘 짤 수 있다.
처음에는 i, j와 같이 날코딩으로 원하는 결과값만 나오게끔 짜도 좋다.
그러나 점점 일반화를 하면서 변수에 적절한 이름을 붙여준다.

마지막으로 up과 left,right를 반복 시행하면서 height가 0일때, 즉 사다리 꼭대기까지 올라왔을 때 멈출 수 있게 flag 기능을 넣어준다.

여러가지 목표지점에 대해 일관적으로 시작점을 찾아낸다면 문제를 해결한 것이다.
이제 100 by 100의 input을 받아보고 testcase에 대해서 정답이 나오는지 체크하면 된다!

`` 7. When stack memory is full, Java runtime throws java.lang.StackOverFlowError whereas if heap memory is full, it throws java.lang.OutOfMemoryError: Java Heap Space error. ``


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
