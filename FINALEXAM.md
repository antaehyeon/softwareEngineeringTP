## 2017-2 소프트웨어공학 기말고사 정리 (최수미 교수님)

[Return README.md](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/README.md)

개인적으로 [이곳](https://blog.naver.com/PostView.nhn?blogId=s2kiess&logNo=220155111239&parentCategoryNo=&categoryNo=159&viewDate=&isShowPopularPosts=true&from=search) 정리 짱 잘함

### 6단원, System Models

> 디자인 해보아라 (Data Processing model 또는 Functional processing)
>
> Data-Flow Diagram

- Model Types (6-6) : DCACS

  - Data Processing model : 데이터가 각각의 단계에서 **어떻게 처리되는지** 보여주는 모델 (데이터 흐름도)

  - Composition model : 엔티티가 **다른 엔티티로 구성**되는 방법을 보여주는 구성 모델 (엔티티-관계 다이어그램)

    - Semantic data models : 시스템에 의해 처리되는 데이터의 논리적인(Logical) 구조를 묘사하기 위해 사용되는 모델 (Database - ER Diagram)

    ![Composition Model Example](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Composition%20Model%20Example.png)

  - Architectural model : 주요 **서브시스템**을 보여주는 모델 (전체적인 구조를 파악)

  - Classification model : 개체(Entity)들이 어떻게 **공통의 특성 (객체 클래스 / 상속 다이어그램)** 을 갖는지를 나타내는 분류모델

  - Stimulus/Response model : 이벤트에 대한 **시스템의 동작**을 보여주는 모델 (상태 다이어그램)

    - **UI(User Interface)** : interaction 한 성격을 지니고 있음

- Behavioural 모델
  - Data-Process 모델

    ![Data-Flow Diagram](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Data-Flow%20Diagram.png)

    - **Data flow diagrams**은 시스템의 데이터 처리를 모델링 하는데 사용
    - 데이터가 시스템을 통과하는 과정에서 처리 단계를 보여줌
    - 많은 분석 방법의 본질적인 부분
    - 고객이 이해할 수 있는 **간단하고 직관적인 표기법**
    - 데이터의 종단간 처리(end-to-end processing)를 보여줌
    - 표기법 : **기능처리, 데이터 저장소 및 데이터 이동**

    ![CASE toolset DFD](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/CASE%20toolset%20DFD.png)

    - DFDs(Data Flow Diagrams)는 시스템을 **기능적인 관점(functional perspective)**에서 모델링함
    - 프로세스 관련된 데이터를 추적하여 시스템에 대한 전반적인 이해를 구축하는 방법을 추적 및 문서화
    - 데이터 흐름 다이어그램은 시스템과 다른 시스템 간 데이터 교환을 보여주는 데에도 사용될 수 있음
    - **Functional Processing, Data Movement, 저장 장소를 표현할 수 있어야함**

    ![Data Processing Model Elements](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Data%20Processing%20Model%20Elements.png)

    - External entity : 데이터의 생산자 또는 소비자 (사람, 장비, 센서, 컴퓨터 시스템 등)
    - Process : 데이터의 변환이 이루어지는 부분 (input - output)
    - Data Flow : 데이터 자체의 흐름을 의미 (data flow)
    - Data Store : 데이터를 잠시 저장할 때 사용

  - State-Machine 모델(로 디자인 하라는 문제가 나올 수 있음)

    ![State machine model](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/State%20machine%20model.png)

    - 해당 모델은 **외부 및 내부 이벤트에 대응하여 시스템의 동작을 모델링함**
    - 자극(stimuli)에 대한 시스템의 반응을 보여주기 때문에 **실시간 시스템**의 모델링에 자주 사용
    - 상태 기계 모델(State machine models)은 시스템 **상태를 노드 간 arcs와 event로 표시**함
    - 이벤트가 발생하면 시스템은 한 상태에서 다른 상태로 전환
    - State-Charts는 UML의 중요한 부분
    - ![Microwave oven operation(a super-state)](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Microwave%20oven%20operation(a%20super-state).png)
    - Super-state를 이용해 모델을 하위 모델로 분류할 수 있음

- 어떤 짧은 모델에 대해서 '특정 모델'로 해보아라 할 수 있음(**각 모델의 Notations가 Point**)

  - Data-Process 모델의 Notations : **기능처리, 데이터 저장소 및 데이터 이동**
  - State-Machine 모델의 Notations : **응답(Stimuli), 상태(State), 행동에 대한 설명(Brief description of the actions in that state)**

- Object models

  - 객체 모델은 객체 클래스의 관점에서 시스템을 설명

  - 개체 클래스는 각 개체가 제공하는 공통적인 속성 및 서비스(Operations)를 가진 개체 집합에 대한 추상화

  - 시스템에 의해 조작되는 현실의 실체를 반영하는 자연적인 방법

  - 추상적인 실체는 이 방법을 사용하여 모델링하는것이 더 어려움

  - 개체 클래스의 식별은 응용 프로그램 도메인의 깊은 이해를 필요로하는 어려운 과정으로 인식

  - 도메인 엔티티를 반영하는 객체 클래스는 시스템에서 재사용 가능

  - 다양한 개체 모델

    - 상속(Inheritance) 모델

      - 도메인의 객체 클래스를 계층 구조로 정리

      - 계층의 최상위 클래스는 모든 클래스의 공통 기능을 반영

      - 객체 클래스는 속성과 서비스를 하나 이상의 상위 클래스에서 상속하며, 필요에 따라 전문화(specialised)할 수 있음

      - 다른 계층의 중복을 피할 필요가 있는 경우, 클래스 계층 설계는 어려운 과정이 될 수 있음

      - The Unified Modeling Language : UML

        ![User Class Hierarchy](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/User%20Class%20Hierarchy.png)

        - 광범위하게 사용되는 객체 지향 분석 및 설계 방법
        - **객체 지향(Object-Oriented) 모델링 표기법에 대한 효과적인 표준**
        - Notation
          - 객체 클래스는 **상단에 있는 이름과 하위 섹션의 속성 및 하위 섹션의 작업을 포함하는 사각형으로 구성**
          - 개체(object) 클래스(연결이라고도 함)간의 관계는 **개체를 연결하는 선**으로 표시
          - **상속**은 일반적으로 생성되며, 계층 내에서 '아래쪽'이 아닌 **위쪽(upwards)**으로 표시 (정의하라는 문제가 나올 수 있음)

    - 집계(Aggregation) 모델

    - 상호작용(Interaction) 모델

      ​



- Sequence Diagram은 (숙제로 하고있으므로) 디테일하게 내지 않음



- Data-Process, State-Machine, Object-Oriented Model
- 특징이 무엇인지 비교했을 때 특징들을 살펴볼 것



### 7단원, Software Prototyping

> 시험에 관해서는 크게 나오지 않음

- 프로토타이핑의 **장점**
  - 소프트웨어 사용자와 개발자 사이의 오해가 드러남
  - 누락된 서비스가 감지되고 혼동되는 서비스를 식별할 수 있음
  - 작업 시스템은 초기 프로세스 사용할 수 있음
  - 프로토 타입은 시스템 사양을 유도하기 위한 기초로 사용될 수 있음
  - 이 시스템은 사용자 교육 및 시스템 테스트를 지원할 수 있음
  - 시스템 가용성 향상
  - 필요한 시스템에 더 가까운 일치
  - 개선된 설계 품질
  - 향상된 유지보수성
  - 전반적인 개발 작업 감소


- 소프트웨어 프로세스의 프로토타입
  - **진화적 프로토타이핑(Evolutionary prototyping)**
    - 초기 프로토 타입이 생성되고, 여러 단계를 거쳐 최종 시스템으로 정제(refineed)되는 시스템 개발 접근 방식
    - 해당 프로토타입의 목적은 최종 사용자에게 작업 시스템을 제공하는 것
    - **개발은 가장 잘 이해된 요구사항으로 시작**
    - 사양을 미리 개발할 수 없는 시스템에 사용(예: AI시스템 및 UI시스템)
    - 빠른 시스템 반복을 가능하게 하는 기술을 기반으로 함
    - 사양이 없으므로 검증이 불가능함 (검증 : 시스템의 타당성을 입증)
    - advantages
      - 시스템의 신속한 전달
        - 신속한 제공 및 구현은 가능성 또는 장기적인 소프트웨어 유지관리보다 중요
      - 시스템 사용자 참여
        - 시스템이 사용자 요구사항을 충족할 가능성이 높아지며, 시스템 사용에 더욱 전념할 가능성이 높음
    - 사양, 설계 및 구현은 상호조정(inter-twined) 됨
    - 이 시스템은 고객에게 전달되는 일련의 증분로 개발
    - CASE도구 및 4GLs과 같은 신속한 시스템 개발을 위한 기법
    - 사용자 인터페이스는 보통 GUI개발 툴킷을 사용하여 개발
    - problem
      - 관리, 경영(Management) 문제
        - 기존 관리 프로세스는 폭포수 모델 개발을 가정
        - 모든 개발팀에서 사용할 수 없는 전문 기술이 필요
      - 유지관리(Maintenance) 문제
        - 지속적인 변경으로 인해 시스템 구조가 손상되어 장기간 유지보수비용이 높아질 수 있음
      - 계약(Contractual) 문제
  - **Throw-away Prototyping**
    - 일반적으로 시스템의 실용적인 구현은 **요구 사항 문제를 발견한 후 폐기하는데 도움**이 됨
    - 다음 시스템이 다른 개발 프로세스를 사용하여 개발
    - 해당 프로토타입(Throw-away Prototyping)은 시스템 요구사항을 **검증**하거나 **유도**하는 것
    - **제대로 이해되지 않은 요구사항부터 시작**
    - 요구사항을 줄이기 위해 사용
    - 프로토타입은 초기 사양에서 개발된 후, 실험을 위해 전달 된 다음 폐기
    - 폐기 시스템의 프로토 타입을 최종 시스템으로 간주해서는 안됨
      - 일부 시스템 특성은 생략될 수 있음
      - 장기간 유지보수를 위한 규격은 없음
      - 이 시스템은 체계화되지 않고 유지보수가 어려움
  - Rapid prototyping techniques
    - 신속한 개발을 위해 다양한 기술을 사용할 수 있음
      - 동적 고급 언어 개발
      - 데이터베이스 프로그래밍
      - 구성 요소 및 응용 프로그램 어셈블러
    - 이들은 독점 기술이 아니라 종종 함께 사용
    - 비주얼 프로그래밍은 대부분의 프로토 타입 개발 시스템에 내재하는 것
- Incremental(증가) development
  - 전체 아키텍쳐를 구축한 후 시스템이 점진적으로 개발 및 제공
  - 각 증분에 대한 요구사항 및 사양이 개발될 수 있음
  - 사용자는 다른사람이 개발하는 동안 납품된 증가분을 사용하여 실험할 수 있음 (프로토 타입 시스템의 한 형태로 역할을 담당)
  - 프로토 타이핑의 장점 중 일부를 결합하기 위해 고안되었지만, 보다 관리 가능한 프로세스와 보다 나은 시스템 구조를 제공























