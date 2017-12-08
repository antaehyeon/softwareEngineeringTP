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
  - User
  - Movie
  - Theater