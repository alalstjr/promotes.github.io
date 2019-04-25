---
layout:     post
title:      JAVA static, final 다형성
author:     쭌프로
tags: 		  JAVA
subtitle:   JAVA static, final 정리노트
category:   JAVA
---
<!-- Start Writing Below in Markdown -->

# static 

정지의 상태, 고정적인, 변화가 없는

## static member

static variable(정적 변수)
static method(정적 메소드)
어디서든 공유해서 사용할 수 있는 변수, 메소드

## static member의 특징

프로그램이 실행되면 메모리(클래스 영역)에 자동으로 로딩됨
프로그램이 끝날 때까지 메모리에 상주함
<b>static method 에서는 static member 만 사용 가능함</b>
<script src="https://gist.github.com/alalstjr/847f5a20446721d391503e6c5b1049ee.js"></script>

단하나의 static 변수만 존재가능합니다.
그러므로 new 를 통해서 객체를 아무라 생산해도 
static 변수는 단 하나만 변경없이 고정으로 존재합니다.

## dynamic member의 특성

프로그램 실행 중에 필요할 때 만들어지고 필요 없으면 삭제됨
stack, heap 영역에 저장됨
메모리 측면으로는 dynamic member 변수가 활용이 더 높다.

# final 

final이 붙은 요소는 변경할 수 없습니다.

final variable 변수 값을 변경할 수 없습니다.
final method  오버라이딩이 금지됩니다.
final class 상속이 금지됩니다.

final 은 최종의 단계이기 때문에 무엇하나 변경하며 상속해줄 수 없습니다.

# 다형성(polymorphism)

여러 가지 형태를 가질 수 있는 능력
하나의 참조변수로 여러 자료형의 객체를 참조할 수 있는 것
Object a = 10;
Object a = 10.5;
Object a = "문자열";

간단하게 예제를 만들어 보았습니다.

<script src="https://gist.github.com/alalstjr/f050cbff7925d8e39933009fae19297e.js"></script>

결과 b 객체와 a 의 객체는 각각 어떤 int a 변수의 값을 출력할까요?

첫번째
BB b = new BB();
b.print();
BB객체의 변수 내부의 a 의 값 20 을 의미합니다.
결과는 20 입니다. 
(super.print 를 할경우 부모 값의 print를 하는것이므로 10을 출력하게 할 수 있습니다.)

두번째
AA a = new BB();
a.print();
여기서도 그러면 AA 객체의 변수 내부의 a의 값 10 을 가져와야하지만
실질적으로 메모리에는 BB객체가 올라가 있기때문에 
결과는 20을 출력합니다.

