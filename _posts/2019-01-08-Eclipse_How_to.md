---

layout: post
title: "Eclipse 단축키 및 사용법"
date: 2019-01-08 11:09:00
sitemap: 
  changefreq: daily
  priority: 1.0
comments: true

---

# Eclipse shortcut(단축키)

## 실행 및 새로고침
*Ctrl + F11* : 실행  
*F5* : refresh

## 코드 찾기, 선택, 이동
*ctrl + ,* : 다음 에러, 워닝으로 점프  
*ctrl + L* : 해당 라인으로 이동  
*alt + shift + 방향키* : 블록 선택  
*ctrl + k* : 다음 문자열 찾기  
*ctrl + D* : 한 줄 삭제  
*F2*: 컴파일 에러 힌트 제공  

## 자동 완성 기능
*ctrl + shift + o* : 자동으로 import  
*ctrl + I* : 들여쓰기 자동 수정  
*ctrl + shift + F* : 코드 자동 정리!  
*main, sysout, try, for + ctrl+space*: templates  
*alt + shift + s*: OOP 관련 templates
*ctrl + space* : 자동 완성  
*ctrl + 1* : 에러 수정

## 화면 컨트롤
*ctrl + shift +* : 코드 크기 확대  
*crl + shift + -* : 코드 크기 축소  
*ctrl + M* : 전체화면 토글  
*ctrl + F6* : 코드 탭간 이동  

## 디버깅
*F5* : Step into, shift+F5를 하면 필터 설정한 클래스에 대해서 step over할 수 있음  
*F6* : Step Over: 현재 명령문을 실행하고 다음 명령문 직전에 다시 멈춤, 한줄씩 실행  
*F7* : Step Return: 현재의 메소드에서 리턴한 직후에 다시 멈춘다.  
*F8* : Resume: 멈추어 있던 쓰레드를 다시 계속 실행, 디버깅 계속  
*F11* : 디버깅 시작  
*ctrl+ R* : 현재 라인까지 실행  

## Display view vs Expression View
소스상에서 필요한 부분을 선택해서 실행 ,한 순간의 값만 필요할 때 볼 수 있음  
복잡한 식, 객체를 디버깅하면서 계속 볼 수 있는 창, 마우스 오른버튼 -> 감시 표시식 추가선택후 사용  
> Quick Access 에서 Variables를 검색후 사용하면 디버깅할 때 정말 편하다.  

## Refactoring
Pull down, Push up  
클래스 관리시 필요
