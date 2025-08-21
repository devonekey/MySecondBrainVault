---
importance: Medium
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - OpenAI
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
package androidx.compose.foundation.layout

@Composable
inline fun Box(
    modifier: Modifier = Modifier,
    contentAlignment: Alignment = Alignment.TopStart,
    propagateMinConstraints: Boolean = false,
    content: @Composable BoxScope.() -> Unit
)
```

```Kotlin
package androidx.compose.foundation.layout

@Composable
fun Box(modifier: Modifier) {
    Layout(measurePolicy = EmptyBoxMeasurePolicy, modifier = modifier)
}
```

##### ℹ️ Description
---
- 자식 [컴포저블](컴포저블%20함수.md)을 겹쳐 쌓아 올리듯 배치하는 레이아웃

##### ⭐️ Feature
---
- Android View 시스템의 `FrameLayout`과 유사
- 자식 컴포저블별 순서 보장

##### 🧩 Parameters
---
- `propagateMinConstraints: Boolean`: 최소 제약 조건을 자식 컴포저블에 전달할지 여부
	- `false`(기본값) → 자식 컴포저블은 자신의 크기에 맞게 배치됨
	- `true` → `Box`의 최소 크기를 자식 컴포저블에 적용
