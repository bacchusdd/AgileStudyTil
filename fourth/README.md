# 날짜별 기록

## 1005
(라이브 세션)
- Spring Security

(프로젝트 및 학습)
- 복합키 설정
  - @IdClass
  - Serializable Id class 생성
- 다대다 연관관계 맵핑
  - @ManyToMany 사용 
  - 중간 단계 entity 생성
  - 기존 entity : @OneToMany, 중간 단계 entity : @ManyToOne
  - @JoinColumn 뒤엔 name = "column 명"
  - @OneToMany 뒤엔 mappedBy = "feild 명"  //ManyToOne 밑에 선언한 class 변수명
  
  </br>
  
 ## 1006
 (프로젝트 및 학습)
  - 생성자 대신 정적 팩토리 메서드?
  - unit 단위 test / TDD
  - snake_case, camelCase db-springboot 호환 방
