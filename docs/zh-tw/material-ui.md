# material-ui

https://material-ui.com/zh/discover-more/related-projects/#carousel

[material-auto-rotating-carousel](https://mui.wertarbyte.com/#material-auto-rotating-carousel)：向新用户介绍您的应用程序。
`npm i --save material-auto-rotating-carousel`
`npm i --save react-swipeable-views`

[material-auto-rotating-carousel example](https://codesandbox.io/s/material-auto-rotating-carousel-example-dphsr) - CodeSandbox

[TextField 文本框](https://material-ui.com/zh/components/text-fields/#textfield)    
[Avatar 头像组件](https://material-ui.com/zh/components/avatars/)  

## Dialog

[Dialog 对话框](https://material-ui.com/zh/components/dialogs/)

```js
<Dialog fullWidth open={
<Dialog fullScreen open={
```

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

## overriding-styles-with-classes

[自定义的组件](https://material-ui.com/customization/components/#overriding-styles-with-classes)

[在React.js Material-UI中设置BottomNavigation的样式](https://www.yuanmacha.com/11986850930.html) (Styling BottomNavigation in React.js Material-UI)

```js
import { makeStyles } from '@material-ui/core/styles';

  const useStyles = makeStyles({
    root: {
      color:"#ffffff",
      "&$selected": {
        color: "#3bd2df"
      }
    },
    selected: {
      color: '#3bd2df',
    },
  });
 const classes = useStyles();
  <BottomNavigationAction label={"INDEX"}  icon={<RestoreIcon/>}
  classes={{
    root: classes.root, // class name, e.g. `classes-nesting-root-x`
    selected: classes.selected, // class name, e.g. `classes-nesting-label-x`
  }}/> 

```

[InputBase API](https://material-ui.com/zh/api/input-base/)
[TextField API](https://material-ui.com/zh/api/text-field/)