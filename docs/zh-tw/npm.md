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

## React Select

[![NPM](https://nodei.co/npm/react-select.png?downloads=true&stars=true)](https://nodei.co/npm/react-select/)


[react-select.com](https://react-select.com/) [styles](https://react-select.com/styles)

```js
import Select from 'react-select';

const Home = () => {

const colourStyles = {
control: styles => (
  { ...styles, backgroundColor: 'black', border: 0, boxShadow: 'none', width: "150px", fontSize: '18px'}
),
menu: styles => (
  { ...styles, backgroundColor: 'black', padding: '2px 0px'}
),
option: (styles) => {

  return {
  ...styles,
  backgroundColor: 'black',
  color: 'white',
  cursor: 'default',

  ':active': {
    ...styles[':active'],
    backgroundColor: 'gray',
    },
  };
},
singleValue: (styles) => ({ ...styles, color: 'white'}),
valueContainer: (styles) => ({ ...styles, padding: '2px 0px'}),
};

const [selectedOption, setSelectedOption] = useState({ value: '1', label: 'USDT' })

const options = [
  { value: '0', label: 'BTC' },
  { value: '1', label: 'USDT' },
  { value: '2', label: 'ETH' },
];

const handleSelectedChange = (selectedOption ) => {
  setSelectedOption(selectedOption)
}

return (
<Select
  value={selectedOption}
  onChange={handleSelectedChange}
  options={options}
  defaultValue={selectedOption[1]}
  styles={colourStyles}
  isSearchable={false}
  components={{
    IndicatorSeparator: () => null
  }}
/>
```

[How can I remove the bar in the react-select?](https://stackoverflow.com/questions/54047325/how-can-i-remove-the-bar-in-the-react-select)  
[select下拉框option的样式修改](https://www.shuzhiduo.com/A/A7zgK97Wz4/)
> option的樣式沒辦法修改 因為option是html固有元素 只能通過div ul li模擬select功能