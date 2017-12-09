## 소프트웨어공학 팀프로젝트 LOG

### 담당한 기능은 '영화예매 시스템'

> 영화 예매 및 취소
>
> 영화 정보 및 기타 할인 적용



### 목표

1. [클래스 정의](https://github.com/antaehyeon/softwareEngineeringTP#클래스-정의)
2. [아키텍쳐 설계](https://github.com/antaehyeon/softwareEngineeringTP#아키텍쳐-설계architecture-design)
3. [Use-case Diagram (Description 포함)](https://github.com/antaehyeon/softwareEngineeringTP#use-case)
4. [Use-case 를 기반으로 Sequence Diagram](https://github.com/antaehyeon/softwareEngineeringTP#sequence-diagram)
5. [State-Chart](https://github.com/antaehyeon/softwareEngineeringTP#state-chart)
6. [Interface 정의](https://github.com/antaehyeon/softwareEngineeringTP#interface-정의)



### 과정

- 일단 툴은 [draw.io](http://draw.io) 를 사용할 것
- 전체 프로젝트를 통합해야 하므로 개념적인 부분을 잘 이해하고 있을 것



### 클래스 정의

- 개념 부분은 [이곳](http://www.nextree.co.kr/p6753/) 을 참고 (UML: 클래스 다이어그램과 소스코드 매핑)

  - Generalization (일반화)

    > Generalization (일반화) 은 Super(부모)클래스와 Sub(자식)클래스간의 Inheritance(상속) 관계를 나타냄
    >
    > 서브클래스가 주체가 되어 서브클래스를 슈퍼클래스로 Generalize 하는 것

    > 반대의 개념은, 슈퍼클래스를 서브클래스로 Specialize(구체화) 하는 것


- 영화예매 시스템에 무엇이 필요할까
  - 고객 데이터
    - 성별, 나이, 이름
  - 영화정보 데이터
    - 영화명, 시간, 영화관람나이
  - 영화관 데이터
    - 영화관

- Class point of view

  ![ClassDiagram-ALL](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/ClassDiagram-ALL.png)

  - Reservation

    ![ClassDiagram-Reservation](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/ClassDiagram-Reservation.png)

    - Variable

      > field : type

      - 상영관 데이터 (theaterData)
      - 유저 정보 (UserData)
      - 예약 날짜 (reservationDate)
      - 인원 수 (numberOfPeople)
      - 금액 (amoutMoney)
      - 결제 수단 (paymentMethod)
      - 상영관 좌석 예약 정보 (theaterSeatingReservationData)

    - Method

      > method(type) : type

      - checkReservationData(String) : boolean
        - 예약이 가능한 날짜인지 확인합니다
      - checkSeatingAvailability(String) : boolean
        - 예매 가능한 좌석인지 확인합니다
      - getTheaterData() : Theater(class)
        - 상영관 정보를 받아옵니다
      - getUserData() : User(class)
        - 유저 데이터를 받아옵니다
      - processPayment(String) : boolean
        - 결제를 진행합니다

  - User

    ![User ClassDiagram](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/ClassDiagram-User.png)

    - Variable
      - 이름 (name)
      - 성별 (sex)
      - 나이 (age)
      - 등급 (grade)
      - 핸드폰 번호 (phoneNumber)
    - Method
      - getName(string) : string
      - getSex(string) : string
      - getAge(int) : int
      - getName()

  - Movie

    ![Movie ClassDiagram](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/ClassDiagram-Movie.png)

    - Variable
      - 영화명 (movieTitle)
      - 영화 시간 (movieTime)
      - 영화 타입 (movieType)
      - 영화 제한 나이 (movieLimitAge)

    - Method

      + method(type) : type

      - getMovieTitle() : int
      - getMovieTime() : int
      - getMovieLimitAge() : int

  - Theater

    ![Theater ClassDiagram](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/ClassDiagram-Theater.png)

    - Variable
      - 상영관 정보 (theaterInfo)
      - 상영관 영화 매칭 데이터 (theaterMovieMatchingData)
      - 좌석 정보 (seatingInfo)
      - 수용 인원 (capacity)
    - Method
      - getTheaterInfo() : string
      - getSeatingInfo() : hashMap
      - getCapacity() : int
      - getTheaterMovieMatchingData() : hashMap



### 아키텍쳐 설계(Architecture Design)

- 영화 예매 서브시스템

  ![Architecture Design](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Architecture%20Design.png)

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
  - 모든 데이터는 생성자(Constructor)를 통해 초기화된다
  - 사용자의 입력이 10분동안 없을 경우 자동 로그아웃을 처리한다
  - 영화 좌석 선택 후 결제단계에 들어가면 해당 좌석은 다른사람이 선택할 수 없게 변경한다
  - 결제 단계에서 실패하였을 경우 해당 좌석을 다시 선택할 수 있게 변경한다



![Reservation Movie Use-Case Expandable](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Reservation%20Movie%20Use-Case%20Expandable.png)

![Reservation Movie Use-Case](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Reservation%20Movie%20Use-Case.png)

- Actor
  - 영화 예매
    - 상영관 선택하기
    - 영화 정보 보기
    - 영화 상영시간 보기
    - 영화 좌석현황 보기
    - 결제
- Description
  - System : 영화 예매 시스템
  - Use-case : Report
  - Actors : 고객(일반 사용자)
  - Data 
    - 로그인한 고객이 영화를 예매할 수 있도록 각 정보(상영관, 좌석, 영화)를 제공합니다.
    - 사용자가 각 정보를 선택하고 결제를 진행할 수 있습니다
  - Stimulus
    - 좌석 정보가 겹치지 않도록 결제단계에 접근하게 되면 해당 좌석을 선택할 수 없게 변경합니다
  - Response
    - 결제가 완료될 경우 해당 예매 데이터를 기록하고 사용자에게 예매 정보를 출력합니다
    - 결제가 실패하였을 경우 해당 좌석을 선택할 수 있게 변경합니다



### Sequence Diagram

> 클래스 연관관계를 보이면 됨
>
> 함수를 호출하는 식으로

![ReservationMovie-SequenceDiagram](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/ReservationMovie-SequenceDiagram.png)

1. 영화정보 선택 - 영화정보 DB
2. 상영관 선택 - 상영관 DB
3. 영화 시간 선택 - 상영관 DB 중 시간 Table
4. 영화 인원 선택 - 사용자 선택
5. 좌석 선택
6. 결제



### State Chart

![State Machine](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/State%20Machine.png)

### Interface 정의

Class Reservation {

​	public boolean checkReservationData(String);

​	public boolean checkSeatingAvailability(String);

​	public Theater getTheaterData();

​	public User getUserData();

​	public boolean processPayment(String);

}



Class User {

​	public string getName();

​	public string getSex();

​	public int getAge();

​	public string getName();

}



Class Movie {

​	public int getMovieTitle();

​	public int getMovieTime();

​	public int getMovieLimitAge();

}



Class Theater {

​	public string getTheaterInfo();

​	public hashMap getSeatingInfo();

​	public int getCapacity();

​	public hashMap getTheaterMovieMatchingData();

}

























