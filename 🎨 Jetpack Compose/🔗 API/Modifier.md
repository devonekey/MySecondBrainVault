---
aliases:
  - 변경자
importance: Highest
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - Book
  - GPT
parent pages:
tags:
  - Jetpack
  - Compose
  - 컴포즈
  - Kotlin
  - API
  - interface
learned:
---
##### 🖋️ Signature
---
```Kotlin
package androidx.compose.ui

@Suppress("ModifierFactoryExtensionFunction")
@Stable
@JvmDefaultWithCompatibility
interface Modifier
```

```Kotlin
package androidx.compose.ui

@Stable
sealed interface Modifier {
    companion object : Modifier {
        override fun toString() = "Modifier"
    }

    fun then(other: Modifier): Modifier
}
```

##### ℹ️ Description
---
- [컴포저블 함수](컴포저블%20함수.md)의 외형과 행위에 영향을 주는 [젯팩 컴포즈](젯팩%20컴포즈.md)의 핵심 기술 ^desc-1
- 컴포저블의 모양, 레이아웃, 동작, 상호작용을 데코레이션하거나 확장하기 위한 불변 객체

##### ⭐️ Feature
---
- Android View 시스템의 `LayoutParams` + `Decorator` + Event Listener 역할을 합쳐놓은 개념
  ex. 크기(`fillMaxSize()`), 패딩(`padding()`), 클릭 이벤트(`clickable`) 등
- 대부분의 확장 함수는 `Modifier`를 반환하는 확장 함수로 이루어짐
	- 컴포저블에 [체이닝](체이닝.md) 방식으로 적용되는 규칙 집합
	- 순서에 따라 결과가 달라짐
	- 확장성이 높음
	- 모든 Compose UI의 공통 API
- 컴포저블 함수가 제공하지 않는 기능이 필요한 경우, [변경자](변경자.md)를 사용해 기능을 추가할 수 있음
