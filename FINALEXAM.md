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


    - **이벤트 기반 제어(Event-based control)**

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



### 10장, Object-oriented Design

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
- 객체지향 프로그래밍(with Wiki)
  - 객체 지향 프로그래밍은 프로그램을 유연하고 변경이 용이하게 만들기 때문에 대규모 소프트웨어 개발에 많이 사용
  - 프로그래밍을 더 배우기 쉽게하고 소프트웨어 개발과 보수를 간편하게 하며, 보다 직관적인 코드분석을 가능하게 하는 장점을 가지고 있음
  - 그러나 지나친 프로그램의 객체화 경향은 실제세계의 모습을 그대로 반영하지 못하는 비판을 받기도 함













