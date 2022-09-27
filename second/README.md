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
- 우선 순위 다시 정하기
- 회원가입은 스크립트보단 기능으로 추가하여 3순위
- ci 정도 고려해보면 좋겠다
- 옵션에 따라 가격 달라지게끔??
- 역할 정하기 (매주 돌아가면서)
- 매주 팀 계획과 요구사항 : 스프린트
- 스프린트
- 프로젝트 세팅
- 이슈 템플릿? pr 템플릿???
- 멘토님 깃헙 리뷰어 지정???? @marco

</br>

## 0923
(scrum)
- 노션에 작성

(학습)
* git 계정 여러개 관리
	- https://gist.github.com/Jonalogy/54091c98946cfe4f8cdab2bea79430f9
	- https://yosuniiiii.com/github-%EA%B3%84%EC%A0%95-%EC%97%AC%EB%9F%AC%EA%B0%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-on-mac-6588237f9671

* pull request
	- https://inpa.tistory.com/entry/GIT-%E2%9A%A1%EF%B8%8F-%EA%B9%83%ED%97%99-PRPull-Request-%EB%B3%B4%EB%82%B4%EB%8A%94-%EB%B0%A9%EB%B2%95-folk-issue

* git action
	- 학습 예정

* git branch 전략
	- [git flow 세가지 전략](https://ujuc.github.io/2015/12/16/git-flow-github-flow-gitlab-flow/)

</br>

## 0926
(학습)
* CI
	- [git action](https://insight-bgh.tistory.com/m/473)
* 라이브세션 미션

</br>

## 0927
* 라이브세션 


</br>

# 라이브세션 개인 미션

* WebFlux
	- [노션 학습 미션](https://www.notion.so/prgrms/5c622ce04dc54082a35b2428cd436626?v=0f5c73169d394488a16d22ab5b42d5d7&p=756db898758f41a1b37fdf034a0cd963&pm=s)
	
* functional programming
	- programming paradigm where programs are constructed by applying and composing functions
	- Avoids changing State and Mutable data (상태, data 변경을 지양) -> 대입문 사용 x, 지역 변수 제거...
	- 모든 것을 순수 함수로 나누어 문제를 해결하는 기법으로, 작은 문제를 해결하기 위한 함수를 작성하여 가독성을 높이고 유지보수를 용이하게
	- 순수 함수 + 1급 시민(객체) + 참조 투명성
		- 순수 함수 = 부수효과 x, 외부에 영향 x, 독립성
		- *1급 시민(객체) = '함수'를 '매개변수', '반화값'으로 사용 가능, 변수/데이터 구조 안에 담을 수 있음, 고유성*
		- 참조 투명성 = 동일 인자는 항상 동일 결과값, 기존값 항상 유지(변경 x)
	- https://mangkyu.tistory.com/111

* 객체지향 vs 절차지향
	- 객채 지향
		: 실제 세계 모델링
		: 기능과 속성을 한 곳에서 관리하는 방식
		: 프로그램을 명령어의 목록이 아닌, 여러개의 독립된 단위인 객체들의 모임으로 파악하고자 하는 프로그래밍 기법
		: (1) 캡슐화 : 관련 데이터와 코드를 하나의 묶음으로 정리, 데이터를 감추고 외부와의 상호작용은 메소드를 통해서
		: (2) 상속 : 이미 작성된 클래스를 이어 받아 새로운 클래스 생성. 기존 코드 재활용
		: (3) 다형성 : 동일 작업 함수에 똑같은 이름 부여 가능
	- 절차 지향
		: 순차적 처리
		: 코드의 순서가 바뀌면 동일한 결과를 보장하기 어려움
		: 컴퓨터의 처리구조와 유사해 실행속도가 빠름
	- https://brownbears.tistory.com/407
	
* REST API
	- AWS : https://aws.amazon.com/ko/what-is/restful-api
	- NHN : https://meetup.toast.com/posts/92

* Annotation
	- @Component
		- container가 생성될 때 component scan을 통해 자동으로 spring ioc conatiner 빈 등록, 해당 클래스의 객체를 빈으로 관리
		- ex) @Controller, @Service, @Repository
		- 개발자가 직접 작성한 class를 bean으로 등록하기 위해 사용 ( cf) @Bean : 개발자가 직접 제어 불가능한 외부 라이브러리 등을 bean으로 만들 때 이용 )
	- @Autowired
		- 필요한 의존 객체 '타입'에 해당하는 bean을 찾아 의존성 주입
		- 해당 변수 및 메서드에 spring이 관리하는 bean을 자동으로 맵핑해줌
		- 생성자, setter 메서드, field(변수, 일반 메서드)에 사용 가능
		- 기본값이 true이기 때문에, 의존성 주입 대상을 찾지 못한다면 어플리케이션 구동에 실패함
		- cf) '이름'으로 의존성을 주입하는 어노테이션은 @Resource (변수, setter 메서드에 사용, bean이 map 타입인 경우에 사용)
		- https://devlog-wjdrbs96.tistory.com/166
		- https://life-with-coding.tistory.com/433
	
	- IoC container에 bean으로 등록이 된 후에 의존성 주입(DI)가 가능함
	
* Quiz
	- *개발자가 클래스에 '---' 해주면 spring이 bean으로 생성해주고 보관해줌*
  	- *개발자가 그 객체가 필요한 클래스에 '---' 해주면, spring이 그것을 보고 의존성 주입*
  	- -> 정답 : (1)@Componenet 관련(bean 등록 관련) annotation 달기 (2)@Autowired (의존성 주입) annotaion 달기
</br>
