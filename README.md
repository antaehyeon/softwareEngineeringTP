## 소프트웨어공학 팀프로젝트 LOG

### 담당한 기능은 '영화예매 시스템'

> 영화 예매 및 취소
>
> 영화 정보 및 기타 할인 적용



### 목표

1. 클래스 정의
2. 아키텍쳐 설계
3. Use-case Diagram (Description 포함)
4. Use-case 를 기반으로 Sequence Diagram
5. State-Chart



### 과정

- 일단 툴은 [draw.io](http://draw.io) 를 사용할 것
- 전체 프로젝트를 통합해야 하므로 개념적인 부분을 잘 이해하고 있을 것



### 클래스 정의

- 개념 부분은 [이곳](http://www.nextree.co.kr/p6753/) 을 참고 (UML: 클래스 다이어그램과 소스코드 매핑)


- 영화예매 시스템에 무엇이 필요할까
  - 고객 데이터
    - 성별, 나이, 이름
  - 영화정보 데이터
    - 영화명, 시간, 영화관람나이
  - 영화관 데이터
    - 영화관
- Class point of view
  - Reservation
    - Variable
      - 상영관 데이터 (theaterData)
      - 유저 정보 (UserData)
      - 예약 날짜 (reservationDate)
      - 인원 수 (numberOfPeople)
      - 금액 (amoutMoney)
      - 결제 수단 (paymentMethod)
      - 상영관 좌석 예약 정보 (theaterSeatingReservationData)
    - Method
      - checkReservationData : 예약이 가능한 날짜인지 확인합니다
      - getTheaterData : 상영관 정보를 받아옵니다
      - getTheaterSeatingData : 상영관 좌석정보를 받아옵니다
      - getUserData : 유저 데이터를 받아옵니다
      - processPayment : 결제를 진행합니다
  - User
    - Variable
      - 이름 (name)
      - 성별 (sex)
      - 나이 (age)
    - Method
  - Movie
    - Variable
      - 영화명 (movieTitle)
      - 영화 시간 (movieTime)
      - 영화 타입 (movieType)
    - Method
  - Theater
    - Variable
      - 상영관 정보 (theaterInfo)
      - 좌석 정보 (seatingInfo)
      - 수용 인원 (capacity)
    - Method



### 아키텍쳐 설계

- 영화 예매 서브시스템
  - Data Collections : 영화 예매를 위한 서브시스템으로 영화상영정보, 영화관 정보, 회원 정보를 가져온다
    - 영화 상영 정보
    - 영화관 정보
    - 회원 정보
  - Purchase : 영화 예매 중 결제를 담당하는 서브시스템이다
    - 카드 정보



### USE-CASE

> 시스템이 사용자에 의해서 어떠한 형태로 사용되는지를 기술하는 UML의 표준 표기법
>
> 시스템이 갖추어야 하는 기능적(Functional) 또는 비기능적(non-Functional) 요구사항을 표현하는 방법
>
> 모델링이 UML로 통합되면서 요구사항을 기술하는 일반적인 방법으로 사용되어짐

> 시스템을 사용하는 사용자와 내가 만들어야 하는 시스템 자체를 설명

- 액터 (Actor) : 시스템을 사용하는 사용자
- 유스케이스 (Use case) : 시스템의 행동
- 주제 영역 (Subject) : 만드려고 하는 소프트웨어 시스템



- 기능적 요구사항(Functional 요구사항) : 시스템이 하는 일에 대한 요구사항
  - 각 서브시스템에서 모든 데이터를 공유할 수 있도록 구성되어 있다
  - ​


- 비기능적 요구사항(Non-Functional 요구사항) : 기능에 대한 제한사항
  - 사용자의 입력이 10분동안 없을 경우 자동 로그아웃을 처리한다
  - 영화 좌석 선택 후 결제단계에 들어가면 해당 좌석은 다른사람이 선택할 수 없다
  - ​



- Actor
  - 영화 예매
    - 상영관 선택하기
    - 영화 정보 보기
    - 영화 상영시간 보기
    - 영화 좌석현황 보기
    - 결제

































