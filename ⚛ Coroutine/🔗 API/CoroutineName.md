---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/2장 - 코루틴 개발 환경 설정]]"
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - data
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
public data class CoroutineName(  
    val name: String  
) : AbstractCoroutineContextElement(CoroutineName)
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)의 이름을 구분하는 클래스
- 코틀린의 이름을 설정

##### ➕ Extra
---
```Kotlin
public data class CoroutineName(  
    val name: String  
) : AbstractCoroutineContextElement(CoroutineName) {
    public companion object Key : CoroutineContext.Key<CoroutineName>
}
```
![[CoroutineContext.md#^desc-1]]
