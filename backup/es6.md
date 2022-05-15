---
title: es6基础到高级
categories:
- 前端
tags:
- es6
abbrlink: 31462
---

# es6基础

## es6

### [es6](./advanced/es6.md)(es2015)

ES6既是一个历史名词也是一个泛指，含义是5.1版本以后的``JavaScript下一代标准``，目前涵盖了ES2015(ES6第一个版本)、ES2016(ES6第二个版本)、ES2017(ES6第三个版本)、ES2018(ES6第四个版本)、ES2019(ES6第五个版本)、ES2020(ES6第六个版本)。

有些文章上提到的ES7(实质上是ES2016)、ES8(实质上是ES2017)、ES9(实质上是ES2018)、ES10(实质上是ES2019)、ES11(实质上是ES2020)，实质上都是一些不规范的概念。

es6学习路径

知识点

> let、const 、var、symbol、set和map、proxy 、reflect、promise、iterator、for…of、generator、async、class、module、Arrary Buffer

1. `表达式`：
	- 声明（let、const、var）
	- 解构赋值(字符串解构、数值解构、布尔解构、对象结构、数组结构、函数参数解构)
2. `内置对象`：
	- 字符串、正则、数值、函数、数值、对象 扩展
	- Symbol、Set 和 Map 数据结构、Proxy、Reflect
3. `语句与运算`
	- class 
	- module
	- Iterator 和 for..of
4. `异步编程`
	- Promise
	- Generator 
	- Async
5. 异步遍历器
6. Array Buffer
7. Decorator

箭头函数

### es7(es2016)

1. 数值扩展
2. 数组扩展

### es8(es2017)

1. 声明
2. 字符串扩展
3. 对象扩展
4. 函数扩展

### es9(es2018)



### es10(es2019)



### es11(es2020)



### es12(es2021)



