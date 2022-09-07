# flutter_bloc_memo

Flutter BLoC 패턴 필기

## BLoC 패턴을 사용하는 이유

위젯간 데이터 전달 및 UI 동적 표현을 위해서 사용함.

블록 패턴이 없으면 데이터 전달에서 하위위젯에게 전달하기 위해 멤버 변수를 연속적으로 선언해야 한다.

하위위젯에서 콜백을 할 때에도 반대로 연속적으로 코드를 수정해야 한다.

![캡처](https://user-images.githubusercontent.com/112848594/188787527-aa49accc-0b4e-4183-8379-6a7317e83652.PNG)

이를 해결하기 위해 블록 패턴을 이용

![캡처3](https://user-images.githubusercontent.com/112848594/188787592-084b026f-1e00-4c91-9bb8-f393539e4997.PNG)

Bussiness Logic Component 로 비즈니스 로직을 UI와 분리하여 UI는 블록으로부터 데이터만 받고 보여주기만 하면 된다.

블록은 state를 관리 : 데이터의 변경 사항을 반영하여 UI 에게 stream으로 전달

![캡처2](https://user-images.githubusercontent.com/112848594/188787603-8d3cadab-b562-491c-a90f-52a345ac57eb.PNG)

![4](https://user-images.githubusercontent.com/112848594/188787606-0afa004a-1273-4a74-b3f8-5ae811c468c6.PNG)

블록을 구독하고 있는 위젯에게만 데이터 전달, 그 위젯들만 변경됨


## BLoC 패턴의 단점

1. 관리되는 블록 파일들이 많아 진다. 복잡한 비즈니스 로직이 있으면 관리 대상이 많아질 수 있다.
2. 진입 장벽이 좀 있다.
