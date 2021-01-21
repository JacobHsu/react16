# lodash

[maxBy](https://lodash.com/docs/4.17.15#maxBy)

> _.maxBy(array, [iteratee=_.identity])

```js
import maxBy from "lodash/maxBy";
import map from "lodash/map";

sellBookList = [
  { price: 2000.00, tokenAmount: 3.21,},
  { price: 3000.00, tokenAmount: 9.11 }
]

const sellMax = sellBookList && maxBy(sellBookList, obj=>parseFloat(obj.tokenAmount))
sellBookList = map(sellBookList, obj => {
  obj.percentage = parseInt((obj.tokenAmount/sellMax.tokenAmount)*100)
  return obj
})

```
