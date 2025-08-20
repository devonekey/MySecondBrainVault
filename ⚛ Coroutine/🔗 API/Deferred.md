---
importance: Highest
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
  - OpenAI
parent pages:
  - "[[Job]]"
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
interface Deferred<out T> : Job
```

##### ℹ️ Description
---
- 미래의 어느 시점에 결괏값이 반환될 수 있음을 표현하는 [코루틴](코루틴.md) 객체
- [Job](Job.md) 인터페이스의 서브타입으로 선언된 인터페이스

##### ➕ Extra
---
- 비동기적으로 수행된 작업의 결과를 포함하는 Job의 하위 유형
- `Job`과 같이 코루틴을 추상화한 객체이지만, 코루틴으로부터 생성된 결괏값을 감싸는 기능을 가짐
- 결과가 준비되면 [await](Deferred.await.md) 함수를 사용하여 결과를 얻을 수 있으며, 작업이 완료될 때까지 [일시 중단](일시%20중단.md)됨
- `Job` 객체의 모든 함수와 프로퍼티를 사용할 수 있음
