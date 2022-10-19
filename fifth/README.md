# 날짜별 기록

## 1013

## 1014
- Soft Delete?
  - [JPA에서 Soft Delete](https://velog.io/@nmrhtn7898/JPA-JPA-Hibernate-%EA%B8%B0%EB%B0%98%EC%9D%98-%EA%B0%9C%EB%B0%9C-%ED%99%98%EA%B2%BD%EC%97%90%EC%84%9C-Soft-Delete-%EA%B5%AC%ED%98%84%ED%95%98%EA%B8%B0)
- In 쿼리
  - JPA findBy~In(찾는 대상 list)
- [Annotation 정리](https://velog.io/@gillog/Spring-Annotation-%EC%A0%95%EB%A6%AC)
- Spring Security JWT
  - [JWT util](https://velog.io/@dhk22/Spring-Security-%ED%86%A0%ED%81%B0%EB%B0%A9%EC%8B%9D-%EC%9D%B8%EC%A6%9D-JWT)
  - [인증 관리](https://velog.io/@_koiil/SpringBoot-JWT%EB%A1%9C-%EC%9D%B8%EC%A6%9D-%EA%B4%80%EB%A6%AC%ED%95%98%EA%B8%B0)
  - [인증 후 로그인 객체](https://djunnni.gitbook.io/springboot/2019-11-30)
  - [현재 로그인 사용자 정보](https://itstory.tk/entry/Spring-Security-%ED%98%84%EC%9E%AC-%EB%A1%9C%EA%B7%B8%EC%9D%B8%ED%95%9C-%EC%82%AC%EC%9A%A9%EC%9E%90-%EC%A0%95%EB%B3%B4-%EA%B0%80%EC%A0%B8%EC%98%A4%EA%B8%B0)
    - 위 두 가지 방법 잘 안됨. 아마도 UserDetails 상속받지 않아서?
 
 </br>
 
## 1018
- jpa repository list 반환시 에러 처리?
  - [optional<~<list>> 사용이 좋지 못한 이유](https://velog.io/@hnsoo/JPA-%EC%9E%98%EB%AA%BB%EB%90%9C-%ED%91%9C%ED%98%84-OptionalListobject)
  - 결론 : Optional은 null 처리 위해 사용, but jpa에서 값 없으면 빈 list를 반환하지 null을 반환하지 않음. list로 받은 후 따로 처리
- [HTTP 상태코드 숫자별 상세 정보](https://ko.wikipedia.org/wiki/HTTP_%EC%83%81%ED%83%9C_%EC%BD%94%EB%93%9C)
    - 404 : 페이지가 없는 경우
    - 일반적으로 내가 생각하는 not found는 400 사용하면 되려나?
- @JsonInclude 이용하여 원하는 값만 출력하기
    - [@JsonInclude](https://alwayspr.tistory.com/m/31)
    
  </br>
  
  ## 1019
  - Moctest with security
    - [임시 user, token 이용하기](https://tecoble.techcourse.co.kr/post/2020-09-30-spring-security-test/)
