---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - suspend
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public suspend fun yield(): Unit
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)으로 하여금 자신이 사용하던 [스레드](스레드.md)를 [양보](양보.md)하는 [일시 중단](일시%20중단.md) 함수

##### ➕ Extra
---
- 해당 함수를 호출한 코루틴이 일시 중단되며, 이 시점에 취소됐는지 확인함
