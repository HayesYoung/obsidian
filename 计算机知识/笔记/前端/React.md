### 介绍
React 是 Facebook 在2013年开源的一款基于 View 层的 Javasrcip 库


### 组件
React 创建的 App 就像一个乐高模型，一个复杂的页面可以由简单的组件(component)构建，React通过组件的思想，将UI界面拆分成一个个可以复用的模块，每一个模块就是一个React组件。

React 组件(component)本质是一个 Js 函数，


 

组件两种实现的方式：
- 函数组件
```js
function Hello() {

  return (<h3>Hello</h3>);
  
}

export default Hello;
```


- 类组件

```js
import React from "react";

class Hello extends React.Component {

  render() {

    return <h1>Hello</h1>;

  }
}

export default Hello;
```