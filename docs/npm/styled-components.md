# styled-components

它特別的地方是它可以把你要用的元素透過 ES6 的字符串模板做出來，
你不用再對每個類別或是HTML元素進行Styling
它能讓你編寫CSS也像是在做Component一樣，把每個CSS都進行組件化。


## styled-system

[![NPM](https://nodei.co/npm/styled-system.png?downloads=true&stars=true)](https://nodei.co/npm/styled-system/)

```js
import React from 'react'
import styled from 'styled-components'
import { color } from 'styled-system'

const TabButtonTitle = styled.div`
    ${color}
    font-size: 10px;
    font-weight: 500;
    margin-top: 5px;
`

const TabButton = ({ icon, title, active, path }) => {
  return (
    <TabButtonContainer>
      <TabButtonTitle color={active ? '#9097FF' : '#F2F2F2'}>{title}</TabButtonTitle>
    </TabButtonContainer>
  )
}

export default TabButton
```
