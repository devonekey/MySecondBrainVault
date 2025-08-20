---
aliases:
  - launch
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/2장 - 코루틴 개발 환경 설정]]"
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
  - "[[📘 코틀린 동시성 프로그래밍/1장 - Hello, Concurrent World!]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineScope]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public fun CoroutineScope.launch(  
    context: CoroutineContext = EmptyCoroutineContext,
    start: CoroutineStart = CoroutineStart.DEFAULT,  
    block: suspend CoroutineScope.() -> Unit  
): Job
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)을 생성하는 [코루틴 빌더](코루틴%20빌더.md) 함수 ^desc-1

##### ➕ Extra
---
- 결과를 반환하지 않는 코루틴을 생성함
- 관련 매개변수 ^desc-2
	- [CoroutineContext](CoroutineContext.md)
	- [CoroutineStart](CoroutineStart.md)
	- [CoroutineScope](CoroutineScope.md)
- [실행 환경](실행%20환경.md)은 아래 절차로 구성됨
	1. `CoroutineScope`로부터 `CoroutineContext` 객체를 제공받음
	2. 제공받은 `CoroutineContext` 객체에 `context`인자로 넘어온 `CoroutineContext`를 덮어씀
	3. 덮어쓴 `CoroutineContext` 객체에, 코루틴 빌더 함수가 호출돼 생성된 새 [Job](Job.md)을 덮어씀
		- 덮어쓰기 전의 `CoroutineContext`의 `Job` 객체는 새 `Job` 객체의 부모가 됨
	4. `block` 람다식의 수신 객체(`CoroutineScope`)를 통해 최종적으로 구성된 실행 환경(`coroutineContext`)에 접근할 수 있음
