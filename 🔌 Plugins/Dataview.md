---
type:
  - Community Plugin
  - Data Visualization
  - Query
  - in Note
  - Block
link: "[Dataview 기초: 소개](https://kaminik.tistory.com/entry/Dataview-%ED%94%8C%EB%9F%AC%EA%B7%B8%EC%9D%B8-%EC%86%8C%EA%B0%9C)"
---
##### ℹ️ Description
---
- 노트들을 SQL과 유사한 쿼리 언어로 조회하고, 목록 및 테이블 등의 형태로 시각화하는 기능을 제공하는 플러그인 ^desc-1

##### 🛠️ How to use?
---
1. 블럭에 dataview 작성
   \`\`\`dataview
   \`\`\`
2. 쿼리 추가
   \`\`\`dataview
   list
   from "🔌 Plugins"
   sort file.name
   \`\`\`
3. 완성
```dataview
list
from "🔌 Plugins"
where file.name != "🗂️ Table of Contents"
sort file.name
```

##### ➕ Extra
---
- 노트의 메타데이터,'file.name'과 같은 자체 내장 필드(Implicit field)를 이용할 수 있음
- 노트/폴더의 경로, 태그, 사용자가 정의한 메타데이터를 활용할 수 있음
