---
importance: Highest
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/4장 - UI 요소 배치]]"
answered by:
  - Claude
parent pages:
  - "[[columnMeasurePolicy]]"
tags:
  - Jetpack
  - Compose
  - 컴포즈
  - Kotlin
  - API
  - fun
  - interface
learned:
---
##### 🖋️ Signature
---
```Kotlin
fun interface MeasurePolicy {
    fun MeasureScope.measure(
        measurables: List<Measurable>,
        constraints: Constraints
    ): MeasureResult
    
    fun IntrinsicMeasureScope.minIntrinsicWidth(
        measurables: List<IntrinsicMeasurable>,
        height: Int
    ): Int
    
    fun IntrinsicMeasureScope.minIntrinsicHeight(
        measurables: List<IntrinsicMeasurable>,
        width: Int
    ): Int
    
    fun IntrinsicMeasureScope.maxIntrinsicWidth(
        measurables: List<IntrinsicMeasurable>,
        height: Int
    ): Int
    
    fun IntrinsicMeasureScope.maxIntrinsicHeight(
        measurables: List<IntrinsicMeasurable>,
        width: Int
    ): Int
}
```

##### ℹ️ Description
---
- 커스텀 레이아웃의 측정 및 배치 로직을 정의하는 함수형 인터페이스
- 자식 요소들을 어떻게 측정하고 배치할지 결정

##### ⭐️ Feature
---
- 

##### 🧩 Parameters
---
- `measurables: List<Measurable>`: 측정해야 할 자식 컴포저블들
- `constraints: Constraints`: 부모로부터 전달받은 크기 제약 조건

##### ⚙️ Mechanism
---
1. 부모가 `Constraints` 전달 → 레이아웃이 가질 수 있는 최소/최대 크기 범위
2. 자식 측정(measure) → 각 `Measurable`을 측정하여 `Placeable` 획득
3. 레이아웃 크기 결정 → `Constraints` 내에서 최종 width, height 계산
4. 자식 배치(place) → `MeasureResult`의 `placementBlock`에서 각 `Placeable`의 위치 지정

##### ➕ Extra
---
- 
