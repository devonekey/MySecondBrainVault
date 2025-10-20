---
importance: Medium
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/2장 - 선언적 패러다임 이해]]"
answered by:
  - OpenAI
parent pages:
  - "[[DropdownMenu]]"
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
expect fun DropdownMenuItem(  
    text: @Composable () -> Unit,  
    onClick: () -> Unit,  
    modifier: Modifier = Modifier,  
    leadingIcon: @Composable (() -> Unit)? = null,  
    trailingIcon: @Composable (() -> Unit)? = null,  
    enabled: Boolean = true,  
    colors: MenuItemColors = MenuDefaults.itemColors(),  
    contentPadding: PaddingValues = MenuDefaults.DropdownMenuItemContentPadding,  
    interactionSource: MutableInteractionSource? = null,  
)
```

##### ℹ️ Description
---
- [DropdownMenu](DropdownMenu.md) 내부에 표시되는 개별 항목을 나타내는 [컴포저블](컴포저블%20함수.md)

##### ⭐️ Feature
---
- 활성, 비활성 제어: `enabled = false`시 비활성화 상태로 표시, 클릭불가
- 터치 피드백 제공: 클릭 시 잉크 리플(ink ripple) 등 머티리얼 반응을 표시함

##### 🧩 Parameters
---
- `text: @Composable () -> Unit`: 메뉴 항목의 본문 텍스트 또는 임의의 콘텐츠 지정
- `onClick: () -> Unit`: 항목 클릭 시 호출되는 콜백, 보통 메뉴 닫기 동작과 함께 수행
- `modifier: Modifier`: 크기, 배경, 정렬 등 레이아웃 속성을 지정
- `leadingIcon: @Composable (() -> Unit)?`: 항목의 앞쪽에 표시할 아이콘
- `trailingIcon: @Composable (() -> Unit)?`: 항목의 뒤쪽에 표시할 아이콘
- `enabled: Boolean`: 클릭 가능 여부
- `colors: MenuItemColors`: 배경색, 텍스트색, 아이콘색 등 상태별 색상 정의
- `contentPadding: PaddingValues`: 항목 내부 여백
- `interactionSource: MutableInteractionSource?`: 클릭, 포커스 등 사용자 상호작용을 추적하는 상태 객체

##### ⚠️ Warning
---
- `onClick`에서 메뉴를 닫는 상태 갱신을 직접 처리하지 않으면, 메뉴가 열린 상태로 남음
