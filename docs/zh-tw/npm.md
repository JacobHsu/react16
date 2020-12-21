# npm

## gh-pages

[![NPM](https://nodei.co/npm/gh-pages.png?downloads=true&stars=true)](https://nodei.co/npm/gh-pages/)

`yarn add gh-pages -D`
`npm install gh-pages --save-dev`

package.json

```js
  "homepage": "https://jacobhsu.github.io/react-material-ui/",
   "dependencies": {
    "gh-pages": "^3.1.0",
  },
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  },
```

## react-code-input

[![NPM](https://nodei.co/npm/react-code-input.png?downloads=true&stars=true)](https://nodei.co/npm/react-code-input/)

https://jacobhsu.github.io/react-password-input/

App.js

```js
import React from "react";
import ReactCodeInput from 'react-code-input';

// function App() {
class App extends React.PureComponent {

  render() { // add
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <ReactCodeInput type='password' fields={6} />
```

## Carousel

[![NPM](https://nodei.co/npm/react-slick.png?downloads=true&stars=true)](https://nodei.co/npm/react-slick/)

[react-slick](https://react-slick.neostack.com/)

## redux

redux
react-redux

## iframe

[![NPM](https://nodei.co/npm/react-iframe-comm.png?downloads=true&stars=true)](https://nodei.co/npm/react-iframe-comm/)

## 自動化檢查代碼質量

[![NPM](https://nodei.co/npm/huskypng?downloads=true&stars=true)](https://nodei.co/npm/husky/)

package.json

```js
  "scripts": {
    "dev": "nodemon",
    "lint": "eslint src --ext js,ts,tsx",
    "lint:fix": "npm run lint -- --fix",
  },

  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "*.{js,ts,tsx}": "npm run lint:fix -- --cache"
  }
```
