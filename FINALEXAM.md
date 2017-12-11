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
>
> 두가지 프로토타이핑이 어떤 측면에서 차이점이 있는가
>
> 언제 사용하고 어떤 장점들이 있는가

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
  - Rapid prototyping techniques(장점 기억할 것)
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



### 8단원, Architectural Design

> 각각의 장단점, 차이점 들을 비교하는 부분을 중점적으로
>
> 자세한 것은 뒷장에서 나오므로

- 소프트웨어 아키텍쳐, Software architecture
  - **시스템을 구성하는 서브시스템을 식별**하고 하위 **시스템 제어 및 통신을 위한 프레임워크**는 **아키텍쳐 설계(architecture)**입니다
  - 이 설계 프로세스의 output은 소프트웨어 아키텍쳐에 대한 설명이다

- Architectural Design

  - 시스템 설계 프로세스의 초기 단계
  - 명세(specification)과 디자인 프로세스 간 연결을 나타냄
  - 종종 일부 명세(specification) 활동과 병행하여 수행
  - 주요 시스템 구성요소와 그 통신을 식별하는 일

- 명시적(explicit) 아키텍쳐의 장점

  - 이해 관계자(Stackholder) 커뮤니케이션
    - 아키텍쳐는 시스템 이해 관계자가 토론의 초점으로 사용할 수 있음
  - 시스템 분석
    - 시스템이 **비 기능 요구사항을 충족시킬 수 있는지 여부**를 분석할 수 있음
  - 대규모 재사용
    - 아키텍쳐는 다양한 시스템에서 **재사용** 할 수 있음

- 아키텍쳐 디자인 프로세스

  - 시스템 구조 조정
    - 이 시스템은 여러개의 주요 서브 시스템으로 분해되고 이러한 서브 시스템간 통신이 식별됨
  - 제어 모델링
    - 시스템의 다른 부분 간 제어 관계 모델이 확립됨
  - 모듈러 분해
    - 식별된 서브시스템이 모듈로 분해됨

- 아키텍쳐 모델

  - 설계 과정에서 다른 아키텍쳐 모델이 생성될 수 있음
  - 각 모델은 아키텍쳐에 대한 다양한 관점을 제시함 **(ASDIR)**
    - 주요 시스템 구성요소를 나타내는 **정적 구조 모델(Static structural model)**
    - 시스템이 실행 시 프로세스에 어떻게 편성되는지를 나타내는 **동적 프로세스 모델(Dynamic process model)**
    - 서브 시스템 인터페이스를 정의하는 **인터페이스 모델(Interfcae model)**
    - 서브 시스템 간 데이터 흐름 등 **관계 모델(Relationships model)**

- Architecture attributes **(아성보안유유)**

  - 성능(Performance) : 서브시스템 간 통신을 최소화 하기 위해 작업의 지역화
  - 보안(Security) : 내부 레이어의 중요 자산과 함께 계층화 된 아키텍쳐 사용
  - 안전(Safety) : 안전에 필수적인 구성요소로 분리
  - 유용성(Availability) : 아키텍쳐에 중복 구성요소 포함
  - 유지보수성(Maintainability) : 쉽게 변경할 수 있는 자체 구성요소를 사용

- 시스템 구조(System structuring) - Block Diagram 출제 될 수 있음

  - 시스템을 상호작용하는 서브 시스템으로 분해하는 것에 대한 우려

    ![Block Diagram](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Block%20Diagram.png)

  - 아키텍쳐 설계는 일반적으로 시스템 구조의 개요를 나타내는 **Block Diagram**으로 표현됨

  - 서브시스템이 어떻게 데이터를 공유하고, 분산되어 있고, 상호 인터페이스가 개발되어 있는지를 보여주는 것 보다 **구체적인 모델(specific model)**로 개발될 수 있음

