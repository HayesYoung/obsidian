### React 是什么
React 是一款构建视图 （View） 层的 JavaScript 库，由 Facebook （meta）在2013年开源
<br/>


### 基础概念
1. 组件：将页面拆分成小而可复用的独立组件，每个组件都封装了自己的特定功能和UI元素

2. JSX：JavaScript的扩展语法，可以在JavaScript中编写类似HTML结构的语法


<br/>

### 设计理念
1. 声明式：React 采用了声明式编程（关注结果，不关注过程）的方式构建页面，开发者只需要关注页面效果，不用关注底层DOM如何执行。

2. 组件化：组件是实现声明式编程的基本单元，组件可以通过嵌套和组合的方式构建更复杂的界面，组件化开发使得代码更易于理解、维护和扩展，提高了开发效率和代码重用性。

3. 单向数据流：React采用了单向数据流的模式，父组件通过props向子组件传递数据，子组件通过回调函数将数据的变化通知给父组件，数据自顶向下的流动方式， 使得数据流动变得可控，减少了复杂度，也降低了组件之间的耦合度

4. 虚拟DOM：



### 核心模块
1. react
2. reactDOM

### 核心功能
组件式开发









### 组件
React 创建的 App 就像一个乐高模型，一个复杂的页面可以由简单的组件(component)构建，React通过组件的思想，将UI界面拆分成一个个独立可复用的模块，每一个模块就是一个React组件。

React 组件(component），有一个外部属性 props (properties)， 来接收外部的参数，



状态： state


在React中，组件可以分为两种类型：类组件和函数组件：
- 函数组件（Function Components）：
```js
function Hello(props) {

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

this.props

react classname 和style区别


React 和 ReactDOM 是 React 库中的两个关键模块，它们有一些区别和不同的职责。


react 项目文档

JSX（JavaScript XML）

React.Fragment  === <>

ReactDOM.render() 在v18中已经弃用，改为了ReactDOM.createRoot()

事件处理函数
onClick = {()=> this.handleClick(id)};
onClick = {this.handleClick.bind(this, id)};

