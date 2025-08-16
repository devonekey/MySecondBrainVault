---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
parent pages:
  - CompletableJob
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
learned:
---
##### 🖋️ Signature
---
```Kotlin
@Suppress("FunctionName")  
public fun SupervisorJob(parent: Job? = null) : CompletableJob
```

##### ℹ️ Description
---
- [자식 코루틴](자식%20코루틴.md)으로부터 [예외를 전파](예외%20전파.md)받지 않는 특수한 [Job](Job.md) 객체

##### 🎯 Purpose
---
- 하나의 자식 코루틴에서 발생한 [예외](예외.md)가 다른 자식 코루틴에게 영향을 미치지 못하도록 만드는 데 사용 ^desc-3

##### ⛔️ How to prevent Exception Propagation?
---
- [SupervisorJob](SupervisorJob.md) 객체를 사용한 [예외 전파 제한](예외%20전파%20제한.md) ^desc-1
	- `SupervisorJob` 생성 함수의 `parent` 인자로 아무것도 넘기지 않으면, `SupervisorJob`을 [루트 Job](루트%20Job.md)으로 만들 수 있음
	- `parent` 인자로 부모 `Job` 객체를 넘기면, 구조화를 깨지 않고 예외 전파를 제한할 수 있음
		- 자동으로 완료되지 않으므로, [complete](CompletableJob.complete.md) 함수를 호출하여 명시적으로 완료 처리를 해야 함
```Kotlin
launch(CoroutineName("Parent Coroutine")) {
    val supervisorJob = SupervisorJob()

	launch(CoroutineName("Child1 Coroutine") + supervisorJob) {
		throw Exception("예외 발생")
	}
	launch(CoroutineName("Child2 Coroutine") + supervisorJob) {
		// 해당 코루틴은 취소되지 않음
	}
}
```
^code-1

```Kotlin
launch(CoroutineName("Parent Coroutine")) {
    val parentJob = this.coroutineContext[Job]
    val supervisorJob = SupervisorJob(parent = parentJob)

	launch(CoroutineName("Child1 Coroutine") + supervisorJob) {
		throw Exception("예외 발생")
	}
	launch(CoroutineName("Child2 Coroutine") + supervisorJob) {
		// 해당 코루틴은 취소되지 않음
	}

	supervisorJob.complete()
}
```
^code-2

- `SupervisorJob` + [CoroutineScope](CoroutineScope.md)를 함께 사용한 예외 전파 제한 ^desc-2
```Kotlin
val coroutineScope = CoroutineScope(SupervisorJob())

coroutineScope.apply {
    launch(CoroutineName("Coroutine1")) {
        throw Exception("예외 발생")
    }
    launch(CoroutineName("Coroutine2")) {
        // do 해당 코루틴은 취소되지 않음
    }
}
```
^code-3

##### ⚠️ Warning
---
- [코루틴 빌더](코루틴%20빌더.md) 함수의 `parent` 인자로 `SupervisorJob` 객체를 넘기고 코루틴이 생성되면, 생성된 `Job` 보다 `SupervisorJob`이 부모에 위치하게 되고, 자식 코루틴의 예외로 인해 다른 자식 코루틴이 취소되는 문제가 발생
```Kotlin
launch(CoroutineName("Parent Coroutine") + SupervisorJob()) {
	launch(CoroutineName("Child1 Coroutine")) {
		throw Exception("예외 발생")
	}
	launch(CoroutineName("Child2 Coroutine")) {
		// Child1 Coroutine의 예외가 Parent Coroutine까지 전파됨에 따라 해당 코루틴은 취소됨
	}

	supervisorJob.complete()
}
```
