# 날짜별 기록

## 0921
(라이브 세션)

[ 피드백 ]

(기획안)
1. 메소드 열 추가해서 작성해주기
2. ci/cd에 대해 고민해보기
3. 근태 일정 공유

(전체)
1. http method : get, post, put, delete, PATCH VS POST? (patch 반드시 사용)
2. API login 전/후
3. 기술 스택 : springboot, java8, orm(jpa), db(변경 가능, 변경하면 따로 말씀드리기)
			+ "spring security"
4. "R&R" : 각 팀원 역할 상세 -> 역할 4개를 매 주차별로 돌아가면서 맡기
			- scrum master
			- pm(team leader)
			- 서기(노션) : 의견 종합해서 정리
			- tech leader(cto)
5. code review - github
	노션 하단 github 사용법 확인


cf) micorsoft - marketplace (소프트웨어 라이센스 관리 프로그램)



[ 수업 ]
* 스프링
  - 자바 기반 동적 웹 개발을 위한 오픈 소스 어플리케이션 프레임워크
  - functional programming
  - di / ioc
  - java 객체의 라이프 사이클을 관리

* 어노테이션
  - 자바 어노테이션
  - 사전적 의미로는 주석
  - @를 이용해서 자바 코드에 의미를 부여하기 위해 붙이는 포스트잇 같은 개념
	ex) @Override <- method에 붙임
		=> 적어주고 안 적어주고의 차이
  - 용도
	1) 컴파일러에게 syntax error를 체크하도록 알려줌
	2) 빌드, 배치할 때 코드를 자동으로 생성하도록 알려줌
	3) 실행(컴파일) 특정 기능을 실행하도록 알려줌

* di
  - 의존성 주입 HOW?

* 문제
  - Q. classA가 필요한 객체를 직접 만들지 않고 classB 객체를 갖고 싶으면 어떻게?
  - A. classA가 classB에 의존하지 안흔ㄴ 3가지 방법
	(1) 객체를 필요로 하는 method의 매개변수로 받기
	(2) classA의 생성자 매개변수로 받아서 classA의 필드로 넣어주기 (매개변수 받은 걸 this.~)
	(3) Spring @Autowired를 필드 위에 추가해주기

* IoC
  - inversion of control (제어권의 역전)
  - 제어권을 직접 갖지 않고, 그 외부에서 객체(의존성) 제어권을 가지는 것

* *spring DI + IoC*
  - Sprig Dependency Instance
  - 스프링이 모든 의존성 객체를 생성도 해주고, 필요한 클래스/메소드에 주입
  - = 제어의 흐름을 스프링에게 맡긴다

* *Spring IoC Container*
  - bean = ioc container의 객체
  - 개발자가 클래스에 '----' 해주면 스프링이 그걸 보고 bean으로 생성/보관
  - 개발자가 그 객체가 필요한 클래스에 '-----' 해주면, 스프링이 그걸 보고 의존성 주입

- 현업에서 일할 땐 aws 사이트에 있는 정도(만) 알면 됨 (매우 많음 ㅎㅎ;)

* REST API
  - uri는 정보의 자원을 표현해야 한다
  - 자원에 대한 행위는 HTTP mthod로 표현한다
  - http 장점을 극대화하여 데이터를 전송하는 방법을 구현하는 것

* functional programming = fp
  - 프로그래밍이 지향하는 바가, "함수(메소드)"
  - 객체 지향 vs 절차 지향

</br>


## 0922
(scrum & 멘토링)

</br>

## 0923
(scrum)
- 노션에 작성

(학습)
* git 계정 여러개 관리
https://gist.github.com/Jonalogy/54091c98946cfe4f8cdab2bea79430f9
https://yosuniiiii.com/github-%EA%B3%84%EC%A0%95-%EC%97%AC%EB%9F%AC%EA%B0%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-on-mac-6588237f9671

* pull request
https://inpa.tistory.com/entry/GIT-%E2%9A%A1%EF%B8%8F-%EA%B9%83%ED%97%99-PRPull-Request-%EB%B3%B4%EB%82%B4%EB%8A%94-%EB%B0%A9%EB%B2%95-folk-issue

* git action
학습 예정

* git branch 전략
- [git flow 세가지 전략](https://ujuc.github.io/2015/12/16/git-flow-github-flow-gitlab-flow/)

</br>

## 0926
* 미션 진행

(scrum)


## 0927
(녹화 강의)


</br>

# 라이브세션 미션

</br>
