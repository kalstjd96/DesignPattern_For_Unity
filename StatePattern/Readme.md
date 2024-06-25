### 참고 ㅣ Unity Square - Unity Resources
# State Pattern
<img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=200&section=header&text=State_Pattern&fontSize=80" /> 

## State 패턴이란
- 객체의 내부 상태에 따라 스스로 행동을 변경
- 상태를 클래스로 캡슐화하고, 상태 전환을 클래스 간의 참조 변경으로 처리
- Ex. 캐릭터 애니메이션 상태, 네트워크 연결 상태, 툴 상태


### 장점  
- 유연한 상태 전환 : 상태를 캡술화하여 상태 전환 로직을 각 상태 클래스에 분리
- 상태 전환을 더 쉽게 관리하고 확장할 수 있게 함
- 가독성 향상 : 상태 전환 로직이 각 상태 클래스에 분리되어 있어, 코드의 가독성이 향상
- 유지보수 용이성 : 상태를 추가 및 변경 시, 다른 상태 클래스의 영향 없이 독립적으로 작업

### 단점   
- 클래스 증가 : 상태별로 별도의 클래스가 필요하기 때문에 클래스의 수가 증가
- 복잡성 증가 : 상태가 많아질 경우 관리해야 할 클래스와 코드의 복잡성이 증가


## FSM, Finite State Machine (유한상태기계)
- 시스템이 가질 수 있는 모든 상태와, 한 상태에서 다른 상태로 전환하는 규칙을 정의하는 모델

** 기본 구성 ** 

```c#
public interface IState
{
     public void Enter()
     {
     // 상태에 처음 진입할 때 실행되는 코드
     }
     public void Update()
     {
     // 프레임당 로직. 새로운 상태로 전환하는 조건 포함
     }
     public void Exit()
     {
     // 상태에서 벗어날 때 실행되는 코드
     }
}
```
