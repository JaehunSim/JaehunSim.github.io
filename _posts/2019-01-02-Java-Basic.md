---

layout: post
title: "Java 기초 정리"
date: 2019-01-02 16:51:00
sitemap: 
  changefreq: daily
  priority: 1.0
comments: true

---

## Java Data Types

* Primitive Data Type
1. 문자형 char  
정수형에 포함될 수 있다.
2. 정수형  
고정값  
byte, short, int, long  
default: int  
3. 실수형  
근사값  
float, double  
default: double  

## Eclipse 시작
1. File-New-other  
2. make new Java class

## class 만든 이후  
1. 자동완성: ctrl + space  
2. ctrl + s: 저장 및 컴파일  
빨강색 줄: 컴파일 에러  
3. main, Sys

명령 프롬트: java  
eclipse: javaw.exe  
디버깅할때 javaw 프로세스를 죽이면 도움 될 수 있다.  

## Eclipse 기능
자리 맞출 때  
ctrl + i 누르면 자동정렬된다.  

## Java 문법

```
    for (int tmp: sizes2) {
			System.out.print(tmp + " ");
		}

		for (int i = 2; i <11; i++) {
    for (int j = 1; j <9; j++) {
			System.out.format("%5s",(i-1)*(2+j-1) + " ");
			}
			System.out.print("\n");
		}  

import java.util.Random;  
Random r = new Random();  
System.out.println(r.nextInt(45)+1);  

```
