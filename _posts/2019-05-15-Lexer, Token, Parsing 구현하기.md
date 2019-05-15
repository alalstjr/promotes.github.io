---
layout:     post
title:      Lexer, Token, Parsing 구현하기
author:     쭌프로
tags:       JAVA 자료구조
subtitle:   Lexer, Token, Parsing 연습코드
category:   JAVA
---

<!-- Start Writing Below in Markdown -->

![Description](https://alalstjr.github.io/jjunpro.github.io/img/java_bg.png)

공부하면서 작성한 <b>주관적인 개인 노트</b>입니다. <br/>
내용이 정확하지 않습니다.

# Lexer, Token, Parsing 란 무엇인가?

<a href="Lexer, Token, Parsing 개념정리">Lexer, Token, Parsing 개념노트 바로가기</a>

# Lexer (어휘 분석)

어떠한 기준으로 토큰을 생성하여 저장 할 것인지 <br/>
Class Enum TokenType 를 생성하여 기준을 만들어 줍니다.

<script src="https://gist.github.com/alalstjr/ac41ff8d8c03ccade36b7504ed86052b.js"></script>

TokenType 에는 두가지 형태로 토큰을 나누었습니다.
<b>형태가 없는 토큰</b> 과 <b>형태가 있는 토큰</b>

## 형태가 없는 토큰

공백 혹은 주석 등등 토큰에 저장될 필요가없는 목록입니다.

## 형태가 있는 토큰

문자열 혹은 숫자 등등 토큰에 저장되어야 하는 목록입니다.

isAuxiliary() 메서드로 토큰의 형태를 확인합니다. <br/>
lexer 검색도중 형태가 없는 토큰이 매칭되면 true 를 반환합니다.

# Token 객체생성

<script src="https://gist.github.com/alalstjr/8ad3cd9486fac6561274e8745bb9e596.js"></script>

Token의 객체 상태(State)와 필드(field)를 작성합니다.

# 참고자료

<a href="http://woowabros.github.io/tools/2017/07/10/java-enum-uses.html">우아한 형제들 - Java Enum 활용기</a>
<a href="https://mainpower4309.tistory.com/15">[자바/JAVA 개발] 자바 Enum 클래스란??</a>
