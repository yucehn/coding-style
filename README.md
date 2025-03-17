# coding-style

[standardjs參考](https://standardjs.com/rules-zhtw)

[typescript-coding-style-guide](https://gist.github.com/anichitiandreea/e1d466022d772ea22db56399a7af576b#typescript-coding-style-guide)

## 輔助工具
- 安裝 prettier
```
npm i prettier
```
- 設定可用： .prettierrc.js & .prettierrc.json
- vscode可打開auto format

- run
```
"prettier": "prettier --write ./app "
```
---
## 项目命名
1. 文件命名不得含有空格
1. 名稱使用小寫字母，不得含大寫字母
1. 名稱較長時採用半角連接符號(-, _)分隔

```
/project-test
```
---
## 文件命名

大駝峰命名元件（component）和頁面（page），其他檔案通常用小駝峰

## 檔案目錄

```
app/
├── components/
│   ├── MyHeader.tsx
│   └── MyFooter.tsx
├── pages/
│   ├── Home.tsx
│   ├── About.tsx
│   └── Widget/
│       ├── components/
│       │   ├── Tool.tsx
│       │   └── Option.tsx
│       ├── helpers/
│       │   └── setOptionStorage.ts
│       ├── Widget.tsx
│       └── index.ts
├── hooks/
│   └── useTheme.ts
├── utils/
│   └── getRamdomNumber.ts
└── constants.ts
```
---
## 命名規則
1. 變數/常數：小駝峰
```
  var getName = 'name';
  const goSportsTeam = true;
```
2. 函式：小駝峰 `function myFunction () { } `

宣告變數和函式時使用駝峰（camelcase）命名。 (eslint: camelcase)
```
  function my_function () { }    // ✗ avoid
  function myFunction () { }     // ✓ ok
```
3. 類別/枚舉(enum)：大駝峰
```
  interface TopicState {
    topics: {
      Id: string;
      name: string;
      startTime: string;
      endTime: string;
      selections: string[];
    }
  }
```

* 以上命名盡量不要縮寫，或提出縮寫建議以達成共識

---
## 語法規則
1. 空格使用方法
- 分號後面要加空格，前面不要加。
```
  for (let i = 0 ;i < items.length ;i++) {...}    // ✗ avoid
  for (let i = 0; i < items.length; i++) {...}    // ✓ ok
```
- 程式區塊前要加空格。
```
  if (admin){...}     // ✗ avoid
  if (admin) {...}    // ✓ ok
```
- 一元運算子後面要加空格
```
  typeof!admin        // ✗ avoid
  typeof !admin        // ✓ ok
``` 

2. imports順序
- React imports (i.e. import React, { useEffect, useMemo } from 'react';)
- React material imports
- 3rd party imports excep
- application imports sorted by type (services, classes, interfaces, enums)

```
  import { debounce, reduce } from 'lodash';
  import React, { useRef } from 'react';
  
  import { createConnection } from '@server/database';
  import { createServer } from '@server/node';
  
  import { initializeApp } from '@core/app';
  import { logger } from '@core/logger';
  
  import { Alert } from '@ui/Alert';
  import { Popup } from '@ui/Popup';
  
  import { Message } from '../Message';
  import { add, filter, repeat } from '../utils';
```
3. Use typescript aliases
```
  // ✗ avoid
  import { UserService } from '../../../services/UserService';
  
  // ✓ ok
  import { UserService } from '@services/UserService';
```

uniopen
