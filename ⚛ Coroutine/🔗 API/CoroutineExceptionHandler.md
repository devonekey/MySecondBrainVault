---
importance: High
originated from:
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
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface CoroutineExceptionHandler : CoroutineContext.Element
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)에서 발생한 [예외 처리](예외%20처리.md)를 정의할 수 있는 인터페이스

##### 🎯 Purpose
---
- 로그 출력 또는 오류 메시지를 표시할 때 사용
	- [CoroutineExceptionHandler](CoroutineExceptionHandler.md)가 동작할 때는 이미 [예외](예외.md)로 인해 코루틴이 완료된 상태로, 복구시킬 수 없음

##### 🪄 How to create?
---
- `CoroutineExceptionHandler` 함수를 사용한 생성
```Kotlin
@Suppress("FunctionName")  
public inline fun CoroutineExceptionHandler(crossinline handler: (CoroutineContext, Throwable) -> Unit): CoroutineExceptionHandler
```

##### 🧯 How to handle?
---
- `CoroutineExceptionHandler` 사용한 예외 처리 ^desc-1
	- 처리되지 않은 예외만 처리함
		- 만약 [부모 코루틴](부모%20코루틴.md)으로 [예외를 전파](예외%20전파.md)하면, [자식 코루틴](자식%20코루틴.md)에서는 예외가 처리됐다고 간주함 → 자식 코루틴에 설정된 `CoroutineExceptionHandler` 객체는 동작하지 않음
		- 최상위 [루트 코루틴](루트%20코루틴.md)에 설정된 `CoroutineExceptionHandler`가 예외를 처리함
	- 예외 전파를 제한하지 않음
		- `try`-`catch` 처럼 [예외 전파를 제한](예외%20전파%20제한.md)하는 것이 아님
```Kotlin
val exceptionHandler = CoroutineExceptionHandler { coroutineContext, throwable ->
	// do something...
}
	CoroutineScope(exceptionHandler).launch(CoroutineName("Coroutin1")) {
	launch(CoroutineName("Coroutine2")) {
		throw Exception("예외 발생")
	}
}
```
^code-1

##### ➕ Extra
---
```Kotlin
public interface CoroutineExceptionHandler : CoroutineContext.Element {
    public companion object Key : CoroutineContext.Key<CoroutineExceptionHandler>
}
```
![[CoroutineContext.md#^desc-1]]
