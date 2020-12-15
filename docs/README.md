# react16

[Create React App](https://zh-hant.reactjs.org/docs/create-a-new-react-app.html)

```js
npx create-react-app my-app
cd my-app
yarn start
```
To start a new [Create React App project with `TypeScript`](https://create-react-app.dev/docs/adding-typescript/), you can run:

```js
npx create-react-app react-ts-app --template typescript
# or
yarn create react-app react-ts-app --template typescript
```

## Hook

Hook 是 React 16.8 中增加的新功能。它讓你不必寫 class 就能使用 state 以及其他 React 的功能。

Hook 是 function，他讓你可以從 function component「hook into」React state 與生命週期功能。

## Effect Hook

你從前可能在 React component 做過 fetch 資料、訂閱、或手動改變 DOM。我們稱這些操作「`side effect`」（或簡稱 effect）因為他們可以影響其他 component 且在 render 期間無法完成。

Effect Hook useEffect 在 function component 中加入運作 side effect 的能力。他和 `componentDidMount`，`componentDidUpdate`，與 `componentWillUnmount` 有著同樣的宗旨，但整合進一個單一的 API。

## docsify

[docsify.js](https://docsify.js.org/#/zh-cn/quickstart)

`$ docsify init ./docs`  
`$ docsify serve docs`
