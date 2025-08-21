---
importance: High
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
  - Material
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
package androidx.compose.material3

@Composable
fun Button(
    onClick: () -> Unit,
    modifier: Modifier = Modifier,
    enabled: Boolean = true,
    shape: Shape = ButtonDefaults.shape,
    colors: ButtonColors = ButtonDefaults.buttonColors(),
    elevation: ButtonElevation? = ButtonDefaults.buttonElevation(),
    border: BorderStroke? = null,
    contentPadding: PaddingValues = ButtonDefaults.ContentPadding,
    interactionSource: MutableInteractionSource? = null,
    content: @Composable RowScope.() -> Unit
)
```

##### ℹ️ Description
---
- 사용자가 클릭하여 액션을 트리거할 수 있는 머티리얼 디자인 버튼 컴포넌트

##### ⭐️ Feature
---
- 수신 객체인 `RowScope`를 제공함으로써 텍스트와 아이콘을 나란히 배치할 수 있음

##### 🧩 Parameters
---
- `interactionSource: MutableInteractionSource?`: 터치, 포커스, 드래그 등 상호작용에 대한 상태 추적
