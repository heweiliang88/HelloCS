---
title: react
categories:
- 前端
tags:
- react
abbrlink: 8196
---


## [react]()

### react

### react-dom



### redux/mobx

- 状态管理

### react-router

- 路由管理

### creat-react-app

- 脚手架工具

### axios/genrate

- 前后端交互

### antd/React-Desktop/Material-UI

- UI框架

### react-native

# React基础

React 学习
是什么
能干什么
视频+文档+项目

#### React 教程//React Native
###### 概念
- React是一个用于**构建用户界面的JAVASCRIPT库**；
- **构建UI**,很多人认为 React 是 MVC 中的 V（视图）；
- 2013年5月开源，起源于Facebook；
额外：
MVC、MVVC、MVP的区别
https://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html
MVC （Model-View-Controller）是**最常见的软件架构**之一，业界有着广泛应用
- 视图（View）：用户界面。
- 控制器（Controller）：业务逻辑
- 模型（Model）：数据保存
MVVC
特点**(声明式设计+高效灵活+JSX+组件+单向响应的数据流)**
- **1.声明式设计** −React采用**声明范式**，可以轻松描述应用。
- **2.高效** −React通过对DOM的模拟，最大限度地减少与DOM的交互。
- **3.灵活** −React可以与已知的库或框架很好地配合。
- **4.JSX** − **JSX 是 JavaScript 语法的扩展**。React 开发不一定使用 JSX ，但我们建议使用它。
- **5.组件** − 通过 React 构建组件，使得代码更加容易得到复用，能够很好的应用在大项目的开发中。
- **6.单向响应的数据流** − React 实现了**单向响应的数据流，从而减少了重复代码**，这也是它为什么比传统数据绑定更简单。
###### 实例
```react
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
     // React + ReactDOM + babel 三个CDN
    <script src="https://cdn.staticfile.org/react/16.4.0/umd/react.development.js"></script>
    <script src="https://cdn.staticfile.org/react-dom/16.4.0/umd/react-dom.development.js"></script>
    <script src="https://cdn.staticfile.org/babel-standalone/6.26.0/babel.min.js"></script>
</head>
<body>
    <div id="example"></div>
    <script type="text/babel">    
 //我们需要使用 JSX，则 <script> 标签的 type 属性需要设置为 text/babel。
        ReactDOM.render(<h1>Hello React!!!</h1>, document.getElementById("example"));
    </script>
</body>
</html>
```
#### React 安装
##### 两种安装方法
###### CDN
引入三个库：  **react.min + rect-dom.min.js + babel.min.js**
- react.min.js ： React 的**核心库**
- react-dom.min.js :提供与 **DOM 相关**的功能
- babel.min.js：将 **ES6 代码转为 ES5 代码**,解决ES6浏览器上执行React 代码
Staticfile React CDN 
```html
<script src="https://cdn.staticfile.org/react/16.4.0/umd/react.development.js"></script>
<script src="https://cdn.staticfile.org/react-dom/16.4.0/umd/react-dom.development.js"></script>
<!-- 生产环境中不建议使用 -->
<script src="https://cdn.staticfile.org/babel-standalone/6.26.0/babel.min.js"></script>
```
官方 React CDN
```html
<script src="https://unpkg.com/react@16/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
<!-- 生产环境中不建议使用 -->
<script src="https://unpkg.com/babel-standalone@6.15.0/babel.min.js"></script>
```
###### 通过 npm 使用 React(4步)
1.  安装Node.js(下载，下一步)
2.  国内使用 npm 速度很慢，你可以使用淘宝定制的 cnpm (gzip 压缩支持) 命令行工具代替默认的 npm:
   ```bash
   //更换
   npm install -g cnpm --registry=https://registry.npm.taobao.org
   npm config set registry https://registry.npm.taobao.org
   //检测
   npm config get registry
   或 npm info express
   或 cnpm -v
   ```
