---
importance: Highest
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - Perplexity
parent pages:
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

@Composable
inline fun <T> remember(crossinline calculation: @DisallowComposableCalls () -> T): T
```

```Kotlin
package androidx.compose.runtime

@Composable
inline fun <T> remember(
    vararg keys: Any?,
    crossinline calculation: @DisallowComposableCalls () -> T
): T
```

##### ℹ️ Description
---
- [컴포즈](젯팩%20컴포즈.md)에서 컴포지션 간에 값을 메모리에 저장하여, [재구성](재구성.md)이 발생하더라도 이전에 계산된 값을 유지하는 함수

##### ⭐️ Feature
---
- 초기 컴포지션에서 계산된 상태를 내부적으로 캐싱하고, 이후 같은 [컴포저블](컴포저블%20함수.md)이 [재구성](재구성.md)될 때 저장된 상태를 반환
- 가변·불변 객체 모두 저장 가능
- 컴포저블의 생명 주기에 종속됨

##### 🧩 Parameters
---
- `vararg keys: Any?`: 특정 키에 대해 값이 변경됐을 경우에만 캐시를 갱신하려고 할 때, 사용하는 장치
- `crossinline calculation: @DisallowComposableCalls () -> T`: 저장할 [상태](상태.md)를 생성하는 람다식

##### ⚠️ Warning
---
- `remember`에 저장된 상태는 해당 컴포저블이 컴포지션에서 제거되면 유지될 수 없으므로, `rememberSeavable` 함수를 사용해야 함
