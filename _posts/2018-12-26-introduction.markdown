---

layout: post
title: "스파크 목차 정리"
date: 2018-12-26 21:42:30
image: "/assets/images/spark_logo.png"
  changefreq: daily
comments: true

---

# 공부를 시작할땐 목차부터 

## Part1 빅데이터와 스파크 

### 1. 아파치 스파크란
1. 철학
2. 등장 배경
3. 역사
4. 현재와 미래
5. 실행
6. 정리

### 2. 스파크 간단히 살펴보기
1. 기본 아키텍처
2. 다양한 언어 API
3. API
4. 시작하기
5. sparkSession
6. DataFrame
7. Transformation
8. 액션
9. Spark UI
10. 종합예제
11. 정리.

### 3. 스파크 기능 둘러보기
1. 운영용 앱 실행
2. Dataset: 타입 안정성 제공하는 구조적 API
3. 구조적 스트리밍
4. 머신러닝, 고급분석
5. 저수준 API
6. sparkR
7. 스파크와 에코시스템, 패키지
8. 정리.

## Part2 구조적 API: DataFrame, SQL, Dataset

### 4. 구조적 API 개요
1. DataFrame과 Dataset
2. 스키마
3. 구조적 데이터 타입 개요
4. 구조적 API 실행 과정
5. 정리

### 5. 구조적 API 기본 연산
1. 스키마  
2. 컬럼과 표현식  
3. 레코드와 로우  
4. DataFrame Transformation  
5. 정리  

### 6. 다양한 데이터 타입 다루기  
1. where is API?  
2. 데이터 타입 변환  
3. boolean  
4. numeric  
5. string  
6. datatime, timestamp  
7. null  
8. sort  
9. 복합 데이터 타입  
10. json  
11. 사용자 정의 함수  
12. Hive UDF  
13. 정리  

### 7. 집계 연산 (group)  
1. 집계함수  
2. 그룹화  
3. 윈도우 함수  
4. 그룹화 셋  
5. 사용자 정의 집계 함수  
6. 정리  

### 8. 조인(join)  
1. 표현식  
2. 타입  
3. inner join  
4. outer join  
5. left outer join  
6. right outer join  
7. left semi join  
8. left anti join  
9. natural join  
10. cross join( cartesian join)  
11. 문제점, 주의 사항  
12. 수행 방식  
13. 정리  

### 9. 데이터소스  
1. 데이터 소스 API구조  
2. csv  
3. json  
4. parquet(파케이)  
5. orc  
6. sql db  
7. text  
8. 고급 I/O 개념  
9. 정리  

### 10. 스파크 SQL  
1. What is SQL  
2. 빅데이터와 SQL: Apache Hive  
3. Spark SQL  
4. sql 쿼리 실행 방법  
5. catalogue(목록)  
6. table  
7. view  
8. db  
9. select statement  
10. 고급 주제  
11. 다양한 기능  
12. 정리  

### 11. Dataset  
1. 사용할 시기  
2. 생성  
3. Action  
4. Transformation  
5. Join  
6. 그룹화와 집계(sum)  
7. 정리  
	
## Part3 저수준 API

### 12. RDD. Resilient Distributed Datasets (회복 가능한 분산 데이터셋)
1. What is 저수준 API?
2. RDD intro
3. RDD 생성
4. RDD 다루기
5. Transformation
6. Action
7. 파일 저장하기
8. 캐싱
9. 체크포인트
10. RDD를 시스템 명령으로 전송하기
11. 정리

### 13. RDD 고급 개념  
1. key-value 형태의 기초 (key-value RDD)  
2. 집계  
3. cogroup  
4. join
5. partition control
6. 사용자 정의 직렬화(serialization)
7. 정리

### 14. 분산형 공유 변수
1. broadcast variable
2. accumulator
3. 정리

## Part4  운영용 애플리케이션

### 15. 클러스터에서 스파크 실행
1. spark app architecture
2. life cycle(outside spark)
3. life cycle(inside spark)
4. 세부 실행 과정
5. 정리

### 16. 스파크 앱 개발
1. 앱 작성
2. 앱 테스트
3. 개발 프로세스
4. 앱 시작
5. 앱 환경 설정
6. 정리

