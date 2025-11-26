---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
  - GPT
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Java
  - API
  - Test
  - annotation
learned:
---
##### 🖋️ Signature
---
```Java
@Target({ ElementType.ANNOTATION_TYPE, ElementType.METHOD })  
@Retention(RetentionPolicy.RUNTIME)  
@Documented  
@API(status = STABLE, since = "5.0")  
@Testable  
public @interface Test
```

##### ℹ️ Description
---
- 테스트 메소드임을 나타내는 어노테이션
