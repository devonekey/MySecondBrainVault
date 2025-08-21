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

@OptIn(ExperimentalMaterial3Api::class)
@Composable
fun TextField(
    value: String,
    onValueChange: (String) -> Unit,
    modifier: Modifier = Modifier,
    enabled: Boolean = true,
    readOnly: Boolean = false,
    textStyle: TextStyle = LocalTextStyle.current,
    label: @Composable (() -> Unit)? = null,
    placeholder: @Composable (() -> Unit)? = null,
    leadingIcon: @Composable (() -> Unit)? = null,
    trailingIcon: @Composable (() -> Unit)? = null,
    prefix: @Composable (() -> Unit)? = null,
    suffix: @Composable (() -> Unit)? = null,
    supportingText: @Composable (() -> Unit)? = null,
    isError: Boolean = false,
    visualTransformation: VisualTransformation = VisualTransformation.None,
    keyboardOptions: KeyboardOptions = KeyboardOptions.Default,
    keyboardActions: KeyboardActions = KeyboardActions.Default,
    singleLine: Boolean = false,
    maxLines: Int = if (singleLine) 1 else Int.MAX_VALUE,
    minLines: Int = 1,
    interactionSource: MutableInteractionSource? = null,
    shape: Shape = TextFieldDefaults.shape,
    colors: TextFieldColors = TextFieldDefaults.colors()
)
```

##### ℹ️ Description
---
- 사용자로부터 입력을 받을 수 있는 머티리얼 디자인 스타일의 입력 컴포넌트

##### 🧩 Parameters
---
- `readOnly: Boolean`: 포커스를 가질 수 있는 읽기 전용, 텍스트 복사 가능
- `visualTransformation: VisualTransformation`: 비밀번호 등에 대해 문자 변환 표시
- `interactionSource: MutableInteractionSource?`:  터치, 포커스, 드래그 등 상호작용에 대한 상태 추적