- 보다 구체적인 표준 모델

  - Repository model

    ![CASE toolset architecture](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/CASE%20toolset%20architecture.png)

    - 서브 시스템은 데이터를 교환해야 하는데, 두가지 방법이 존재
      - 공유 데이터는 **중앙 데이터베이스 또는 저장소**에 보관되며, 모든 하위 시스템에 액세스 할 수 있음
      - **각 서브 시스템은 자체 데이터베이스를 유지/관리**하고 다른 서브 시스템에 데이터를 명시적으로 전달
    - 대량의 데이터를 공유해야 하는 경우 공유의 저장소 모델이 가장 일반적으로 사용됨
    - **Advantages**
      - 대량의 데이터를 효율적으로 공유하는 방법
      - 서브 시스템은 데이터가 생성되는 방식에 관여할 필요가 없음 (예 : 백업, 보안 등)
      - 공유 모델이 저장소 스키마로 게시됨
    - **DisAdvantages**
      - 서브 시스템은 저장소 데이터 모델에 동의해야 함 (필연적으로 타협)
      - 데이터 진화(Data Evolution)는 어렵고 비용이 많이 듬
      - 특정 관리 정책에 대한 범위가 없음
      - 효율적으로 배포하기 어려움

  - Client-Server model

    ![Film and picture library](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Film%20and%20picture%20library.png)

    - 다양한 구성요소에서 데이터 처리가 어떻게 분산되는지를 나타내는 **분산시스템 모델**
    - 인쇄, 데이터 관리 등의 특정 서비스를 제공하는 **독립형 서버 세트(Set of stand-alone servers)**
    - 이러한 서비스를 요청하는 **클라이언트 집합**
    - 클라이언트가 서버에 액세스 할 수 있는 **네트워크**
      - **Advantages**
        - 데이터의 배포가 간단
        - 네트워크로 연결된 시스템을 효과적으로 사용, 하드웨어 비용이 저렴해질 수 있음
        - 새로운 서버를 추가하거나 기존 서버의 업그레이드가 용이
      - **DisAdvantages**
        - 하위 시스템이 다른 데이터 구성을 사용하도록 공유된 데이터 모델이 존재하지 않음
        - 백업 및 복구 등을 각 서버에서 중복적으로 관리
        - 이름과 서비스에 대한 중앙 등록이 없음
          - 어떤 서버와 서비스를 사용할 수 있는지 찾기 힘듬

  - Abstract machine model (layered model)

    ![Version management system](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Version%20management%20system.png)

    - 서브 시스템의 인터페이스를 모델링하는데 사용
    - 시스템을 일련의 레이어(또는 추상 머신)로 구성하여 각 레이어가 일련의 서비스를 제공
    - [장점] 서로다른 계층에서 **서브시스템의 점진적 개발을 지원**
    - [특이한 점] 계층 인터페이스가 변경되면 **인접 계층만 영향**을 받음
    - 그러나 이런방식으로 시스템을 구조화하기에는 어려움이 따름
    - 예 : OSI 7 계층

  - Control models

    > 각각이 무엇인지 파악할 것

    - **서브시스템 간 제어 흐름에 관계**하고 있으며, 시스템 분해모델과 구별됨

    - 구조 모델에는 제어 정보가 포함되어 있지 않음

    - **중앙집중식 제어(Centralised control)**

      ![Centralised management model Real-time system control](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Centralised%20management%20model%20Real-time%20system%20control.png)

      - 하나의 서브 시스템은 제어에 대한 전반적인 책임을 가지며, 다른 서브시스템을 시작 및 중지함

      - 제어 서브 시스템은 다른 서브시스템의 실행을 관리하는데 책임이 있음

        - **Call-Return model**

          ![Call-return model](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Call-return%20model.png)

          - 서브 루틴 계층 구조의 맨 위에서 제어가 시작되고 아래쪽으로 이동하는 **하향식 서브루틴 모델**
          - 순차 시스템에 적용 가능

        - **Manager model**

          - **동시 시스템(concurrent system)**에 적용가능
          - 하나의 시스템 구성요소는 다른 시스템프로세스의 시작, 중지 및 조정을 제어
          - 순차적 시스템에서 case문으로 구현가능
          - 종종 'soft' 실시간 시스템에 사용됨

    - 이벤트 기반 제어(Event-based control)

      - 각 서브 시스템은 다른 서브 시스템 또는 시스템의 외부에서 발생한 이벤트에 대응할 수 있음

      - Event-driven systems

        - 이벤트를 처리하는 서브 시스템을 제어하는 이벤트가 외부에서 발생하는 외부 생성 이벤트에 의해 유발

        - 두개의 주요 이벤트 구동 모델

          - **브로드캐스트 모델**

            ![Selective_broadcasting](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Selective_broadcasting.png)

            - 이벤트는 모든 서브 시스템에 방송(전파)됨
            - 이벤트를 처리할 수 있는 서브 시스템은 모두 가능
            - 네트워크의 여러 시스템에서 **서브 시스템을 통합**하는데 효과적
            - 서브 시스템은 특정 이벤트에 대한 관심을 보임
            - 이벤트가 발생할 경우 컨트롤이 해당 이벤트를 처리할 수 있는 서브시스템으로 전송
            - 제어 정책은 이벤트 및 메시지 핸들러에 포함되지 않으며, **서브 시스템은 관심(interest) 이벤트를 결정**
            - **그러나 서브 시스템은 이벤트가 언제 처리될지 또는 언제 처리될지 알지 못함**

          - **인터럽트 구동 모델**

          ![Interrupt-driven-control](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Interrupt-driven-control.png)

          - 인터럽트가 인터럽트 **핸들러**에 의해 감지되고 처리를 위해 다른 구성요소로 전달되는 **실시간 시스템에서 사용**
          - 이벤트에 대한 빠른 응답이 필수적인 **'hard' 실시간 시스템**에 사용됨
          - 각 유형에 대해 **핸들러가 정의된 알려진 인터럽트 유형이 존재**
          - 각 유형의 메모리 위치에 관련된 하드웨어 스위치는 핸들러에 전송함
          - **빠른 응답을 가능하게 하지만 프로그램이 복잡하고 검증하기 어려움**

        - 다른 이벤트 기반 모델에는 AI에서 사용되는 스프레드 시트 및 규칙 기반 생산시스템이 포함됨


  - 모듈 분해(Modular decomposition)

    > 각각의 장점을 파악해 둘 것

    - **서브 시스템이 모듈로 분해**되는 다른 구조 수준 (Modular : 서브시스템 보다 아랫단계)
    - 2개의 모듈 분해 모델이 포함됨
      - 시스템이 상호작용하는 객체로 분해되는 **객체지향모델**
        - 잘 정의된 인터페이스를 사용하여, 느슨하게 결합 된 개체의 집합으로 시스템을 구성
        - 객체 지향 분해 (object-oriented decomposition)는 **객체 클래스, 객체의 속성 및 기능**을 식별하는 것과 관련이 있음
        - 구현 시 객체가 생성되고, 객체 작업을 조정하는 데 사용되는 일부 제어모델이 생성됨
      - 시스템이 **입력을 출력으로 변환**하는 기능모듈로 분해되는 **데이터 흐름모델** 또는 **파이프 라인 모델**이라고도 함
        - 함수 변환은 입력을 처리하여 출력을 생성
        - **파이프 및 필터 모델**이라고도 함(UNIX shell과 같이)
        - 이 방법의 변형은 매우 흔함
        - 변환이 순차적일 때, 이는 **데이터 처리 시스템에서 광범위하게 사용**되는 일괄 배치 모델임
        - **대화형 시스템에는 적합하지 않음**
    - 가능한 경우 모듈이 구현될 때 까지 동시성에 대한 결정을 지연해야함

  - 도메인 별 아키텍쳐 (Domain-specific architectures)

    - 일부 애플리케이션 도메인에만 적용되는 아키텍쳐 모델
    - 2가지 유형의 도메인 특정 모델
      - 다수의 실제 시스템으로부터의 추상화되는 **일반적인 모델(Generic models)**
        - **Bottom-up**
        - 이러한 시스템의 주요 특징을 캡슐화함
        - 많은 사람들이 사용함 (예: UML)
      - 보다 추상적이고 이상적인 **참조모델(Reference model)**
        - **Top-down**
        - 시스템 클래스에 대한 정보를 제공하고 다양한 아키텍처를 비교
        - 누가 주는 것?



