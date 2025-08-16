---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
  - OpenAI
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - interface
learned:
---
##### 🖋️ Signature
---
```Kotlin
@SinceKotlin("1.3")  
public interface Continuation<in T>
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)의 [일시 중단](일시%20중단.md) 지점에 코루틴의 실행 상태를 저장하며, 다음에 실행해야 할 작업에 대한 정보가 포함된 객체
- `suspend` 재개 상태를 담은 객체

##### ➕ Extra
---
- 코루틴 [재개](재개.md) 시 코루틴의 상태를 복원하고 이어서 작업을 진행도록 만듦
- 고수준의 API는 `Continuation` 객체를 캡슐화해 사용자에 노출하지 않지만 내부적으로는 일시 중단과 재개가 `Continuation` 객체를 통해 이뤄짐
- 일시 중단이 일어나면 `Continuation`에 실행 정보가 저장되며, 일시 중단된 코루틴은 `Continuation` 객체에 대해 `resume` 함수가 호출돼야 재개됨
