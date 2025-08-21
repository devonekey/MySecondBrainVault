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
  - Util
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
package androidx.compose.ui.res

@Composable
@ReadOnlyComposable
fun stringResource(@StringRes id: Int): String
```

```Kotlin
package androidx.compose.ui.res

@Composable
@ReadOnlyComposable
fun stringResource(@StringRes id: Int, vararg formatArgs: Any): String
```

##### ℹ️ Description
---
- Android 리소스 시스템에 정의된 문자열을 가져오는 [Compose](젯팩%20컴포즈.md) 유틸리티 함수
