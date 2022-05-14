# TodoList
Clean Architecture based Project 




TDD - Test Driven Development의 약자로, 테스트가 개발을 이끌어감을 의미
테스트를 먼저 만들고 테스트를 통과하기 위한 것을 것
결정과 피드백 사이에 Gap을 조절 할 수 있는 테크닉 중 하나

TDD가 필요한 이유 - 잦은 피드백과 협력을 증진 시킬 수 있는 방법

TDD가 필요한 상황
1. 결과가 너무나도 뻔하다면 굳이 TDD로 개발하진 않아도 된다.
2. 자신감 지수가 낮은 경우
3. 요구사항이 빈번하게 변경 되는 경우
4. 테크니컬한 스펙, 비지니스 로직이 자주 바뀌는 경우
5. 개발하고 난 이후에 다른 개발자에게 인스인계가 필요한 경우

그럼에도 TDD가 어려운 경우
1. 개발시간의 증가 -> 필요성을 못느끼는 경영, 실무진이 있음
2. TDD 자체가 어렵다.
   -일반적인 개발방식과 반대로 진행 from(개발->테스트) to (테스트 ->개발)
   -체득한 것을 놓기 어려움

TDD를 위한 진입장벽
- 툴(단위테스트 프레임워크) 이용에 대한 강박 -> 그럴 필요없다. 베이스 코드가 필요하긴 하지만..
- 규픽에 얽메이면 개발을 주도해가기 어려움

TDD를 잘 하는 방법
1. 피드백을 자주 받을 수 있는 환경을 만든다.
- 테스트 케이스 작성
- 주기적인 프로세스 검증
2. 작업을 협력할 수 있는 방법으로 고민
- 비지니스 로직을 고민
- 프로덕트 스펙을 잘게 쪼갠다.
- 민첩하게 비지니스 로직을 수현 -> 빠르게 검증

TDD 구현 과정
- 비지니스 로직을 분리 할 수 있는 클린아키텍처 basecamp구축
- 유닛테스트 구현을 위한 도구 도입 (DI, Mock)
- 각 유닛테스트 파일 생성 및 목적에 맞는 시나리오 작성하기
- 시나리오에 필요한 Usecase작성, 각 레이어 구축 ( Repository, Model)
- 각 상태를 Sate Pattern으로 표현하여 쉬운 방법으로 결과 검증

이 프로젝트에서 설계할 시나리오
- Todo 아이템 데이터 Insert -> 잘 불러와지는지 확인
- 아이템 업데이트, 삭제 동작 확인
- 상세화면 아이템 정보 확인
- 작성, 수정에 따른 Todo 추가 업데이트 확인

클린 아키텍처를 위한 세가지 레이어
- Presentation Layer : View(Activity, Fragment) , Presenter(Controller, Presenter, ViewModel )
- Domain Layer: Usecase , Translater(Entity-> Model)
- Data Layer:  Repository ( Domain과 data store, remote layer를 연결하기 위함), Entity ( 최소단위 비지니스 객체) 

