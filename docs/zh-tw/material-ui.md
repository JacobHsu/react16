# material-ui

https://material-ui.com/zh/discover-more/related-projects/#carousel

[material-auto-rotating-carousel](https://mui.wertarbyte.com/#material-auto-rotating-carousel)：向新用户介绍您的应用程序。
`npm i --save material-auto-rotating-carousel`
`npm i --save react-swipeable-views`

[material-auto-rotating-carousel example](https://codesandbox.io/s/material-auto-rotating-carousel-example-dphsr) - CodeSandbox

## button

https://material-ui.com/zh/components/buttons/#button

```js
const LoginButton = withStyles(theme => ({
    root: {
      height: 36,
      width: "80%",
      backgroundColor: "#eee",
      '&:hover': {
        backgroundColor: "#00273d",
      },
      borderRadius:10,
      borderColor: "#009caa"
    },
    label: {
        color: '#009caa',
        fontSize: '14px',
    },
  }))(Button);
  
<LoginButton variant="outlined" style={{
    alignSelf:'center',
    marginTop:12,
    }} onClick={()=>{

    }}>
    BTN
</LoginButton>    
```
