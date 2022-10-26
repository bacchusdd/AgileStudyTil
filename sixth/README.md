# 날짜별 기록

## 1020
- 테스트 관련
  - [MockMvc를 이용한 HTTP methods 테스트](https://shinsunyoung.tistory.com/m/52)
  - [Controller 단위 테스트](https://goodteacher.tistory.com/257)
  - [MockMvc를 활용한 Controller 테스트](https://erjuer.tistory.com/113)
  - [단위 테스트 vs 통합 테스트](https://tecoble.techcourse.co.kr/post/2021-05-25-unit-test-vs-integration-test-vs-acceptance-test/)
  - 출처 : 교육 강사님
- [throw vs throws](https://codechacha.com/ko/java-throw-and-throws/)
  - throw :  Exception을 발생시킬 때
  - throws : 메소드에서 잠재적으로 어떤 Exception이 발생할 수 있는지 명시
  
  </br>
  
## 1021
- openapi-swagger 설정
  - [초기 기본 설정](https://wildeveloperetrain.tistory.com/156)
  - [@RequestBody에 schema 적용](https://stackoverflow.com/questions/64645528/java-spring-boot-openapi-3-how-to-add-description-for-requestbody)
  - [공식 문서](https://springdoc.org/properties.html)
  - [공식 문서 보기 좋게](https://oingdaddy.tistory.com/272)
  - [자세한 설명](https://blog.jiniworld.me/91)
</br>

## 1024
- [@ReqeustParam vs @PathVairable](https://velog.io/@dmchoi224/Rest-API-RequestParam-%EA%B3%BC-PathVariable)
  - REST를 따르기 위해서는 {~} @PathVariable 사용할 것
  - [언제 무엇을 사용하는가](https://medium.com/@fullsour/when-should-you-use-path-variable-and-query-parameter-a346790e8a6d)
  - Path Variable은 REST API에서 값을 호출할 때 주로 사용되고, Query Parameter는 게시판의 페이지 및 검색 정보를 전달하는 방식에서 많이 사용된다.
  - [Paging에 ReqeustParam 넘겨주기](https://velog.io/@conatuseus/JPA-Paging-%ED%8E%98%EC%9D%B4%EC%A7%80-%EB%82%98%EB%88%84%EA%B8%B0-o7jze1wqhj)
</br>


## 1026
- Spring Security 권한 설정
  - user table에 권한 column 추가하지 않고, role table 따로 둬서 관리하는 방법
  - UserDetails + GrantedAuthority
  - [UserDetails interface 이해하기](https://zgundam.tistory.com/49)
  - [한 user 여러 권한 관리](https://gaemi606.tistory.com/entry/Spring-Boot-Spring-Security-%ED%95%9C-%EC%9C%A0%EC%A0%80%EC%97%90%EA%B2%8C-%EC%97%AC%EB%9F%AC-AuthorityROLE-%EB%B6%80%EC%97%AC%ED%95%98%EA%B8%B0-UserDetails)
