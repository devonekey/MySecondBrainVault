---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineContext]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - operator
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface CoroutineContext {
	public operator fun plus(context: CoroutineContext): CoroutineContext
}
```

##### ℹ️ Description
---
- [CoroutineContext](CoroutineContext.md)를 구성하는 연산자 함수

##### ➕ Extra
---
```Kotlin
val context = CoroutineName("코루틴 이름") + Dispatchers.IO + Job() + CoroutineExceptionHandler { coroutineContext, throwable -> }
```
- 연산자 함수이기 때문에 `+`로 대체할 수 있음
- 키에 값을 직접 대입하지 않고 `CoroutineContext` 객체 간에 더하기 연산자(`+`)를 사용해 구성
- 설정되지 않은 구성 요소는 설정되지 않은 상태로 유지됨
- 만약 같은 구성 요소가 둘 이상 더해진다면, 나중에 추가된 구성 요소가 이전의 값을 덮어씌움
- `Job`을 직접 추가하면, 구조화가 깨지기 때문에 주의해야 함
