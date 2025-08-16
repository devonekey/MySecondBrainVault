---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
  - OpenAI
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Java
  - API
  - Test
  - annotation
learned: false
---
##### 🖋️ Signature
---
```Java
@Target({ ElementType.ANNOTATION_TYPE, ElementType.METHOD })  
@Retention(RetentionPolicy.RUNTIME)  
@Documented  
@API(status = STABLE, since = "5.0")  
public @interface BeforeEach
```

##### ℹ️ Description
---
- 모든 테스트 실행 전에 공통으로 실행됨을 표시하는 어노테이션
- 테스트 클래스나 메서드가 실행되기 전 설정 작업을 정의하는 어노테이션
