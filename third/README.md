# 날짜별 기록

## 0928
(라이브세션)
* 좋은 코드란?
  - 메모리, 시간이 효율적인 코드 : stack, heap... 메모리 영역을 시스템 따라서 조절해야할 수 도 있음
  - 주석이 없어도 잘 읽히는 코드 : 로직 클린 코드
  - 유지보수 쉬운 코드 : functinal programming, module
  - 가독성, 컨벤션...
* docker : 데몬 실행 후 컨테이너를 돌려야함
* 쿠키 vs 세션

(학습)
* Spring Security
  - 보안(authentication + authorization + protection) Spring Framework
  - 인증 -> 인가(접근 권한 확인)
  - 공식 docs : https://docs.spring.io/spring-security/reference/index.html
  - https://mangkyu.tistory.com/76
  - https://dev-coco.tistory.com/174

</br>

## 0929
(학습)
* Spring Security
  - 'filter' 흐름
  - Client (request) → Filter → DispatcherServlet → Interceptor →  Controller(실제로 Interceptor가 Controller로 요청을 위임하는 것은 아님, Interceptor를 거쳐서 가는 것)
* Swagger UI
  - 기본 -> 도메인 별로 구분하여 보기 힘듦
    - commonApi
  - 전체 -> 도메인 별로 구분하여 볼 수 있음
    - base를 package에 두기
    - [예시](https://github.com/bacchusdd/MileageSystem/blob/master/src/main/java/com/example/triple/config/SwaggerConfig.java)
  - 사용법
    - @ApiIgnore : 제외하고 싶은 controller 위에 붙여주기
    - extends WebMvcConfigurationSupport -> registry.addResourceHandler
      - ???
      
  - https://nahwasa.com/entry/%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8-Swagger-UI-300-%EC%A0%81%EC%9A%A9-%EB%B0%A9%EB%B2%95-%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8-22-%EC%9D%B4%EC%83%81-Spring-Boot-Swagger-UI
  - https://velog.io/@wotj7687/Spring-Boot-Swagger-3.0.0-%EC%A0%81%EC%9A%A9

(scrum & project)
* Swagger UI 설정
* git 올리는 방식 : issue 통해 branch 생성 -> 코드 commit/push -> pull reqeust 통해 리뷰 받고 branch에 합치기

</br>

## 0930
(학습)
* 팀미션, 개인미션
* Java :: (더블 클론)
  - 메소드 레퍼런스, 람다식과 유사
  - 인스턴스 활용하여 메소드 전달
  - class/참조변수 이름 :: method 이름
* Java 람다식
  - https://khj93.tistory.com/entry/JAVA-%EB%9E%8C%EB%8B%A4%EC%8B%9DRambda%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B4%EA%B3%A0-%EC%82%AC%EC%9A%A9%EB%B2%95
(scrum with 멘토님)
* 특이 사항 없음

</br>

## 1003
* 
</br>

## 1004
* 미션 학습
* 다대다 관계 맵핑
* repository 의존성 주입 안 되는 거 해결 못함...


# 라이브세션 미션
* optional + stream
  - *stream*
    - A sequence of elements supporting sequential and parallel aggregate operations.
    - data 읽기만, 변경 x
    - 일회용
    - 계산식 람다 표현이 중요 (jvm에게 람다식 넘겨주어 계산)
    - collection보다 가볍게 (메모리 사용 낮추며) 사용 가능
    - filter(조건 걸러주기), map(조건 해당 값 반환), flatMapto~(중첩구조 개선), sorted, collcet(결과 요약), collectors(결과 분할)
    - https://www.baeldung.com/java-8-collectors
  - *optional*
    - A container object which may or may not contain a non-null value.
    - NPE 방지 위해 사용
    - Optional<T> : null이 올 수 있는 값을 감싸는 Wrapper 클래스
      - 참조하더라도 NPE가 발생하지 않도록 도와줌
      - Optional 클래스는 value에 값을 저장하기 때문에 값이 null이더라도 바로 NPE가 발생하지 않으며, 클래스이기 때문에 각종 메소드를 제공
    - https://mangkyu.tistory.com/70
  - https://velog.io/@gjrjr4545/JAVA-8-3-Stream-Optional%EC%9D%98-%EB%93%B1%EC%9E%A5
* stream method 중 findAny(), findFirst()
  - stream에서 일치하는 요소 1개 찾을 때 사용
  - stream 직렬 처리 시 둘 차이 x
  - stream 병렬 처리 시 반환값 달라짐 ( stream().parallel(),filter() )
    - findAndy() : stream에서 가장 먼저 찾은 요소 반환. stream 상 순서가 앞이라는 보장 x
    - findFirst() : filter 조건에 맞는 요소들 중 stream에서의 순서가 가장 앞인 요소 반환
  - https://codechacha.com/ko/java8-stream-difference-findany-findfirst/
* jwt
* **쿠키 vs 세션 vs 토큰 (vs 캐시)**
  - Cookie
    - 사용자 정보를 사용자 브라우저의 '쿠키'에 저장
    - 쿠키이름, 쿠키값, 만료시간, 전송할 도메인명, 전송할 경로, 보안연결여부, HttpOnly여부 등으로 구성
  - Session
    - 브라우저가 종료되기 전까지 클라이언트의 요청을 유지하게 해주는 기술
    - 사용자의 인증 정보가 서버의 세션에 저장됨
    - stateless한 HTTP protocol 이용시 정보를 저장하기 위해
    - 브라우저는 모든 요청에 사용자가 누구인지 알리는데 사용
  - Token
    -	토큰 기반 인증에서는 쿠키&세션 사용 x
    -	토큰 : 서버로의 모든 request에 대해 유저를 인증하기 위해 사용
    - 인증 정보를 클라이언트가 직접 들고 있는 방식
    -	Token format : jwt(bearer), oauth,
    -	Authentication(인증:신원 확인) vs Authorization(승인:권ㅇ한 부여)
    -	Stateless = connection등의 상태 정보를 저장하지 않음
    -	독립적 : http request를 생성할 수 있는 클라이언트라면 누구든지 서버로 요청 보낼 수 있으며, 
    -	No CSRF(no cookie-session) : autherntication header 내에 token이 포함되기 때문에 CSRF 방지
    -	서버는 토큰만 방지, 저장은 클라이언트만!

* Spring 공통 업무 중복 코드 제거 위한 방법
  - filter
    - 요청/응답을 걸러줌 : dispatcher servlet에 요청 전달되기 전후에 url-pattern에 맞는 모든 요청에 대해 부가 작업을 처리할 수 있도록
    - 요청/응답이 spring container가 아닌, spring 외부 **web container** (tomcat...)에 의해 관리됨
    - javax.servlet의 Filter interface 구현하여 사용
    - init() : 필터 객체 초기화, 서비스에 추가 // doFilter() : http 요청이 servlet으로 전달되기 전 web-container에 의해 실행 // destroy90 : 필터 객체 제거, 자원 반환
  - interceptor
    - 요청에 대한 작업 전후로 요청을 가로채는 역할 : dispatcher servlet이 controller 호출 전후에 요청과 응답을 찹조하거나 가공할 수 있도록
    - **spring context**에서 동작
    - method : ??
  - AOP(관점 지향 프로그래밍)
  - https://dev-coco.tistory.com/173
* Entity vs DTO vs VO
  - **Entity**
    - 실제 DB table과 맵핑 (1:1)
    - Core class, request/response 객체로 절대 사용하지 말아야 함
    - 외부에서 getter method 이용하지 않도록
  - **DTO**
    - Data Transfer Object
    - 계층 간 데이터 "전달"을 위한 객체
    - *로직을 갖지 않음*
    - 데이터를 담고 꺼내기만 함 (getter/setter)
  - **VO**
    - Value Object
    - "값을 표현"하는 객체
    - *로직을 가질 수 있음*
    - 객체의 불변성 보장
    - 값 비교를 위해 equals()와 hashCode() 메소드를 오버라이딩 해줘야 함
      - 주소가 아닌 '값'을 비교하기 때문!
  - DTO vs VO
    - DTO는 받아온 VO를 Back-end내에서 (비즈니스 로직 등..) 매핑/처리가 필요할 경우에 변환하여 사용하는 객체
    - ![dtovo](https://github.com/bacchusdd/AgileStudyTil/blob/main/third/dtovo.png)
    - https://parkadd.tistory.com/53
    - https://yeonyeon.tistory.com/163
