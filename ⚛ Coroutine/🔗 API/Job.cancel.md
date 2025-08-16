---
aliases:
  - cancel
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
parent pages:
  - "[[Job]]"
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
public interface Job : CoroutineContext.Element {
	public fun cancel(cause: CancellationException? = null)
}
```

##### ℹ️ Description
---
- 생성 또는 실행 중인 [코루틴](코루틴.md)을 취소하는 함수

##### ➕ Extra
---
- 함수를 호출했더라도 즉시 취소되는 것이 아닌 [Job](Job.md) 객체 내부의 취소 확인용 플래그가 '취소 요청됨'으로 변경됨
- 미래의 어느 시점에 취소 TODO("내용 보충 필요")
