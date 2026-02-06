---
importance: Highest
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/4장 - UI 요소 배치]]"
answered by:
  - Claude
parent pages:
  - "[[Column]]"
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

@PublishedApi
@Composable
internal fun columnMeasurePolicy(
    verticalArrangement: Arrangement.Vertical,
    horizontalAlignment: Alignment.Horizontal
): MeasurePolicy
```

##### ℹ️ Description
---
- [Column](Column.md) 내부에서 사용되는 측정 정책을 생성하는 [컴포저블](컴포저블%20함수.md)
- 수직 배치와 수평 정렬 방식에 따라 자식 컴포저블들을 측정하고 배치하는 규칙을 정의

##### ⭐️ Feature
---
- `@PublishedApi internal`로 선언되어 인라인 함수에서만 접근 가능하며, 일반 개발자는 직접 사용 불가
- [remember](remember.md)를 통해 배치/정렬 변경 시에만 재생성(Recreation)되도록 최적화
- [Layout](Layout.md)의 측정/배치 로직을 별도의 정책 객체로 분리하여 재사용성과 테스트 용이성 확보

##### 🧩 Parameters
---
- `verticalArrangement: Arrangement.Vertical`: 자식 요소들의 수직 배치 방식 지정
- `horizontalAlignment: Alignment.Horizontal`: 자식 요소들의 수평 정렬 방식 지정