### 9단원, Distributed Systems Architectures

- Distributed systems

  - 사실상 모든 대형 컴퓨터 기반은 모두 분산 시스템(Distributed System)
  - 정보처리는 단일컴퓨터에 국한되지 않고, 여러대의 컴퓨터에 분산됨
  - 분산된 소프트웨어 엔지니어링은 매우 중요

- Distributed system 특징

  - **자원 공유(Resource sharing)** : 네트워크상의 다른 컴퓨터와 관련된 H/W 및 S/W 자원공유
  - **개방성(Openness)** : 새로운 비 독점 자원을 추가하여 확장할 수 있는 범위
  - **동시성(Concurrency)** : 여러 프로세스가 동시에 작동할 수 있음
  - **확장성(Scalability)** : 새로운 리소스를 추가하여 시스템의 기능을 향상시킬 수 있음
  - **내결함성(Fault tolerance)** : 일부 H/W 및 S/W 오류의 허용 오차
  - **투명성(Transparency)** : 시스템의 분산된 속성 사용자로부터의 은닉

- Distributed system 결함

  - **복잡성(Complexity)** : 중앙 집중식 시스템보다 복잡하며, 초기 속성을 파악하고 시스템을 테스트하기가 더 어려움
  - **보안(Security)** : 시스템을 여러대의 컴퓨터에서 접근할 수 있으며, 네트워크의 트래픽은 도청대상이 될 수 있음
  - **관리 가능성(Manageability)** : 시스템이 서로 다른 유형일 수 있으며 운영체제 버전이 다를 수 있음
  - **예측 불가능(Unpredictability)** : 응답은 시스템의 전반적인 부하, 조직 및 네트워크 부하에 따라 달라짐

