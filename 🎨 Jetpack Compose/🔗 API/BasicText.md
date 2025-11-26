---
importance: Medium
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/3장 - 컴포즈 핵심 원칙 자세히 알아보기]]"
answered by:
  - Claude
parent pages:
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
@Composable
fun BasicText(
    text: AnnotatedString,
    modifier: Modifier = Modifier,
    style: TextStyle = TextStyle.Default,
    onTextLayout: ((TextLayoutResult) -> Unit)? = null,
    overflow: TextOverflow = TextOverflow.Clip,
    softWrap: Boolean = true,
    maxLines: Int = Int.MAX_VALUE,
    minLines: Int = 1,
    inlineContent: Map<String, InlineTextContent> = mapOf(),
    color: ColorProducer? = null
)
```

##### ℹ️ Description
---
- 스타일링된 텍스트를 렌더링하는 가장 기본적인 저수준 텍스트 [컴포저블](컴포저블%20함수.md)로, Material Design 테마나 추가 기능 없이 순수하게 텍스트만 표시

##### ⭐️ Feature
---
- 저수준 API: 테마, 터치 리플 등의 Material 요소가 없는 순수한 텍스트 렌더링
- 성능 최적화: 불필요한 Material 오버헤드가 없어 대량의 텍스트 렌더링 시 유리
- 유연한 스타일링: `AnnotatedString`을 통해 부분별로 다른 스타일 적용 가능
- 인라인 컨텐츠: 텍스트 내부에 이미지, 아이콘 등 커스텀 컴포저블 삽입 가능

##### 🧩 Parameters
---
- `color: ColorProducer?`: 동적 색상 제공, `style`의 색상보다 우선 적용되며 [재구성](재구성.md) 최적화

##### ⚠️ Warning
---
- Material Design 스타일이 자동 적용되지 않고, 테마 색상이나 타이포그래피는 명시적으로 `style`에 지정할 수 있음
- 색상은 `style.color` < `color` < `AnnotatedString` 내부의 `SpanStyle` 순서로 우선됨

##### ➕ Extra
---
- 성능이 중요한 상황이나 Material이 불필요한 경우에 해당 컴포저블 사용
