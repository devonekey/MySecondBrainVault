---
importance: High
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - Perplexity
parent pages: []
tags:
  - Jetpack
  - Compose
  - 컴포즈
  - Kotlin
  - API
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
package androidx.compose.runtime

@StateFactoryMarker
fun <T> mutableStateOf(
    value: T,
    policy: SnapshotMutationPolicy<T> = structuralEqualityPolicy()
): MutableState<T>
```

##### ℹ️ Description
---
- [컴포즈](젯팩%20컴포즈.md)에서 [상태](상태.md)를 관리하는 데 사용되는 함수
- 상태 객체를 생성하는 팩토리 함수

##### ⭐️ Feature
---
- `mutableStateOf`로 감싼 변수 변경 시, [재구성](재구성.md)됨
  → `MutableState` 객체는 상태를 읽거나 쓸 때 Compose 런타임에 변화를 알림
- 구조 분해 할당을 이용하면 상태 값과 상태 변경 함수를 동시에 다룰 수 있음

##### 🧩 Parameters
---
- `value: T`: 초기에 사용할 값
- `policy: SnapshotMutationPolicy<T>`: 상태 비교 시 비교에 사용할 정책

##### 🎤 How to declare State?
---
- 기본 사용
```Kotlin
val state = mutableStateOf(value)
```
- by 위임(getter, setter 위임)
```Kotlin
var state by mutableStateOf(value)
```
- 구조 분해 할당
```Kotlin
val (state, setState) = mutableStateOf(value)
```

##### ⚠️ Warning
---
- [remember](remember.md)없이 단독으로 사용하는 경우, 재구성될 때마다 이전의 상태가 아닌 초기 상태를 갖게 됨
