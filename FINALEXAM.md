## 2017-2 소프트웨어공학 기말고사 정리 (최수미 교수님)

[Return README.md](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/README.md)

개인적으로 [이곳](https://blog.naver.com/PostView.nhn?blogId=s2kiess&logNo=220155111239&parentCategoryNo=&categoryNo=159&viewDate=&isShowPopularPosts=true&from=search) 정리 짱 잘함

### 6단원(System Models)

> 디자인 해보아라 (Data Processing model 또는 Functional processing)
>
> Data-Flow Diagram

- Model Types (6-6) : DCACS

  - Data Processing model : 데이터가 각각의 단계에서 **어떻게 처리되는지** 보여주는 모델 (데이터 흐름도)

  - Composition model : 엔티티가 **다른 엔티티로 구성**되는 방법을 보여주는 구성 모델 (엔티티-관계 다이어그램)

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

  - State-Machine 모델

    ![State machine model](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/State%20machine%20model.png)

    - 해당 모델은 **외부 및 내부 이벤트에 대응하여 시스템의 동작을 모델링함**
    - 자극(stimuli)에 대한 시스템의 반응을 보여주기 때문에 **실시간 시스템**의 모델링에 자주 사용
    - 상태 기계 모델(State machine models)은 시스템 **상태를 노드 간 arcs와 event로 표시**함
    - 이벤트가 발생하면 시스템은 한 상태에서 다른 상태로 전환
    - State-Charts는 UML의 중요한 부분
    - ![Microwave oven operation(a super-state)](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/Microwave%20oven%20operation(a%20super-state).png)
    - 모델을 하위 모델로 분류할 수 있음

- 어떤 짧은 모델에 대해서 '특정 모델'로 해보아라 할 수 있음(**각 모델의 Notations가 Point**)

  - Data-Process 모델의 Notations : **기능처리, 데이터 저장소 및 데이터 이동**
  - State-Machine 모델의 Notations : **응답(Stimuli), 상태(State), 행동에 대한 설명(Brief description of the actions in that state)**

- The Unified Modeling Language : UML

  ![User Class Hierarchy](https://github.com/antaehyeon/softwareEngineeringTP/blob/master/image/User%20Class%20Hierarchy.png)

  - 광범위하게 사용되는 객체 지향 분석 및 설계 방법
  - **객체 지향(Object-Oriented) 모델링 표기법에 대한 효과적인 표준**
  - Notation
    - 객체 클래스는 **상단에 있는 이름과 하위 섹션의 속성 및 하위 섹션의 작업을 포함하는 사각형으로 구성**
    - 개체(object) 클래스(연결이라고도 함)간의 관계는 **개체를 연결하는 선**으로 표시
    - 상속은 일반적으로 생성되며, 계층 내에서 '아래쪽'이 아닌 **'위쪽(upwards)'**으로 표시



- State machine model 로 디자인 하라
  - State 단위로 해서 event가 움직이는
  - 복잡하면 Super-state로 구성하고, 설명한다던지



- 상속을 이용해서 정의해봐라
- UML Notation (10-29) 에 맞게 그릴 것
- Sequence Diagram은 (숙제로 하고있으므로) 디테일하게 내지 않음



- Data-Process, State-Machine, Object-Oriented Model
- 특징이 무엇인지 비교했을 때 특징들을 살펴볼 것