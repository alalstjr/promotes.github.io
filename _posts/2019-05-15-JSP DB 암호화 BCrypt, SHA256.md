---
layout:     post
title:      JSP DB 암호화 BCrypt, SHA256
author:     쭌프로
tags:       JAVA
subtitle:   JSP DB 암호화 BCrypt, SHA256 정리노트
category:   JAVA
---

<!-- Start Writing Below in Markdown -->

![Description](https://alalstjr.github.io/jjunpro.github.io/img/java_bg.png)

# 데이터베이스 암호화

1. 암호화의 중요성
  - 개인정보보호법에 의거하여 회원의 중요한 정보들(교유식별번호, 비밀번호, 바이오정보 등)은 반드시 암호화하여 처리해야 합니다.
  - 개인정보보호법에 의하여 비밀번호는 일방향 암호화를 해야 함(복호화 금지)
  
2. 대칭키 알고리즘
  - 암호화와 복호화에 같은 키를 사용하여 데이터를 암호화하고 복호화함
  