3. 安装React
   ```bash
   cnpm install -g create-react-app 或 npm install -g create-react-app
   // cnpm/npm 安装 -全局 create-react-app
   ```
4.  使用 create-react-app 快速构建 React 开发环境
   ```bash
   create-react-app my-app //my-app 项目名
   // creat-react-app 项目名
   cd my-app/
   npm start /cnpm start
   ```
###### 目录结构
#### React 元素渲染
**元素是构成React应用的最小单位**，它用于描述屏幕上输入的内容
###### 将元素渲染到 DOM 中
###### 更新元素渲染	
#### React JSX **像 XML 的 JavaScript 语法扩展**
###### 语法
React 使用 **JSX 来替代常规的 JavaScript**。
JSX 是一个看起来很**像 XML 的 JavaScript 语法扩展**。
我们不需要一定使用 JSX，但它有以下优点：
- JSX 执行**更快**，因为它在编译为 JavaScript 代码后进行了优化。
- 它是**类型安全**的，在编译过程中就能发现错误。
- 使用 JSX **编写模板更加简单快速**。
```react
const element = <h1>Hello, world!</h1>;
var myDivElement = <div className="foo" />;
ReactDOM.render(myDivElement, document.getElementById('example'));
```
这种看起来可能有些奇怪的标签语法既不是字符串也不是 HTML。它被称为 JSX， 
一种 JavaScript 的语法扩展。 我们推荐在 React 中使用 JSX 来描述用户界面。
JSX 是在 JavaScript 内部实现的。
我们知道**元素是构成 React 应用的最小单位**，JSX 就是用来**声明 React 当中的元素**。
与浏览器的 DOM 元素不同，**React 当中的元素事实上是普通的对象**，React DOM 可以确保 浏览器 DOM 的数据内容与 React 元素保持一致。
**要将 React 元素渲染到根 DOM 节点中，我们通过把它们都传递给 ReactDOM.render() 的方法来将其渲染到页面上**：
注意
由于 JSX 就是 JavaScript，一些标识符像 `class` 和 `for` 不建议作为 XML 属性名。作为替代，React DOM 使用 `className` 和 `htmlFor` 来做对应的属性。
###### 使用JSX
- 代码中嵌套多个 HTML 标签，需要使用一个 div 元素包裹它
- 实例中的 p 元素添加了自定义属性 **data-myattribute**，添加自定义属性需要使用 **data-** 前缀。
```react
ReactDOM.render(
    <div>
    <h1>h1</h1>
    <h2>h2</h2>
    <p data-myattribute = "somevalue">这是一个很不错的 JavaScript 库!</p>
    </div>
    ,
    document.getElementById('example')
);
```
###### 独立文件
React JSX代码可以放在一个独立文件(创建文件helloworld_react.js)上
```react
<script type="text/babel" src="helloworld_react.js"></script>
```
###### Javascript表达式
在JSX中使用Javasript表达式。表达式写在花括号{}中
```react
{12+90};
```
注意：在 JSX 中不能使用 **if else** 语句，但可以使用 **conditional (三元运算)** 表达式来替代
```react
<script type="text/babel">
var i = 10;
ReactDOM.render(
    <div>
      <h1>{i == 1 ? 'True!' : 'False'}</h1>
    </div>
    ,
    document.getElementById('example')
);
</script>
```
###### 样式
React 推荐使用内联样式。我们可以使用 **camelCase** 语法来设置内联样式.  **style = {样式名}**
**React 会在指定元素数字后自动添加 px** 。
```react
var myStyle = {
    fontSize: 100,{/*React 会在指定元素数字后自动添加 px  */}
    color: '#FF0000'
};
ReactDOM.render(
    <h1 style = {myStyle}>菜鸟教程</h1>,
   {/*
   style = {样式名}
   */}
    document.getElementById('example')
);
```
###### 注释
注释需要写在花括号中
```react
{/*注释....*/} 
```
###### 数组
JSX 允许在模板中插入数组，数组会自动展开所有成员：
使用
定义 var 数组名 = [元素标签1，元素标签2]；
引用 {数组名}
```react
var arr = [<p>p</p>,<h1>h1</h1>]; {/* 数组的定义*/}
ReactDOM.render(
    <div>{arr}</div>,
    doucuement.getElementById('example');
);
```
#### React 组件
**组件使得我们的应用更容易来管理**
###### 定义组件
- 使用函数定义组件
  ```react
  function HelloMessage(props){
  	return <h1>Hello World</h1>;
  }
  const element = <HelloMessage />;
  ReactDOM.render(
  	element,doucument.getELementById('example')
  );	
  ```