- Distributed systems 구조

  - Client-server 구조
    - 클라이언트에 의해 호출되는 분산 서비스. 서비스를 제공하는 서버는 서비스를 사용하는 클라이언트와 다르게 처리
  - Distributed object 구조
    - 클라이언트와 서버간의 차이가 없음. 시스템의 모든 개체는 다른 개체의 서비스를 제공하고 사용할 수 있음

- 계층화된 애플리케이션 구조

  ![Application layers](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Application%20layers.png)

  - 프리젠테이션 계층
    - 계산 결과를 시스템 사용자에게 제시하고 사용자 입력을 수집하는 것에 대해 우려함
  - 응용프로그램 처리계층
    - 예를 들어, 은행 시스템과 같은 애플리케이션 특정 기능(입금, 출금, 대출 등)을 제공하는 것과 같은 것
  - 데이터 관리 계층
    - 시스템 데이터베이스 관리와 관련됨

- Thin 및 Fat 클라이언트

  > 각각 어떨 때 이 모델을 사용하는지

  ![Thin and fat clients](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Thin%20and%20fat%20clients.png)

  - 2계층 클라이언트-서버 구조
    - Thin-client 모델
      - Thin-Client 모델에서는 **모든 응용프로그램 처리 및 데이터관리가 서버에서 수행**됨
      - 클라이언트는 단순히 프리젠테이션 소프트웨어(?)를 실행할 책임이 있다
      - — 
      - 레거시 시스템이 클라이언트-서버 아키텍쳐로 마이그레이션 될 때 사용
        - 레거시 시스템은 클라이언트에 구현된 그래픽 인터페이스를 사용하여 자체 서버로 작동
      - 가장 큰 단점은, **서버와 네트워크 모두에 많은 처리부하**가 걸림
      - 이 모델은 클라이언트가 PC 또는 워크스테이션이 아닌 단순한 네트워크 장치일 때도 구현이 가능
    - Fat-client 모델
      - Fat-Client 모델에서는 서버가 **데이터 관리에 대해서만 책임**을 가집니다
      - 클라이언트의 소프트웨어는 애플리케이션 논리와 시스템 사용자와의 상호작용을 구현
      - —
      - **애플리케이션 처리가 로컬로 실행**됨 (클라이언트가 더 많은 처리를 담당)
      - 클라이언트 시스템의 기능을 미리 알고있는 새로운 C/S 시스템에 최적
      - 특히 관리측면에서 씬 클라이언트 모델보다 **복잡**함. 새로운 버전의 응용프로그램을 모든 클라이언트에 설치해야함(**큰 비용 요구**)

- 3계층 아키텍쳐![A 3-tier C:S architecture](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/A%203-tier%20C:S%20architecture.png)

  - 3계층 아키텍쳐에서 각 애플리케이션 아키텍쳐 계층은 별도의 프로세서에서 실행될 수 있음
  - 씬 클라이언트 접근 방식보다 **우수한 성능을 제공**하며, 팻 클라이언트 방식보다 **관리가 더 간단함**
  - **확장성이 뛰어난** 아키텍쳐 - 수요가 증가함에 따라 추가 서버를 추가할 수 있다

- 분산 객체 아키텍쳐

  ![Distributed object architecture](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Distributed%20object%20architecture.png)

  - 클라이언트와 서버간 분산 객체 아키텍쳐는 **차이점이 없음**
  - 각 분산 가능한 엔티티는 다른 개체에 서비스를 제공하고 다른 개체로부터 서비스를 수신하는 객체 **(양방향)**
  - 개체 통신은 개체 요청 브로커(소프트웨어 버스)라는 미들웨어 시스템을 통해 이루어짐
  - 그러나 C/S 시스템보다 디자인이 더 **복잡** (융통성이 높아질수록 테스트할 때 어려움)

- 분산 객체 아키텍쳐의 장점

  - 이 시스템은 시스템 설계자가 서비스를 제공(어디에서, 어떻게)하는 부분에 대한 결정을 지연시킬 수 있음
  - 이는 매우 개방적인 시스템 아키텍쳐로서, 필요에 따라 새로운 리소스를 추가할 수 있음
  - 소프트웨어 버스 표준은 서로 다른 프로그래밍 언어로 작성된 객체를 사용하여, 서로 통신하고 서비스를 제공할 수 있도록 함
  - 이 시스템은 유연하고 확장 가능함
  - 필요에 따라 네트워크를 통해 이동하는 개체로, 시스템을 동적으로 재구성 할 수 있음

