---
importance:
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/2장 - 선언적 패러다임 이해]]"
answered by:
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
expect fun DropdownMenu(
    expanded: Boolean,
    onDismissRequest: () -> Unit,
    modifier: Modifier = Modifier,
    offset: DpOffset = DpOffset(0.dp, 0.dp),
    scrollState: ScrollState = rememberScrollState(),
    properties: PopupProperties = DefaultMenuProperties,
    shape: Shape = MenuDefaults.shape,
    containerColor: Color = MenuDefaults.containerColor,
    tonalElevation: Dp = MenuDefaults.TonalElevation,
    shadowElevation: Dp = MenuDefaults.ShadowElevation,
    border: BorderStroke? = null,
    content: @Composable ColumnScope.() -> Unit
)
```

##### ℹ️ Description
---
- 버튼 클릭 등 특정 트리거로 열리고 닫히는 팝업 메뉴 [컴포저블](컴포저블%20함수.md)

##### ⭐️ Feature
---
- 상태 제어형 메뉴: `expanded`를 `true`로 맞추면 팝업 메뉴가 열리고, `false`로 맞추면 팝업 메뉴가 닫힘
- 자동 닫힘 처리: `onDismissRequest`를 통해 외부 터치나 조건에서 닫기 동작을 지정할 수 있음 
- 스크롤 지원: `ScrollState`를 통해 많은 메뉴 항목을 스크롤할 수 있음
- 팝업 제어 속성 지원: `properties`를 통해 포커스, 입력, dismiss 정책을 조정할 수 있음

##### 🧩 Parameters
---
- `expanded: Boolean`: 팝업 메뉴를 열고 닫는 동작을 제어
- `onDismissRequest: () -> Unit`: 메뉴 외부 클릭이나 dismiss 이벤트 발생 시 호출되는 콜백
- `modifier: Modifier`: 메뉴의 크기, 배경, 정렬 등 레이아웃 속성을 지정
- `offset: DpOffset`: 앵커(anchor) 기준으로 메뉴의 x, y 위치를 보정, 기본값으로 `0.dp`, `0.dp` 사용
- `scrollState: ScrollState`: 메뉴 아이템이 많을 때 스크롤 위치를 제어, 기본적으로 [[rememberScrollState()]] 사용
- `properties: PopupProperties`: 팝업의 포커스, 키보드 입력, dismiss 동작 등을 제어, 기본값으로 [[DefaultMenuProperties]] 사용
- `shape: Shape`: 메뉴의 외곽선을 정의, 기본적으로 [[MenuDefaults.shape]] 사용
- `containerColor: Color`: 메뉴의 배경색, 기본적으로 [[MenuDefaults.containerColor]] 사용
- `tonalElevation: Dp`: 
- `shadowElevation: Dp`: 그림자 깊이
- `border: BorderStroke?`: 메뉴의 테두리
- `content: @Composable ColumnScope.() -> Unit`: 메뉴 내부 콘텐츠 영역, [DropdownMenuItem](DropdownMenuItem.md)들을 배치

##### ⚠️ Warning
---
- `onDismissRequest`를 구현하지 않으면, 메뉴가 닫히지 않고 남을 수 있음
- `expanded`를 [상태](상태.md)로 관리하지 않으면, UI가 갱신되지 않음
정