- 使用ES6 class来定义一个组件
  ```react
  class Wellcome extends React.Component{
  	render(){
  		return <h1>Hello React!!!</h1>;
  	}
  }
  ```
- 参数传递 
  ```react
  function 方法名(props){
      return <h1><{props.name}/h1>
  }
  const element = <方法名 name="属性">
  ReactDOM.render(
   	element,doucument.getElementById('');        
  );        
  ```
  ```react
  function HellMessages(props){
  	return <h1>Helle {props.name}</h1>
  }
  const element = <HelloMessage name="Message">;
  ReactDOM.render(
  	element,document.getElementById('example');
  );
  ```
- 注意
  原生 HTML 元素名以小写字母开头，而**自定义的 React 类名以大写字母开头**，比如 HelloMessage 不能写成 helloMessage。除此之外还需要注意组件类只能包含一个顶层标签，否则也会报错。
###### 复合组件
我们可以通过创建多个组件来合成一个组件，即把组件的不同功能点进行分离。
```react
function Name(props) {
      return <h1>{props.name}</h1>;
}
function Age(props) {
      return <h1>{props.age}</h1>;
}
function Ssex(props) {
      return <h1>{props.sex}</h1>;
}
function App() {
 	  return (
        <div>
            <Name name="张三" /> /{/*不用符号结尾 */}
            <Age age="18" />
            <Ssex sex="男" />
         </div>
); {/* 结尾;号*/}
}
ReactDOM.render(
            <App />, document.getElementById('example')
);
```
#### React State(状态)
###### State状态的概念 组件渲染用户界面的状态
**React 把组件看成是一个状态机**（State Machines）。
**通过与用户的交互，实现不同状态，然后渲染 UI，让用户界面和数据保持一致。**
React 里，只需**更新组件的 state**，然后根据**新的 state 重新渲染用户界面（不要操作 DOM）。**
以下实例创建一个名称扩展为 React.Component 的 ES6 类，在 render() 方法中使用 this.state 来修改当前的时间。
添加一个类构造函数来初始化状态 this.state，类组件应始终使用 props 调用基础构造函数。
```react
class Clock extends React.Component {
//定义一个Clock类进行封装Clock组件    
  constructor(props) { //constructor 构造器 一个类构造函数来初始化状态this.state
    super(props);
    this.state = {date: new Date()};
  }
  render() { //渲染函数
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>现在是 {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
ReactDOM.render(
  <Clock />,
  document.getElementById('example')
);
```
###### 将**生命周期**方法添加到类中 (React生命周期）
在具有许多组件的应用程序中，在销毁时释放组件所占用的资源非常重要。
每当 Clock 组件第一次**加载到 DOM 中的时候，我们都想生成定时器**，这在 React 中被称为**挂载**。
同样，每当 Clock 生成的这个 **DOM 被移除的时候，我们也会想要清除定时器**，这在 React 中被称为**卸载**。
我们可以在组件类上声明特殊的方法，当组件挂载或卸载时，来运行一些代码：
| **componentDidMount()** 与 **componentWillUnmount()** | 生命周期钩子   |
| ----------------------------------------------------- | -------------- |
| **componentDidMount()** 钩子                          | 设置一个定时器 |
| **componentWillUnmount()**钩子                        | 卸载定时器     |
**componentDidMount()** 与 **componentWillUnmount()** 方法被称作生命周期钩子。
在组件输出到 DOM 后会执行 **componentDidMount()** 钩子，我们就可以在这个钩子上设置一个定时器。
this.timerID 为定时器的 ID，我们可以在 **componentWillUnmount()** 钩子中卸载定时器。
**定时器例子**
```react
class Clock extends React.Component {
  constructor(props) { //构造函数
    super(props);
    this.state = {date: new Date()};
  }
 //生命周期钩子 componentDidMount()和componentWillUnmount()
  componentDidMount() {
    this.timerID = setInterval(
      () => this.tick(),
      1000
    );
  }
  componentWillUnmount() {
    clearInterval(this.timerID);
  }
  tick() {
    this.setState({
      date: new Date()
    });
  }
  render() { //渲染函数
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>现在是 {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
ReactDOM.render(
  <Clock />,
  document.getElementById('example')
);
```
###### 数据自顶向下流动 不知道组件状态的
**父组件或子组件都不能知道某个组件是有状态还是无状态**，并且它们**不应该关心某组件是被定义为一个函数还是一个类。**
这就是为什么**状态通常被称为局部或封装**。 除了拥有并设置它的组件外，其它组件不可访问。
以下实例中 FormattedDate 组件将在其属性中接收到 date 值，并且不知道它是来自 Clock 状态、还是来自 Clock 的属性、亦或手工输入：
#### React Props
state 和 props 主要的区别在于 **props 是不可变的**，而 **state 可以根据与用户交互来改变**。这就是为什么**有些容器组件需要定义 state 来更新和修改数据**。 而子组件只能通过 **props 来传递数据。**
| props（道具） | 不可变的             | 传递数据       |
| ------------- | -------------------- | -------------- |
| state(状态)   | 根据与用户交互来改变 | 更新和修改数据 |
###### 使用Props
```react
function HelloMessage(props) {
    return <h1>Hello {props.name}!</h1>;
}
// name属性可以通过props.name来获取 
const element = <HelloMessage name="Message"/>;
ReactDOM.render(
    element,
    document.getElementById('example')
);
```
###### 默认Props
组件类的defaultProps属性设置默认值
```react
class HelloMessage extends React.Component{
 	render(){
 		return(
 			<h1>Hello,{this.props.name}</h1>
 		);
 	}
}
HelloMessage.defaultProps = {
	name : 'Message'
};
const element = <HelloMessage />;
ReactDOM.render(
	element,doucumentById('example')
);
```
###### State和Props
如何在应用中组合使用 state 和 props 。我们可以**在父组件中设置 state**， 并通过**在子组件上使用 props 将其传递到子组件上**。在 render 函数中, 我们设置 name 和 site 来获取父组件传递过来的数据。
```react
// 三个组件 WebSite父组件和Name和Link子组件
class WebSite extends React.Component {
  constructor() {
      super();
      this.state = {
        name: "Name",
        site: "Site"
      }
    }
  render() {
    return (
        // 两个子组件的使用
      <div>
        <Name name={this.state.name} />
        <Link site={this.state.site} />
      </div>
    );
  }
}
class Name extends React.Component {
  render() {
    return (
      <h1>{this.props.name}</h1>
    );
  }
}
class Link extends React.Component {
  render() {
    return (
      <a href={this.props.site}>
        {this.props.site}
      </a>
    );
  }
}
ReactDOM.render(
  <WebSite />,
  document.getElementById('example')
);
//结果
// Name Site(链接的格式)
```
###### Props验证（propTypes）
**React.PropTypes 在 React v15.5 版本后已经移到了** **prop-types** **库。**
```react
<script src="https://cdn.bootcss.com/prop-types/15.6.1/prop-types.js"></script>
```
Props 验证使用 **propTypes**，它可以**保证我们的应用组件被正确使用**，
React.PropTypes 提供很多验证器 (validator) 来验证传入数据是否有效。当向 props 传入无效数据时，JavaScript 控制台会抛出警告。
实例:创建一个 Mytitle 组件，属性 title 是必须的且是字符串**，非字符串类型会自动转换为字符串** ：
React 16.4版本
使用
```react
组件.ropTypes = {
	titile:PropTypes.string
	//过滤规则
}
```
```react
<script src="https://cdn.staticfile.org/react/16.4.0/umd/react.development.js"></script>
<script src="https://cdn.staticfile.org/react-dom/16.4.0/umd/react-dom.development.js"></script>
<script src="https://cdn.staticfile.org/prop-types/15.6.1/prop-types.js"></script>
<script src="https://cdn.staticfile.org/babel-standalone/6.26.0/babel.min.js"></script>
var title = "HelloTitle";
// var title = 123;
class MyTitle extends React.Component {
  render() {
    return (
      <h1>Hello, {this.props.title}</h1>
    );
  }
}
MyTitle.propTypes = {
  title: PropTypes.string
};
ReactDOM.render(
    <MyTitle title={title} />, //要传递参数
    document.getElementById('example')
);	
```
Reacr 15.4
```react
<script src="https://cdn.staticfile.org/react/15.4.2/react.min.js"></script>
<script src="https://cdn.staticfile.org/react/15.4.2/react-dom.min.js"></script>
<script src="https://cdn.staticfile.org/babel-standalone/6.22.1/babel.min.js"></script>
var title = "HelloTitle";
// var title = 123;
var MyTitle = React.createClass({
  propTypes: {
    title: React.PropTypes.string.isRequired,
  },
  render: function() {
     return <h1> {this.props.title} </h1>;
   }
});
ReactDOM.render(
    <MyTitle title={title} />,
    document.getElementById('example')
);
```
#### React 事件处理
React 元素的事件处理和 DOM 元素类似。但是有一点语法上的不同:
- React 事件绑定属性的命名采用驼峰式写法，而不是小写。
- 如果采用 JSX 的语法你需要传入一个函数作为事件处理函数，而不是一个字符串(DOM 元素的写法)
#### React 条件渲染
#### React 列表 & Keys
#### React 组件 API
###### React API
| 方法名       | 功能             |
| ------------ | ---------------- |
| setState     | 设置状态         |
| replaceState | 设置状态         |
| setProps     | 设置属性         |
| replaceProps | 替换属性         |
| forceUpdate  | 替换属性         |
| findDOMNode  | 获取DOM节点      |
| findDOMNode  | 判断组件挂载状态 |
#### React 组件生命周期
组件的生命周期可分成三个状态：
- Mounting：已插入真实 DOM
- Updating：正在被重新渲染
- Unmounting：已移出真实 DOM
#### React AJAX
**AJAX 用JavaScript执行异步网络请求**
**React 组件的数据可以通过 componentDidMount 方法中的 Ajax 来获取**，
**当从服务端获取数据时可以将数据存储在 state 中**，再用 **this.setState 方法重新渲染 UI**。
**当使用异步加载数据时，在组件卸载前使用 componentWillUnmount 来取消未完成的请求。**
以下实例演示了获取 Github 用户最新 gist 共享描述:
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>React 实例</title>
//使用 jQuery 完成 Ajax 请求    
<script src="https://cdn.staticfile.org/react/16.4.0/umd/react.development.js"></script>
<script src="https://cdn.staticfile.org/react-dom/16.4.0/umd/react-dom.development.js"></script>
<script src="https://cdn.staticfile.org/babel-standalone/6.26.0/babel.min.js"></script>
<script src="https://cdn.staticfile.org/jquery/2.1.4/jquery.min.js"></script>
</head>
<body>
<div id="example"></div>
<script type="text/babel">
class UserGist extends React.Component {
  constructor(props) {
      super(props);
      this.state = {username: '', lastGistUrl: ''};
  }
  componentDidMount() {
    this.serverRequest = $.get(this.props.source, function (result) {
      var lastGist = result[0];
      this.setState({
        username: lastGist.owner.login,
        lastGistUrl: lastGist.html_url
      });
    }.bind(this));
  }
  componentWillUnmount() {
    this.serverRequest.abort();
  }
  render() {
    return (
      <div>
        {this.state.username} 用户最新的 Gist 共享地址：
        <a href={this.state.lastGistUrl}>{this.state.lastGistUrl}</a>
      </div>
    );
  }
}
ReactDOM.render(
  <UserGist source="https://api.github.com/users/octocat/gists" />,
  document.getElementById('example')
);
</script>
</body>
</html>
```
#### React 表单与事件
React表单
Select下拉菜单
多个表单
React事件
```react
class HelloMessage extends React.Component {
            constructor(props) {
                super(props);
                this.state = { value: 'Hello React' };
                this.handleChange = this.handleChange.bind(this);
            }
            handleChange(event) {
                this.setState({ value: 'Hello World' }); //setState 设置状态
            }
            render() {
                var value = this.state.value;
                return (
                    <div>
                        <button onClick={this.handleChange}>按钮</button>
                        <h4>{value}</h4>
                    </div>
                );
            }
        }
        ReactDOM.render(
            <HelloMessage />, document.getElementById('example')
        );
