---
importance: Medium
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - GPT
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
inline fun Column(
    modifier: Modifier = Modifier,
    verticalArrangement: Arrangement.Vertical = Arrangement.Top,
    horizontalAlignment: Alignment.Horizontal = Alignment.Start,
    content: @Composable ColumnScope.() -> Unit
)
```

##### ℹ️ Description
---
- 자식 [컴포저블](컴포저블%20함수.md)들을 수직 방향으로 배치하는 레이아웃

##### ⭐️ Feature
---
- Android 웃View 시스템의 `LinearLayout`과 유사
- 수신 객체인 `ColumnScope` 내에서만 사용할 수 있는 확장 함수 제공
