---
importance: Low
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/2장 - 선언적 패러다임 이해]]"
answered by:
  - OpenAI
parent pages:
tags:
  - Jetpack
  - Compose
  - 컴포즈
  - Kotlin
  - API
learned:
---
##### 🖋️ Signature
---
```Kotlin
fun Activity.setContentView(layoutResID: Int)
```

```Kotlin
fun Activity.setContentView(view: View)
```

```Kotlin
fun Activity.setContentView(view: View, params: ViewGroup.LayoutParams)
```

##### ℹ️ Description
---
- `Activity`의 화면(UI)을 설정하는 메소드
- XML 기반 `View` 시스템에서 UI를 구성하는 방식

##### ⭐️ Feature
---
- XML에 정의된 레이아웃(`R.layout....`)을 `Activity`에 연결
- `findViewById()`로 XML 내 `View`를 참조

##### 🧩 Parameters
---
- `layoutResID: Int`: 레이아웃 XML 파일의 리소스 ID
- `view: View`: 커스텀 `View` 객체
- `params: ViewGroup.LayoutParams`: 루트 뷰의 배치 및 크기를 제어할 레이아웃 파라미터

##### ⚠️ Warning
---
- `onCreate()` 이전에 호출하면 예외 발생
- 여러 번 호출하면, 이전 뷰는 모두 교체됨

