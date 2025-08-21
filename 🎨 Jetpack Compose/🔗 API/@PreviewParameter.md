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

annotation class PreviewParameter(
    val provider: KClass<out PreviewParameterProvider<*>>,
    val limit: Int = Int.MAX_VALUE
)
```

##### ℹ️ Description
---
- [@Preview](@Preview.md) 미리보기를 사용할 때 외부 데이터를 주입하여 다양한 UI 상태를 미리볼 수 있도록 도와주는 어노테이션
- [@Preview](@Preview.md) 미리보기 함수의 매개변수에 샘플 데이터를 주입하는 어노테이션

##### ⭐️ Feature
---
- 앱 실행없이 다양한 입력 데이터에 따른 UI 상태 변화 확인
- Provider가 제공하는 여러 데이터로, 여러 Preview 생성

##### 🧩 Parameters
---
- `provider: KClass<out PreviewParameterProvider<*>>`: `PreviewParameterProvider<T>`를 구현한 클래스 지정, Preview에 데이터 제공
- `limit: Int`: Provider가 반환하는 데이터 개수 지정

##### ➕ Extra
---
- Provider 구현한 클래스 예시
```Kotlin
class NameProvider : PreviewParameterProvider<String> {
    override val values = sequenceOf("Alice", "Bob", "Charlie")
    override val count: Int get() = values.count()
}
```
- Preview 함수에 사용 예시
```Kotlin
@Preview
@Composable
fun GreetingPreview(
    @PreviewParameter(NameProvider::class, limit = 2) name: String
) {
    Text(text = "Hello, $name!")
}
```
