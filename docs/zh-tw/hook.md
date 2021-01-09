# Hooks API

## [useContext](https://zh-hant.reactjs.org/docs/hooks-reference.html#usecontext)

Create a Context constant and export it  

Context.js

```js
import React from "react";
export const Context = React.createContext();
```

In App.js Import and provide the context to all Functional Components  

App.js

```js
import React, { useState } from "react";
import { Context } from "./Context.js";

import ComponentA from "./ComponentA";
import ComponentB from "./ComponentB";

export default function App() {
  const [context, setContext] = useState("default context value");
  return (
    <Context.Provider value={[context, setContext]}>
      <ComponentA />
      <ComponentB />
    </Context.Provider>
  );
}
```

set/change value  

ComponentA.js

```js
import React, { useContext } from "react";
import { Context } from "./Context";

export default function ComponentA() {
  const [context, setContext] = useContext(Context);
  return (
    <div>
      ComponentA:
      <button onClick={() => setContext("New Value")}>
        Change Context Value
      </button>
    </div>
  );
}
```

ComponentB.js

```js
import React, { useContext } from "react";
import { Context } from "./Context";

export default function ComponentB() {
  const [context, setContext] = useContext(Context);
  return <div>ComponentB: {context}</div>;
}
```
