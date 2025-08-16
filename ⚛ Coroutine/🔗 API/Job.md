---
importance: Highest
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - interface
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface Job : CoroutineContext.Element
```

```Kotlin
public fun Job(parent: Job? = null): CompletableJob
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)을 추상화한 객체

##### ⛔️ How to prevent Exception Propagation?
---
- [Job](Job.md) 객체를 사용한 [예외 전파 제한](예외%20전파%20제한.md) ^desc-1
	- 부모 코루틴과의 구조화를 깨 [예외가 전파](예외%20전파.md)되지 못하도록 만듦
	- [예외 전파](예외%20전파.md)를 제한하는 것뿐만 아니라 [취소 전파](취소%20전파.md)도 제한됨 → [비동기 작업](비동기%20작업.md)을 불안정하게 만듦
```Kotlin
launch(CoroutineName("Parent Coroutine")) {
	launch(CoroutineName("Child Coroutine") + Job()) {
	    throw Exception("예외 발생")
	}
	// 해당 코루틴은 취소되지 않음
}
```
^code-1

##### ➕ Extra
---
- 상태를 추적하고 제어하는 데 사용
```Kotlin
public interface Job : CoroutineContext.Element
    public companion object Key : CoroutineContext.Key<Job>
}
```
![[CoroutineContext.md#^desc-1]]
- 내부에 정의된 `Job?` 타입의 `parent` 프로퍼티를 통해 [부모 코루틴](부모%20코루틴.md)의 [Job](Job.md) 객체에 대한 참조를 가짐
- `Sequence<Job>` 타입의 `children` 프로퍼티를 통해 [자식 코루틴](자식%20코루틴.md)의 `Job`에 대한 참조를 가짐
