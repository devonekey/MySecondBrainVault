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
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface CoroutineContext {
	public fun minusKey(key: Key<*>): CoroutineContext
}
```

##### ℹ️ Description
---
- [CoroutineContext](CoroutineContext.md)로부터 `key` 인자로 넘긴 구성요소를 제외하고, 새 `CoroutineContext` 객체를 반환하는 함수

##### ➕ Extra
---
```Kotlin
val newContext = coroutineContext.minusKey(CoroutineName)
```
- `minusKey` 함수를 호출한 `CoroutineContext` 객체의 유지되고 새 `CoroutineContext` 객체가 반환됨
