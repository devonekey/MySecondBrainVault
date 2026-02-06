---
importance: Medium
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/4장 - UI 요소 배치]]"
answered by:
  - GPT
  - Claude
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
- Android View 시스템의 `LinearLayout`과 유사
- 수신 객체인 `ColumnScope` 내에서만 사용할 수 있는 확장 함수 제공

##### 🧩 Parameters
---
- `verticalArrangement: Arrangement.Vertical`: 자식 요소들의 수직 배치 방식 지정
	- `Arrangement.Top`: 상단 정렬(기본값)
	- `Arrangement.Center`: 중앙 정렬
	- `Arrangement.Bottom`: 하단 정렬
	- `Arrangement.SpaceBetween`: 양 끝 배치 후 균등 간격
	- `Arrangement.SpaceEvenly`: 모든 간격 균등 배치
	- `Arrangement.SpaceAround`: 각 요소 주변 동일 간격
	- `Arrangement.spacedBy`: 지정한 간격(dp)으로 배치
- `horizontalAlignment: Alignment.Horizontal`: 자식 요소들의 수평 정렬 방식 지정
	- `Alignment.Start`: 시작점 정렬(기본값, LTR에서 왼쪽)
	- `Alignment.CenterHorizontally`: 수평 중앙 정렬
	- `Alignment.End`: 끝점 정렬 (LTR에서 오른쪽)
- `content: @Composable ColumnScope.() -> Unit`: 내부에 배치할 컴포저블들을 정의하는 람다

##### ⚠️ Warning
---
- `Column` 내부에 `Column`을 과도하게 중첩하면, [재구성](재구성.md) 범위가 넓어져 성능이 저하될 수 있음