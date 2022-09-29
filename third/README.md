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
