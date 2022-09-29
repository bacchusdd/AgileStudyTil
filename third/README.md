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

(scrum with 멘토님)
*

</br>

## 0930
## 1003
## 1004


# 라이브세션 미션
* optional + stream
* stream method 중 findAny(), findFirst()
* spring security
* jwt
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
