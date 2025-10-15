---
importance: High
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/1장 - 컴포즈 앱 첫 빌드]]"
answered by:
  - OpenAI
parent pages:
  - "[[ComponentActivity]]"
  - "[[ComposeView]]"
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
package androidx.activity.compose

@Composable
fun ComponentActivity.setContent(
    parent: CompositionContext? = null,
    content: @Composable () -> Unit
): Composition
```

```Kotlin
package androidx.compose.ui.platform

class ComposeView @JvmOverloads constructor(
    context: Context,
    attrs: AttributeSet? = null,
    defStyleAttr: Int = 0
) : AbstractComposeView(context, attrs, defStyleAttr) {
	fun setContent(content: @Composable () -> Unit)
}
```

##### ℹ️ Description
---
- [젯팩 컴포즈](젯팩%20컴포즈.md)의 `Activity`나 `ComposeView`의 UI 콘텐츠를 선언적으로 정의할 때 사용하는 함수

##### ⭐️ Feature
---
- `setContentView`의 Compose 버전
- `content` 블록 내에서 [@Composable](@Composable.md) 함수들을 호출하여 화면 UI를 [구성](구성.md)
  → [@Composable](@Composable.md) 함수만 들어가야 함
- 내부적으로 컴포지션 객체를 생성하고, UI 트리를 관리
- `ComponentActivity`의 생명 주기에 맞춰 컴포지션을 관리

##### 🧩 Parameters
---
- `parent: CompositionContext?`: 상위 컴포지션과 연결
