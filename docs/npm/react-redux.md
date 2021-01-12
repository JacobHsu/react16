# react-redux

`npm i redux react-redux`

```js
import { useDispatch, useSelector } from 'react-redux'
import * as navDuck from '../store/ducks/nav.duck'

const AppRouter = () => {
  const dispatch = useDispatch()
  const { tabIndex } = useSelector(state => state.nav)
```
