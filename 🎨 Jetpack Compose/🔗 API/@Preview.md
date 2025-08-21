---
importance: Medium
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - Book
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
package androidx.compose.ui.tooling.preview

@MustBeDocumented
@Retention(AnnotationRetention.BINARY)
@Target(
    AnnotationTarget.ANNOTATION_CLASS,
    AnnotationTarget.FUNCTION
)
@Repeatable
annotation class Preview(
    val name: String = "",
    val group: String = "",
    @IntRange(from = 1) val apiLevel: Int = -1,
    val widthDp: Int = -1,
    val heightDp: Int = -1,
    val locale: String = "",
    @FloatRange(from = 0.01) val fontScale: Float = 1f,
    val showSystemUi: Boolean = false,
    val showBackground: Boolean = false,
    val backgroundColor: Long = 0,
    @UiMode val uiMode: Int = 0,
    @Device val device: String = Devices.DEFAULT,
    @Wallpaper val wallpaper: Int = Wallpapers.NONE,
)
```

##### ℹ️ Description
---
- Android Studio에 [컴포저블 함수](컴포저블%20함수.md)를 렌더링하기 위해 사용하는 어노테이션
- 개발 단계에서 미리보기를 제공하는 어노테이션

##### ⭐️ Feature
---
- [@Composable](@Composable.md)과 반드시 함께 사용

##### 🧩 Parameters
---
- `group: String`: Preview들그룹화
- `apiLevel: Int`: 특정 API Level 환경에서 실행
- `showSystemUi: Boolean`: Status Bar, Navigation Bar 포함 여부
- `uiMode: Int`: 다크·라이트 모드
