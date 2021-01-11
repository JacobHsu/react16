# react-router-dom

```js
import React from 'react'
import {
  HashRouter,
  Switch,
  Route
} from 'react-router-dom'
import Router from './router'

const App = () => {
  return (
    <HashRouter>
      <Switch>
        <Route path="/" component={Router} />
      </Switch>
    </HashRouter>
  )
}

export default App

```
