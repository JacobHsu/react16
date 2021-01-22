# react-hook-form

[Get Started](https://react-hook-form.com/get-started)

```js
import { useForm } from 'react-hook-form'

const [inputAmount, setInputAmount] = useState("")
const { register, handleSubmit, formState, errors } = useForm({
  mode: 'onChange'
})
const onSubmit = data => {
  dispatch(modalDuck.actions.openWithdrawVerificationModal(true))
  console.log(555, data)
}

const handleChange = (e) => {
  setInputAmount(e.target.value);
}

<Input type="number" ref={register({ required: true, min: 0.1 })} name="amount" placeholder="請輸入金額" value={inputAmount} onChange={handleChange}/>
```
