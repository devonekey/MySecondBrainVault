---
importance: Highest
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/3장 - 컴포즈 핵심 원칙 자세히 알아보기]]"
answered by:
  - Claude
  - Book
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
@Suppress("ComposableLambdaParameterPosition")
@UiComposable
@Composable
inline fun Layout(
    content: @Composable @UiComposable () -> Unit,
    modifier: Modifier = Modifier,
    measurePolicy: MeasurePolicy
)
```

##### ℹ️ Description
---
- [Jetpack Compose](젯팩%20컴포즈.md)의 가장 기본적인 레이아웃 빌딩 블록으로, 자식 [컴포저블](컴포저블%20함수.md)들을 측정하고 배치하는 방식을 직접 정의할 수 있는 저수준 API

##### ⭐️ Feature
---
- 저수준 제어: 자식 요소의 측정(`measure`)과 배치(`place`)를 개발자가 직접 제어
- 단일 측정 원칙: "자식을 한 번만 측정"하는 규칙을 준수해야 함

##### ⚙️ Mechanism
---
0. `Layout` 컴포저블이 `ReusableComposeNode()` 컴포저블을 호출함
![[ReusableComposeNode#^mech-1]]
![[ReusableComposeNode#^mech-2]]
![[ReusableComposeNode#^mech-3]]

##### 🧩 Parameters
---
- `content: @Composable () -> Unit`: 레이아웃 내부에 배치될 자식 컴포저블들
- `modifier: Modifier`: 레이아웃 자체에 적용될 [변경자](변경자.md)
- `measurePolicy: MeasurePolicy`: 자식들을 측정하고 배치하는 정책을 정의하는 객체

##### ⚠️ Warning
---
- 각 자식은 `measurables[i].measure`를 정확히 한 번만 호출해야 함, 여러 번 호출하면 런타임 에러 발생
- `layout(width, height) { }` 블록 내에서 모든 자식을 `placeRelative()` 또는 `place()`로 배치해야 함

##### ➕ Extra
---
- 기본 레이아웃으로 구현이 어려운 복잡한 배치가 필요할 때 사용
- 대부분의 경우 `Layout` 대신 `SubcomposeLayout` 또는 기본 레이아웃 조합으로 해결
