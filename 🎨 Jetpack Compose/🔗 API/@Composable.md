---
importance: Highest
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
  - annotation
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
@MustBeDocumented
@Retention(AnnotationRetention.BINARY)
@Target(
	AnnotationTarget.FUNCTION,
	AnnotationTarget.TYPE,
	AnnotationTarget.TYPE_PARAMETER,
	AnnotationTarget.PROPERTY_GETTER
)
annotation class Composable
```

##### ℹ️ Description
---
- [Jetpack Compose](젯팩%20컴포즈.md)의 핵심 어노테이션

##### ➕ Extra
---
- 이 함수가 UI를 그리기 위해 컴포지션(Composition) 시스템 안에서 호출돼야 한다는 표시
- 컴포즈 컴파일러에 해당 함수가 데이터를 UI 요소로 변환한다는 것을 알림
