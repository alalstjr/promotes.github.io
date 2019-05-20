---
layout:     post
title:      JSP MyBatis 란
author:     쭌프로
tags:       JAVA
subtitle:   JSP MyBatis 필기노트
category:   JAVA
---

<!-- Start Writing Below in Markdown -->

![Description](https://alalstjr.github.io/jjunpro.github.io/img/java_bg.png)

# MyBatis

1. 개발자가 지정한 SQL, 저장프로시저를 지원하는 프레임워크

2. 프로그램 소스 안에 SQL문을 작성하던 기존 JDBC 방식과 달리 SQL문을 프로그램에서 분리하여 XML 파일에 별도로 작성

3. MyBatis의 장점
  - 코딩량 절감
  - 간편한 유지보수 (SQL을 변경하고자 할 경우 기존처럼 프로그램을 수정하는 것이 아니라 
  XML 파일의 SQL문만을 변경하면 되기 때문에 SQL변환이 자유로움)
  
4. ibatis 라는 이름으로 2.5까지 개발

5. 3.0 버전부터 MyBatis로 이름이 바뀜

6. https://blog.mybatis.org/p/products.html 설치 주소

7. MyBatis 설정 방법
  - MyBatis-x.x.x.jar lib 폴더에 복사
  - MyBatisManager.java - MyBatis framework을 실행할 수 있는 세션
  - sqlMapConfig.xml - MyBatis 기본설정 파일
  - mapper 파일 - 실제 sql query문장
  
# MyBatis를 활용한 한줄 메모장

web.xml (배치기술서)

Controller
  - MemoController.java
  
Model
  - MemoDTO.java
  - MemoDAO.java

View
  - memo.jsp : ajax 요청 페이지, 메모입력
  - memo_list.jsp : 메모목록
  - memo_view.jsp : 메모 보기, 수정, 삭제 기능
  
## CRUD

- Create : insert
- Read : select
- Update : update
- Delete : delete

## 메모장 목록

list.do (web.xml에 맵핑)

Controller
  - MemoController.java

Model
  - MemberDAO.java
  - MemberDTO.java
  
View
  - memo_list.jsp
  
list.do => MemoController.java => MemoDAO.java = > 메모리스트 리턴 =>
request객체에 저장 => memo_list.jsp로 포워딩


# 참고자료

<a href="https://hyeonstorage.tistory.com/278">sqlMapConfig 코드</a>
<a href="https://hunit.tistory.com/200">sqlMapConfig-mysql 코드</a>