> 书籍
>
> - [x] [ES6 入门教程 ](https://es6.ruanyifeng.com/)
> - [x] [ECMAScript 6 入门 - 《阮一峰 ECMAScript 6 (ES6) 标准入门教程 第三版》 - 书栈网 · BookStack](https://www.bookstack.cn/read/es6-3rd/sidebar.md)
>
> 教程
>
> - [ ] [1.5万字概括ES6全部特性(已更新ES2020)](https://juejin.cn/post/6844903959283367950)
> - [ ] [ES6 完全使用手册](https://juejin.cn/post/6844903726201700365)
> - [ ] [近一万字的ES6语法知识点补充](https://juejin.cn/post/6844903775329583112)
> - [ ] [ES6、ES7、ES8、ES9、ES10新特性一览](https://juejin.cn/post/6844903811622912014)
>
> 视频
>
> - [ ] [4小时快速体验ES6-10的强大-慕课网](https://www.imooc.com/learn/1222)
> - [ ] [尚硅谷Web前端ES6教程，涵盖ES6-ES11_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1uK411H7on?from=search&seid=16458503401564236104)
> - [ ] [2019全新javaScript进阶面向对象ES6_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Kt411w7MP?from=search&seid=16458503401564236104)
>
> 
>
> - [ ] [ES6 入门教程 ](https://es6.ruanyifeng.com/)
> - [ ] [1.5万字概括ES6全部特性(已更新ES2020)](https://juejin.cn/post/6844903959283367950)
> - [ ] [ES6 完全使用手册](https://juejin.cn/post/6844903726201700365)
> - [ ] [近一万字的ES6语法知识点补充](https://juejin.cn/post/6844903775329583112)
> - [ ] [ES6、ES7、ES8、ES9、ES10新特性一览](https://juejin.cn/post/6844903811622912014)

> es6 = es2015 + es2016 + es2017 + es2018 + es2019 + es2020 + es提案

es6 新增内容

- 表达式：声明、解构赋值
- 内置对象：字符串扩展、数值扩展、对象扩展、数组扩展、函数扩展、正则扩展、Symbol、Set、Map、Proxy、Reflect
- 语句与运算：Class、Module、Iterator
- 异步编程：Promise、Generator、Async

es6 版本

- es2015
- es2016 
	- `** 指针运算符(数值求幂)`
	- `includes()（包含） 是否存在指定成员 `
- es2017
- es2018
- es2019
- es2020
- es提案

扩展

- 字符串
- 数值

## 概念

ECMASCript与JavaScript的关系

- 1998-06 ES2 发布、2015-06 ES6（ES2015 ）正式通过 成为国际标准。标准在每年的 6 月份正式发布一次，作为当年的正式版本。 ES2016 ( ES6.1)、ES2017 ( ES6.2)
- **ES6**是`ECMA`为`JavaScript`制定的第6个标准版本
- ES是JS的标准 或 规格 （ES是对ECMAScript的缩写）、JS是ES的实现，日常场合，两个词可以互换
- ES6 既是一个历史名词，也是一个泛指，含义是 5.1 版以后的 JavaScript 的下一代标准，涵盖了 ES2015、ES2016、ES2017 等等，而 ES2015 则是正式名称，特指该年发布的正式版本的语言标准。本书中提到 ES6 的地方，一般是指 ES2015 标准，但有时也是泛指“下一代 JavaScript 语言”。

## 声明

ES6的六种声明变量

- var、function  ES5
- let、const ES6新增
- import、class

| 关键字 | 作用                                                         | 作用范围       |
| ------ | ------------------------------------------------------------ | -------------- |
| let    | 声明变量、形成块级作用域、不存在变量提升、 暂时性死区、不允许重复声明 | 代码块中执行   |
| const  | 声明常量                                                     | 代码块中执行   |
| var    | 可以声明变量 也可以声明常量                                  | 全局代码中执行 |

### var 

- 全局变量 可以直接使用
- var 不受块级作用域的影响

```js
window.location.href === location.href
```
let和const的主要区别

- let声明变量
- const声明常量

### let

- let声明的变量只能在当前（块级）作用域内有效 代码块内有效
- 不能被重复声明

```js
var str = 'abc';
console.log(str);
var str = '';
console.log(str);
//   abc abc
var str = 'abc';
console.log(str);
var str = 'cdf';
console.log(str);
//   abc cdf
let num = 10;
let num = 12; 报错
```

- 不存在变量提升

```js
console.log(num)
var num = 12;
// undefined
console.log(num)
let num = 12;
// 报错
let num = 10;
{
	console.log(num); //拿不到num
	let num = 20; // let不存在变量提升
}
console.log(num);
// 报错
```

- let受块级作用域的影响

```js
var a = [];
for (var i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6](); // 10

var a = [];
for (let i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6](); // 6
```

- 暂存死区（就是变量声明和使用的问题） 暂时性死区 TDZ  块级作用域内存在`let`命令，它所声明的变量就“绑定”（binding）这个区域，不再受外部的影响
	- 变量的声明和使用的问题 变量一定要在声明之后使用，否则就报错
	- ES6 明确规定，如果区块中存在`let`和`const`命令，这个区块对这些命令声明的变量，从一开始就形成了封闭作用域。凡是在声明之前就使用这些变量，就会报错。
	- 在代码块内，使用`let`命令声明变量之前，该变量都是不可用的。这在语法上，称为“暂时性死区”（temporal dead zone，简称 TDZ）。
	- 暂时性死区的本质就是，只要一进入当前作用域，所要使用的变量就已经存在了，但是不可获取，只有等到声明变量的那一行代码出现，才可以获取和使用该变量。

```js
if (true) {
  tmp = 'abc'; // ReferenceError 使用  TDZ开始
  console.log(tmp); // ReferenceError
  let tmp; // TDZ结束 
  console.log(tmp); // undefined
  tmp = 123;
  console.log(tmp); // 123
}
```

### 作用域

- 全局作用域 `window`   ES5
- 函数作用域 `function(){}` ES5
- eval作用域 ES5
- 块级作用域 `{}`  ES6  let为JavaScript 新增了块级作用域

没有块级作用域的缺点

- 第一种场景，内层变量可能会覆盖外层变量

```js
var tmp = new Date();
function f() {
  console.log(tmp);
  if (false) {
    var tmp = 'hello world';
  }
}
f(); // undefined
```

- 第二种场景，用来计数的循环变量泄露为全局变量

```js
var s = 'hello';
for (var i = 0; i < s.length; i++) {
  console.log(s[i]);
}
console.log(i); // 5
```

一对花括号中的区域{.......}
块级作用域可以嵌套

```js
// 例子
if(){} 
for(){}
try{
}catch(err){
}
while(){}
//特殊 {} 是一个对象不是块级作用域
var object= {
	a:1
}
```
值格式化的问题

```js
// 问题
var i = 0
for(i = 1; i <= 10; i++){
    console.log(i)
}
// ES5
var i = 0
for(i = 1 ;i <= 10;i++){
    (function(i){
        console.log(i)
    })(i)
}
// ES6
for(let i = 1;i <= 10;i++){
	console.log(i)
}          
```
- ES6 允许块级作用域的任意嵌套 多层作用域

```js
{{{
	let a = 100;
	{ let b = 200; }
}}}
```

- 块级作用域的出现，实际上使得获得广泛应用的匿名立即执行函数表达式（匿名 IIFE）不再必要了。

```js
(function(){
	// 
}());

{
	let temp = 100;
}
```

匿名函数

```js
(function(参数1，参数2){
})(参数1，参数2);
(function(){
})();
```

- 全局作用域 (window)
- 函数作用域
- eval作用域
- 块级作用域

```js
//声明在全局作用域下，对全局作用域造成了一个污染
const FINGERS = 10
const HEAD = 1;
function Person(){
}
//解决方法使用匿名函数
(function(window,doucument){
    const FINGERS = 10
    const HEAD = 1;
    function Person(){
    }
    window.Person = Person; //把Person方法暴露在window里
})(window,doucument); //直接把参数传递进来，减轻函数往外搜索参数，提高性能
```

### const

> `const`实际上保证的，并不是变量的值不得改动，而是变量指向的那个内存地址所保存的数据不得改动。对于简单类型的数据（数值、字符串、布尔值），值就保存在变量指向的那个内存地址，因此等同于常量。但对于复合类型的数据（主要是对象和数组），变量指向的内存地址，保存的只是一个指向实际数据的指针，
>
> `const`只能保证这个指针是固定的（即总是指向另一个固定的地址），至于它指向的数据结构是不是可变的，就完全不能控制了。因此，将一个对象声明为常量必须非常小心。

- 常量-不可改变的量
- 和声明变量一样，基本只是关键字的区别
- 常量必须在声明的时候赋值
- 与letl类似的特性
- 不能重复声明
- 不存在提升
- 只在当前（块级）作用域内有效
```js
var v = '变量'
var v = '常量'
const c = '常量'
```
常量不可变？

- 一旦声明常量，就不能再改变（引用类型需要冻结）
- 常量为引用类型的时候 不能保证不改变(可以改变引用类型)

```js
const xiaoming = {
    age: 14,
    name: '小明'
};
console.log(xiaoming);
xiaoming.age = 20;  //地址没有改变
console.log(xiaoming);
xiaoming = {}	//地址改变
console.log(xiaoming); //报错
const  arr = []
arr.push(1);
console.log(arr);
arr = []; //报错
```
- 怎么防止常量为引用类型的时候能够被修改的情况;

```js
Object.freeze(常量名); //冻结常量为引用类型的时候能够被修改
```
```js
 const xiaoming = {
     age: 14,
     name: '小明'
};
Object.freeze(xiaoming) //不能修改 冻结        
console.log(xiaoming);
xiaoming.age = 20;  //地址没有改变
console.log(xiaoming);
xiaoming = {}	//地址改变
console.log(xiaoming); //报错
const  arr = []
Object.freeze(arr) //不能修改 冻结    
arr.push(1);
console.log(arr);
arr = []; //报错
```
es6之前声明常量

- 声明常量

```js
// 假装是常量
var BASE_COLOR = '#ff0000'
Object.defineProperty()//往一个对象上添加一个属性，同时可以进行描述
var CST = {}
Object.defineProperty(CST,'BASE_NAME',{
	value: '小明',
	writable: false //只读
});
Object.seal(CST) //不能扩展但能修改(防止对象被扩展)
//第三个参数描述 第二个参数属性名 第一个参数 ：往那个对象上修改添加属性
```
```js
var ST = {a :1}
Object.defineProperty(CST,'a',{
	writable: false //只读
});
Object.seal(CST) //不能扩展但能修改(防止对象被扩展),只用Object.freeze(常量名);的一半功能
```
- 封装一个常量

```js
// 遍历属性和方法
// 修改遍历到的属性的描述
// Object.seal()包装
Object.defineProperty(Object, 'freezePolyfill', {
    value: function (obj) {
        var i;
        for (i in obj) {
            if (obj.hasOwnProperty(i)) {
                Object.defineProperty(obj, i, {
                    writable: false
                });
            }
        }
        Object.seal(obj);
    }
});
const xiaoming = {
    age: 14,
    name: '小明'
    //		obj:{  a:1}
};
//		const Arr = []
Object.freezePolyfill(xiaoming);
```
- hasOwnProperty()

```js
var obj1 = {
    a: 1,
    b: 2
}
var obj2 = Object.create(obj1);
obj2.c = 3;
obj2.d = 4;
// obj2 本身只有c：3 d:4 // a:1与b:2不 是他原型上的,不要
for (let i in obj2) {
    // 解决方法 自身
    if (obj2.hasOwnProperty(i)) {
        document.body.innerHTML += (i + ':' + obj2[i] + '<br>');
    }
}
```

### 顶层对象

JavaScript 语言存在一个顶层对象，它提供全局环境（即全局作用域），所有代码都是在这个环境中运行。

- 浏览器 window 
- Node global
- 浏览器和 web worker self指向顶层对象   

同一段代码为了能够在各种环境，都能取到顶层对象，现在一般是使用`this`变量，但是有局限性。

- 全局环境 this 返回顶层对象 模块中 this 返回当前对象
- 函数中this 指向 顶层对象 严格模式this指向undefined
- 不管严格模式，还是普通模式 ，总是会返回全局对象

ES5 顶层对象的属性与全局变量挂钩

```js
// ES5 中 顶层对象的属性与全局变量是等价的 window.a = a
window.a = 1000;
a = 200;
window.a // 200
```

ES6  开始将全局变量逐步与顶层对象的属性脱钩

- `var`命令和`function`命令声明的全局变量，依旧是顶层对象的属性
- `let`命令、`const`命令、`class`命令声明的全局变量，不属于顶层对象的属性。

在所有情况下，都取到顶层对象

```js
// 方法一
(typeof window !== 'undefined'
   ? window
   : (typeof process === 'object' &&
      typeof require === 'function' &&
      typeof global === 'object')
     ? global
     : this);
// 方法二
var getGlobal = function () {
  if (typeof self !== 'undefined') { return self; }
  if (typeof window !== 'undefined') { return window; }
  if (typeof global !== 'undefined') { return global; }
  throw new Error('unable to locate global object');
};
```

ES 2020 `globalThis` 作为顶层对象。也就是说，任何环境下，`globalThis`都是存在的，都可以从它拿到顶层对象，指向全局环境下的`this`。

## 解构赋值

- 解构赋值语法是一个Javascript 表达式，这使得可以将值从数组或属性从对象提取到不同的变量中
- ES6允许按照一定模式，从数组和对象中提取值，对变量进行赋值，这被称为解构（Destructuring）
- 按照对应位置，对变量赋值。本质上，这种写法属于“模式匹配”，只要等号两边的模式相同，左边的变量就会被赋予对应的值
- 解构赋值的规则是，只要等号右边的值不是对象或数组，就先将其转为对象。由于`undefined`和`null`无法转为对象，所以对它们进行解构赋值，都会报错。

### 解构赋值

分类

- 数组  `[]`
- 对象 `{}`
	- 字符串 `[] `
	- 数值与布尔值 `number true/false`
- 函数参数  `function(){}`

作用

- 交换变量的值
- 从函数返回多个值 arr obj 
- 函数参数的定义 传递一个数组 传递一个对象进去
- 提取 JSON 数据  重要
- 函数参数的默认值
- 遍历 Map 结构
- 输入模块的指定方法

```js
[x,y] = [y,x]

function example(){
    return [1,2,3]; // return arr
}
let [a,b,c] = example()
function example(){
    return {  // return obj
        foo: 1,
        bar: 2
    };
}
let { foo,bar } = example()

// 参数是一组有次序的值
function f([x, y, z]) { ... }
f([1, 2, 3]);
// 参数是一组无次序的值
function f({x, y, z}) { ... }
f({z: 3, y: 2, x: 1});

let user = {
    id: 10001,
    name: Tom,
    status:"OK"
    data:[1000,2000]
}; 
let {id,name,status,data} = user; 
// data 
// data:number numer = [1000,2000]         
//遍历 Map 结构                     
const map = new Map();
map.set('first', 'hello');
map.set('second', 'world');
for (let [key, value] of map) {
  console.log(key + " is " + value);
}
// first is hello
// second is world
 // 获取键名
for (let [key] of map) {
  // ...
}
// 获取键值
for (let [,value] of map) {
  // ...
}   
                       
// 加载模块时，往往需要指定输入哪些方法。解构赋值使得输入语句非常清晰                       
const { SourceMapConsumer, SourceNode } = require("source-map");                     
```

### 数组解构

- 数组要新建变量名
- 左右两边的类型 右边是值 左边是key
- 如果等号的右边不是数组，会报错

```js
const arr = [1,2,3,4];
let [a,b,c,d] = arr
let a = arr[0];
```
更复杂的匹配规则
```js
const arr = ['a','b',['c','d',['e','f','g']]];
const [a,b] = arr //拿到a、b的值
const [,b] = arr; // b的值
const [, ,[,d]] = arr;
const [ , , g] = ['e','f','g']; // g的值
const [ , , [ , , g]] = ['c' , 'd' , ['e','f','g']];
const [ , , [ , , [ , , g]]] = arr;
const [,,[,,[,f]]] = arr;
 //不用逗号前空格,元素后面不用逗号
```
扩展运算符 `...`
```js
const arr1 = [1,2,3];
const arr2 = ['a','b','c'];
const arr3 = ['zz',1];
//const arr4 = [arr1,arr2,arr3];
const arr4 = [...arr1,...arr2,....arr3];
const arr = [1,2,3,4];
const [a,b,...c] = arr; //a=1 b = 2 c =[3,4] 还没所有的值
```
默认值 在变量设置

- 没有赋值或解构不成功，变量的值等于underfined

```js
const arr = [1,underfined,underfined];
const [a,b,c,d] = arr; //d underfined 
const [a,b = 2,c,d = 'bbb'] = arr; //b 2 d = bbb 设置默认值 
const arr = [1,underfined,null];
const [a,b,c,d] = arr; //c null 
```
交换变量
```js
 let a = 20;
 let b = 10;
 let temp;
 temp = a;
 a = b;
 b = temp;
 //解构赋值
 [a,b] = [b,a];
```
接受多个函数返回值
```js
function getUserInfo(id){
	return[ true,
		{
		name : '小明'，
		gender:'女'，
		id: id
		},
		'请求成功'
	];
};
// 新方法
const [status,data,msg] = getUserInfo(123);
// true  {name : '小明'，gender:'女'，id: 123} 请求成功
// 以前的方法
const resData = getUserInfo(123);
let status = resData[0];
```
Set 结构，也可以使用数组的解构赋值

```js
let [x,y,z] = newSet(['a','b','c'])
x // 'a'
```

### 对象解构

- 对象的结构赋值与数组的结构赋值相似
- 等号左右两边都为对象结构  const {a,b} = {a:1,b:2}
- 左边的{}中为**需要赋值得变量**
- 右边为需要**解构的对象**
  对象的解构赋值的主要用途
- 提取对象属性
- `变量必须与属性同名`，才能取到正确的值
- 对象的解构赋值的内部机制，是先找到同名属性，然后再赋给对应的变量。真正被赋值的是后者，而不是前者。

```js
let { foo,bar } = { foo:'aaa', bar:'bbb' };
等同于
let { foo:foo1,bar:bar2 } = { foo:'aaa',bar:'bbb' } 
foo1 = aaa bar2 = bbb
// 模式：变量
// foo bar 是匹配模式 foo1 bar2 才是变量
let { bar,foo } = { foo:'aaa', bar:'bbb' };
let { baz } = { foo:'aaa',bar:'bbb'} // underfined

const { name , hobby } = {
	name:'小红'，
	hobby:['学习']
}
```

- 变量名与属性名不一致

```js
let { foo: baz } = { foo:'aaa',bar:'bbb' }
baz // "aaa"
let { a:num } = { a:1000,b:2000 }
num // 1000
```

- 可以将现有对象的方法，赋值到某个变量

```js
let { log,sin,cos } = Math;
const { log } = console
log('hello')
```

- 使用对象传入乱序的函数参数

```js
//function AJAX(option){
// 	var type = option.type || 'get';
// 	console.log(option);
//};
function AJAX({
	url,
	data,
	type = 'get'
}){
	console.log(type);
};
AJAX({
	url:'/getinfo',
	data:{
		a:1
	},
});
```

- 获取多个函数返回值

```js
function getUserInfo()
{
 	return {
 		status:true,
 		data:{
 			name:'小红'
 		},
 		msg:'请求成功'
 	}；
};
const {status,data,msg} = getUserInfo(123)
// const {status,data,msg : message} = getUserInfo(123)
```

- 对象结构赋值的用法
```js
const obj = {
    num : '100',
    name : '张三',
        id :[
        {
            a: 1,
            b: 2,
            c: 3
        }, {
            d: 1,
            f: 2,
            g: 3
        }, {
            j: 1,
            k: 2,
            l: 3
        }
        ]
}; // ;
const { num } = obj;
const { name } = obj //不用逗号分隔
// const { num, name } = obj;
const { id: [id1] } = obj; //只能取出id的第一项，不能取出id的值
const {id:[id1,{a},{a:as}]} = obj 
const { id: [id1,{a}] } = obj;
//const { skill } = obj
//const [ id1 ]  = id; 第一项
```
稍微复杂的解构条件
扩展运算符
```js
const obj ={
	a:'1',
	b:'2',
	c:'3'
};
const {a,...oth} = obj; //可以拿到oth = b、c 
const obj1 = {
	num : '100',
	...obj,
};
```
如何对已经申明了的变量进行对象的解构赋值
```js
let age;
const obj = {
	name: '小明'，
	age:22
};
//两种方法
({ age }) = obj;
let { age } = obj;
```
默认值

- 默认值生效的条件是，对象的属性值严格等于underfined

```js
let girlfriend = {
	name:'小红'，
	age:22, //age:underfined 去默认值
};
let { name,age = 24, hobby =['学习'] } = girlfriend
```
### 字符串解构

```js
const str = "Switch is my first game";
const [ a, b, c] = str;
const [ a, b, c,...oth] = str; //扩展
//分解字符串的三种方式
const [...spStr1 ] = str;
const spStr2 = str.split('');
const spStr3 = [...str];
// 提取属性
const {length,split} = str;
```
数组的对象都有一个`length`属性，因此还可以对这个属性解构赋值。

```js
let { length:len } = 'message'
len // 5
```

### 数值与布尔解构

解构赋值时，如果等号右边是数值和布尔值，则会先转为对象。

```js
const {valueOf} = 1;
const {toString:ts } = false
let {toString: s} = 123;
s === Number.prototype.toString // true
let {toString: s} = true;
s === Boolean.prototype.toString // true
```
### 函数解构

- 参数 可以是对象和数组 设置默认值
- 返回值 可以是对象和数组

```js
function swap ([x,y]){
 	return [y,x];
};
let  arr = [1,2];
stt = swap(arr);
[[1, 2], [3, 4]].map(([a, b]) => a + b);
// [ 3, 7 ]
```
```js
function Computer({
	cpu,
	memory,
	software = ['ie6'],
	OS = 'Windows 3.5'
}){
	console.log(CPU);
	console.log(memory);
	console.log(sofeware);
	console.log(OS);
};
new Computer({
	memory:'128G',
	cpu:'80',
	OS:'windows 10'
})
```
- 函数设置默认值 重点

```js
function move({ x = 0, y = 0} = {}) {
  return [x, y];
}
move({x: 3, y: 8}); // [3, 8]
move({x: 3}); // [3, 0]
move({}); // [0, 0]
move(); // [0, 0]

function move({x, y} = { x: 0, y: 0 }) {
  return [x, y];
}
move({x: 3, y: 8}); // [3, 8]
move({x: 3}); // [3, undefined]
move({}); // [undefined, undefined]
move(); // [0, 0]
```

- `undefined`就会触发函数参数的默认值。

```js
[1, undefined, 3].map((x = 'yes') => x);
// [ 1, 'yes', 3 ]
```

圆括号问题

- 不能使用圆括号的情况
	- 变量声明语句
	- 函数参数
	- 赋值语句的模式
- 可以使用圆括号的情况：可以使用圆括号的情况只有一种：赋值语句的非模式部分，可以使用圆括号

## 扩展语法

### 字符串

扩展

- Unicode表示法
	- 编码 utf-8 utf-16 unicode
	- Unicode 表示法 `\uxxxx`
		-  `xxxx`是码点 
		- ES5 范围  \u0000`~`\uFFFF 超出这个范围的字符，必须用两个双字节的形式表示。
		- ES6   `只要将码点放入大括号，就能正确解读该字符`不再局限范围
			- 大括号表示法与四字节的 UTF-16 编码是等价的

```js
'\z' === 'z'  // true
'\172' === 'z' // true
'\x7A' === 'z' // true
'\u007A' === 'z' // true
'\u{7A}' === 'z' // true
```

- 字符串的遍历接口
	- `for...of`循环遍历 除了遍历字符串，这个遍历器最大的优点是可以识别大于`0xFFFF`的码点，传统的`for`循环无法识别这样的码点。

```
for(let codePoint of ‘foo’){
	console.log(codePoint)
}
```

- 直接输入U+2028和U+2029 分隔符 
	- 中文字符直接 转码点 	“中”的 Unicode 码点是 U+4e2d，你可以直接在字符串里面输入这个汉字，也可以输入它的转义形式`\u4e2d`，两者是等价的。
		- “中” ===  \u4e2d
	- JavaScript 规定有5个字符，不能在字符串里面直接使用，只能使用转义形式。
		- U+005C：反斜杠（reverse solidus) `\u005C`
		- U+000D：回车（carriage return）
		- U+2028：行分隔符（line separator）
		- U+2029：段分隔符（paragraph separator）
		- U+000A：换行符（line feed）
		- 字符串里面不能直接包含反斜杠，一定要转义写成`\\`或者`\u005c`
- JSON.stringify()的改造

> UTF-8 标准规定，`0xD800`到`0xDFFF`之间的码点，不能单独使用，必须配对使用。比如，`\uD834\uDF06`是两个码点，但是必须放在一起配对使用，代表字符`𝌆`。这是为了表示码点大于`0xFFFF`的字符的一种变通方法。单独使用`\uD834`和`\uDFO6`这两个码点是不合法的，或者颠倒顺序也不行，因为`\uDF06\uD834`并没有对应的字符。

JSON.stringify 

- 返回 0xD800 到 0xDFFF之间的单个码点
- 如果遇到`0xD800`到`0xDFFF`之间的单个码点，或者不存在的配对形式，它会返回转义字符串，留给应用自己决定下一步的处理。

```js
JSON.stringify('\u{D834}') // "\u{D834}"
JSON.stringify('\uDF06\uD834') // ""\\udf06\\ud834""
```

- 模板字符串 template string  是增强版的字符串，用反引号（`）标识。它可以当作普通字符串使用，也可以用来定义多行字符串，或者在字符串中嵌入变量。
	- 嵌入变量 `$(name)`
	- 如果使用模板字符串表示多行字符串，所有的空格和缩进都会被保留在输出之中。
	- 如果你不想要这个换行，可以使用`trim`方法消除它。

```js
let name = 'Java',time = 'now';
console.log(`hello ${name},how are you $(time)?`);
// 模板字符串之中还能调用函数。
function fn() {
  return "Hello World";
}
`foo ${fn()} bar`
// foo Hello World bar
// 如果模板字符串中的变量没有声明，将报错
// 变量place没有声明
let msg = `Hello, ${place}`;
// 报错
// 模板字符串的大括号内部，就是执行 JavaScript 代码，因此如果大括号内部是一个字符串，将会原样输出。
`Hello ${'World'}`
// "Hello World"
`${ 1+1 }` // 2
`${ JavaScript执行代码 }`
// 模板字符串甚至还能嵌套。
// 如果需要引用模板字符串本身，在需要时执行，可以写成函数。
let func = (name) => `Hello ${name}!`;
func('Jack') // "Hello Jack!"
```

- 实例：模板编译
- 标签模板
- 模板字符串的限制

新增方法

| 方法                                 | 作用                                                         |        |
| ------------------------------------ | ------------------------------------------------------------ | ------ |
| String.fromCodePoint()               | `Unicode码点转字符`从 Unicode 码点返回对应字符，但是这个方法不能识别码点大于`0xFFFF`的字符。 |        |
| codePointAt()                        | 能够正确处理 4 个字节储存的字符，返回一个字符的码点          |        |
| String.raw()                         | 该方法返回一个斜杠都被转义（即斜杠前面再加一个斜杠）的字符串，往往用于模板字符串的处理方法。 |        |
| normalize()                          | 用来将字符的不同表示方法统一为同样的形式，这称为 Unicode 正规化。 |        |
| includes()、startsWith()、endsWith() | 确定一个字符串``是否包含``在另一个字符串中                   |        |
| repeat()                             | 字符串``重复``                                               |        |
| padStart()、padEnd()                 | 字符串``补全长度``的功能。如果某个字符串不够指定长度，会在头部或尾部补全。 | ES2017 |
| trimStart()、trimEnd()               | `消除空格`                                                   | ES2019 |
| matchAll()                           | 返回一个正则表达式在当前字符串的所有匹配                     |        |

- `fromCodePoint`方法定义在`String`对象上，而`codePointAt`方法定义在字符串的实例对象上。
- `codePoint` JavaScript 内部，字符以 UTF-16 的格式储存，每个字符固定为`2`个字节。对于那些需要`4`个字节储存的字符（Unicode 码点大于`0xFFFF`的字符），JavaScript 会认为它们是两个字符。

```js
String.fromCodePoint(0x20BB7) // Unicode码点转字符
// "𠮷"

codePointAt()
let s = '𠮷a';
s.codePointAt(0) // 134071
s.codePointAt(1) // 57271
s.codePointAt(2) // 97
// 十六进制
s.codePointAt(0).toString(16) // "20bb7"
s.codePointAt(2).toString(16) // "61"


String.raw()  返回一个斜杠都被转义（即斜杠前面再加一个斜杠）的字符串，往往用于模板字符串的处理方法。
// 专用于模板字符串的标签函数
String.raw`Hi\n${2+3}!`
// 实际返回 "Hi\\n5!"，显示的是转义后的结果 "Hi\n5!"
String.raw`Hi\u000A!`;
// 实际返回 "Hi\\u000A!"，显示的是转义后的结果 "Hi\u000A!"
String.raw`Hi\\n`
// 返回 "Hi\\\\n"
String.raw`Hi\\n` === "Hi\\\\n" // true
// `foo${1 + 2}bar`
// 等同于
String.raw({ raw: ['foo', 'bar'] }, 1 + 2) // "foo3bar"

String.raw实现代码
String.raw = function (strings, ...values) {
  let output = '';
  let index;
  for (index = 0; index < values.length; index++) {
    output += strings.raw[index] + values[index];
  }
  output += strings.raw[index]
  return output;
}

normalize()  用来将字符的不同表示方法统一为同样的形式，这称为 Unicode 正规化。
// 参数 NFC NFD NFKC NFKD
// normalize方法目前不能识别三个或三个以上字符的合成。这种情况下，还是只能使用正则表达式，通过 Unicode 编号区间判断。
'\u01D1'.normalize() === '\u004F\u030C'.normalize()
// true
'\u004F\u030C'.normalize('NFC').length // 1
'\u004F\u030C'.normalize('NFD').length // 2

indexOf() lastindexOf() 是否包含 返回-1或索引值
let s = 'Hello world!';
s.indexOf('z') // -1
str.indexOf('e') // 0

inclues() startsWith endsWith()  是否包含 返回布尔值
// 字符串是否包含在另一个字符串中，返回布尔值 
// 第一个参数搜索的字符串 第二个参数 开始搜索的位置
let s = 'Hello world!';
s.startsWith('Hello') // true
s.endsWith('!') // true
s.includes('o') // true
s.startsWith('world', 6) // true
s.endsWith('Hello', 5) // true
s.includes('Hello', 6) // false
// 用第二个参数n时，endsWith的行为与其他两个方法有所不同。它针对前n个字符，而其他两个方法针对从第n个位置直到字符串结束。
// endsWith 向前找 startsWith 和 includes 向后找

repeart() 重复
// 参数如果是小数，会被取整
// 如果repeat的参数是负数或者Infinity，会报错
// 如果参数是 0 到-1 之间的小数，则等同于 0，这是因为会先进行取整运算。0 到-1 之间的小数，取整以后等于-0，repeat视同为 0。
// 如果repeat的参数是字符串，则会先转换成数字
'xy'.repeat(10)
'na'.repeat('na') // ""
'na'.repeat('3') // "nanana"

padStart padEnd() 补全长度
// 两个参数，第一个参数是字符串补全生效的最大长度，第二个参数是用来补全的字符串。
// 如果原字符串的长度，等于或大于最大长度，则字符串补全不生效，返回原字符串。
// 如果用来补全的字符串与原字符串，两者的长度之和超过了最大长度，则会截去超出位数的补全字符串。
// 如果省略第二个参数，默认使用空格补全长度。
'x'.padStart(10,'abc')
'x'.padEnd(10,'abc')
// 空格自动补全
'x'.padStart(4) // '   x'
'x'.padEnd(4) // 'x   '
//padStart()的常见用途是为数值补全指定位数。下面代码生成 10 位的数值字符串。
'1'.padStart(10, '0') // "0000000001"
'12'.padStart(10, '0') // "0000000012"
'123456'.padStart(10, '0') // "0000123456"
//提示字符串格式
'12'.padStart(10, 'YYYY-MM-DD') // "YYYY-MM-12"
'09-12'.padStart(10, 'YYYY-MM-DD') // "YYYY-09-12"

trimStart trimEnd() trim() 消除空格 
let str = "         x        "
str.trimEnd()
str.trimStart()

matchAll() 正则表达式匹配字符串 
```

### 数值

#### Number

- 二进制、八进制和十六进制的表示法
	- ES5 开始，在严格模式之中，八进制就不再允许使用前缀`0`表示，ES6 进一步明确，要使用前缀`0o`表示
	- 二进制 0b 或 0B 
	- 八进制 0o 或 0o 表示法
	- 十六进制

```js
Number('ob111') // 7 八进制转十进制
Number('0o100') //
```

| 方法                                                 | 作用                                                         |
| ---------------------------------------------------- | ------------------------------------------------------------ |
| Number.isFinite()、Number.isNaN()                    | 是否为有限的、是否为非数字                                   |
| Number.pareInt()、Number.parseFloat()                | 整型、浮点类型                                               |
| Number.isInteger()                                   | 判断一个数值是否为整数                                       |
| Number.ESSILON                                       | 一个极小的常量`Number.EPSILON`。根据规格，它表示 1 与大于 1 的最小浮点数之间的差。 是 JavaScript 能够表示的最小精度 引入一个这么小的量的目的，在于为浮点数计算，设置一个误差范围。我们知道浮点数计算是不精确的。 |
| Number.isSafeInteger()                               | 判断一个整数是否落在这个范围之内 安全整数                    |
| Number.MAX_SAFE_INTEGER<br />Number.MIN_SAFE_INTEGER |                                                              |

- ES6 引入了`Number.MAX_SAFE_INTEGER`和`Number.MIN_SAFE_INTEGER`这两个常量，用来表示这个范围的上下限。

```js
Number.isFinite() Number.isNaN() 是有限 是非数字
// 检查一个数值是否为有限的（finite），即不是Infinity
// 检查一个值是否为NaN
// 如果参数类型不是数值，Number.isFinite一律返回false。 
// 如果参数类型不是NaN，Number.isNaN一律返回false
Number.isFinite(0.8); // true
Number.isFinite(NaN); // false
Number.isFinite(Infinity); // false
Number.isFinite(-Infinity); // false
Number.isFinite('foo'); // false
Number.isFinite('15'); // false
Number.isFinite(true); // false
isFinite(25) // true
isFinite("25") // true
Number.isFinite(25) // true
Number.isFinite("25") // false
isNaN(NaN) // true
isNaN("NaN") // true
Number.isNaN(NaN) // true
Number.isNaN("NaN") // false
Number.isNaN(1) // false

Number.pareInt() Number.parseFloat()  解析成Int 或 Float类型
// ES6 将全局方法parseInt()和parseFloat()，移植到Number对象上面，行为完全保持不变 逐步减少全局性方法，使得语言逐步模块化
// ES5的写法
parseInt('12.34') // 12
parseFloat('123.45#') // 123.45
// ES6的写法
Number.parseInt('12.34') // 12
Number.parseFloat('123.45#') // 123.45

Number.isInteger()  判断一个数值是否为整数
// JavaScript 内部，整数和浮点数采用的是同样的储存方法，所以 25 和 25.0 被视为同一个值。
//  如果参数不是数值，Number.isInteger返回false
// 如果对数据精度的要求较高，不建议使用Number.isInteger()判断一个数值是否为整数。
Number.isInteger(25) // true
Number.isInteger(25.1) // false
Number.isInteger() // false
Number.isInteger(null) // false
Number.isInteger('15') // false
Number.isInteger(true) // false
// 高精度误判
Number.isInteger(3.0000000000000002) // true
Number.isInteger(5E-324) // false 一个数值的绝对值小于Number.MIN_VALUE（5E-324），即小于 JavaScript 能够分辨的最小值，会被自动转为 0
Number.isInteger(5E-325) // true

Number.ESSILON 最小精度
// Number.EPSILON可以用来设置“能够接受的误差范围”。
Number.EPSILON === Math.pow(2, -52)
// true
Number.EPSILON
// 2.220446049250313e-16
Number.EPSILON.toFixed(20)
// "0.00000000000000022204"

Number.isSafeInteger() 判断一个整数是否落在这个范围之内 安全整数
Number.isSafeInteger('a') // false
Number.isSafeInteger(null) // false
Number.isSafeInteger(NaN) // false
Number.isSafeInteger(Infinity) // false
Number.isSafeInteger(-Infinity) // false
Number.isSafeInteger(3) // true
Number.isSafeInteger(1.2) // false
Number.isSafeInteger(9007199254740990) // true
Number.isSafeInteger(9007199254740992) // false
Number.isSafeInteger(Number.MIN_SAFE_INTEGER - 1) // false
Number.isSafeInteger(Number.MIN_SAFE_INTEGER) // true
Number.isSafeInteger(Number.MAX_SAFE_INTEGER) // true
Number.isSafeInteger(Number.MAX_SAFE_INTEGER + 1) // false

实现方法
Number.isSafeInteger = function (n) {
  return (typeof n === 'number' &&
    Math.round(n) === n &&
    Number.MIN_SAFE_INTEGER <= n &&
    n <= Number.MAX_SAFE_INTEGER);
}
```

#### Math

| 方法                                          | 作用                                                         |
| --------------------------------------------- | ------------------------------------------------------------ |
| Math.trunc()                                  | 去除一个数的小数部分，返回整数部分                           |
| sign()                                        | 判断一个数到底是正数、负数、还是零。对于非数值，会先将其转换为数值 |
| cbrt()                                        | 立方根                                                       |
| 32位                                          |                                                              |
| clz32()                                       | 将参数转为 32 位无符号整数的形式，然后返回这个 32 位值里面有多少个前导 0 |
| imul()                                        | 返回两个数以 32 位带符号整数形式相乘的结果，返回的也是一个 32 位的带符号整数。 |
| fround()                                      | 返回一个数的32位单精度浮点数形式。                           |
| hypot()                                       | 所有参数的平方和的平方根                                     |
| sinh()、asinh                                 |                                                              |
| asinh()、acosh()、atanh()                     | 反双曲正弦\余弦\正切                                         |
| expm1()<br />log1p()<br />log10()<br />log2() | `Math.expm1(x)`返回 ex - 1，即`Math.exp(x) - 1`。<br />`Math.log1p(x)`方法返回`1 + x`的自然对数<br />`Math.log10(x)`返回以 10 为底的`x`的对数。<br />`Math.log2(x)`返回以 2 为底的`x`的对数。 |

双曲线函数方法

- `Math.sinh(x)` 返回`x`的双曲正弦（hyperbolic sine）
- `Math.cosh(x)` 返回`x`的双曲余弦（hyperbolic cosine）
- `Math.tanh(x)` 返回`x`的双曲正切（hyperbolic tangent）
- 
- `Math.asinh(x)` 返回`x`的反双曲正弦（inverse hyperbolic sine）
- `Math.acosh(x)` 返回`x`的反双曲余弦（inverse hyperbolic cosine）
- `Math.atanh(x)` 返回`x`的反双曲正切（inverse hyperbolic tangent）

- sign() 判断数的类型
	- 参数为正数，返回`+1`；
	- 参数为负数，返回`-1`；
	- 参数为 0，返回`0`；
	- 参数为-0，返回`-0`;
	- 其他值，返回`NaN`。

```js
Math.trunc() 去除小数部分 返回整数部分
Math.trunc('123.780') // 非数值，Math.trunc内部使用Number方法将其先转为数值
Math.trunc(underfined/'foo'/NaN) //空值和无法截取整数的值，返回NaN

Math.sign() 正负值类型
Math.sign('')  // 0
Math.sign(true)  // +1
Math.sign(false)  // 0
Math.sign(null)  // 0
Math.sign('9')  // +1
Math.sign('foo')  // NaN
Math.sign()  // NaN
Math.sign(undefined)  // NaN

Math.hypot()
Math.hypot(3, 4);        // 5
Math.hypot(3, 4, 5);     // 7.0710678118654755
Math.hypot();            // 0
Math.hypot(NaN);         // NaN
Math.hypot(3, 4, 'foo'); // NaN
Math.hypot(3, 4, '5');   // 7.0710678118654755
Math.hypot(-3);          // 3
// 3 的平方加上 4 的平方，等于 5 的平方。
```

#### 指数运算符

```js
// 指数运算符 `**`
2**3**4
// 指数运算符可以与等号结合，形成一个新的赋值运算符（**=）
a **=2;
// 等同于 a = a * a;
b **=3;
// 等同于 b = b * b * b;
```

#### BigInt数据类型

简介

> JavaScript 所有数字都保存成 64 位浮点数，这给数值的表示带来了两大限制。
>
> - 2^^53 到 2^^1024
> - 一是数值的精度只能到 53 个二进制位（相当于 16 个十进制位），大于这个范围的整数，JavaScript 是无法精确表示的，这使得 JavaScript 不适合进行科学和金融方面的精确计算。
> - 二是大于或等于2的1024次方的数值，JavaScript 无法表示，会返回`Infinity`。

```js
// 超过 53 个二进制位的数值，无法保持精度
Math.pow(2, 53) === Math.pow(2, 53) + 1 // true
// 超过 2 的 1024 次方的数值，无法表示
Math.pow(2, 1024) // Infinity
```

BigInt 一种新的数据类型 大整型 ，来解决这个问题。BigInt 只用来表示整数，没有位数的限制，任何位数的整数都可以精确表示。

- 为了与 Number 类型区别，BigInt 类型的数据必须添加后缀`n`
- BigInt 同样可以使用各种进制表示，都要加上后缀`n`
- BigInt 与普通整数是两种值，它们之间并不相等。
- typeof`运算符对于 BigInt 类型的数据返回`bigint
- BigInt 可以使用负号（`-`），但是不能使用正号（`+`），因为会与 asm.js 冲突。

```js
const a = 2172141653n;
const b = 15346349309n;
// BigInt 可以保持精度
a * b // 33334444555566667777n
// 普通整数无法保持精度
Number(a) * Number(b) // 33334444555566670000

1234 // 普通整数
1234n // BigInt
// BigInt 的运算
1n + 2n // 3n

0b1101n // 二进制
0o777n // 八进制
0xFFn // 十六进制

42n === 42 // false

typeof 123n // 'bigint'

-42n // 正确
+42n // 报错

let p = 1n;
for (let i = 1n; i <= 70n; i++) {
  p *= i;
}
console.log(p); // 11978571...00000000n
```

BigInt对象

JavaScript 原生提供`BigInt`对象，可以用作构造函数生成 BigInt 类型的数值。转换规则基本与`Number()`一致，``将其他类型的值转为 BigInt`。

BigInt 转换数据类型 

- 无参数、underfined、null、小数、字符串、已经是bigint类型 报错

```js
BigInt(123) // 123n
BigInt('123') // 123n
BigInt(false) // 0n
BigInt(true) // 1n

new BigInt() // TypeError
BigInt(undefined) //TypeError
BigInt(null) // TypeError
BigInt('123n') // SyntaxError
BigInt('abc') // SyntaxError

BigInt(1.5) // RangeError
BigInt('1.5') // SyntaxError
```

方法

- BigInt 对象继承了 Object 对象的两个实例方法
	- `BigInt.prototype.toString()`
	- `BigInt.prototype.valueOf()`
- 继承了 Number 对象的一个实例方法
	- `BigInt.prototype.toLocaleString()`
- 三个静态方法
	- `BigInt.asUintN(width, BigInt)`： 给定的 BigInt 转为 0 到 2width - 1 之间对应的值。
	- `BigInt.asIntN(width, BigInt)`：给定的 BigInt 转为 -2width - 1 到 2width - 1 - 1 之间对应的值。
	- `BigInt.parseInt(string[, radix])`：近似于`Number.parseInt()`，将一个字符串转换成指定进制的 BigInt。

```js

```

转换规则 将 BigInt 可以转为布尔值、数值和字符串类型

- Boolean()
- Number()
- String()

取反运算符（`!`）也可以将 BigInt 转为布尔值

```js
Boolean(0n) // false
Boolean(1n) // true
Number(1n)  // 1
String(1n)  // "1"
!0n // true
!1n // false
```

数学运算

BigInt 类型的`+`、`-`、`*`和`**`这四个二元运算符，与 Number 类型的行为一致。除法运算`/`会舍去小数部分，返回一个整数。

```js
9n / 5n
// 1n
```

BigInt 不能与普通数值进行混合运算。

如果一个标准库函数的参数预期是 Number 类型，但是得到的是一个 BigInt，就会报错

其他运算

BigInt 与字符串混合运算时，会先转为字符串，再进行运算

```
'' + 123n // "123"
```





### 对象

扩展

- 属性的简洁表示法
- 属性名表达式
- 方法的name属性
- 属性的可枚举和遍历
- super关键字
- 对象的扩展运算符
- 链判断运算符
- Null判断运算符

```js

```

新增方法

| 方法                                                         | 作用 |
| ------------------------------------------------------------ | ---- |
| Object.is()                                                  |      |
| Object.assign()                                              |      |
| Object.getOwnPropertyDescriptors()、Object.setPrototypeOf()、Object.getPrototypeOf() |      |
| ``__proto__`属性                                             |      |
| Object.keys() Object.values() Object.entries()               |      |
| Object.fromEntries()                                         |      |

```js

```

### 数组

扩展运算符 `spread` 

扩展运算符（spread）是三个点（`...`）。它好比 rest 参数的逆运算，将一个数组转为用逗号分隔的参数序列。





数组的空位

| 方法                      | 作用 |
| ------------------------- | ---- |
| Array.prorotype.sort()    |      |
| Array. from()             |      |
| Array.of()                |      |
| copyWithin()              |      |
| find()和findIndex()       |      |
| fill()                    |      |
| entries() keys() values() |      |
| includes()                |      |
| flat()、flatMap()         |      |
| sort()                    |      |

```js

```

扩展运算符的应用

- 复制数组
- 合并数组
- 与解构赋值结合
- 字符串
- 实现了 Iterator 接口的对象
- Map 和 Set 结构，Generator 函数



### 函数

- 函数参数的默认值
- rest参数
- 严格模式
- name属性
- 箭头函数
- 尾调用优化
- 函数参数的尾逗号
- Function.prototype.toString()
- catch命令的参数省略

```js

```

### 正则

RegExp构造函数

Unicode属性类

具名组匹配

正则匹配索引

字符串

- 字符串的正则方法
- String.prototype.matchAll()

RegExp.prototpye.unicode属性

RegExp.prototype.sticky属性

RegExp.prototype.flags属性

修饰符

- u修饰符
- y修饰符
- s修饰符：dotAll 模式

后行断言



## 数据结构





## Symbol

- Symbol()
- Symbol.for()
- Symbol.keyFor()
- Symbol.prototype.description()
- Object.getOwnPropertySymbols()
- 内置Symbol属性



## Set和Map

### set

- new Set()

- constructor


size 

- add()

- delete()

- has()

- clear()

- keys()

- values()

- entries()

- forEach()


WeakSet

### map 

- new Map()

- constructor

- size 

- get()

- set()

- delete()

- has()

- clear()

- keys()

- values()

- entries()

- forEach()

- WeakMap

## Proxy

概述

是什么？



new Proxy()



Proxy.revovable()



Proxy实例的方法

拦截方法13个

| 方法                                          | 作用 |
| --------------------------------------------- | ---- |
| **get(target, propKey, receiver)**            |      |
| **set(target, propKey, value, receiver)**     |      |
| **has(target, propKey)**                      |      |
| **deleteProperty(target, propKey)**           |      |
| **ownKeys(target)**                           |      |
| **getOwnPropertyDescriptor(target, propKey)** |      |
| **defineProperty(target, propKey, propDesc)** |      |
| **preventExtensions(target)**                 |      |
| **getPrototypeOf(target)**                    |      |
| **isExtensible(target)**                      |      |
| **setPrototypeOf(target, proto)**             |      |
| **apply(target, object, args)**               |      |
| **construct(target, args)**                   |      |



## Reflect

get()



set()



has()



deleteProperty()



defineProperty()



ownKeys()



getOwnPropertyDescriptor()



getPrototypeOf()



setPrototypeOf()





isExten











## Promise

- (是什么)异步编程的一种解决方案，比传统的解决方案callback更加的优雅
- 对象的状态不受外界影响（Promise对象代表一个异步操作，有三种状态）
	- pending (执行中) 初始状态
- resolved (成功，又称Fullfilled)
- rejected

pending为初始状态，fulfilled和rejected为结束状态（结束状态表示promise的生命周期已结束）。promise只有异步操作的结果，可以决定当前是哪一种状态，任何其他操作都无法改变这个状态.。

一旦状态改变，就不会再变，任何时候都可以得到这个结果

Promisse对象的状态改变，只有两种可能

从Pending变为Resolved
从Pending变为Rejected

只要这两种情况发生，状态就凝固了，不会再变了，会一直保持这个结果

Promise对象的缺点：

无法取消Promise，一旦新建它就会立即执行，无法中途取消。
如果不设置回调函数，Promise内部抛出的错误，不会反应到外部。
当处于Pending状态时，无法得知目前进展到哪一个阶段（刚刚开始还是即将完成。
4、promise兼容性：除了IE这种古老的浏览器和一些低版本的安卓外，大部分的浏览器对于promise的兼容性还是很友好的，所以我们可以在谷歌的控制台直接测试我们的代码。

解决什么问题：解决回调层层嵌套的问题、代码不够直观，逻辑梳理上困难

简单的解释给小朋友听

```js
// callback 回调函数 回调地狱

let promise1 =   new promise(function(){
    
}).then(fucntion(succle){
    console.log('成功')
}).catch(funciton(error){
     console.log('失败' + error);     
})
```

| 方法         | 作用 |
| ------------ | ---- |
| resolve()    |      |
| reject()     |      |
| try()        |      |
| then()       |      |
| catch()      |      |
| finally()    |      |
| all()        |      |
| race()       |      |
| allSettled() |      |
| any()        |      |

### new Promise()



### then()



### catch()



### Promise.all()



### Promise.race()



### Promise.resolve()



### Promise.reject()





## Iterator和 for of 循环



### 迭代器(for-of)



### next()



### return()



### throw()



## 箭头(Arrow)函数

- 单个参数名
- 多个参数名

```js
function Buy(){ }
() => 
() =>{  }
```



- 变量声明let与const
- 变量的解构赋值
	+ 数组解构赋值
	+ 对象解构赋值
	+ 字符串解构赋值
- 字符串扩展
	+ includes()
	+ startsWith()
	+ endsWith()
	+ 模板字符串
- 函数扩展
	+ 参数默认值
	+ 参数结构赋值
	+ rest参数
	+ 扩展运算符
	+ 箭头函数
- 类与继承

```js
function Animal(name){
	this.name = name;
}
Animal.prototype.showName = function(){
	console.log(this.name);
}
var a = new Animal('Tom');
a.showName();
var a1 = new Animal('Jerry');
a1.showName()
// ------------------
class Animal{
    //静态方法(静态方法只能通过类名调用，不可以使用实例对象调用)
    static showInfo(){
        console.log('hi')
    }
    // 构造函数
    constructor(name){
        this.name = name;
    }
    showName(){
        console.log(this.name);
    }
}
let a = new Animal('spike');
a.showName();
Animal.showInfo();
// 类的继承 extends
面向对象的编程语言
class Dog extend Animal{
    constructor(name,color){
       	super(name); //super 用来调用父类 
        this.color = color;
    }
    showColor(){
        console.log(this.color);
    }
}
let d = new Dog('gg','yellow');
d.showColor();
d.showName();
Dog.showInfo();
```





## 异步遍历器



## 反射机制









## Template









## Async







## Class 

- 类
	- 继承 封装 多态
- 定义类 `class 类名`
	- 构造函数（constructor） 实例化的时候将会被调用，如果不指定，那么会有一个不带参数的默认构造函数`constructor(属性值,属性值)`
	- 原型对象上的属性`toString()`
- 使用类 `new 类名() 对象名.值 对象名.方法`  
	- 实例化对象 `new 类名()`
	- 对象名.属性方法
	- 对象名.属性值
- 类的三大特性
	- 封装 
	- 继承 `extends`
	- 多态

类的封装

```js
class Animal{
	// 构造函数
    let num = 1000;
    constructor(name,age){
        this.name = name;
        this.age = age;
    }
    // toString 是原型对象上的属性
    toString(){
        console.log('name'+ this.name + 'age' + this.age);
    }
    tell(){
        console.log('Hi Hi Hi')
    }
}

var animal = new Animal('dog',100);
animal.num;
animal.toString();
animal.tell();
```

类的继承

```js
class Cat extends Animal{
   constructor(action){
       super('cat','white');
       this.action = action; 
   }
   toString(){
       console.log(super.toString());
   }    
}

var cat = new Cat('catch')
cat.toString();
```

类的多态

```js

```

### class



### constructor



### 关键字





### 静态属性





### 静态方法



### name属性



### 属性表达式



### Generator



### Async



### new.target













## Generator

### 语法

`*`命令



yeild 命令





`yeild*`命令





### next()



### return()



### throw()

### 异步应用

## Module

1. 了解企业级的开发形式——模块化的使用
2. 2、学习将一个复杂的功能拆分，从而提高复用率
3. 3、了解如何更好的维护代码
4. 4、掌握babel转换器的使用，解决ES6的兼容问题
5. 5、学习如何将Webpack与配合Babel使用，完成更高效的开发
6. 6、掌握Webpack项目构建配置

模块化

语法

ES5不支持原生的模块化，在ES6中模块作为重要的组成部分被添加进来。模块的功能主要由 export 和 import 组成。每一个模块都有自己单独的作用域，模块之间的相互调用关系是通过 export 来规定模块对外暴露的接口，通过import来引用其它模块提供的接口。同时还为模块创造了命名空间，防止函数的命名冲突。

### export 

```js

```

### import

```js

```

### 复合模式

```

```

加载

## ArrayBuffer





## Decorator



## Mixin



## SIMD





## 函数式编程





# es6深入

## 块级绑定

## 字符串与正则表达式

## 函数

## 扩展的对象功能

## 更方便的数据访问

## 符号与符号属性

## Set和Map

## 迭代器与生成器

## JS的类

## 增强的数组功能

## Promise与异步编程

## 代理



## 用模块封装代码



# es2016

> 指针运算符、includes(包含值,查找位置)函数 包含 

## 数值扩展（指针运算符(**)）

- 指数运算符(**)：数值求幂(相当于Math.pow())

```js
Math.pow(2,5) === 2**5 
```

## 数组扩展（includes() 包括）

- includes()：包括 是否存在指定成员

```js
arr.includes(valueToFind[, fromIndex]) return boolean
// 第一个值查找的元素、第二个值开始查找的位置 return boolean
// 第二个值为负数：如果计算出的索引小于 0，则整个数组都会被搜索
// 查找的元素值
// 如果 fromIndex 大于等于数组的长度，则会返回 false，且该数组不会被搜索。
```

```js
[1,2,3,4,5,6].includes(1) //true

[1,2,3,4,5,6].includes(1,2) // true
[1,2,3,4,5,6].includes(1,6) // false
[1,2,3,4,5,6].includes(1,10) // false
```

# es2017

## 声明

- 共享内存和原子操作：由全局对象SharedArrayBuffer和Atomics实现，将数据存储在一块共享内存空间中，这些数据可在JS主线程和web-worker线程之间共享

## 扩展

- 6个 2字符 3对象 1函数
	- padStart padEnd()
	- Object.getOwnPropertyDescriptors()、Object.values()、Object.entries()

|            |                                                              |                                                      |                                          |
| ---------- | ------------------------------------------------------------ | ---------------------------------------------------- | ---------------------------------------- |
| 字符串扩展 | str.padStart(targetLength（指目标字符串长度） [, padString]（补全长度的字符串）) padStart()：把指定字符串填充到字符串头部，返回新字符串 | padEnd()：把指定字符串填充到字符串尾部，返回新字符串 |                                          |
| 对象扩展   | Object.getOwnPropertyDescriptors()：返回对象所有自身属性(非继承属性)的描述对象 | Object.values()：返回以值组成的数组                  | Object.entries()：返回以键和值组成的数组 |
| 函数扩展   | 函数参数尾逗号：允许函数最后一个参数有尾逗号                 |                                                      |                                          |

```js
'helloes2017'.padStart(12,'Start')
// 第一个值是指插入字符串后，整个字符串的长度 所以第一个值可以插入多次 
'helloes2017’.padEnd(12,'End')
"123".padStart(12)  // "         123" 
```

## Async

```js

```



# es2018

## 扩展

### 字符串



### 对象



### 正则





## Promise

- finaly  指定不管最后状态如何都会执行的回调函数

```js
new Promise()
```

## Async

- 异步迭代器for-await-of  循环等待每个`Promise对象`变为`resolved状态`才进入下一步

# es2019

## 扩展

### 字符串

- JSON.stringify()：可返回不符合UTF-8标准的字符串
- trimStart()：消除字符串头部空格，返回新字符串
- trimEnd()： 消除字符串尾部空格，返回新字符串

```js
var str = '   testtest    ';
str.trimStart();
str.trimEnd();
```

### 对象

- Object.fromEntries()：返回以键和值组成的对象(`Object.entries()`的逆操作)

### 数组

- **sort()稳定性**：排序关键字相同的项目其排序前后的顺序不变，默认为`稳定`
-  **flat()**：扁平化数组，返回新数组
-  **flatMap()**：映射且扁平化数组，返回新数组(只能展开一层数组)

```js
var arr = [34,234,445,56,8]
arr.sort()
var twoArr = [34,234,[34,[34,234,445,56,8],234,445,56,8],445,56,8]
twoArr.flat()
```

### 函数

-  **toString()改造**：返回函数原始代码(与编码一致)
-  **catch()参数可省略**：`catch()`中的参数可省略

## Symbol

- description: 返回Symbol值的描述

# es2020

|          |      |      |
| -------- | ---- | ---- |
| 声明     |      |      |
| 扩展     |      |      |
| Module   |      |      |
| Iterator |      |      |
| Promise  |      |      |

## 声明 globalThis

globalThis：作为顶层对象，指向全局环境下的this

- Browser：顶层对象是window
- Node：顶层对象是global
- WebWorker：顶层对象是self
- 以上三者：通用顶层对象是globalThis

## 扩展

|          |                                                 |      |
| -------- | ----------------------------------------------- | ---- |
| 数值扩展 | BigInt任何位数的整数(新增的数据类型，使用n结尾) |      |
| 对象扩展 | 链判断操作符(?.) 空判断符(??)                   |      |
| 正则扩展 | matchAll()：返回所有匹配的遍历器                |      |

### 数值扩展

BigInt :

- Bigint()：转换普通数值为Bigint类型
- BigInt.asUintN()：转换BigInt为0到2n-1之间对应的值
- BigInt.asIntN()：转换BigInt为-2n-1 到2n-1-1
- BigInt.parseInt()：近似于Number.parseInt()，将一个字符串转换成指定进制的BigInt类型

### 对象扩展

**链判断操作符(?.)**：是否存在对象属性(不存在返回`undefined`且不再往下执行)

- 对象属性：`obj?.prop`、`obj?.[expr]`
- 函数调用：`func?.(...args)`

 **空判断操作符(??)**：是否值为`undefined`或`null`，是则使用默认值

### 正则扩展

- matchAll()：返回所以匹配的遍历器

```js

```

## Module

- import ：动态导入(返回`Promise`)

```js
import
```

## iterator

- for-in 遍历顺序

```js

```

## Promise

- Promise.allSettled

# es提案

## 声明

- do：封装块级作用域的操作，返回内部最后执行表达式的值(`do{}`)
- throw：直接使用`throw new Error()`，无需`()`或`{}`包括
- !#命令：指定脚本执行器(写在文件首行)

```js
!# 指定脚本
do()
throw new Error()
```

## 扩展

### 数值扩展

- 数值分隔符：使用`_`作为千分位分隔符(增加数值的可读性)
- Math.signbit：返回数值符号是否设置

```js
const num = 100_393
const num2 = 122_100_393
cosole.log(num,num2) // 100393 122100393
Math.signbit(num) 
```

### 正则扩展



### 函数扩展



## Realm

- 定义：提供`沙箱功能`，允许隔离代码，防止被隔离的代码拿到全局对象
	- 声明：`new Realm().global`

```js
new Realm().global
```

## Class



## Module

- import.meta：

## Iterator







## Async







