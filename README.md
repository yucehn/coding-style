# coding-style

## 命名規則
1. 變數：小駝峰，禁縮寫
2. 函式：小駝峰，禁縮寫
3. 類別/枚舉(enum)：大駝峰，禁縮寫
4. 常數：全大寫，多單字使用 _ 底線隔開

宣告變數和函式時使用駝峰（camelcase）命名。 (eslint: camelcase)
```
  function my_function () { }    // ✗ avoid
  function myFunction () { }     // ✓ ok

  var my_var = 'hello'           // ✗ avoid
  var myVar = 'hello'            // ✓ ok
```
[standardjs參考](https://standardjs.com/rules-zhtw)

[typescript-coding-style-guide](https://gist.github.com/anichitiandreea/e1d466022d772ea22db56399a7af576b#typescript-coding-style-guide)

---
## 語法規則
1. 空格使用方法

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
