---
importance: Highest
originated from:
  - "[[📘 젯팩 컴포즈로 개발하는 안드로이드 UI/3장 - 컴포즈 핵심 원칙 자세히 알아보기]]"
answered by:
  - Book
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
@ExplicitGroupsComposable
inline fun <T, reified E : Applier<*>> ReusableComposeNode(
    noinline factory: () -> T,
    update: @DisallowComposableCalls Updater<T>.() -> Unit,
    noinline skippableUpdate: @Composable SkippableUpdater<T>.() -> Unit,
    content: @Composable () -> Unit
)
```

##### ℹ️ Description
---
- [Compose](젯팩%20컴포즈.md) UI 트리에 재사용 가능한 노드를 생성하는 저수준 API

##### ⭐️ Feature
---
- 노드 재사용: [재구성](재구성.md) 시 기존 노드를 폐기하지 않고 재사용하여 메모리 할당과 초기화 비용을 절감
- 이중 업데이트: `update`(필수 업데이트)와 `skippableUpdate`(스킵 가능한 업데이트)로 나누어 재구성에 최적화

##### 🧩 Parameters
---
- `factory: () -> T`: 노드 객체를 생성하는 팩토리 함수, 최초 생성 시에만 호출됨
- `update: Updater<T>.() -> Unit`: 재구성 시 항상 실행되는 업데이트 로직
- `skippableUpdate: SkippableUpdater<T>.() -> Unit`: 입력이 변경되지 않으면 스킵 가능한 업데이트 로직, Composable 함수 호출 가능
- `content: @Composable () -> Unit`: 이 노드의 자식 [컴포저블](컴포저블%20함수.md) 콘텐츠

##### ⚙️ Mechanism
---
1. 새로운 노드를 생성해야할지 또는 기존 노드를 재사용해야 할지를 결정함 ^mech-1
2. 업데이트를 수행함 ^mech-2
3. `content()`를 호출해 콘텐츠를 노드에 내보냄 ^mech-3

##### ⚠️ Warning
---
- 일반 개발자가 직접 사용할 일은 거의 없으며, 주로 Compose UI의 내부 구현이나 커스텀 레이아웃 시스템을 만들 때만 필요
- `update`와 `skippableUpdate`의 역할 차이를 명확히 이해하지 못하면 예상치 못한 재구성 동작이 발생할 수 있음