### 17. 스파크 배포 환경
1. 앱 실행을 위한 클러스터 환경
2. 클러스터 매니저
3. 기타 고려사항
4. 정리

### 18. 모니터링, 디버깅
1. 모니터링 범위
2. 모니터링 대상
3. 스파크 로그
4. 스파크 UI
5. 디버깅 및 스파크 응급 처치
6. 정리

### 19. 성능 튜닝
1. 간접적 성능 향상 기법
2. 직적벅 성능 향상 기법
3. 정리

## Part5  스트리밍

### 20. 스트림 처리의 기초
1. What is 스트림 처리?
2. 핵심 설계 개념
3. 스파크 	
4. 정리		

### 21. 구조적 스트리밍의 기초
1. 기초
2. 핵심 개념
3. 활용
4. transformation
5. I/O
6. streaming dataset api
7. 정리

### 22. 이벤트 시간과 상태 기반 처리
1. 이벤트 시간 처리
2. 상태 기반 처리
3. 임의적인 상태 기반 처리
4. 이벤트 시간 처리의 기본
5. 이벤트 시간 윈도우
6. 스트림에서 중복 데이터 제거
7. 임의적인 상태 기반 처리(확장)
8. 정리

### 23. 운영 환경에서의 구조적 스트리밍
1. fault tolerence, 체크포인팅
2. 앱 변경
3. 메트릭과 모니터링
4. 알림
5. 스트리밍 리스터를 사용한 고급 모니터링
6. 정리

## Part6  고급분석과 머신러닝

### 24. 고급분석과 머신러닝 개요
1. 고급 분석 짧은 입문서
2. 스파크 고급 분석 툴킷
3. 고수준 MLlib 개념
4. MLlib 실제 사용
5. 모델 배포 방식
6. 정리

### 25. 데이터 전처리 및 피처 엔지니어링
1. 사용 목적에 따라 모델 서식 지정
2. 변환자
3. 전처리 추정자
4. 고수준 변환자
5. 연속형(continuous) 특징 처리
6. 범주형(categorical) 특징 처리
7. 텍스트 데이터 변환자
8. 특징 조작
9. 특징 선택
10. 고급 주제
11. 정리

### 26. 분류(Classification)
1. 활용 사례
2. 분류 유형
3. MLlib 분류 모델
4. 로지스틱 회귀
5. 의사결정트리
6. RF, GBT
7. Naive Bayes
8. 분류와 자동 모델 튜닝을 위한 평가기(Evaluation)
9. 세부 평가지표
10. 일대다 분류기
11. 다층 퍼셉트론
12. 정리

### 27. 회귀(Regression)
1. 활용 사례
2. MLlib 회귀 모델
3. 선형 회귀
4. 일반화 선형 회귀
5. DT
6. RF, GBT
7. 고급 방법론
8. 평가기와 모델 튜닝 자동화
9. 평가지표
10. 정리

### 28. 추천
1. 활용 사례
2. 교차최소제곱 알고리즘을 이용한 CF 구현
3. 추천을 위한 평가기
4. 성과 평가지표
5. Frequent Pattern 마이닝
6. 정리

### 29. 비지도 학습
1. 활용 사례
2. 모델 확장성
3. k-mean
4. binary k-mean
5. Gaussian Mixture 모델
6. Latent Dirichlet Allocation (NLP) 
7. 정리

### 30. 그래프 분석
1. 그래프 작성
2. 그래프 쿼리
3. 모티브(motifs) 찾기
4. 그래프 알고리즘
5. 정리

### 31. 딥러닝
1. What is 딥러닝?
2. 스파크에서 딥러닝 사용하는 법
3. 딥러닝 라이브러리
4. 딥러닝 파이프라인을 사용한 간단한 예제
5. 정리

## Part7 에코시스템

### 32. 언어별 특성: 파이썬(PySpark) 과 R(SparkR, sparklyr)
1. PySpark
2. R로 스파크 사용하기
3. 정리

### 33. 에코시스템과 커뮤니티
1. 스파크 패키지
2. 커뮤니티
3. 정리

### 부록 A 스파크 설치 및 실행  

### 부록 B 더블린 원정대: 스파크 서밋 2017 더블린 참관기  
