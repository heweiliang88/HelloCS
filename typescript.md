---
title: typescript
categories:
- 前端
tags:
- typescript
abbrlink: 26221
---
# 优雅的TypeScript

> - [ ] [TypeScript 入门教程](https://ts.xcatliu.com/)
> - [ ] [TypeScript中文网 · TypeScript——JavaScript的超集](https://www.tslang.cn/docs/home.html)
> - [x] [尚硅谷2021版TypeScript教程](https://www.bilibili.com/video/BV1Xy4y1v7S2?from=search&seid=5846073422451256988)
> - [ ] [Typescript教程_Typescript视频教程 ts入门实战视频教程](https://www.bilibili.com/video/BV1yt411e7xV?from=search&seid=5846073422451256988)
> - [ ] [TypeScript 系统入门到项目实战-慕课网](https://coding.imooc.com/class/412.html)
> - [ ] [2小时极速入门 TypeScript-慕课网](https://www.imooc.com/learn/1306)
> - [ ] [TypeScript 入门教程](https://ts.xcatliu.com/introduction/what-is-typescript.html)

## 报错问题

typescript 无法重新声明块范围变量

> [TypeScript无法重新声明块范围变量](https://blog.csdn.net/qq_45587822/article/details/106736207)

```json
// tsconfig.json
{
  // "include": ["src", "demo"],
  "compilerOptions": {
    "module": "commonjs",
    "noImplicitReturns": true,
    "noUnusedLocals": true,
    "esModuleInterop": true,
    "target": "esnext",
    "strict": true,
    "outDir": "app",
    "declaration": true,
    "sourceMap": true
  }
}
```

## 基础知识

TypeScript : Typed JavaScript at Any Scale 静态系统、静态类型、弱类型

- 一个javascript 的超集
- 以JavaScript为基础构建的语言
- 可以在任何支持JavaScript的平台上执行
- TypeScript扩展了JavaScript并添加了类型
- TypeScript是静态类型
	- 类型系统按照类型检查的时机来分类，可以分为动态类型和进静态类型
		- 动态类型是指在运行时才会进行类型检查，这种语言的类型错误往往会导致运行时错误。JavaScript 是一门解释型语言[[4\]](https://ts.xcatliu.com/introduction/what-is-typescript.html#link-4)，没有编译阶段，所以它是动态类型。
		- 静态类型是指编译阶段就能确定每个变量的类型，这种语言的类型错误往往会导致语法错误。
			- TypeScript(静态类型)  运行前需要先编译为 JavaScript，而在编译阶段就会进行类型检查
		- 超级重点： JavaScript 代码经过少量修改就变成TypeScript ，原因是TypeScript强大的类型推论 ，不去手动声明变量也会自动推论出相应类型
- TS不能被JS解析器直接执行 ，要将TS解析为JS文件

什么是TypeScript

- TypeScript 是添加了类型系统的 JavaScript，适用于任何规模的项目。
- TypeScript 是一门静态类型、弱类型的语言。
- TypeScript 是完全兼容 JavaScript 的，它不会修改 JavaScript 运行时的特性。
- TypeScript 可以编译为 JavaScript，然后运行在浏览器、Node.js 等任何能运行 JavaScript 的环境中。
- TypeScript 拥有很多编译选项，类型检查的严格程度由你决定。
- TypeScript 可以和 JavaScript 共存，这意味着 JavaScript 项目能够渐进式的迁移到 TypeScript。
- TypeScript 增强了编辑器（IDE）的功能，提供了代码补全、接口提示、跳转到定义、代码重构等能力。
- TypeScript 拥有活跃的社区，大多数常用的第三方库都提供了类型声明。
- TypeScript 与标准同步发展，符合最新的 ECMAScript 标准（stage 3）

TyepeScript的特点

- 添加了``类型系统``的JavaScript
- 是静态类型的
- 是弱类型的
	- 什么是弱类型、什么是强类型？
	- 类型系统按照[是否允许隐式类型装换] 来分类 ，可以分为强类型和弱类型
	- TypeScript 和 JavaScript 一样都是隐式类型转换的

TypeScript:添加的内容

- 类型
- 支持ES的新特性
- 添加ES6不具备的新特性
- 丰富的配置选项
- 强大的开发工具

JavaScript的缺点

- 它没有类型约束，一个变量可能初始化时是字符串，过一会儿又被赋值为数字。
- 由于隐式类型转换的存在，有的变量的类型很难在运行前就确定。
- 基于原型的面向对象编程，使得原型上的属性或方法可以在运行时被修改。
- 函数是 JavaScript 中的一等公民[[2\]](https://ts.xcatliu.com/introduction/what-is-typescript.html#link-2)，可以赋值给变量，也可以当作参数或返回值。
- 代码质量参差不齐，维护成本高，运行时错误多

### 安装

```bash
npm install -g typescript
cnpm install -g typescript 
npm  install -g ts-node
cnpm  install -g ts-node
```
查看Typescript版本号
```bash
tsc -v
```
![img](https://i.loli.net/2020/08/08/FTt2i67YuPWGZbO.png)
运行`.ts文件`sdasdas

- typescript 相当于JavaScript添加了编译这一步 编译 ==> 运行

```bash
tsc test.ts
node test.js
```
```tsx
// test.js
function tsfunc(){
	let msg: string = 'Hello World'
	console.log(msg)
}
tsfunc()

// 声明变量 变量名:类型
function sayTs(lang:string){
    return 'Hello' + lang
}

let langs = 'TypeScript'
console.log(s)

tsc test.ts
node test.js


tsc demots.ts && node demots.js 
ts-node test.js // 直接执行上面两部
```

tsconfig.json 配置

```json
// tsconfig.json
{
  // "include": ["src", "demo"],
  "compilerOptions": {
    "module": "commonjs",
    "noImplicitReturns": true,
    "noUnusedLocals": true,
    "esModuleInterop": true,
    "target": "esnext",
    "strict": true,
    "outDir": "app",
    "declaration": true,
    "sourceMap": true
  }
}
```

## 数据类型

### 类型声明

```js
let 变量:类型;
let 变量:类型 = 值;
let name:string = 'hwl'

funciton fn(参数:类型,参数:类型){
}
```

| 类型             | 表达式                                           |
| ---------------- | ------------------------------------------------ |
| 布尔值           | `let isTrue:boolean = false`                     |
| 字符串           | `let str:string = 'String'`                      |
| 数值             | `let num:number = 100`                           |
| void             | `function alertMsg():void{}`                     |
| null和underfined | `let u:undefined = undefined;let n:null = null;` |

JavaScript的数据类型分为两种

- （7种）原始数据类型（primitive data types）:布尔值 、数值、字符串、null、underfined、Symbol（es6）、BigInt（es10）
- 对象属性类型 (Object types)

类型声明

#### 布尔值

```tsx
let isTrue:boolean = false; // 布尔值
let newboolean:boolean = new Boolean(1) // 返回的是一个Boolean对象
```

#### 数值

```tsx
// 二进制、八进制、十进制、NaN、Infinity
let num:number = 100 // 0xf00o 0xf00d 0o347 NaN Infinity
```

#### 字符串

```tsx
let str:string = 'String';
let strName:string = `${str}` // 模板字符串
console.log(strName)
```

#### 空值 void

```tsx
function alertMsg():void{ // 没有返回值的函数 函数():void
  	alert('这是一条弹窗消息')
}

//  声明void的变量没有作用
let uAge：void
uAge = 18 
let uAge:void = 18 //  报错

let uVoid:void = underfined
let uVoid:void = null 
```

#### null和underfined

null 和 underfined vs void 

- underfined 和 null 是所有类型的子类型 undefined 类型可以赋值给number类型的变量

```tsx
let u:undefined = undefined;
let n:null = null;

let num:number = undefined;

let u:underfined;
let num:number = u;
```

#### 数组类型

- 5种方法
- 类型 + 方括号 `number[]`
- 数组泛型 `Array<number>`
- 接口  `interface { [index:number]:number }`
	- 不常用表示数组、常用来表示类数组
	- 索引的类型是数字时，那么值的类型必须是数字
- 类数组 Array-link Object 不是数组类型 
	-  类数组都有自己的接口定义 IArguments 、NodeList、HTMLCollection
- any[]

```tsx
// 「类型 + 方括号」 number[]
let fib:number[] = [1,2,3,4,5];
// 数组项不允许出现其他的类型

// 数组泛型 Array<number>
let arr:Array<number> = [1,2,3,4,5];

// 接口数组
interface numArray{
    [index:number]:number // [下标:类型]:类型
}
let arr:numArray = [1,2,3,4,5]

// 类数组
funciton Person(){
    // let args: number[] = arguments
    let args: {
        [index.name]:string;
        length:number;
        func:Function
    } = arguments
    // let args: IArguments = arguments
    interface IArguments {
        [index: number]: any;
        length: number;
        callee: Function;
    }
}


// 任意值 any 允许数组中出现任意类型
let list:any[] = ['hwl', 18, { website: 'http://hwl.com' }];
```

#### 函数类型

定义的两种方式

- 函数声明 
- 函数表达式
- 两者的区别 就是  函数表达式会给出一个变量 

函数声明 Function Declaration

```js
// js
function sum(x,y){
	return x + y;
}
// ts  
// c int sum (int a,int b){}
function sum(x:number,y:number):number{
    return x + y
}

sum(10,20)
sum(12)  // 输入多余的（或者少于要求的）参数，是不被允许的
sum(100,200,300)
```

函数表达式 Fucntion Expression

```tsx
// js
let sum = funciotn(x,y){
    return x + y; 
}

// es6 箭头函数
let pe = phone => console.log('vivo-z3') 
pe()

// ts  => 用来表示函数的定义，左边是输入类型，需要用括号括起来，右边是输出类型。

// (输入类型) => (输出类型)  


// ts
let mySum = function(x:number,y:number):number{
    return x + y
}
```

- ts 箭头函数
	- 箭头函数 Arrow function
	- 函数
		- 参数 几个
		- 返回值  有无

```js
let fun1 = () => 1 + 2 + 3;

let fun2 = () => { return 1+ 2+3 }
// :(变量:number) =>number  是函数类型

// 一个参数 （没有指定返回类型的时候，函数会自动推导）
let fun3:(data:number)=>number = (data:number)=> data * data;

// 一个参数 指定返回类型number
let fun4 = (num0:number) => { num0 * num0 }
let fun4 = (num0:number) => {return num0 * num0 }

// 两个参数 没有指定返回类型的时候，函数会自动推导）
let fun5 = (num1:number,num2:number) => { num1 * num2 }
let fun5 = (num1:number,num2:number) => { return num1 * num2 }

// 箭头函数的作用简化回调函数
[1,2,4].map(x => x * x)

let result = [1,8,4,6,9].sort(function(a,b){
    return a - b
})
let result =  [1,8,4,6,9].sort((a,b) => a - b)
```

参数

可选参数



参数默认值



剩余参数



重载





### 任意值 Any

- 用来表示允许赋值为任意类型

- 这种任意值类似javascript的赋值方法

任意值类型

- 如果是一个普通类型，在赋值过程中改变类型是不被允许的

```tsx
let name:string = 'hwl'
name = 100 // 报错
```

- 解决方法可以设置该类型为any类型，则允许被赋值为任意类型

```tsx
let name:any = 'hwl'
naem = 100 // 成功赋值
```

任意值的属性和方法

可以访问任何属性

```tsx
let thing:any = 'hello'
console.log(thing.myName)
console.log(thing.myName.firstName)
```

可以调用任何方法

```tsx
let thing:any = 'bag'
thing.setName('king')
thing.setName('queen')
thing.myName.setFirstName('Bing')
```

- **声明一个变量为任意值之后，对它的任何操作，返回的内容的类型都是任意值**

未声明类型的变量

- 超级重点

```tsx
let name;  // 等同于 let name:any
name = 'hwl'
name = 100
name.setName('liang')
```

### 类型推论

- Type Inference

- 在没有明确的指定类型的时候推测出一个类型，这就是类型推论
- 如果定义的时候没有赋值，不管之后有没有赋值，都会被推断成 `any` 类型而完全不被类型检查

```tsx
let name = 'king'; // let name:any = 'king'
name = 100 // 报错
```















## 编译选项

| 选项                           | 类型    | 默认值 | 描述                                                         |
| ------------------------------ | ------- | ------ | ------------------------------------------------------------ |
| `allowJs`                      | boolean | false  | 允许编译js文件                                               |
| `allowSyntheticDefaultImports` | boolean | false  | 允许对不包含默认导出的模块使用默认导入。这个选项不会影响生成的代码，只会影响类型检查。 |







## 运算符

运算符









## 语句

### 顺序





### 条件









### 循环

语法
```
for ( init; condition; increment ){
    statement(s);
}
```
for 循环
```tsx
var num: number = 5;
var i: number;
var factorial: number = 1;
for (i = num; i >= 1; i--) {
    factorial *= i;
}
```
for… in 循环
```tsx
var j: any;
var n: any = 'abc';
for (j in n) { 
    console.log(n[j]);
}
```
for…of 
```
for..of
```
forEach
```

```
every 
```

```
some 循环
```

```
while
```
while(condition)
{
   statement(s);
}
```
do..while
```

```
break 语句
```

```
continue 语句
```

```
无限循环
```

```


## 任意值



## 类型推论



## 类型断言

类型断言(Type Assertion)





## 声明文件



## 内置对象

内置对象是指根据标准在全局作用域（Global）上存在的对象。这里的标准是指 ECMAScript 和其他环境（比如 DOM）的标准。

- ECMAScript的内置对象
	- Array、String、Boolean、Error、Date、RegExp
- DOM和BOM的内置对象
	- Document 、HTMLElement 、Event、NodeList
- TypeScript核心库的定义文件

```tsx
let b: Boolean = new Boolean(1);
let e: Error = new Error('Error occurred');
let d: Date = new Date();
let r: RegExp = /[a-z]/;
let n: Number = new Number(100)
let s: String = new String()
```



## 静态类型

- Static Typing 静态类型 

```tsx
let count : number = 1;
count = 'str' // 报错
count = 100

interface Student{
    uname:string,
    age: number
}

const zhangsan: Student = {
    uname: '张三',
    age: 22
}

console.log(zhangsan.uname)
console.log(zhangsan.age)
```

基础静态类型

- number、string、null、undefinde、boolean、void、symbol

```tsx
const count: number = 100;
const name : string = 'Hello TypeScript'
// 对象类型
const obj:{
    name: string,
    age: number
} = {
    name: 'zhangsan',
    age：20 
}
// 数组类型
const obj : string [] = ['张三','李四','王五']
// 类类型
class Person{} // 类
const per1 : Person = new Person()
// 函数类型
const func : () => string =() => {return 'Hello TypeScript'}
```

类型注解和类型推断

- 类型注解 type annotation 

```tsx
let count = number;
count = 100; // 类型注解


```



- 类型推断 type inference 





### 字符串字面量类型



### 函数

函数参数和返回类型的注解





函数参数和返回类型的注解







数组类型注解的方法





元组的使用和类型









### Number

### String

### Array(数组)

### 元组

### 联合类型



### 枚举





## 面向对象

### 类





### 抽象类





### 对象





### 接口









### 构造函数和this





函数参数和返回值类型的注解







### 命名空间

### 模块

### 声明文件





### 继承





### 封装







### super关键字





### 泛型



### 声明和并





# 项目配置



