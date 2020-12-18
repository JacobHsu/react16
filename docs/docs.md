## Effect Hook

[使用 Effect Hook](https://zh-hant.reactjs.org/docs/hooks-effect.html)

Effect Hook 讓你可以使用 function component 中的 side effect

```js
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // 相似於 componentDidMount 和 componentDidUpdate:
  useEffect(() => {
    // 使用瀏覽器 API 更新文件標題
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```