```
当你需要从子组件中更新父组件的 **state** 时，你需要在父组件通过创建事件句柄 (**handleChange**) ，并作为 prop (**updateStateProp**) 传递到你的子组件上。
```react
class Content extends React.Component {
  render() {
    return  <div>
              <button onClick = {this.props.updateStateProp}>点我</button>
              <h4>{this.props.myDataProp}</h4>
           </div>
  }
}
class HelloMessage extends React.Component {
  constructor(props) {
      super(props);
      this.state = {value: 'Hello Runoob!'};
      this.handleChange = this.handleChange.bind(this);
  }
  handleChange(event) {
    this.setState({value: '菜鸟教程'})
  }
  render() {
    var value = this.state.value;
    return <div>
            <Content myDataProp = {value} 
              updateStateProp = {this.handleChange}></Content>
        //myDataProp = {value}  传输参数
     	// updateStateProp = {this.handleChange} 
           </div>;
  }
}
ReactDOM.render(
  <HelloMessage />,
  document.getElementById('example')
);
```
#### React Refs
*refs abbr. references （与to连用）提及, 涉及, 参考 n. 裁判员( ref的复数形式 )*
React 支持**一种非常特殊的属性 Ref** ，你可以**用来绑定到 render() 输出的任何组件**上。
这个特殊的属性允许你引用 render() 返回的相应的支撑实例（ backing instance ）。这样就可以确保在任何时间总是拿到正确的实例。
使用方法
```react
this.refs.myInput.focus();   //this.refs(重点)
 <input type="text" ref="myInput" /> //绑定render函数的input 
```
绑定一个 ref 属性到 render 的返回值上：
```react
class MyComponent extends React.Component {
  handleClick() {
    // 使用原生的 DOM API 获取焦点
    this.refs.myInput.focus();
  }
  render() {
    //  当组件插入到 DOM 后，ref 属性添加一个组件的引用于到 this.refs
    return (
      <div>
        <input type="text" ref="myInput" />
        <input
          type="button"
          value="点我输入框获取焦点"
          onClick={this.handleClick.bind(this)}
        />
      </div>
    );
  }
}
ReactDOM.render(
  <MyComponent />,
  document.getElementById('example')
);
```
事件绑定
```react
按钮 onClick={this.函数名.bind(this)}
```

# Redux

