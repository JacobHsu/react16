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

## useEffect

[How to call loading function with React useEffect only once](https://stackoverflow.com/questions/53120972/how-to-call-loading-function-with-react-useeffect-only-once)

> If you only want to run the function given to useEffect after the initial render, you can give it an empty array as second argument.

```js
function MyComponent() {
  useEffect(() => {
    loadDataOnlyOnce();
  }, []);

  return <div> {/* ... */} </div>;
}
```

## React.Fragment

`React.Fragment`  
There will be no extra element right here  

```js
render() {
  return (
    <React.Fragment>
      <ChildA />
      <ChildB />
      <ChildC />
    </React.Fragment>
  );
}
```
