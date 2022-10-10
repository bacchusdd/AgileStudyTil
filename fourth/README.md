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
  - DTO 생성자 대신 정적 팩토리 메서드?
    - https://velog.io/@harukawa99/정적-팩토리-메소드
  - unit 단위 test / TDD
  - snake_case, camelCase db-springboot 호환 방
  - response config
    - [https://velog.io/@leeeeeyeon/Spring-boot-Response-형식-만들기](https://velog.io/@leeeeeyeon/Spring-boot-Response-%ED%98%95%EC%8B%9D-%EB%A7%8C%EB%93%A4%EA%B8%B0)
    - [https://devlog-wjdrbs96.tistory.com/182](https://devlog-wjdrbs96.tistory.com/182)
    - [https://devlog-wjdrbs96.tistory.com/197?category=882974](https://devlog-wjdrbs96.tistory.com/197?category=882974)
    
  </br>
  
  ## 1011
  - Spring의 ResponseEntity 사용하기
    - [https://hyeonic.tistory.com/197](https://hyeonic.tistory.com/197)
    - [https://thalals.tistory.com/268](https://thalals.tistory.com/268)


</br>
# 학습 미션

* SOLID 원칙 —> 클린 코드

객체 지향 프로그래밍에서 지켜야하는 5대 원칙으로 해당 원칙을 철저히 지키면 시간이 지나도 변경이 용이하고 유지보수와 확장이 쉬운 소프트웨어를 개발하는데 도움을 줌. ( 높은 응집도 낮은 결합도 )

### 객체 지향의 설계 과정

1. 요구사항을 찾아 세분화 및 추상화
2. 기능을 구현하는데 필요한 데이터를 객체에 추가
3. 데이터를 이용하는 기능을 구현 ( 기능은 최대한 캡슐화 )
4. 객체 간에 어떻게 메소드 호출을 주고받을 지 결정

### S : SRP ( Single Responsibility Principle) - 단일 책임 원칙

하나의 클래스(모듈)는 하나의 책임(기능)을 가져야함.  모듈이 변경되는 이유가 한가지여야 함.

책임이 여러개라면 클래스 내부의 함수끼리 강한 결합이 발생할 가능성이 높음. 

- 예시
    
    <aside>
    💡
    
    **class** 강아지 {
    
    **final** static **Boolean** 수컷 = true;
    
    **final** static **Boolean** 암컷 = false;
    
    **Boolean** 성별;
    
    **void** 소변보다() {
    
    **if** (this.성별 == 수컷) {
    
    // 한쪽 다리를 들고 소변을 보다.
    
    } **else** {
    
    // 뒷다리 두 개를 굽혀 앉은 자세로 소변을 본다.
    
    }
    
    }
    
    }
    
    </aside>
    
    위의 코드는 강아지의 암컷과 수컷을 모두 구현하려고하여 SRP를 위반하고 있음
    
    <aside>
    💡
    
    **abstract** **class** **강아지** {
    
    **abstract** void 소변보다();
    
    }
    
    **class** **수컷강아지** **extends** **강아지** {
    
    void 소변보다() {
    
    // 한쪽 다리를 들고 소변을 본다.
    
    }
    
    }
    
    **class** **암컷강아지** **extends** **강아지** {
    
    void 소변보다() {
    
    // 뒷다리 두 개로 앉은 자세로 소변을 본다.
    
    }
    
    }
    
    </aside>
    
    암컷과 수컷을 분리하여 기능을 구현함.
    

### O : OCP ( Open-Closed Principle ) - 개방 폐쇄 원칙

확장은 열려 있고 변경에는 닫혀 있어야함. → 기존의 코드를 변경하지 않고 기능을 수정하거나 추가할 수 있도록 설계해야함.

위의 그림처럼 운전자가 자동차를 접근할 때 공통으로 상속받는 상위 클래스 또는 인터페이스를 중간에 둠으로써 다양한 자동차가 생겨도 운전자는 각 차량별 특성에 영향을 받지 않게 됨. 다양한 자동차가 생기는 것은 자동차입장에서 자신의 확장에 개방되어 있고, 운전자의 입장에서 주변의 변화에 폐쇄되어 있음.

### L : LSP ( Listov Substitution Principle ) - 리스코프 치환 법칙

하위 클래스 is a kind of 상위 클래스 - 하위 분류는 상위 분류의 한 종류다.

구현 클래스 is able to 인터페이스 - 구현 분류는 인터페이스할 수 있어야 한다.

### I : ISP ( Interface Segregation Principle ) - 인터페이스 분리법칙

클라이언트는 자신이 사용하는 메소드에만 의존해야함. → 자신이 사용하지 않는 인터페이스는 구현X

→ 하나의 통상적인 인터페이스보다는 차라리 여러개의 세부적인 인터페이스가 더 나음.

인터페이스는 해당 인터페이스를 사용하는 클라이언트를 기준으로 잘게 분리해야함. ( 인터페이스는 하위 클래스에게 구현을 강제하도록함. 최소한의 기능만을 제공하면서 하나의 역할에 집중 )

### D : DIP ( Dependency Inversion Principle ) - 의존 역전 법칙

의존 관계를 맺을 때에는 변하기 쉬운 것(구현체) 보다 변하기 어려운 것 (추상체)에 의존해야함.

⇒ 구체화된 클래스보다 추상 클래스나 인터페이스에 의존하는 것이 바람직함.

자동차의 타이어에 대한 의존 관계를 맺을 떄 스노우타이어, 일반 타이어, 광폭 타이어 보다 타이어 인터페이스를 의존 관계로 함으로써 타이어가 변경되어도 자동차는 영향을 받지 않음.

[https://devlog-wjdrbs96.tistory.com/380](https://devlog-wjdrbs96.tistory.com/380)

[https://velog.io/@haero_kim/SOLID-원칙-어렵지-않다](https://velog.io/@haero_kim/SOLID-%EC%9B%90%EC%B9%99-%EC%96%B4%EB%A0%B5%EC%A7%80-%EC%95%8A%EB%8B%A4)

출처 : [두성님](https://www.notion.so/prgrms/Week4-SOLID-930aead155c8476481b7c6a578a7249a)
