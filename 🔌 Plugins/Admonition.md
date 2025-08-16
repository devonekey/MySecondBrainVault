---
type:
  - Community Plugin
  - Style
  - in Note
  - Block
---
##### ℹ️ Description
---
- 강조하려는 텍스트(콜 아웃)를 예쁜 스타일로 꾸미는 기능을 제공하는 플러그인 ^desc-1

##### 🛠️ How to use?
---
1. 블럭에 'ad-' 입력
   \`\`\`ad-
   강조하려는 텍스트
   \`\`\`
2. 스타일 선택
   \`\`\`ad-note
   강조하려는 텍스트
   \`\`\`
3. 완성
```ad-note
강조하려는 텍스트
```

##### ➕ Extra
---
- 기본적으로 제공하는 제목, 아이콘, 색상 등을 변경할 수도 있음
- 아이콘은 FontAwesome, RPGA wesome에서 제공하는 아이콘 이름만을 사용
- 블럭에 코드를 추가할 수 있음
```ad-note
title: My Code
icon: code
color: 121, 229, 203
~~~Kotlin
println("Hello Admonition")
~~~
```