- 분산 객체 아키텍쳐의 용도

  - 시스템을 구조화하고 구성할 수 있는 **논리적 모델**
  - 이 경우 서비스 및 서비스 조합만으로 응용프로그램 기능을 제공하는 방법에 대해 생각해볼 수 있음
  - 클라이언트-서버 시스템 구현에 대한 **유연한 접근방식**
  - 시스템의 논리적 모델은 클라이언트-서버 모델이지만 클라이언트 서버 모두 소프트웨어 버스를 통해 통신하는 분산 객체로 구현



### 10단원, Object-oriented Design

> UML로 간단하게 그려보는 정도
>
> Notation, Object-Oriented Design 을 어디에 사용하는지
>
> 어떤 장점이 있고, 어떤 단점(어려운점이 있는가
>
> 디자인 측면은 제외(숙제, 프로젝트에 나온 부분)하지만 간단한 Class-Diagram은 그려보라 나올 수 있음

- OOD Advantages
  - 간편한 유지관리, 개체가 독립 실행형 엔티티로 인식될 수 있음
  - 개체는 재사용 가능한 구성요소 되어있음
  - 일부 시스템의 경우, 실제 엔티티에서 시스템 오브젝트로의 매핑이 있을 수 있음
- OOD DisAdvantages
  - 객체지향 프로그램은 다른 프로그램보다 규모가 훨씬 커집니다
  - 객체지향 프로그램은 다른 프로그램보다 속도가 느립니다
    - 더 많은 자원 필요
- Object-oriented development
  - 객체지향 분석, 디자인 및 프로그래밍은 서로 관련되어 있지만 구별됨
  - **OOA(Object Oriented Analysis)**는 응용프로그램 도메인의 개체 모델 개발과 관련이 있음
  - **OOD(Object Oriented Design)**는 요구사항을 구현하기 위해 객체지향시스템 모델을 개발하는 것과 관련이 있음
  - **OOP(Object Oriented Programming)**는 Java또는 C++와 같은 OO 프로그래밍 언어를 사용하여 OOD를 구현하는것과 관련이 있음
- 객체지향 프로그래밍(with Wik)
  - 객체 지향 프로그래밍은 프로그램을 유연하고 변경이 용이하게 만들기 때문에 대규모 소프트웨어 개발에 많이 사용
  - 프로그래밍을 더 배우기 쉽게하고 소프트웨어 개발과 보수를 간편하게 하며, 보다 직관적인 코드분석을 가능하게 하는 장점을 가지고 있음
  - 그러나 지나친 프로그램의 객체화 경향은 실제세계의 모습을 그대로 반영하지 못하는 비판을 받기도 함




### 11단원, Real-time Software Design

> Real-time System이 무엇인가

- Real-time System

  > 각각이 무엇인지 파악

  - 실시간 시스템은 시스템의 올바른 기능이 시스템에 의해 생성된 결과와 이러한 결과가 생**성되는 시간에 의존하는 소프트웨어 시스템**
  - 'soft' real-time system
    - 시스템은 결과가 지정된 타이밍 요구사항에 따라 생성되지 않으면 성능이 저하되는 시스템
  - 'hard' real-time system
    - 결과가 타이밍 사양에 따라 결과를 산출하지 않으면 작동하지 않는 시스템

- Stimuls/Response System

  - 입력(자극, Stimulus)이 주어질 때, 시스템은 지정된 시간 내에 응답을 해야함
  - 주기적인 자극. **예측 가능한 시간 간격**으로 발생하는 입력(Stimuli)
    - 예를들어, 온도센서는 초당 10회씩 측정될 수 있음
  - 비주기적인 자극. **예상치 못한 시기**에 일어나는 입력(Stimuli)
    - 예를들어, 시스템 전원 오류로 인해 시스템에서 처리해야 하는 인터럽트가 트리거가 될 수 있음

- 아키텍쳐 고려사항(considerations)

  > 어떻게 처리를 보장하는가
  >
  > interrupt 레벨에서 처리하는 메모리가 따로 존재하며 전용 핸들러가 있는 장치들이 존재함

  - 다른 자극/응답에 의해 만들어진 타이밍 요구에 응답할 필요가 있기 때문에, 시스템 아키텍쳐는 **자극 핸들러 간 빠른 전환을 허용**해야함
  - 서로 다른 자극의 타이밍 요구가 다르므로 간단한 순차적 반복이 일반적으로 적절하지 않음
  - 실시간 시스템은 일반적으로 이러한 프로세스를 제어하는 실시간 실행프로그램과 협력(cooperating) 프로세스로 설계됨

- System design

  - **시스템과 관련된 하드웨어/소프트웨어를 모두 설계**
  - 하드웨어 또는 소프트웨어에 대한 파티션 기능
  - 설계 결정은 **비 기능 시스템 요구사항**에 기초하여 이루어져야 함
  - 하드웨어는 더 나은 성능을 제공하지만, 잠재적으로 개발 기간이 길고 변경 범위가 적음
    - 하드웨어는 소프트웨어보다 처리속도면에서는 항상 월등함, Real-system 에서 하드웨어가 필요하다면 꼭 적용

- R-T 시스템 디자인 프로세스

  > Real-time executive = 작은 OS

  - 자극과 응답처리를 **병행프로세스(concurrent processes)**로 수집
  - 프로세스는 자극 및 반응의 각 부류와 연관됨
  - 자극과 대응의 각 등급을 처리하기 위한 설계 **알고리즘**
  - 주어진 타이밍 요구사항을 충족해야 함
  - 마감일을 맞추기 위해 제 시간에 프로세스를 시작할 수 있도록 **예약 시스템**을 설계
  - **실시간 경영진 또는 운영체제(excutive)를 사용**하여 통합
  - state machine 모델링이 유용함

- 타이밍 제약조건(Timing Constraints)

  - 시스템에 의해 충족되는지 확인하기 위해 광범위한 시뮬레이션과 실험이 필요할 수 있음
  - 추가적인 오버헤드로 인해 객체지향 디자인과 같은 특정설계전략을 사용할 수 없음
  - 성능상의 이유로 낮은 수준의 프로그래밍 언어를 사용해야함

- State machine modeling

  - 실시간 시스템의 자극 효과가 있는 상태에서 다른 상태로의 전이를 일으킬 수 있음
  - **유한 상태 기계(Finite state machines)**는 실시간 시스템을 모델링하는데 사용할 수 있음
  - 그러나, FSM모델은 구조가 결여되어 있음. 간단한 시스템도 복잡한 모델을 가질 수 있음
  - UML은 상태머신모델을 정의하기 위한 표기법

- Real-time excutives

  - 실시간 경영진은 RTS의 프로세스를 관리하는 전용 운영 체제
  - 프로세스 관리 및 자원(프로세서 및 메모리) 할당을 담당
  - 파일 관리 등의 기능은 포함하지 않음



### 12단원, Software testing

- 테스트 프로세스

  - 구성요소 테스트
    - 개별 프로그램 구성요소 테스트
    - 일반적으로 구성요소 개발자의 책임(때로는 중요한 시스템의 경우 제외)
    - 테스트는 개발자의 경험으로부터 얻어짐
  - 통합 시험
    - 시스템 또는 서브 시스템을 만들기 위해 통합된 구성요소 그룹 테스트
    - 독립적인 테스트 팀의 책임
    - 테스트는 시스템 사양을 기반으로 진행

- Black-box 테스팅

  ![Black-box testing](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Black-box%20testing.png)

  - 프로그램이 '블랙 박스'로 간주되는 시험방법
  - 내부를 모르기 때문에 기능이 되는지 안되는지(functional testing)
  - 프로그램 테스트 사례는 시스템 사양을 기반으로 진행
  - 입력 및 관련 출력을 연구함으로써
    - I : 변칙적인 행동을 일으키는 입력들
    - O^e : 결함의 존재를 나타내는 출력

- 등가 분할(Equivalence partitioning )

  - 입력 데이터와 출력 결과는 클래스의 모든 멤버가 관련된 다른 클래스로 분류되는 경우가 종종 있음
  - 각 클래스의 각 프로그램이 각 클래스 멤버에 대해 동일한 방식으로 작동하는 등가 파티션
  - 각 파티션에서 테스트 사례를 선택해야함
  - 최소, 최대, 중간값으로 테스트

- 구조 테스팅(Structural testing)

  ![White-box testing](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/White-box%20testing.png)

  - '화이트 박스' 테스팅이라고 불리는 경우
  - 프로그램 structure 구조물에 따른 시험 사례의 파생
  - 프로그램에 대한 지식(알고리즘)은 추가 테스트 사례를 식별하는데 사용됨
    - 예 : Binary search 를 알고있다면 어떻게 동작하는지 알기 때문에 짝수일때와 홀수일때의 조건을 미리 추가할 수 있음 (유명한 알고리즘에 대해서는 모두 오픈되어있으므로)
  - 목표는 모든 프로그램(모든 경로조합이 아닌)을 연습하는 것

- 경로 테스팅(Path testing)

  - 경로 테스트의 목적은 프로그램의 각 경로가 적어도 한번 실행되도록 하기위한 시험을 실시하는 것
  - 경로시험의 시작점은 프로그램의 결정을 나타내는 노드와 제어흐름을 나타내는 아크를 나타내는 프로그램 흐름 그래프
  - 따라서 조건부 문장은 흐름 그래프의 노드이다

- 프로그램 흐름 그래프

  ![binary search flow graph](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/binary%20search%20flow%20graph.png)

  - 프로그램 제어 흐름을 설명합니다. 각 분기는 별도의 경로로 표시되며 화살표는 루프 조건 노드로 다시 루프됨
  - 순환적 복잡성을 계산하기 위한 기초로 사용됨

- 통합 테스트(Integration testing)

  ![Incremental integration testing](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Incremental%20integration%20testing.png)

  - 통합 구성 요소로 구성된 전체 시스템 또는 서브 시스템을 테스트
  - 통합 테스트는 사양에서 파생된 테스트를 사용하여 '블랙 박스' 테스트를 수행해야함
  - 주요 어려움은 오류를 찾는 것
  - 점진적 통합 테스트를 통해 이 문제를 줄일 수 있다

- **테스팅 방법**

  - 구조 검증(Architectural validation)
    - Top-down 통합 테스트는 시스템 아키텍쳐의 오류를 발견하는데 적합함
  - 시스템 시연(System demonstration)
    - Top-down 통합 테스트를 통해 개발의 초기 단계에서는 제한된 데모가 가능
  - 테스트 구현(Test implementation)
    - Bottom-up 통합 테스트를 통해 간편하게 수행
  - 시험 관찰(Test Observation)
    - 두가지 접근법의 문제점(검사를 관찰하기 위해 추가 코드가 필요할 수 있음)이 존재

- 인터페이스 테스팅

  ![Interface testing](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Interface%20testing.png)

  - 모듈이나 서브시스템을 통합하여 대규모 시스템을 구축할 때 사용
  - 인터페이스 오류 및 인터페이스에 대한 **잘못된 가정에 의한 오류를 감지하는 것이 목적**
  - **객체가 인터페이스에 의해 정의**되기 때문에 **객체 지향 개발에서 특히 중요**

- 인터페이스 타입

  - 파라미터 인터페이스
    - 한 절차에서 다른 절차로 전달된 데이터
  - 공유 메모리 인터페이스
    - 절차 간에 메모리 블록 공유
  - 절차 인터페이스
    - 서브 시스템은 다른 서브 시스템에 의해 불려가는 일련의 절차를 캡슐화함
  - 메시지 전달 인터페이스
    - 서브시스템은 다른 서브 시스템에서 서비스를 요청

- 인터페이스 오류

  - 인터페이스 오용
    - 호출 구성 요소가 다른 구성 요소를 호출하고, 잘못된 순서의 매개변수를 사용하여 인터페이스를 사용하는데 오류가 발생함
  - 인터페이스 오해(misunderstanding)
    - 호출 구성 요소는 잘못된 구성 요소의 동작에 대해 가정
  - 타이밍 오류(Timing errors)
    - 호출 및 호출 구성요소가 서로 다른 속도로 작동하고 오래된 정보에 액세스함

- 스트레스 테스팅

  - 최대 설계 하중을 초과하여 시스템을 테스팅. 시스템에 압력을 가하면 결함이 발생함
  - 시스템 테스트 실패 행위를 간소화함. 시스템은 치명적으로 고장이 나지 않아야 한다. 
  - 스트레스 테스트는 허용되지 않은 서비스 또는 데이터의 손실여부를 점검함
  - 네트워크가 과부화되면 성능의 심각한 저하를 보일 수 있는 분산시스템과 관련이 있음

- Object-oriented 테스팅

  - 테스트 할 구성요소는 객체로 인스턴스화 되는 객체 클래스임
  - 개별 기능보다 입자가 크기 때문에 화이트 박스 테스트에 접근을 확장해야 함
  - 하향식 통합 및 테스트를 위한 확실한 방법이 존재하지 않음
  - 테스트가 어려운 이유는 순서대로 흘러가지 않고 Object끼리 interaction 하기 때문이다



### 13단원, Software cost estimation

> cost estimation 5가지 방법에 대한 설명
>
> 너무 간략하게 쓰지는 말고 디테일 하게
>
> Cost와 Price의 차이점 (Cost 언제 정하는지)

- 소프트웨어 비용 컴포넌트

  - 하드웨어 및 소프트웨어 비용
  - 여행 및 교육 비용
  - 노력 비용 (대부분 프로젝트에서 지배적인 요인)
    - 프로젝트에 종사하는 엔지니어의 급여
    - 보험료
  - 노력비용은 오버헤드를 고려해야함
    - 건물, 난방, 조명비용
    - 네트워킹 및 통신비용
    - 공유 시설 비용 (도서관, 직원 식당 등)

- 생산성 측정(Productivity measure)

  - 소프트웨어 프로세스에서 어떤 **출력에 따라 관련 크기를 측정**함
  - 이것은 전달된 소스코드(라인 수), 객체 코드 명령어 등이 될 수 있음
    - 예전에는 코드라인으로 판단(전통적인 부분), 현재는 그렇지 않음
  - **기능 관련 측정**은 제공된 소프트웨어의 기능에 대한 예상치를 기반으로 함
  - **기능 점수**는 이러한 유형의 측정값으로 가장 잘 알려져 있음

- 함수-포인트 수

  - 프로그램 특성의 조합에 기반
    - 외부 입력 및 출력
    - 사용자 상호작용
    - 외부 인터페이스
    - 시스템에서 사용하는 파일
  - 가중치는 이들 각각과 연관되어 있음
  - 기능 점수는 각 원시 계수에 가중치를 곱하고 모든 값을 합산하여 계산됨

- 측정 기술

  - 소프트웨어 시스템 개발에 필요한 노력을 정확하게 예측할 간단한 방법은 없음
    - 초기 추정치는 사용자 요구사항 정의의 불충분한 정보를 기반으로 진행
    - 이 소프트웨어는 익숙하지 않은 컴퓨터에서 실행되거나 새로운 기술을 사용할 수 있음
    - 그 프로젝트의 사람들은 알 수 없을지도 모름
  - 프로젝트 비용 추정치는 자기 충족일 수 있음
    - 견적은 예산을 정의하고 예산을 충족하도록 제품을 조정

- **측정 방법**

  > 측정하는 방법 정도가 무엇인가

  - 알고리즘 비용 모델링 (COCOMO, 수학적인 계수를 조정해서 해보는 것)
    - 히스토리 비용정보를 기반으로 하고, 일반적으로 소프트웨어의 크기를 기반으로 하는 공식적인 접근법
  - 전문가 판단 (전문가를 데려옴)
    - 소프트웨어 개발 및 응용 도메인에서 한 명 이상의 전문가가 소프트웨어 비용을 예측하는 경험을 가지고 있음
    - 프로세스는 합의가 있을때까지 반복
    - 장점 : 상대적으로 저렴한 평가방법. 전문가가 유사한 시스템을 경험하였을 경우 정확한 정보를 얻을 수 있음
    - 단점 : 전문가를 구하기 힘들고 구하지 못하면 매우 부정확함
  - 유추에 의한 추정 (수학적인 부분에 근거하여)
    - 프로젝트 비용을 동일한 프로젝트 도메인과 유사한 프로젝트와 비교하여 계산
    - 장점 : 프로젝트 데이터를 사용할 수 있는경우 정확함
    - 단점 : 비교 가능한 프로젝트가 없다면 불가능
  - 파킨슨 법칙 (내가 할 수 있는 부분에 대해서 모두 해보는 것)
    - 작업은 가능한 시간 내에서는 계속되고, 비용이 있으면 다 쓰게 된다는 의미
    - 일은 무조건 데드라인에 맞춰 끝나게 되어있음
    - 비용은 객관적인 평가가 아니라 이용 가능한 자원에 의해 결정됨
      - 소프트웨어를 12개월로 제공, 5명이 60명분일 경우
    - 장점 : 초과 지출 없음
    - 단점 : 시스템이 대부분 미완성됨
  - 우승하기 위한 가격 정책 (갑을 관계에서 시키는 대로) - 능력별 지급
    - 프로젝트 비용은 고객이 무엇을 하고있어도 괜찮음
    - 장점 : 당신은 계약을 체결
    - 단점 : 고객이 원하는 시스템을 얻을 수 있는 확률이 적으며, 비용은 필요한 작업량을 정확히 반영하지 않음

- 교수님 말씀

  - 알고리즘의 수치값은 시기마다 달라짐
    - COCOMO 2차 버전에서는 공식이 달라지기 때문에 시기마다 달라질 수 있음
  - 아키텍쳐 설계가 끝나면 적어도 비용이 계산되어야 함


- 직원 배치 요구사항
  - 필요한 일정에 따라 개발시간을 단축함으로써 필요한 인원수를 산출할 수 없음
  - 프로젝트에 참여하는 사람의 수는 프로젝트 단계에 따라 달라짐
  - 프로젝트에서 일하는 사람이 많을수록 더 많은 노력이 필요함
  - 사람들이 매우빠른속도로 쌓이는 것은(?) 종종 일정의 착오(미끄러짐)과 관련이 있음





- distributed 에서 시스템에서 하나 나온다고 하면
- Real-time
- Object-oriented
  - Design X
- 6장부터 13장까지 골고루
- 테스트 방법 다르고
- 각 챕터마다 중요한것이 나올것이고
- 골고루 분배되서 나옴
















