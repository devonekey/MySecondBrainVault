---
aliases:
  - async
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
  - "[[📘 코틀린 동시성 프로그래밍/1장 - Hello, Concurrent World!]]"
answered by:
  - Book
  - OpenAI
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
public fun <T> CoroutineScope.async(
    context: CoroutineContext = EmptyCoroutineContext,
    start: CoroutineStart = CoroutineStart.DEFAULT,
    block: suspend CoroutineScope.() -> T
): Deferred<T>
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)을 생성하는 [코루틴 빌더](코루틴%20빌더.md) 함수 ^desc-1

##### 🎯 Purpose
---
- [비동기 작업](비동기%20작업.md)으로부터 결과를 수신해야 하는 경우에 사용

##### ⭐️ Feature
---
- 결괏값이 있는 코루틴 객체인 [Deferred](Deferred.md)가 반환되며, [await](Deferred.await.md) 함수를 사용해 결괏값을 수신할 수 있음함

##### 🔥 Exception Propagation
--- 
- `async` 코루틴 실행 도중 [예외](예외.md)가 발생해 결괏값이 없다면, `await` 함수 호출 시 예외가 노출됨 ^desc-2
- `async` 코루틴에서 예외가 발생하면, [부모 코루틴](부모%20코루틴.md)으로 [예외를 전파](예외%20전파.md)함 ^desc-3

##### 🧯 How to handle Exception?
---
- [supervisorScope](supervisorScope.md)를 사용한 예외 전파 제한 + `try`-`catch`문으로 `await` 함수 호출 시 노출되는 [예외를 처리](예외%20처리.md) ^desc-4
```Kotlin
supervisorScope {
    val deferred = async {
        throw Exception("예외 발생")
    }

	try {
        deferred.await()
    } catch (e: Exception) {
        // do something...
    }
}
```
^code-1

##### ➕ Extra
---
![[CoroutineScope.launch.md#^desc-2]]
