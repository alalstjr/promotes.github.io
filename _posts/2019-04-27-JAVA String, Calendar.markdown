---
layout:     post
title:      JAVA String, Calendar
author:     쭌프로
tags:       JAVA
subtitle:   JAVA String, Calendar 정리노트
category:   JAVA
---

<!-- Start Writing Below in Markdown -->

![Description](https://alalstjr.github.io/jjunpro.github.io/img/java_bg.png)

# String Class

## 1. 문자열은 문자배열 char[] 로 처리됨

## 2. String 은 객체자료형이지만 자주 사용되므로 new 를 생략할 수 있슴

String str = "hello";
String str = new String("hello");

## 3. String의 내용 비교

A = "안녕";
B = "안녕";
A.equals(B)
A == B (주소값을 비교하므로 False 를 출력합니다.)

## 4. String의 사용 방법

new 연산자를 사용하지 않을 경우 Heap 내부의 String Constant Poll 에 생성되어 공유됩니다.
String str = "hello";

new 연산자를 사용하면 항상 새로운 문자열 인스턴스를 생성함
String str = new String("hello");

## 5. String 의 불변성(immutable) 

String 내용은 final 문자배열에 저장되며 수정할 수 없습니다.

String a = "hello";
참조변수 a는 String의 내용을 가리킴
String 내용은 
final char[] value = {'h','e','l','l','o'}; 
형식으로 저장됩니다.

a = "java";
새로운 String 이 만들어지고 a는 기존의 "hello"가 아닌 "java" 문자열을 가리키게 됩니다.

결론은 hello 의 메모리값은 사라지는것이 아닌 java 라는 문자열의 메모리가 새로 생기고
a 는 java 라는 문자열을 가리키게 되는것 입니다.

## String의 초기화

빈문자열("")과 null
String a = ""; 빈 문자열을 가리킴
String a = null; 가리키는 내용이 없음

null 
가리키는 내용이 없음, 값이 미정인 상태
참조변수가 가리키는 내용이 없는 상태에서 연산을 하게 되면
NullPointerException 이 발생합니다.

## 문자열과 기본형간의 변환

1. 기본형 값을 문자열로 바꾸는 방법
String str = 1000 + "";
String str = String.valueOf(1000);
이렇게 하면 int 형 은 문자형으로 변환되어 저장됩니다.

2. 문자열을 기본형 값으로 변환하는 방법
int a = Interger.parselnt("100");
int b = Interger.valueOf("100");
이렇게 하면 문자형은 int 형으로 변환되어 저장됩니다.

char c = "A".charAt(0); 문자열 "A" 를 문자 'A' 로 변화

3. StringBuffer, StringBuilder

String처럼 문자형 배열(char[]) 을 내부적으로 가지고 있다.
String클래스와 달리 내용을 변경할 수 있습니다.

StringBuilder sb = new StringBuilder("hello ");
sb.append("world");

원본 내용에 계속하여 추가합니다.

# Calendar 날짜

<script src="https://gist.github.com/alalstjr/87a9546ce46a527160ba99f2976dbe44.js"></script>
