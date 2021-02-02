# material-ui

https://material-ui.com/zh/discover-more/related-projects/#carousel

[material-auto-rotating-carousel](https://mui.wertarbyte.com/#material-auto-rotating-carousel)：向新用户介绍您的应用程序。
`npm i --save material-auto-rotating-carousel`
`npm i --save react-swipeable-views`

[material-auto-rotating-carousel example](https://codesandbox.io/s/material-auto-rotating-carousel-example-dphsr) - CodeSandbox

[TextField 文本框](https://material-ui.com/zh/components/text-fields/#textfield)    
[Avatar 头像组件](https://material-ui.com/zh/components/avatars/)  

## TextField

[TextField 文本框](https://material-ui.com/zh/components/text-fields/)

`<TextField id="outlined-basic" label="Outlined" variant="outlined" />`

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

[How to center a button in material ui](https://stackoverflow.com/questions/51010599/how-to-center-a-button-in-material-ui)

`<DialogActions style={{justifyContent: 'center'}}>`

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

## material-icons

[material-icons](https://material-ui.com/zh/components/material-icons/)
[底部导航栏](https://material-ui.com/components/bottom-navigation/)

```js
<BottomNavigationAction label="Recents" icon={<img src="imageLink"/>} />
```

[Icons 图标](https://material-ui.com/zh/components/icons/#svg-material-icons)

src\images\icons\index.svg

```css
<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 27 27">
    <path d="M13.5-.5c7.73 0 14 6.27 14 14s-6.27 14-14 14-14-6.27-14-14 6.27-14 14-14zm0 1C6.323.5.5 6.323.5 13.5s5.823 13 13 13 13-5.823 13-13-5.823-13-13-13z" transform="translate(-28 -235) translate(-1 226) translate(18 9) translate(11)"/>
    <path d="M13 0v27c0 .276.224.5.5.5s.5-.224.5-.5V0c0-.276-.224-.5-.5-.5s-.5.224-.5.5z" transform="translate(-28 -235) translate(-1 226) translate(18 9) translate(11)"/>
    <path d="M0 14h27c.276 0 .5-.224.5-.5s-.224-.5-.5-.5H0c-.276 0-.5.224-.5.5s.224.5.5.5zM22.7 3.735C20.682 5.558 17.241 6.7 13.5 6.7c-3.761 0-7.195-1.125-9.2-2.937-.204-.185-.52-.169-.705.036-.185.205-.17.521.035.706C5.833 6.497 9.506 7.7 13.5 7.7c3.976 0 7.656-1.221 9.87-3.223.205-.185.22-.501.035-.706-.185-.205-.501-.22-.706-.036zM23.37 22.523C21.156 20.52 17.476 19.3 13.5 19.3c-3.994 0-7.667 1.203-9.87 3.195-.205.185-.22.501-.035.706.185.205.501.22.706.036C6.305 21.425 9.739 20.3 13.5 20.3c3.742 0 7.183 1.142 9.2 2.965.204.185.52.169.705-.036.185-.205.17-.52-.035-.706z" transform="translate(-28 -235) translate(-1 226) translate(18 9) translate(11)"/>
    <path d="M13.675 26.45c-4.056-2.853-6.538-7.653-6.538-12.922 0-5.257 2.468-10.05 6.51-12.894.226-.159.28-.47.121-.697-.159-.226-.47-.28-.696-.121-4.31 3.032-6.934 8.13-6.934 13.712 0 5.594 2.639 10.7 6.962 13.74.226.16.538.105.696-.12.16-.227.105-.539-.12-.698z" transform="translate(-28 -235) translate(-1 226) translate(18 9) translate(11)"/>
    <path d="M14.097 27.268c4.323-3.04 6.962-8.146 6.962-13.74 0-5.562-2.635-10.667-6.932-13.711-.226-.16-.538-.106-.698.119-.16.225-.106.537.12.697 4.032 2.856 6.51 7.658 6.51 12.895 0 5.27-2.481 10.07-6.537 12.922-.226.16-.28.471-.122.697.16.226.471.28.697.121z" transform="translate(-28 -235) translate(-1 226) translate(18 9) translate(11)"/>
</svg>
```

组件属性 通过 “url-loader” 或 “file-loader” 加载也是可行的。 [Create React App 也是这样使用的](https://material-ui.com/zh/components/icons/#svg-material-icons)。

```js
import { ReactComponent as IndexIcon }  from './images/icons/index.svg';
  function HomeIcon(props) {
    return (
      <SvgIcon {...props}>
        <IndexIcon/>
      </SvgIcon>
    );
  }

<BottomNavigationAction label={"INDEX"}  icon={<HomeIcon />}
```

## CardActionArea

[CardActionArea API](https://material-ui.com/zh/api/card-action-area/)
[background-image](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-image)

```js
// import BGIMG from './images/bg.png'; // 路徑放這
// result[1].bgImgPath = BGIMG
 <CardActionArea  style={{
      backgroundColor:"#eeeeee",
      flexDirection: "row",
      display: 'flex',
      justifyContent:'space-between',
      alignItems: 'center',
      paddingTop:8,
      paddingBottom:8,
      paddingLeft:16,
      paddingRight:16,
      backgroundImage: `url(${bg.iconPath})`
    }}
```
