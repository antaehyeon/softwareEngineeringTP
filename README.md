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
  - ​





































