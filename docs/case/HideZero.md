# 隱藏0資產

```js
const tokenList = [
{
  id: 'eth',
  amount: 0.0001
}
{
  id: 'btc',
  amount: 0
}    
const [hideZero, setHideZero] = useState(false)

<Checkbox title="隱藏0資產" onClick={(e) => {
     setHideZero(e.target.checked)
   }}/>

   {
     tokenList.filter(token => hideZero ? token.amount > 0 : true).map((token, index) => {
```
