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
    public operator fun <E : Element> get(key: Key<E>): E?
}
```

##### ℹ️ Description
---
- [CoroutineContext](CoroutineContext.md)의 구성 요소에 접근하는 연산자 함수

##### ➕ Extra
---
```Kotlin
coroutineContext.get(CoroutineName)
coroutineContext[CoroutineName]
```
- 연산자 함수이기 때문에 `[]`로 대체할 수 있음
