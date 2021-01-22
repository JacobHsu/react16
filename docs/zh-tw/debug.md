# debug

>  Failed form propType: You provided a value prop to a form field without an onChange handler.

Input value onChange

```
<Input type="number" ref={register({ required: true, min: 0.1 })} name="amount" placeholder="請輸入金額" value={inputAmount}/>
```

Input [defaultValue](http://react-china.org/t/react-value/9773)

```
<Input type="number" ref={register({ required: true, min: 0.1 })} name="amount" placeholder="請輸入金額" defaultValue={inputAmount}/>
```
