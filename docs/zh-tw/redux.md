# redux

Redux Saga | Redux 界的非同步救星

Redux - Saga 在 Redux 中是以 Middleware （中間件）存在的，因此它能夠在程式調用 Store 的時候處理 Async Action


原本被 `dispatch` 觸發的 Method 從 Reducer 變成 Redux - Saga 。
換句話說
Redux - Saga 成為 Component 及 Reducer 之間溝通的橋樑。


index.js

```js
import store from './store/store'
ReactDOM.render(
  <React.StrictMode>
    <Provider store={store}>
      <I18nProvider i18n={i18n}>
        <ThemeProvider theme={theme}>
          <App />
        </ThemeProvider>
      </I18nProvider>
    </Provider>
  </React.StrictMode>,
  document.getElementById('root')
)
```
