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
inline fun Row(
    modifier: Modifier = Modifier,
    horizontalArrangement: Arrangement.Horizontal = Arrangement.Start,
    verticalAlignment: Alignment.Vertical = Alignment.Top,
    content: @Composable RowScope.() -> Unit
)
```

##### ℹ️ Description
---
- 자식 [컴포저블](컴포저블%20함수.md)들을 수평 방향으로 배치하는 레이아웃

##### ⭐️ Feature
---
- Android View 시스템의 `LinearLayout`과 유사
- 수신 객체인 `RowScope` 내에서만 사용할 수 있는 확장 함수 제공
	- 자식 컴포저블들로 하여금 `Modifier.weight` 함수를 사용할 수 있도록 기능 제공
