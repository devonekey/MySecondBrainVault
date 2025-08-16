---
importance: Highest
originated from:
  - "[[📘 코틀린 코루틴의 정석/2장 - 코루틴 개발 환경 설정]]"
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
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
public interface CoroutineScope {
    public val coroutineContext: CoroutineContext
}
```

##### ℹ️ Description
---
- 자신의 범위 내에서 생성된 [코루틴](코루틴.md)들에게 [실행 환경](실행%20환경.md)을 제공하는 객체

##### ⭐️ Feature
---
- 코루틴들의 실행 범위를 관리하는 역할을 함

##### 🪄 How to create?
---
- `CoroutineScope` 인터페이스 구현을 통한 생성
```Kotlin
class CustomCoroutineScope : CoroutineScope {
    override val coroutineContext: CoroutineContext =
        newSingleThreadContext("MyThread") + Job()
}
```
- `CoroutineScope` 함수를 사용한 생성
	- `context` 인자로 입력된 [CoroutineContext](CoroutineContext.md)의 구성 요소로 [Job](Job.md)이 포함되지 않으면, 새로운 `Job`을 생성함
```Kotlin
@Suppress("FunctionName")  
public fun CoroutineScope(context: CoroutineContext): CoroutineScope =  
    ContextScope(if (context[Job] != null) context else context + Job())
```

##### 📍 Point
---
- `CoroutineScope`는 `coroutineContext` [불변 변수](불변%20변수.md)를 가지는 데, 이 사실을 통해  `CoroutineScope` 확장 함수인 [launch](CoroutineScope.launch.md), [async](CoroutineScope.async.md) 함수에서 `block` 람다식 수신 객체(`CoroutineScope`)로 [실행 환경](실행%20환경.md)(`CoroutineContext`)을 구성하여 제공함을 알 수 있음
- [cancel](CoroutineScope.cancel.md), [isActive](CoroutineScope.isActive.md)로 비추어볼 때, `CoroutineScope`를 다루는 것은 `coroutineContext` 구성 요소인 [Job](Job.md) 객체를 다루는 것임을 알 수 있음
