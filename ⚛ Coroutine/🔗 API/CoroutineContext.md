---
importance: Highest
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
  - GPT
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
public interface CoroutineContext
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)을 실행하는 [실행 환경](실행%20환경.md)을 설정하고 관리하는 인터페이스
- 코루틴의 실행을 위한 [컨텍스트](코루틴%20컨텍스트.md) 정보를 포함하는 인터페이스

##### ⭐️ Feature
---
- 다양한 요소와 요소들의 결합 및 수정 규칙을 정의하는 기능을 제공
- 코루틴을 실행하고 관리하는 데 핵심적 역할
- 구성 요소들을 키-값 쌍으로 관리하고, 각 구성 요소는 객체를 하나씩만 가짐
```Kotlin
val singletonKey = CoroutineName.Key
val key = CoroutineName
val keyProperty = coroutineName.key
``` 

##### 🎼 Composition
---
- [CoroutineName](CoroutineName.md)
- [CoroutineDispatcher](CoroutineDispatcher.md)
- [Job](Job.md)
- [[CoroutineExceptionHandler]]

##### 🔑 How to get a key?
---
- 구성 요소 키 획득 방법 ^desc-1
	- 싱글톤 키
	- 구성 요소 자체
	- 구성 요소의 `key` 프로퍼티

##### 🔗 API
---
- [CoroutineContext.plus](CoroutineContext.plus.md): `CoroutineContext`를 구성하는 연산자 함수
- [CoroutineContext.get](CoroutineContext.get.md): 구성 요소에 접근하는 연산자 함수
- [CoroutineContext.minusKey](CoroutineContext.minusKey.md): 구성 요소를 제외하는 함수(새 `CoroutineContext` 객체 생성하여 반환)
