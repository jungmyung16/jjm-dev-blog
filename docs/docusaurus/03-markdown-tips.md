---
sidebar_position: 3
---

# 3. 마크다운 가이드

Docusaurus 전용 마크다운 확장 기능(MDX) 정리.

## Admonitions (강조 박스)

```markdown
:::note
일반 노트
:::

:::tip
팁/권장사항
:::

:::warning
주의사항
:::

:::danger
위험/금지
:::
```

## Tabs (탭 기능)

코드 블록 등을 탭으로 구분 시 사용.

```jsx
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="npm" label="npm" default>
    npm install
  </TabItem>
  <TabItem value="yarn" label="Yarn">
    yarn add
  </TabItem>
</Tabs>
```

## Code Block

### Title & Highlight
파일명 표시 및 특정 라인 강조 기능.

```js title="config.js" {2,4-6}
const init = () => {
  console.log('Start'); // 강조됨
  
  // 4~6라인 강조
  const config = {
    env: 'production'
  };
};
```

## Details (접기/펼치기)

```markdown
<details>
<summary>상세 내용 보기</summary>

여기에 숨겨진 콘텐츠 작성.

</details>
```
