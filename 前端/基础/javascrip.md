---
title: 全网最全的JavaScript学习路线
categories:
  - 前端
tags:
  - 前端
  - JavaScript
abbrlink: 53226
---
# 基础知识

- 继承、原型链、this指向、设计模式、call, apply, bind,；
- new实现、防抖节流、let, var, const 区别、暂时性死区、event、loop；
- promise使用及实现、promise并行执行和顺序执行；
- async/await的优缺点；
- 闭包、垃圾回收和内存泄漏、数组方法、数组乱序, 数组扁平化、事件委托、事件监听、事件模型

> - [ ] [由浅入深，66条JavaScript面试知识点](https://juejin.cn/post/6844904200917221389#heading-89)
> - [ ] [JavaScript专题系列20篇正式完结！](https://juejin.cn/post/6844903506017517582)
> - [ ] [32个手写JS，巩固你的JS基础（面试高频）](https://juejin.cn/post/6875152247714480136#heading-0)
> - [ ] [从2.4万篇文章中挑出的最棒的 JavaScript 学习指南（2018版） - 知乎](https://zhuanlan.zhihu.com/p/33298555)
> - [ ] [JavaScript八张思维导图](https://juejin.cn/post/6844903556839899144)
> - [ ] [这一次，彻底弄懂 JavaScript 执行机制](https://juejin.cn/post/6844903512845860872)
> - [ ] [JavaScript八张思维导图](https://juejin.cn/post/6844903556839899144)
> - [ ] [从2.4万篇文章中挑出的最棒的 JavaScript 学习指南（2018版） - 知乎](https://zhuanlan.zhihu.com/p/33298555)
> - [ ] [JavaScript深入系列15篇正式完结！](https://juejin.cn/post/6844903479429824526)
> - [ ] [JavaScript教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1022910821149312)
> - [ ] [由浅入深，66条JavaScript面试知识点](https://juejin.cn/post/6844904200917221389)
> - [ ] [JavaScript专题系列20篇正式完结！](https://juejin.cn/post/6844903506017517582)
> - [ ] [从2.4万篇文章中挑出的最棒的 JavaScript 学习指南（2018版） - 知乎](https://zhuanlan.zhihu.com/p/33298555)
> - [ ] [JavaScript深入系列15篇正式完结！ · Issue #17 · mqyqingfeng/Blog](https://github.com/mqyqingfeng/Blog/issues/17)
> - [ ] [32个手写JS，巩固你的JS基础（面试高频）](https://juejin.cn/post/6875152247714480136)
> - [ ] [一个合格的中级前端工程师需要掌握的 28 个 JavaScript 技巧](https://juejin.cn/post/6844903856489365518)
> - [ ] [JavaScript八张思维导图](https://juejin.cn/post/6844903556839899144)
> - [ ] [这一次，彻底弄懂 JavaScript 执行机制](https://juejin.cn/post/6844903512845860872)
> - [ ] [stephentian/33-js-concepts: 每个 JavaScript 工程师都应懂的33个概念 @leonardomso](https://github.com/stephentian/33-js-concepts)
> - [ ] [字节跳动最爱考的前端面试题：JavaScript 基础](https://juejin.cn/post/6934500357091360781)
> - [ ] [JavaScript 工具函数大全（新）](https://juejin.cn/post/6844903966526930951)
> - [ ] [[译] 送你 43 道 JavaScript 面试题](https://juejin.cn/post/6844903869378461710)
> - [ ] [22 道高频 JavaScript 手写面试题及答案](https://juejin.cn/post/6844903911686406158)
> - [ ] [7道简单的 JavaScript 面试题，三个月没招到一个人](https://juejin.cn/post/6844903986231771143)
> - [ ] [【译】JavaScript 完整手册](https://juejin.cn/post/6844903727027978253#heading-94)
> - [ ] [JavaScript设计模式es6（23种)](https://juejin.cn/post/6844904032826294286)
> - [ ] [JavaScript 秘密花园](http://bonsaiden.github.io/JavaScript-Garden/zh/)

## 基础

> JavaScript = 基础 + 对象 + BOM + DOM + ES6
>
> - 内置的JavaScript 对象
> - 浏览器对象（BOM）brower object modle
> - DOM对象(DOM) document object modle
## 概念
1.  JavaSciprt是一种脚本语言，也是一种**弱类型的语言**
2.  JavaScript是一种运行在浏览器中的`解释型`的**编程语言**
3.  在Web世界里，只有JavaScript能跨平台、跨浏览器驱动网页，与用户交互（行为）、实现表单的验证、设置网页的动态效果
> **Javascript是脚本语言还是编程语言？**
>
> ==脚本语言==：脚本语言又被称为扩建的语言，或者动态语言，是一种编程语言，用来控制软件应用程序，脚本通常以文本（如[ASCII](https://baike.baidu.com/item/ASCII))保存，只在被调用时进行解释或编译。（解释器）
>
> ==编程语言==：编程语言（programming language）可以简单的理解为一种计算机和人都能识别的语言。一种计算机语言让程序员能够准确地定义计算机所需要使用的数据，并精确地定义在不同情况下所应当采取的行动。（编译器）
>
> 脚本语言只是编程语言这个概念的子集。它是编程语言的一种类型。
>
> 硬要说和脚本语言相对的概念，那应该是编译型语言。
>
> 简单地来说，编译型语言在经过编译之后就是机器可以直接运行的代码了。
>
> 但是脚本语言，或者说解释型语言很多时候不需要提前编译，而是在运行时被解释器即时翻译成机器可以理解的机器指令。
>
> 但是这样的概念并不是绝对的。
>
> 实际上像Java和C#这样的语言，编译器只会把源代码编译成一种中间语言，在运行时再被各自的虚拟机和运行时即时翻译成机器指令。
>
> ==标记语言==：HTML
### 历史
- 1995年，网景公司的Brendan Eich用10天设计出Javascript语言，与Java没有关系，只是为了提高知名度，才取名Javascript。
### 组成部分
 `ECMAScript(语法+基本对象) + DOM + BOM`
|         名称          |           内容           |
| :-------------------: | :----------------------: |
|  ECMAScript（核心）   | 描述语言的语法和基本对象 |
|   DOM(文档对象模型)   |    操作HTML document     |
| BOM（浏览器对象模型） |     操作浏览器window     |
ECMScript (标准)（ES6 2015）== JavaScript（商标）
1. Javascript是一个网景公司注册的商标，而**ECMAScript是一个语言标准**
2. ECMA组织 定制了JavaScript的语言标准 == ECMAScript标准
3. ECMAScript是一种语言标准，而JavaScript是网景公司对ECMAScript标准的一种实现，ECMAscript可以默认是Javascript

### 版本

（ES6 2015）
1. 2015.6 ,最新版ECMAScript 6标准（简称ES6）发布，所以，讲到JavaScript的版本，实际上就是说它实现了ECMAScript标准的哪个版本。
2. ES5、ES6、.....、ES10 、…..
> ECMAScript 6 也称为 ECMAScript 2015(ES6)。
>
> ECMAScript 7 也称为 ECMAScript 2016(ES7)。
>
> ES8  ES2017
>
> ES9 ES2018
>
> …
>
> ES12 ES2021
## 语法
### 语法规制
1. 每个语句以分号结尾 `;`（可以不用分号结尾，不强制要求）
2. 语句块以`{ } ` 包围
3. 字符串使用 `'单引号'或者 "双引号"`，多重嵌套可以"双引号加'' 单引号"进行区分
### 命名规则
[命名与注释规范详解 - 前端 ](https://juejin.im/entry/599d433cf265da24797b5c66)
### script标签

的位置与使用

可以在head里面，也可以放在body里面
1. 内联
```html
//可以在head内，也可以body内
<script></script>
```
2. 外联
```js
<script src="js文件"></script>
```
### 输入与输出

(提示框

#### 输入: `提示框`
```js
let input = prompt("请输入一个数字")
window.prompt("sometext(提示信息)","defaultvalue(默认值)") //提示框  
```
#### 输出：`四种方法 document.write() console.log() alert() innerHTML = " "`
```js
// 方法一
//将内容写入到HTML文档
document.write('hello world!!!');
//JavaScript：直接写入 HTML 输出流 && 不支持style
document.write('<h1>hello world!!!</h1>');
// 多次执行doucument,write() 时追加内容
//doucument,write() 内容为空时清空页面元素，但不清空document.write()写入的内容
//如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖。
//弹出警告框
document.write('<h1 style="color:red;text-align: center;">Message</h1>')
//可以自定义样式
// 方法二
window.alert()
alert('hello world!!!');
//控制台输出
// 方法三
console.log('hello world!!!');
// 方法四
//写入到HTML元素
element.innerHTML = ""
//插入标签和添加内容
element.innerText = ""
// js DOM操作 增、删、改、查、元素
doucument.getElementById("demo").innerHTML = "<h1 style="color:purple;font-size:30px">段落修改<h1>"; 
//修改内容
doucument.getElementById("demo").innerText = "段落修改";
```
### 变量

变量声明与提升的机理

- `var ES6变量(let)与常量(const)`

> [var、let、const三者的区别](https://www.cnblogs.com/zhuoshen/p/9577220.html)

1. let声明的变量只在let命令所在的代码块内有效（块级作用域）
2. const声明一个只读的常量，一旦声明，常量的值就不能改变
3. 全局变量（全局作用域）与函数内的局部变量（函数作用域）

字面量

- 都是一些不可改变的值
- 字面量都是可以直接使用，但是我们一般不会直接使用字面量

变量

- 变量是可以变化的数值，常量固定不变的数值
- 变量在JavaScript中就是用一个变量名表示，
- 变量名是大小写英文、数字、`$`和`_`的组合，且不能用数字开头。变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
- 变量名也不能是JavaScript的关键字，申明一个变量用`var`语句
- 大小写敏感
- 一条语句，可以使用多个变量
```js
var num = 值;
let num = 变量;
const num = 常量;
var x,y,z = 1; //x,y = undefinded z = 1
var x = 10,y,z = 20 
//经常会声明无值的变量。未使用值来声明的变量，其值实际上是undefined
var x;  // x = underfined
//重新声明Javascript的值，变量的值不会丢失
var x = 100;
var x;
console.log(x);
```
#### var && let&& const
##### const`并非真正的变量 数组或者对象的属性可以改变`
用于声明一个或多个常量，声明时必须进行初始化，且初始化后值不可再改变
`const`定义常量与使用`let` 定义的变量相似：
- 二者都是块级作用域
- 都不能和它所在作用域内的其他变量或函数拥有相同的名称，两者还有以下两点区别：
- `const`声明的常量必须初始化，而`let`声明的变量不用
- ==const 定义常量的值不能通过再赋值修改，也不能再次声明。而 let 定义的变量值可以修改==。
- const 的本质：const 定义的变量并非真正的常量，并非不可改变，它定义了一个常量引用一个值。
- 使用const定义的对象或者数组，其实是可变。代码不会报错
```js
// 创建常量对象
const car = {type:"Fiat", model:"500", color:"white"};
// 修改属性:
car.color = "red";
// 添加属性
car.owner = "Johnson";
```
不能对常量对象重新赋值
```js
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"];    // 错误
```
Internet Explorer 10 及更早版本的浏览器不支持 const 关键字。
#### 全局变量和局部变量
- var 在函数外声明的变量作用域是全局的
- 全局变量在 JavaScript 程序的任何地方都可以访问。
- 函数内使用 var 声明的变量只能在函数内容访问，如果不使用 var 则是全局变量。
- 在函数体内使用 **var** 和 **let** 关键字声明的变量有点类似。它们的作用域都是 **局部的**
- 在函数体外或代码块外使用 **var** 和 **let** 关键字声明的变量也有点类似。它们的作用域都是 **全局的**:
```js
// 使用 var
function myFunction() {
    var carName = "Volvo";   // 局部作用域
}
// 使用 let
function myFunction() {
    let carName = "Volvo";   //  局部作用域
}
// 使用 var
var x = 2;       // 全局作用域
// 使用 let
let x = 2;       // 全局作用域
```
#### 作用域

> [JS中的作用域和作用域链 ](https://www.cnblogs.com/leftJS/p/11067908.html)

- 全局作用域 和  局部作用域
- 函数作用域： function
- 块级作用域（Block Scope）: ES6可以使用let关键字来实现块级作用，let声明的变量只能在let命令所在的代码块{} 内有效，在{}之外不能访问

- 循环作用域

```js
var i = 5;
for (var i = 0; i < 10; i++) {
    // 一些代码...
}
// 这里输出 i 为 10
let i = 5;
for (let i = 0; i < 10; i++) {
    // 一些代码...
}
// 这里输出 i 为 5
```
- 词义作用域

####  HTML 代码中使用全局变量

- 在 JavaScript 中, 全局作用域是针对 JavaScript 环境。
- 在 HTML 中, 全局作用域是针对 window 对象。
- 使用 **var** 关键字声明的全局作用域变量属于 window 对象:

```js
var carName = "Volvo";
// 可以使用 window.carName 访问变量
// 使用 let 关键字声明的全局作用域变量不属于 window 对象:
let carName = "Volvo";
// 不能使用 window.carName 访问变量
```
#### 变量提升
- var关键字定义的变量可以在使用后声明，也就是变量可以先使用再声明
- const关键字定义的变量则不可以在使用后声明，也就是变量需要先声明再使用
- let关键字定义的变量则不可以在使用后声明，也就是变量需要先声明再使用。
### 语句标识符

(关键字)

JavaScript 语句通常以一个 **语句标识符** 为开始，并执行该语句。
语句标识符是保留关键字不能作为变量名使用。

标识符

- 在JS中所有可以自主命名都可以称为标识符
- 变量名 、函数名 、属性目标名都是标识符
- 标识符中可以含有字母、数字、_、$
- 不能以数字开头
- 标识符不能是ES中的关键字或保留字
- 标识符一般采用驼峰命名法 
	- 首字母小写，每个字母的开头字母大写，其余字母小写
- JS底层保存标识符时实际上采用的Unicode编码
	- 理论上讲，所有的utf-8中含有的内容都可以作为标识符

|     语句     |                             描述                             |
| :----------: | :----------------------------------------------------------: |
|    break     |                        用于跳出循环。                        |
|    catch     |      语句块，在 try 语句块执行出错时执行 catch 语句块。      |
|   continue   |                    跳过循环中的一个迭代。                    |
| do ... while |    执行一个语句块，在条件语句为 true 时继续执行该语句块。    |
|     for      |      在条件语句为 true 时，可以将代码块执行指定的次数。      |
|  for ... in  | 用于遍历数组或者对象的属性（对数组或者对象的属性进行循环操作）。 |
|   function   |                         定义一个函数                         |
| if ... else  |             用于基于不同的条件来执行不同的动作。             |
|    return    |                           退出函数                           |
|    switch    |             用于基于不同的条件来执行不同的动作。             |
|    throw     |                     抛出（生成）错误 。                      |
|     try      |              实现错误处理，与 catch 一同使用。               |
|     var      |                        声明一个变量。                        |
|    while     |              当条件语句为 true 时，执行语句块。              |
### 注释

```js
// 单行注释
/*
多行
注释
*/
```
### 运算符
### 语句 

- `三种语句 顺序/条件/循环`

#### 顺序语法
```js
var num = 100;
console.log(num)
```
#### 条件语句
```js
// 第一种
if(){
}
//第二种
if(){
}else{
}
//第三种
if(){
}else if(){       
}else{  
}
//第四种
switch(){
       case:  ;
       case:  ;
       case:  ; 
       default: ;
}
```
#### 循环语句
```js
for(){
}
while(){
}
do() 
while{
}
```
#### 代码块
```js
function myFunction(){
	//JavaScript 可以分批地组合起来。代码块的作用是一并地执行语句序列。
}
```
#### 三个关键字 `break \ continue \ return`

-  break : 跳出
-  continue：继续
- return：返回值

### 数据类型

基本数据类型和复杂数据类型使用

深入理解数据类型转换与检测

`6+3  (Number 、Boolean 、String 、Null 、Undefined 、Symbool) + (Array 、Object、Function)`

- Number、Boolean、String 
	- Null 、Undefined、Symbol 
- Array、Object、Function
---
> 值类型(基本类型)：
>
> - 字符串（String）、数字（Number）、布尔（Boolean）、
>
> - 对空（Null）、未定义（Undefined）、Symbool（独一无二的值）
>
> - 引用数据类型：对象（Object）、数组(Array)、函数（function）
>
>
> Symbol 是 ES6 引入了一种新的原始数据类型，表示独一无二的值。
> 计算机是可以做数学计算的机器，计算机程序可以处理各种数值，不止可以处理数值，文本，图形，音频，视频，网页等各种各样的数据，不同的数据，需要定义不同的数据类型。
- NaN 的数据类型是 number
- 数组(Array)的数据类型是 object
- 日期(Date)的数据类型为 object
- null 的数据类型是 object
- 未定义变量的数据类型为 undefined

#### 基本数据类型

- Number + Boolean + String + Null + Undefined + Symbool

##### Number 数字

---
- Javascript不区分整数和浮点数，统一用Number表示
- 特殊情况：
  - NaN   非数字
  - infiniry 无穷大
- 由于JavaScript这个设计缺陷，不要使用`==` 相等运算符比较，始终坚持使用`===`严格相等运算符 比较。 
- 科学计数法
```js
const y = 123e5; //12300000
const z = 123e-5; //0.00123
```
- 唯一能判断某个值是不是数字的方法是通过`isNaN()`函数：
```js
isNaN(NaN); // true
// NaN 非数字  是不是NaN（非数字）不是false 是true
isNaN(1000)  //false
```
##### String 字符串（类似数组）
---
> - length
> - toUpperCase() toLowerCase()
> - indexOf('指定字符串')
> - substring(索引区间)
- 存储和处理文本
- 字符串是以''单引号或""双引号括起来的任意文本
- 字符串是不可变的，通过索引赋值，没有错误，也没有效果、操作字符串
- 可以使用索引位置来访问字符串中的每个字符
- 字符串长度：字符串.length
- 获取字符串的某个指定位置的字符：类似Array的下标操作，索引值从0开始
- 大写：字符串`.toUpperCase()`
- 小写:   字符串`.toLowerCase()`
- 指定字符串出现的位置：字符串.indexOf('指定字符串')
- 返回指定索引区间的子串： 字符串.substring(索引区间)，只有一个为从这个索引开始到结束、你也可以在字符串添加转义字符来使用引号：
```js
var x = 'It\'s alright';
var y = "He is called \"Johnny\"";
```
##### Boolean布尔值
- true/false  1/0
##### null 空值 和undefined 未定义

- Undefined 表示变量不含有值
- 可以通过将变量的值设置为null来清空变量
###### 声明变量类型
可以使用关键字“new”来声明其类型；
```js
var carname = new String;
var x =      new Number;
var y =      new Boolean;
var cars =   new Array;
var person = new Object;
```
> JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。
#### 引用数据类型 

- Object、Array、Function

---
##### 数组 [ ]

- 可以存储任意类型的数据类型，通过索引来访问每个元素。
##### 对象 { } 对象属性 和 对象方法()

- JavaScript对象是拥有`属性和方法`的数据
	- 属性没有括号
	- 方法有括号
- Javascript的对象是一组由键-值组成的无序集合（相当于map）键值对通常写法为 **name : value** (键与值以冒号分割)。键值对在 JavaScript 对象通常称为 **对象属性**。

```js
var person = {firstname:'John',lastname:'Doe',id:5566};
var person = {
    name: 'Bob',
    age: 20,
    tags: ['js', 'web', 'mobile'],
    city: 'Beijing',
    hasCar: true,
    zipcode: null
};
// 访问对象属性
// 使用的方法
name = person.lastname;
// 重点
name = person.tags[0]; 
访问对象方法
// 方法一
methodName : function(){ code lines }
// 方法二
objectName.methodName()
```
- 键都是字符串类型，值可以是任意数据类型。
- 使用：获取一个对象的属性，用`对象变量.属性名`的方式
- 语法注意： = 号 	,号 最后一个是没有逗号的，末尾；号
- 对象中的数组可以使用`对象变量.属性名[数字下标]`的方式
- 对象的方法定义了一个函数，并作为对象的属性存储。对象方法通过添加 () 调用 (作为一个函数)。
###### Javascript变量的生存期

- JavaScript 变量的生命期从它们被声明的时间开始。
- 局部变量会在函数运行以后被删除。
- 全局变量会在页面关闭后被删除。

###### 向未声明的 JavaScript 变量分配值

如果您把值赋给尚未声明的变量，该变量将被自动作为 window 的一个属性。该属性可以删除 如 carname="Volvo";

将声明 window 的一个属性 carname。

非严格模式下给未声明变量赋值创建的全局变量，是全局对象的可配置属性，可以删除。

```js
var var1 = 1; // 不可配置全局属性
var2 = 2; // 没有使用 var 声明，可配置全局属性
console.log(this.var1); // 1
console.log(window.var1); // 1
delete var1; // false 无法删除
console.log(var1); //1
delete var2; 
console.log(delete var2); // true
console.log(var2); // 已经删除 报错变量未定义
```
typeof、null、underfined、valueOf()

typeof()操作符 

你可以使用typeof操作符来检测变量的数据类型

在JavaScript中，``数组是一种特殊的对象类型``。 因此 typeof [1,2,3,4] 返回 object。

```js
typeof([]) //object
```
数组是Object类型
null `什么都没有 Object 类型`
null是一个只有一个值的特殊类型。表示一个空对象引用。
清空对象的两种方法

```js
var person = null;// 值为null 空，但类型为对象
var person = underfined; //值为undefined 类型为underfined
```
undefined 一个没有设置值的变量
在 JavaScript 中, **undefined** 是一个没有设置值的变量。
**typeof** 一个没有值的变量会返回 **undefined**。
undefined和null的区别 

- null和undefined的值相等，但类型不等 null的类型是object

```js
typeof undefined  //undefined
typeof null //object
null === undefined false
null == undefined // true
```
### 类型转换
- Number() 转换为数字，
- string()转换为字符串，
- Boolean转为布尔值。
#### constructor属性
constructor属性返回所有JavaScript变量的构造函数
```js
"John".constructor                 // 返回函数 String()  { [native code] }
(3.14).constructor                 // 返回函数 Number()  { [native code] }
false.constructor                  // 返回函数 Boolean() { [native code] }
[1,2,3,4].constructor              // 返回函数 Array()   { [native code] }
{name:'John', age:34}.constructor  // 返回函数 Object()  { [native code] }
new Date().constructor             // 返回函数 Date()    { [native code] }
function () {}.constructor         // 返回函数 Function(){ [native code] }
```
#### 类型装换

JavaScript变量可以转换为新变量或其他数据类型：

##### 转字符串 string()

全局方法 **String()** 可以将数字转换为字符串。
该方法可用于任何类型的数字，字母，变量，表达式：

Number 方法 **toString()** 也是有同样的效果。

| 方法            | 描述                                                 |
| :-------------- | :--------------------------------------------------- |
| toExponential() | 把对象的值转换为指数计数法。                         |
| toFixed()       | 把数字转换为字符串，结果的小数点后有指定位数的数字。 |
| toPrecision()   | 把数字格式化为指定的长度。                           |
| toString()      |                                                      |
| String()        |                                                      |
```js
var d = (12312).toExponential() //1.2312e+4" 指数计数法
var d = (12312).toFixed(3) //"12312.000" 小数点后面的数字
var d = (12312).toPrecision(2) //"1.2e+4" 保留的数字数量
var str = (123123).toString()
typeof str 
String(123)
```
##### js字符与ASCII码互转

> [ASCII编码对照表_911查询](http://ascii.911cha.com/)

- charCodeAt()  字符串 ==> ASCII码
- String.fromCharCode() 字符串 <==  ASCII码
- `from CharCode At`
- 大写字母A-Z对应的ASCII码值是65-90
- 小写字母a-z对应的ASCII码值是97-122
```js
// 将字母转为ascii嘛的方法：
var str = "A";
str.charCodeAt();  // 65
var str1 = 'a';
str1.charCodeAt();  // 97
// 将ascii码转为对应字母的方法：
var num = 97;
String.fromCharCode(num);  // 'a'
var num1 = 100;
String.fromCharCode(num1);  // 'd'
```
##### 字符串=>数字

全局方法 **Number()** 可以将字符串转换为数字。
字符串包含数字(如 "3.14") 转换为数字 (如 3.14).
空字符串转换为 0。
其他的字符串会转换为 NaN (不是个数字)。

| 方法         | 描述                               |
| :----------- | :--------------------------------- |
| parseFloat() | 解析一个字符串，并返回一个浮点数。 |
| parseInt()   | 解析一个字符串，并返回一个整数。   |
```js
var str = '123.456'
Number(str);
var x = parseFloat(str); //123.456
va y = parseInt(str) //123
```
##### 转字符串

全局方法 **String()** 可以将布尔值转换为字符串。
全局方法 **String()** 可以将布尔值转换为字符串。

```js
String(false)  //"false"
false.toString() //"false"
```
##### 转数字

全局方法 **Number()** 可将布尔值转换为数字。

```js
Number(false)  //0
Number(true)  //1
```
日期=>字符串
Date() 返回字符串。
全局方法 String() 可以将日期对象转换为字符串。
Date 方法 **toString()** 也有相同的效果。
| 方法                       | 描述                                        |
| :------------------------- | :------------------------------------------ |
| getDate()                  | 从 Date 对象返回一个月中的某一天 (1 ~ 31)。 |
| getFullYear() 年           | 从 Date 对象以四位数字返回年份。            |
| getMonth() 月              | 从 Date 对象返回月份 (0 ~ 11)。             |
| getDay() 日                | 从 Date 对象返回一周中的某一天 (0 ~ 6)。    |
| getHours() 时              | 返回 Date 对象的小时 (0 ~ 23)。             |
| getMinutes() 分            | 返回 Date 对象的分钟 (0 ~ 59)。             |
| getSeconds() 秒            | 返回 Date 对象的秒数 (0 ~ 59)。             |
| getMilliseconds() （毫秒） | 返回 Date 对象的毫秒(0 ~ 999)。             |
| getTime()                  | 返回 1970 年 1 月 1 日至今的毫秒数。        |
##### 日期=>数字

全局方法 **Number()** 可将日期转换为数字。
日期方法 **getTime()** 也有相同的效果。

```js
dTime = new Date();
Number(dTime);
dTime = new Date();
dTime.getTime();
// 月份+1
// FullYear(年) Month(月 + 1) Day(日) Hours(时) Minutes(分) Seconds(秒) MillSeconds（毫秒）
// getDate()、getTime()
console.log(dTime.getFullYear)
```
##### 自动转换类型

当 JavaScript 尝试操作一个 "错误" 的数据类型时，会自动转换为 "正确" 的数据类型。

```js
5 + null    // 返回 5         null 转换为 0
"5" + null  // 返回"5null"   null 转换为 "null"
"5" + 1     // 返回 "51"      1 转换为 "1" 
"5" - 1     // 返回 4         "5" 转换为 5
```
##### 自动转换为字符串

当你尝试输出一个对象或一个变量时 JavaScript 会自动调用变量的 toString() 方法：

| 原始值              | 转换为数字 | 转换为字符串      | 转换为布尔值 |
| :------------------ | :--------- | :---------------- | :----------- |
| false               | 0          | "false"           | false        |
| true                | 1          | "true"            | true         |
| 0                   | 0          | "0"               | false        |
| 1                   | 1          | "1"               | true         |
| "0"                 | 0          | "0"               | true         |
| "000"               | 0          | "000"             | true         |
| "1"                 | 1          | "1"               | true         |
| NaN                 | NaN        | "NaN"             | false        |
| Infinity            | Infinity   | "Infinity"        | true         |
| -Infinity           | -Infinity  | "-Infinity"       | true         |
| ""                  | 0          | ""                | false        |
| "20"                | 20         | "20"              | true         |
| "Runoob"            | NaN        | "Runoob"          | true         |
| [ ]                 | 0          | ""                | true         |
| [20]                | 20         | "20"              | true         |
| [10,20]             | NaN        | "10,20"           | true         |
| ["Runoob"]          | NaN        | "Runoob"          | true         |
| ["Runoob","Google"] | NaN        | "Runoob,Google"   | true         |
| function(){}        | NaN        | "function(){}"    | true         |
| { }                 | NaN        | "[object Object]" | true         |
| null                | 0          | "null"            | false        |
| undefined           | NaN        | "undefined"       | false        |
#### 一元运算符 +

**Operator +** 可用于将变量转换为数字：
如果变量不能转换，它仍然会是一个数字，但值为 NaN (不是一个数字):

### 保留关键字

Javascript 的保留关键字不可以用作变量、标签或者函数名。有些保留关键字是作为 Javascript 以后扩展使用。
| abstract | arguments | boolean    | break     | byte         |
| -------- | --------- | ---------- | --------- | ------------ |
| case     | catch     | char       | class*    | const        |
| continue | debugger  | default    | delete    | do           |
| double   | else      | enum*      | eval      | export*      |
| extends* | false     | final      | finally   | float        |
| for      | function  | goto       | if        | implements   |
| import*  | in        | instanceof | int       | interface    |
| let      | long      | native     | new       | null         |
| package  | private   | protected  | public    | return       |
| short    | static    | super*     | switch    | synchronized |
| this     | throw     | throws     | transient | true         |
| try      | typeof    | var        | void      | volatile     |
| while    | with      | yield      |           |              |
\* 标记的关键字是 ECMAScript5 中新添加的。

### 对象、属性和方法

对象 Object 引用数据类型

- 基本数据类型 Number Boolean Underfined Null  String 单一的值
	- 值和值之间没有任何联系 
- 对象属于一种复合的数据类型，在对象中可以保存多种不同的数据类型的属性
- 

对象的分类

- 内建对象 Math String Number Boolean Function Object 
- 宿主对象
	- JS的运行环境提供的对象，目前来讲主要指由浏览器提供的对象
	- BOM DOM 
- 自定义对象
	- 开发人员自已创建的对象



```js
// 创建一个对象
var obj = new Object(); 

var obj = {
    name : "hwl",
    age: '22'
}

cosole.log(typeof obj) // Object 

// 在对象中保存的值称为属性
// 向对象添加属性
// 语法 对象.属性名 = 属性值
obj.name = 'heweiliiang'
obj.age = 18
obj.ssex = '男'

// 读取对象中的属性
// 语法：对象.属性名
console.log(obj.age + obj.ssex)

// 修改对象的属性值
// 语法,对象.属性名 = 新值
obj.name = 'newhwl'

// new 关键字调用的函数，是构造函数 constructor
// 构造函数是专门用来创建对象的函数

// 删除对象属性
delete obj.name

// 如果要使用特殊的属性名，不能采用 . 的方式来操作
// 需要使用另一种方式
// 语法 对象[“属性名”] = 属性值
// 读取时也需要采用这种方式

// 使用[] 这种形式 去操作属性,更加的灵活
// 在[]中可以直接传递一个变量 ,这样变量值是多少就会选取那个属性

obj['123'] = 789
obj['msg'] = 'msg'
console.log(obj['msg'])

obj['num'] = '1000'
var newNum = num
consoe.log(obj[newNum])

// 属性值
// JS对象的属性值，可以是任意的数据类型
obj.type = true;
console.log(obj.type)

var obj2 = new Object();
obj.test = obj2 //

// in 运算符
通过该运算符可以检查一个对象中是否含有指定的属性
如果有则返回true 没有则返回false
语法
属性名 in 对象
console.log('name4' in obj)

// 
obj.tellName = function(){
    
};
// console.log(obj.tellName)
obj.sayName();

// 函数也可以称为对象的属性 如果一个函数作为一个对象的属性保存 那么我们称这个函数是这个对象的方法 调用函数就说调用对象的方法


var obj3 = {
    name: 'king',
    age: 100,
    sayName:function(){
        console.log(obj3.name)
    }
}

obj3.sayName()

// 枚举对象里面的属性 for ... in语句

for(var 变量 in 对象){
    
}

for(var n in obj){
    console.log(n)
    console.log)(obj[n])
}
```

Unicode编码表

```js
console.log('\u2620')
// 在网页中使用Unicode编码 
// $#编码 编码使用的是10进制
// \u2620 (16进制) ==> 10进制 9760
<h1>$#9760;</h1>
```

代码块

```js
{
	// 代码块 使用{ }来分组 
    alert('Hello Statement')
    console.log('Hello Statement')
    prompt('Hello Statement')
}

console.log('This is a message!!!')
```

基本数据类型 vs 引用数据类型

- 基本数据类型
- 引用数据类型

立即执行函数

```
(function(num1,num2){
	sum = num1 + num2
	alert('Message')
})(100,200);
```





全局作用域  scope

- 作用域指一个变量的作用范围

```

```

函数作用域



debug  排错; 调试; 除错

打断点 程序在小断点处停止

定位错误位置 在断点处停止 不往下执行 

在哪一行停止，就是还没有执行要执行







this



使用工厂方法创建对象

- 使用工厂方法创建的对象，使用的构造函数都是Object 
- 所以创建的对象都是Object这个类型
- 就导致我们无法区分多种不同类型的对象

```js
var obj = {
	name:'hwl',
    age:20,
    hobby:function(){
        console.log(this.name)
    }
}

obj.hobby()

var obj = [{},{},{}]

// 工厂方法创建对象
funciton createPerson(name,age){
    // 创建一个新的对象
    var obj = new Object();
    obj.name = name
    obj.age =  age
    obj.hobby = function(){
        console.log(this.name)
    }    
    // 将新的对象返回
    return obj;   
}

var obj2 = createPerson('hwl','21');
var obj3 = createPerson('hwl','25');
var obj4 = createPerson('hwl','26');


var name = 'hwl'
function yourName(name){
    var name =  // name = 1000
    // name 是 函数内部的值 this.name 是  全局变量的值
    this.name = name  // this.name == window.name = ‘hwl’
}

yourName(1000)
```

构造函数

```
this的情况 
当以函数的形式调用，this是window
当以方法的形式调用时，谁调用方法this 就是谁
当以构造函数的形式调用时，this就是新创建的那个对象
```

原型对象

- 创建的每一个函数，解析器就先函数添加一个属性prototype
- 这个属性对应着一个对象，这个对象就是我们所谓的原型对象

```js
function Person(){

}

console.log(Person.prototype)
```



垃圾回收（GC）





call apply



arguments





包装类



类

```
class 
```







您也应该避免使用 JavaScript 内置的对象、属性和方法的名称作为 Javascript 的变量或函数名：
| Array     | Date     | eval     | function      | hasOwnProperty |
| --------- | -------- | -------- | ------------- | -------------- |
| Infinity  | isFinite | isNaN    | isPrototypeOf | length         |
| Math      | NaN      | name     | Number        | Object         |
| prototype | String   | toString | undefined     | valueOf        |
### Windows 保留关键字
JavaScript 可以在 HTML 外部使用。它可在许多其他应用程序中作为编程语言使用。
在 HTML 中，您必须（为了可移植性，您也应该这么做）避免使用 HTML 和 Windows 对象和属性的名称作为 Javascript 的变量及函数名：
| alert          | all                | anchor      | anchors            | area               |
| -------------- | ------------------ | ----------- | ------------------ | ------------------ |
| assign         | blur               | button      | checkbox           | clearInterval      |
| clearTimeout   | clientInformation  | close       | closed             | confirm            |
| constructor    | crypto             | decodeURI   | decodeURIComponent | defaultStatus      |
| document       | element            | elements    | embed              | embeds             |
| encodeURI      | encodeURIComponent | escape      | event              | fileUpload         |
| focus          | form               | forms       | frame              | innerHeight        |
| innerWidth     | layer              | layers      | link               | location           |
| mimeTypes      | navigate           | navigator   | frames             | frameRate          |
| hidden         | history            | image       | images             | offscreenBuffering |
| open           | opener             | option      | outerHeight        | outerWidth         |
| packages       | pageXOffset        | pageYOffset | parent             | parseFloat         |
| parseInt       | password           | pkcs11      | plugin             | prompt             |
| propertyIsEnum | radio              | reset       | screenX            | screenY            |
| scroll         | secure             | select      | self               | setInterval        |
| setTimeout     | status             | submit      | taint              | text               |
| textarea       | top                | unescape    | untaint            | window             |
### HTML 事件句柄
除此之外，您还应该避免使用 HTML 事件句柄的名称作为 Javascript 的变量及函数名。
实例：
| onblur    | onclick    | onerror     | onfocus     |
| --------- | ---------- | ----------- | ----------- |
| onkeydown | onkeypress | onkeyup     | onmouseover |
| onload    | onmouseup  | onmousedown | onsubmit    |
|           |            |             |             |
### 非标准 JavaScript

除了保留关键字，在 JavaScript 实现中也有一些非标准的关键字。
一个实例是 **const** 关键字，用于定义变量。 一些 JavaScript 引擎把 const 当作 var 的同义词。另一些引擎则把 const 当作只读变量的定义。
Const 是 JavaScript 的扩展。JavaScript 引擎支持它用在 Firefox 和 Chrome 中。但是它并不是 JavaScript 标准 ES3 或 ES5 的组成部分。**建议：不要使用它**。
this
#### JavaScript this 关键字
面向对象语言中 this 表示当前对象的一个引用。
但在 JavaScript 中 this 不是固定不变的，它会随着执行环境的改变而改变。
- 在方法中，this 表示该方法所属的对象。
- 如果单独使用，this 表示全局对象。
- 在函数中，this 表示全局对象。
- 在函数中，在严格模式下，this 是未定义的(undefined)。
- 在事件中，this 表示接收事件的元素。
- 类似 call() 和 apply() 方法可以将 this 引用到任何对象。
var person = {  firstName: "John",  lastName : "Doe",  id       : 5566,  fullName : function() {    return this.firstName + " " + this.lastName;  } };
------
### 方法中的 this
在对象方法中， this 指向调用它所在方法的对象。
在上面一个实例中，this 表示 person 对象。
fullName 方法所属的对象就是 person。

fullName : function() {  return this.firstName + " " + this.lastName; }

### 单独使用 this
单独使用 this，则它指向全局(Global)对象。
在浏览器中，window 就是该全局对象为 [**object Window**]:
var x = this;
严格模式下，如果单独使用，this 也是指向全局(Global)对象。

解析器在调用函数每次都会向函数内部传递一个隐含的参数

这个隐含的参数就是this,this 是指向的是一个对象

这个对象我们称为函数执行的上下文对象

根据函数调用方式的不同，this会指向不同的对象

- 以函数的形式调用时，this永远都是widow
- 以方法的形式调用时，this就是调用方法的那个对象

```js
var name = '你的名字'

function fun(a,b){
	console.log(this)	// 指window上的属性
    console.log(this.name)  // window.name 
}
fun() // window.fun() 
// 你的名字

var obj = {
    name:'hwl',
    age: 20,
    sayName: fun
};
console.log(obj)
obj.sayName() // this就是调用方法的对象 obj 


function fun(){
    console.log(this.name) // obj2.name  obj3.name  调用者的不同动态变化
}

var obj2 = {
    name:'obj2',
    sayName:fun 
}

var obj3 = {
     name:'obj3',
     sayName:fun
}

obj2.sayName() // obj2
obj3.sayName() // obj3
```



## 数据类型

### 引用类型

Object









## 作用域、变量和内存问题

全局作用域 和 函数作用域



词法作用域 和 







基本类型和引用类型的值



执行环节及作用域



垃圾收集











## 面向对象

1. 学习this规则与使用
2. 2、掌握构造函数概念以及创建、调用与使用
3. 3、理解原型和原型链的关系与运用
4. 4、闭包和作用域应用
5. 5、熟练使用面向对象思想进行DOM编程
6. 6、掌握JS模块化编程方式，编写高质量代码
7. 7、掌握模块化开发技巧，解决企业级编程协同问题

理解对象





创建对象





继承









## 事件

https://www.jianshu.com/p/2f226461712a
键盘事件
鼠标事件
单击事件
DOM事件
什么是事件
事件就是文档或浏览器中发生的一些特定的交互瞬间。
两种事件
HTML事件
直接在HTML元素标签内添加事件，执行脚本
语法：<tag 事件>
DOM0级事件
js事件
判断鼠标的点击相互转换：
方法一：判断
事件绑定的几种方法
方法一

```js
 var inp = document.getElementsByTagName('input')[0];
     inp.onclick = myClick;
     function myClick() {
        alert('你点击了按钮');
      }
	//document.getElementById('XX').onclick=function(){};
```

方法二

```js
 inp.onclick = function myClick() {
      alert('你点击了按钮');
     }
```

方法三



事件流



事件处理程序



事件对象







## 严格模式

"use strict"; var x = this;

### 函数中使用 this（默认）
在函数中，函数的所属者默认绑定到 this 上。
在浏览器中，window 就是该全局对象为 [**object Window**]:

function myFunction() {  return this; }

### 函数中使用 this（严格模式）
严格模式下函数是没有绑定到 this 上，这时候 this 是 **undefined**。

"use strict"; function myFunction() {  return this; }

### 事件中的 this
在 HTML 事件句柄中，this 指向了接收事件的 HTML 元素：

### 对象方法中绑定
下面实例中，this 是 person 对象，person 对象是函数的所有者：
```
var person = {  firstName  : "John",  lastName   : "Doe",  id         : 5566,  myFunction : function() {    return this;  } };
var person = {  firstName: "John",  lastName : "Doe",  id       : 5566,  fullName : function() {    return this.firstName + " " + this.lastName;  } };
```
说明: **this.firstName** 表示 **this** (person) 对象的 **firstName** 属性。

### 显式函数绑定
在 JavaScript 中函数也是对象，对象则有方法，apply 和 call 就是函数对象的方法。这两个方法异常强大，他们允许切换函数执行的上下文环境（context），即 this 绑定的对象。
在下面实例中，当我们使用 person2 作为参数来调用 person1.fullName 方法时, **this** 将指向 person2, 即便它是 person1 的方法：
var person1 = {  fullName: function() {    return this.firstName + " " + this.lastName;  } } var person2 = {  firstName:"John",  lastName: "Doe", } person1.fullName.call(person2);  // 返回 "John Doe"
### 错误 throw try catch
#### try语句测试代码块的错误。
catch语句处理错误
throw语句创建自定义错误
finally语句在try和catch语句之后，无论是否触发异常，该语句都会执行。
JavaScript 错误
当 JavaScript 引擎执行 JavaScript 代码时，会发生各种错误。
可能是语法错误，通常是程序员造成的编码错误或错别字。
可能是拼写错误或语言中缺少的功能（可能由于浏览器差异）。
可能是由于来自服务器或用户的错误输出而导致的错误。
当然，也可能是由于许多其他不可预知的因素。
JavaScript 抛出（throw）错误
当错误发生时，当事情出问题时，JavaScript 引擎通常会停止，并生成一个错误消息。
描述这种情况的技术术语是：JavaScript 将抛出一个错误。
#### JavaScript try 和 catch
try 语句允许我们定义在执行时进行错误测试的代码块。
catch 语句允许我们定义当 try 代码块发生错误时，所执行的代码块。
JavaScript 语句 try 和 catch 是成对出现的。
```
try {
    ...    //异常的抛出
} catch(e) {
    ...    //异常的捕获与处理
} finally {
    ...    //结束处理
}
```
#### finally 语句
finally 语句不论之前的 try 和 catch 中是否产生异常都会执行该代码块。
#### Throw 语句
throw 语句允许我们创建自定义错误。
正确的技术术语是：创建或**抛出异常**（exception）。
如果把 throw 与 try 和 catch 一起使用，那么您能够控制程序流，并生成自定义的错误消息。
```
throw exception
```
异常可以是 JavaScript 字符串、数字、逻辑值或对象。
### 调试
JavaSript调试工具
在程序代码中寻找错误叫做代码调试。
调试很难，但幸运的是，很多浏览器都内置了调试工具。
内置的调试工具可以开始或关闭，严重的错误信息会发送给用户。
有了调试工具，我们就可以设置断点 (代码停止执行的位置), 且可以在代码执行时检测变量。
浏览器启用调试工具一般是按下 F12 键，并在调试菜单中选择 "Console" 。
设置断点
在调试窗口中，你可以设置 JavaScript 代码的断点。
在每个断点上，都会停止执行 JavaScript 代码，以便于我们检查 JavaScript 变量的值。
在检查完毕后，可以重新执行代码（如播放按钮）
debugger 关键字
debugger 关键字用于停止执行 JavaScript，并调用调试函数。
这个关键字与在调试工具中设置断点的效果是一样的。
如果没有调试可用，debugger 语句将无法工作。
开启 debugger ，代码在第三行前停止执行。
主要浏览器的调试工具
Chrome 浏览器 f12 浏览器
变量提升（hoisting）  `定义 var a; 初始化 var a = 100`
变量提升的是var y 定义
JavaScript 中，函数及变量的声明都将被提升到函数的最顶部。
JavaScript 中，变量可以在使用后声明，也就是变量可以先使用再声明。
变量提升：函数声明和变量声明总是会被解释器悄悄地被"提升"到方法体的最顶部。
JavaScript 初始化不会提升
JavaScript 只有声明的变量会提升，初始化的不会。
变量声明 (var y) 提升了，但是初始化(y = 7) 并不会提升，所以 y 变量是一个未定义的变量。
在头部声明你的变量
对于大多数程序员来说并不知道 JavaScript 变量提升。
如果程序员不能很好的理解变量提升，他们写的程序就容易出现一些问题。
为了避免这些问题，通常我们在每个作用域开始前声明这些变量，这也是正常的 JavaScript 解析步骤，易于我们理解。
JavaScript 严格模式(strict mode)不允许使用未声明的变量。
在下一个章节中我们将会学习到 "严格模式(strict mode)" 
### 严格模式
##### strict模式（严格模式）
JavaScript在设计之初，为了方便初学者学习，并不强制要求用`var`申明变量。这个设计错误带来了严重的后果：如果一个变量没有通过`var`申明就被使用，那么该变量就自动被申明为全局变量：在同一个页面的不同的JavaScript文件中。
如果都不用`var`申明，恰好都使用了变量`i`，将造成变量`i`互相影响，产生难以调试的错误结果。
使用`var`申明的变量则不是全局变量，它的范围被限制在该变量被申明的函数体内（函数的概念将稍后讲解），同名变量在不同的函数体内互不冲突。
ECMA在后续的版本中推出strict模式
使用方法：

```js
'use strict';
```
JavaScript 严格模式（strict mode）即在严格的条件下运行。
"use strict" 指令在 JavaScript 1.8.5 (ECMAScript5) 中新增。
它不是一条语句，但是是一个字面量表达式，在 JavaScript 旧版本中会被忽略。
"use strict" 的目的是指定代码在严格条件下执行。
`严格模式下你不能使用未声明的变量。`
为什么使用严格模式:
- 消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为;
- 消除代码运行的一些不安全之处，保证代码运行的安全；
- 提高编译器效率，增加运行速度；
- 为未来新版本的Javascript做好铺垫。
"严格模式"体现了Javascript更合理、更安全、更严谨的发展方向，包括IE 10在内的主流浏览器，都已经支持它，许多大项目已经开始全面拥抱它。
另一方面，同样的代码，在"严格模式"中，可能会有不一样的运行结果；一些在"正常模式"下可以运行的语句，在"严格模式"下将不能运行。掌握这些内容，有助于更细致深入地理解Javascript，让你变成一个更好的程序员。
不允许使用未声明的变量：
 对象也是一个变量。
不允许删除变量或对象。
不允许变量重名:
不允许使用八进制:
不允许使用转义字符:
不允许对只读属性赋值:
不允许对只读属性赋值:
不允许对一个使用getter方法读取的属性进行赋值
不允许删除一个不允许删除的属性：
变量名不能使用 "eval" 字符串:
变量名不能使用 "arguments" 字符串:
不允许使用以下这种语句:
由于一些安全原因，在作用域 eval() 创建的变量不能被调用：
禁止this关键字指向全局对象。
保留关键字
为了向将来Javascript的新版本过渡，严格模式新增了一些保留关键字：
- implements
- interface
- let
- package
- private
- protected
- public
- static
- yield
 "use strict" 指令只允许出现在脚本或函数的开头
### 使用误区
赋值运算符应用错误
在 JavaScript 程序中如果你在 if 条件语句中使用赋值运算符的等号 (=) 将会产生一个错误结果, 正确的方法是使用比较运算符的两个等号 (==)。
比较运算符常见错误
在常规的比较中，数据类型是被忽略的，以下 if 条件语句返回 true：
在严格的比较运算中，=== 为恒等计算符，同时检查表达式的值与类型，以下 if 条件语句返回 false：
加法与连接注意事项
加法是两个数字相加。
连接是两个字符串连接。
JavaScript 的加法和连接都使用 + 运算符。
接下来我们可以通过实例查看两个数字相加及数字与字符串连接的区别：
浮点型数据使用注意事项
JavaScript 中的所有数据都是以 64 位浮点型数据(float) 来存储。
所有的编程语言，包括 JavaScript，对浮点型数据的精确度都很难确定：
```js
var x = 0.1;
var y = 0.2;
var z = x + y            // z 的结果为 0.30000000000000004
if (z == 0.3)            // 返回 false
// 为解决以上问题，可以用整数的乘除法来解决：
var z = (x * 10 + y * 10) / 10;       // z 的结果为 0.3
```
JavaScript 字符串分行
JavaScript 允许我们在字符串中使用断行语句:
```js
var x =
"Hello World!";
var x = "Hello
World!";
```
但是，在字符串中直接使用回车换行是会报错的：
return 语句使用注意事项
JavaScript 默认是在代码的最后一行自动结束。
数组中使用名字来索引
许多程序语言都允许使用名字来作为数组的索引。
使用名字来作为索引的数组称为关联数组(或哈希)。
JavaScript 不支持使用名字来索引数组，只允许使用数字索引。
在 JavaScript 中, 对象 使用 名字作为索引。
如果你使用名字作为索引，当访问数组时，JavaScript 会把数组重新定义为标准对象。
执行这样操作后，数组的方法及属性将不能再使用，否则会产生错误:
实例
Undefined 不是 Null
在 JavaScript 中, null 用于对象, undefined 用于变量，属性和方法。
对象只有被定义才有可能为 null，否则为 undefined。
如果我们想测试对象是否存在，在对象还没定义时将会抛出一个错误。
错误的使用方式：
```js
if (myObj !== null && typeof myObj !== "undefined") 
正确的方式是我们需要先使用 typeof 来检测对象是否已定义：
if (typeof myObj !== "undefined" && myObj !== null) 
```
程序块作用域
在每个代码块中 JavaScript 不会创建一个新的作用域，一般各个代码块的作用域都是全局的。
以下代码的的变量 i 返回 10，而不是 undefined：
```js
for (var i = 0; i < 10; i++) {
    // some code
}
return i;
```
## 函数

函数基础与函数高级应用

掌握函数封装，提升编码质量

参数



重载

### 函数表达式

递归









`定义、参数、调用、闭包`

### 函数 function

函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块
```js
带参数
function functionname(val1,val2){
	代码
}
functionname(argument1,argument2);
带返回值
function functionname(val1,val2){
	const x = 5;
    return x;
}
```
### 定义 `构造函数、匿名函数、自调用函数、函数提升、ES6箭头函数`
JavaScript使用关键字function定义函数
```js
function functionName(parameters){
	函数体;
	return ;
}
```
#### 函数可以为一个值使用
#### 构造函数 `不常使用构造函数，避免使用关键字new`
通过内置的JavaScript函数构造器（Function()）定义
```js
var myFunction = new Function("a","b","return a + b");
var x = myFunction(8,9);
```
#### 匿名函数
函数没有名称，函数存储在变量中，不需要函数名称，通常通过变量名来调用。
```js
var z = function(a,b){
	return a * b;
}
var z = x(10,9);
console.log(z)
```
#### 函数提升(Hoisting) `使用表达式定义函数时无法提升`
提升（Hoisting）是JavaScript默认将当前作用域提升到前面去的行为
提升（Hoisting）应用在变量的声明与函数的声明。
```js
myFunction(5);
function myFunction(y) {
    return y * y;
}
```
#### 函数是一个对象
==JavaScript 函数有属性和方法==
在 JavaScript 中使用 **typeof** 操作符判断函数类型将返回 "function" 。
arguments.length 属性返回函数调用过程接收到的参数个数：
toString() 方法将函数作为一个字符串返回:
#### <font color="red">自调用函数</font>
`自调用表达式会自动调用、表达式后面紧跟 () ,则会自动调用、不能调用声明的函数`
```js
(function () {
    var x = "Hello!!";      // 我将调用自己
    alert(x);
})();
```
#### <font color="red">ES6 箭头函数</font> `解决的是匿名函数，没有函数名的`
箭头函数表达式的语法比普通函数表达式更简洁
```js
var x = function(x,y){
	return x * y;
} 
x(12,90);
var x = () =>{}
// x 函数名/变量名 匿名函数
// 多个函数
(参数1,参数2,参数3)=>{函数声明}
// 单一函数
(单一参数)=>{函数声明}
单一参数 =>{函数声明}
// 没有参数
()=>{函数声明}
var x = () =>{}
```
有的箭头函数都没有自己的 **this**。 不适合定义一个 **对象的方法**。
当我们使用箭头函数的时候，箭头函数会默认帮我们绑定外层 this 的值，所以在箭头函数中 this 的值和外层的 this 是一样的。
箭头函数是不能提升的，所以需要在使用之前定义。
使用 **const** 比使用 **var** 更安全，因为函数表达式始终是一个常量。
如果函数部分只是一个语句，则可以省略 return 关键字和大括号 {}，这样做是一个比较好的习惯:
### 参数 `显式参数与隐式参数 参数默认值 arguments 对象 通过值（对象）传递参数`
JavaScript 函数对参数的值没有进行任何的检查。
#### 函数显式参数(Parameters)与隐式参数(Arguments)
```js
functionName(parameter1, parameter2, parameter3) {    // 要执行的代码…… }
```
- 函数显式参数`形参`在函数定义时列出。
- 函数隐式参数`实参`在函数调用时传递给函数真正的值。
------
#### 参数规则
- JavaScript 函数定义显式参数时没有指定数据类型。
- JavaScript 函数对隐式参数没有进行类型检测。
- JavaScript 函数对隐式参数的个数没有进行检测。
------
#### 默认参数
- ES5 中如果函数在调用时未提供隐式参数，参数会默认设置为： undefined
- 有时这是可以接受的，但是建议最好为参数设置一个默认值：
```js
function myFunction(x, y) {    if (y === undefined) {          y = 0;    }  }
function myFunction(x, y) {    y = y || 0; }
```
> 如果y已经定义 ， y || 返回 y, 因为 y 是 true, 否则返回 0, 因为 undefined 为 false。
如果函数调用时设置了过多的参数，参数将无法被引用，因为无法找到对应的参数名。 只能使用 arguments 对象来调用。
#### ES6 函数可以自带参数（默认值）
ES6 支持函数带有默认参数，就判断 undefined 和 || 的操作：
```js
function myFunction(x, y = 10) {
    // y is 10 if not passed or undefined
    return x + y;
}
myFunction(0, 2) // 输出 2
myFunction(5); // 输出 15, y 参数的默认值
```
------
#### arguments 对象
**JavaScript 函数有个内置的对象 arguments 对象。**
argument 对象包含了函数调用的参数数组。
通过这种方式你可以很方便的找到最大的一个参数的值：
```js
x = findMax(1, 123, 500, 115, 44, 88);
function findMax() {
    var i, max = arguments[0];
    if(arguments.length < 2) return max;
    for (i = 0; i < arguments.length; i++) {
        if (arguments[i] > max) {
            max = arguments[i];
        }
    }
    return max;
}
```
或者创建一个函数用来统计所有数值的和：
```js
=x = sumAll(1, 123, 500, 115, 44, 88);
function sumAll() {
    var i, sum = 0;
    for (i = 0; i < arguments.length; i++) {
        sum += arguments[i];
    }
    return sum;
}
```
#### 通过值传递参数
在函数中调用的参数是函数的隐式参数。
JavaScript 隐式参数通过值来传递：函数仅仅只是获取值。
如果函数修改参数的值，不会修改显式参数的初始值（在函数外定义）。

隐式参数的改变在函数外是不可见的。

#### 通过对象传递参数
在JavaScript中，可以引用对象的值。
因此我们在函数内部修改对象的属性就会修改其初始的值。
修改对象属性可作用于函数外部（全局变量）。
修改对象属性在函数外是可见的。
### 调用	`调用 || this的指代问题 JavaScript 函数有 4 种调用方式。`
### ==作为一个函数调用、函数作为方法调用（Object）、使用构造函数调用函数、作为函数方法调用函数==
每种方式的不同在于 **this** 的初始化。
#### this关键字
**this指向函数执行时的当前对象，this是保留关键字，不能修改this的值**
随着函数使用场合的不同，this 的值会发生变化。但是有一个总的原则，那就是this指的是，调用函数的那个对象。
```js
alert(this); //[Object Window]
```
#### 调用JavaScript函数
```js
myFunction(10,2);
```
#### 一、作为一个函数调用
```js
function myFunction(a,b){
	return a * b;
}
myFunction(10,2);  //浏览器窗口（window对象 默认全局对象）
== window.myFunction(10, 2);    // window.myFunction(10, 2) 返回 20
```
- 以上函数不属于任何对象。但是`在 JavaScript 中它始终是默认的全局对象`。
- `在 HTML 中默认的全局对象是 HTML 页面本身`，所以函数是属于 HTML 页面。
- `在浏览器中的页面对象是浏览器窗口(window 对象)。以上函数会自动变为 window 对象的函数`。
- myFunction() 和 window.myFunction() 是一样的：
#### 全局对象 `是浏览器窗口（window对象）全局对象 == 浏览器窗口（window对象）`
==当函数没有被自身的对象调用时this的值就会变成全局对象==
在web浏览器中全局对象是浏览器窗口（window对象）
```js
function myFunction(){
	retrun this;
}
myFunction(); //返回window对象
```
函数作为全局对象调用，会使this的值成为全局对象。
使用window对象作为一个变量容易造成程序崩溃
#### `二、函数作为方法`调用 `函数可以写在对象内，this指定此对象`
`函数作为对象调用，会使得this的值成为对象本身。`
```js
var myObject = {
    firstName:"John",
    lastName: "Doe",
    fullName: function () {
        return this.firstName + " " + this.lastName; //this 指定myObject
    }
}
myObject.fullName();         // 返回 "John Doe"
var myObject = {
    firstName:"John",
    lastName: "Doe",
    fullName: function () {
        return this;//this 指定myObject
    }
}
myObject.fullName();          // 返回 [object Object] (所有者对象)
```
#### 三、使用`构造函数`调用函数
如果函数调用前使用了 **new** 关键字, 则是调用了构造函数。
这看起来就像创建了新的函数，但实际上 JavaScript 函数是重新创建的对象：

构造函数就是一个普通的函数。创建方式和普通函数没有区别

不同的是构造函数习惯首字母大写

构造函数和普通函数的区别 就是调用方式不同

- 普通函数直接调用
- 构造函数需要使用new 关键字来调用

构造函数的 执行流程

- 立刻创建一个新的对象
- 将新建的对象设置为函数中this ，在构造函数中可以使用this来引用新建的对象
- 逐行执行函数的代码
- 将新建的对象作为返回值返回

使用同一个构造函数创建的对象，我们称为一个对象，也将一个构造函数称为一个类

通过一个构造函数创建的对象，称为是该类的实例

```js
function myFunction(arg1,arg2){
	this.firstName = arg1;
	this.lastName = arg2;
}
var x = new myFunction("John","Doe"); 
x.firstName;

function Person(name,age){
 	this.name = name
    this.age = age
    this.sayHell = funciton(){
        console.log(this.name)
    }
}

// 新建一个Object 
var obj = new Object()

var p = Person() // 普通函数  
var p2 = new Person('hwl',12) // 构造函数  Person类型的 而不是 工厂模式中 创建的 Object类型  p2 是实例
var p = new Person() // 构造函数
```
使用instanceof 可以检查一个对象是否是一个类的实例

语法： 对象 instanceof  构造函数

```
console.log()
```



原型 实例 原型链





#### 四、作为`函数方法 call() apply()`调用函数

在 JavaScript 中, 函数是对象。函数有它的属性和方法。
`call() 和 apply()是预定义的函数方法。` 两个方法可用于调用函数，两个方法的第一个参数必须是对象本身。

```js
function myFunction(a, b) {
    return a * b;
}
myObject = myFunction.call(myObject, 10, 2);     // 返回 20
function myFunction(a, b) {
    return a * b;
}
myObject = myFunction.call(myObject, 10, 2);     // 返回 20
```
两个方法都使用了对象本身作为第一个参数。 两者的区别在于第二个参数： apply传入的是一个参数数组，也就是将多个参数组合成为一个数组传入，而call则作为call的参数传入（从第二个参数开始）。
在 JavaScript 严格模式(strict mode)下, 在调用函数时第一个参数会成为 **this** 的值， 即使该参数不是一个对象。
在 JavaScript 非严格模式(non-strict mode)下, 如果第一个参数的值是 null 或 undefined, 它将使用全局对象替代。
通过 call() 或 apply() 方法你可以设置 **this** 的值, 且作为已存在对象的新方法调用。
### 闭包 `私有变量可以用到闭包\使得函数拥有私有变量变成可能`
==闭包是一种保护私有变量的机制，在函数执行时形成私有的作用域，保护里面的私有变量不受外界干扰。==
==直观的说就是形成一个不销毁的栈环境==
JavaScript变量可以是局部变量或全局变量
私有变量可以用到闭包
### 全局变量与局部变量 || 私有变量
全局变量属于window对象、
全局变量可应用于页面上的所用脚本(就是不同的js文件加载到html后可以相互访问)
局部变量只能用于定义它函数内部。对于其他的函数或脚本代码是不可用的。
全局和局部变量即便名称相同，它们也是两个不同的变量。修改其中一个，不会影响另一个的值。
==不使用var关键字，那么它是一个全局属性，即便它在函数内定义，函数外也能访问==

```js
c = 1000;
var b = 10;  //全局变量
function myFunction(){
	var a = 100; // 局部变量
	console.log(a);
	console.log(b);
	//函数可以访问函数内部定义的变量也可以访问外部定义的变量
}
console.log(a)//报错，函数外没有办法访问函数内的变量
```
### 变量的生命周期
全局变量的作用域是全局性的，即在整个JavaScript程序中，全局变量处处都在。
而在函数内部声明的变量，只在函数内部起作用。这些变量是局部变量，作用域是局部性的；函数的参数也是局部性的，只在函数内部起作用。
### `计时器困境=>内嵌函数=>闭包`
### 计时器困境
问题：计时器进行设置初始值时如果设置为
全局变量=>任何的js文件都能修改初始值的大小，而不用通过函数
局部变量=>没有办法更改初始值的大小
```js
var count = 0; //页面上的任何脚本都能改变计数器，即便没有调用 add() 函数。
function add(){
	var count = 0;//如果我在函数内声明计数器，如果没有调用函数将无法修改计数器的值：
	return counter += 1;
}
```
### 内嵌函数解决计时器困境
```js
function add(){
	var counter = 0;
	function plus(){
		couter += 1
	}
	plus();
	return counter;
}
```
### 闭包`是使用自调用函数解决问题`
```js
var add = (function(){
	var count = 0;
	return 	function(){
		count + = 1;
	}
})();
function addNum(){
	console.log(add());
}
```
这个叫作 JavaScript **闭包。**它使得函数拥有私有变量变成可能。
变量 **add** 指定了函数自我调用的返回字值。
==自我调用函数只执行一次==。设置计数器为 0。并返回函数表达式。
add变量可以作为一个函数使用。非常棒的部分是它可以访问函数上一层作用域的计数器。
这个叫作 JavaScript **闭包。**它使得函数拥有私有变量变成可能。
计数器受匿名函数的作用域保护，只能通过 add 方法修改。
>闭包是一种保护私有变量的机制，在函数执行时形成私有的作用域，保护里面的私有变量不受外界干扰。
>
>直观的说就是形成一个不销毁的栈环境。
### `IIFE`
立即执行函数
https://segmentfault.com/a/1190000003985390
IIFE（立刻调用函数表达式）是`一个定义时就会执行的Javascript函数`
```js
(function () {
    statements
})();
```
这是一个被称为 [自执行匿名函数](https://developer.mozilla.org/en-US/docs/Glossary/Self-Executing_Anonymous_Function) 的设计模式，主要包含两部分。第一部分是包围在 [`圆括号运算符`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Grouping) `()` 里的一个匿名函数，这个匿名函数拥有独立的词法作用域。这不仅避免了外界访问此 IIFE 中的变量，而且又不会污染全局作用域。
第二部分再一次使用 `()` 创建了一个立即执行函数表达式，JavaScript 引擎到此将直接执行函数。
JavaScript----> ES6 ---> TS
[(6条消息)JavaScript、TypeScript、ES6三者之间的联系和区别_JavaScript_qq_38531678的博客-CSDN博客](https://blog.csdn.net/qq_38531678/article/details/84066673)
面向对象
面向对象不是新的东西，它只是过程式代码的一-种高度封装，目的在于提高代码的开发效率和可维护性。
继承及应用
闭包
递归和拷贝
正则表达式
表格
类数组对象
**NodeList、HTMLCollection、NamedNodeMap**
**NodeList**
Nodelist对象的特点
- NodeList是一种**类数组对象**，用来保存一组有序的节点
- 可以通过方括号语法来访问NodeList的值，有**item方法与length属性**
- 它并不是Array的实例，**没有数组对象的方法**
```js
var box = doucument.getElementById("box");
var nodes = box.childNodes;
console.log(nodes);
console.log(nodes[1]); console.log(nodes.item[1]);
//  nodelist ---->array
function makeArray(nodeList){
    try{
        return Array.prototype.slice.call(nodeList); //解决IE浏览器不兼容的方法
    }catch(e){
        var arr = new Array();
        for(var i = 0,len = nodeList.length;i < len;i++){
            arr.push(nodeList[i]);
        }
        return arr;
    }   
}
var newNodeList = makeArray(nodes);
newNodeList.push("<li>节点四</li>");
console.log(newNodeList)
```
类数组对象HTMLCollection
- Ele.getElementsByTagName()
- document.script //script
- document.link //a标签
- document.images //images
- document.forms //forms表单
- tr.cells //td
- select.options //选项
```
console.log();
console.log();
console.log();
console.log();
console.log();
```
**类数组对象NamedNodeMap**
**Ele.attributes //获取元素的属性**
```js
<ul id="box" data-url="index.html" node-action="submit">
	<li><节点一/li>
	<li>节点二</li>
	<li>节点三</li>
</ul>
var box = document.getElementById("box");
var attrs = box.attributes;
console.log(attrs);
console.log(attrs.length);  //3个属性
console.log(attrs[0]);  //id
console.log(attrs.item(1)); //data-url
```
**类数组对象的动态性**
- NodeList、HTMLCollection、NamedNodeMap三个集合都是动态的，是有生命、有呼吸的对象
- 它们实际上是基于DOM结构动态执行查询的结果，因此DOM结构的变化能自动反映这些对象中
- 每当文档结构发生变化时，它们都会得到更新。因此，它们始终都会保持着最新、最准确的信息
```js
<div></div>
<div></div>
<div></div>
// HTMLCollection类数组对象的动态性造成的，每次在循环的时候会重新计算div的个数 divs会和i一起递增
var divs = document.getElementByTagName("div");
var i = 0;
while(i < divs.length){
	document.body.appendChild(document.createElement("div"));
	i++;
}
//解决方法
// 创建多三个div
var divs = document.getElementByTagName("div");
var length = divs.length;
var i = 0;
while(i < length){
	document.body.appendChild(document.createElement("div"));
	i++;
}
```
节点查找
前三个所有浏览器都能用，后面三个较新的浏览器用
一定要document,只能通过document对象获取，不能通过element对象获取
document.getElementById()  通过ID属性
```
var box = document.getElementById("box");
//只能用doucument调用
```
解决IE浏览器下相同值下，没有办法正确找到id的属性
```js
<a name="target" >这是一个错误的链接</a>
<p id="target">这是一个正确的链接</p>
<input id="btn" value="按钮" />
var ps = document.getElementById("target");
var btn = document.getElementById("input");
var getElementById = function(id){
	var el = document.getElementById(id);
	if(!+"\v1"){ //利用各浏览器对转义字符  ‘\v’的解释 
	//IE浏览器 没有转义 得到字符 v  相当于 v1   其他浏览器  \v 解释为垂直的制表符，相当于空格  1
	// 加号把后面的字符串转换为数字  叹号取反
	// IE notanumber == >true          其他浏览器 1 ===> 0 ===> false     
		if(el && el.id === id){
			return el;
		}else{
		 	var els = document.all[id],
		 	n = els.length;
		 	for(var i = 0;i < n;i++){
		 		if(els[i].id === id){
		 			return els[i];
		 		}
		 	}
		}
	}
	return el;
};
console.log(getElementById("target").tagName);
```
document.getElementsByName()    //s 返回的是一个集合 name属性
```js
<div name="mydiv"></div>
<div name="mydiv"></div>
var mydiv = document.getElementsByName("mydiv");
console.log(mydiv.length);
```
getElementsByTagName() //s 根据**标签元素的名称**获取元素
```js
var lis = document.getElementsByTagName("li"); //元素不分大小写 Li
var inputs = document.getElementsByTagName("input");
var comment = document.getElementByTagName("!"); // 获取注释
var all = document.getElementByTagName("*"); //获取页面上所有的元素
console.log(lis.length);
console.log(inputs[0].vaule);
console.log(comment[0].nodeValue);// 获取注释的内容
console.log(comment[1].nodeValue);
for(var i = 0;len = all.length.i < len; i++){
   console.log(all[i].tagName); 
}
```
getElementsByClassName()  // 类名 class
```js
<div class="hello"></dv>
<div class="hello world"></dv> //<div class="world hello"></dv> 一样
var hellos = document.getElementsByClassName("hello");
var hellosworlds= document.getElementsByClassName("hello world");
```
**IE8以下浏览器 不兼容获取类名**
主流浏览器基本都支持这两个属性
**querySelector**
返回文档中匹配**指定CSS选择器的一个元素**
**querySelectorAll()**
返回文 档中匹配**指定CSS选择器的一组元素**
```js
<div id="myDiv">
<ul id="myUl">
	<li>1</li>
	<li>2</li>
	<li>3</li>
</ul>
</div>
//**querySelector**
<div class="foo:bar"></div>
var myDiv = document.getElementById("myDiv");
var ul = myDiv.querySelector("myUl");
var myDiv = myDiv.querySelector("myDiv");
var li = myDiv.querySelector("li:first-child");
var els = myDiv.querySelector("li,input");
var els2 = myDiv.querySelector(".foo:\bar"); //冒号要转义字符
//不存在的元素 ===》 null
//**querySelectorAll()**  获得一个集合
//不存在的元素 ===》 []
```
```js
//解决方法
// 创建多三个div
var divs = document.querySelectorAll("div");
var i = 0;
while(i < divs.length){
	document.body.appendChild(document.createElement("div"));
	i++;
}
```
## 表单
### JavaScript 表单验证
HTML 表单验证可以通过 JavaScript 来完成。
以下实例代码用于判断表单字段(fname)值是否存在， 如果不存在，就弹出信息，阻止表单提交：

function validateForm() {    var x = document.forms["myForm"]["fname"].value;    if (x == null || x == "") {        alert("需要输入名字。");        return false;    } }

### JavaScript 验证输入的数字
JavaScript 常用于对输入数字的验证：
请输入 1 到 10 之间的数字：

 提交

### HTML 表单自动验证
HTML 表单验证也可以通过浏览器来自动完成。
如果表单字段 (fname) 的值为空, **required** 属性会阻止表单提交：
<form action="demo_form.php" method="post">  <input type="text" name="fname" required="required">  <input type="submit" value="提交"> </form>
> Internet Explorer 9 及更早 IE 浏览器不支持表单自动验证。
------
### 数据验证
数据验证用于确保用户输入的数据是有效的。
典型的数据验证有：
- 必需字段是否有输入?
- 用户是否输入了合法的数据?
- 在数字字段是否输入了文本?
大多数情况下，数据验证用于确保用户正确输入数据。
数据验证可以使用不同方法来定义，并通过多种方式来调用。
**服务端数据验证**是在数据提交到服务器上后再验证。
**客户端数据验证**是在数据发送到服务器前，在浏览器上完成验证。
------
### HTML 约束验证
HTML5 新增了 HTML 表单的验证方式：约束验证（constraint validation）。
约束验证是表单被提交时浏览器用来实现验证的一种算法。
HTML 约束验证基于：
- **HTML 输入属性**
- **CSS 伪类选择器**
- **DOM 属性和方法**
### 约束验证 HTML 输入属性
| 属性     | 描述                     |
| :------- | :----------------------- |
| disabled | 规定输入的元素不可用     |
| max      | 规定输入元素的最大值     |
| min      | 规定输入元素的最小值     |
| pattern  | 规定输入元素值的模式     |
| required | 规定输入元素字段是必需的 |
| type     | 规定输入元素的类型       |
完整列表，请查看 [HTML 输入属性](https://www.runoob.com/html/html5-form-attributes.html)。
### 约束验证 CSS 伪类选择器
| 选择器    | 描述                                    |
| :-------- | :-------------------------------------- |
| :disabled | 选取属性为 "disabled" 属性的 input 元素 |
| :invalid  | 选取无效的 input 元素                   |
| :optional | 选择没有"required"属性的 input 元素     |
| :required | 选择有"required"属性的 input 元素       |
| :valid    | 选取有效值的 input 元素                 |
### 表单验证
------
### JavaScript 表单验证
JavaScript 可用来在数据被送往服务器前对 HTML 表单中的这些输入数据进行验证。
表单数据经常需要使用 JavaScript 来验证其正确性：
- 验证表单数据是否为空？
- 验证输入是否是一个正确的email地址？
- 验证日期是否输入正确？
- 验证表单输入内容是否为数字型？
------
### 必填（或必选）项目
下面的函数用来检查用户是否已填写表单中的必填（或必选）项目。假如必填或必选项为空，那么警告框会弹出，并且函数的返回值为 false，否则函数的返回值则为 true（意味着数据没有问题）：
function validateForm() {  var x=document.forms["myForm"]["fname"].value;  if (x==null || x=="")  {    alert("姓必须填写");    return false;  } }
以上函数在 form 表单提交时被调用:
<form name="myForm" action="demo-form.php" onsubmit="return validateForm()" method="post"> 姓: <input type="text" name="fname"> <input type="submit" value="提交"> </form>
[](https://www.runoob.com/try/try.php?filename=tryjs_form_validation)

### E-mail 验证
下面的函数检查输入的数据是否符合电子邮件地址的基本语法。
意思就是说，输入的数据必须包含 @ 符号和点号(.)。同时，@ 不可以是邮件地址的首字符，并且 @ 之后需有至少一个点号：
function validateForm(){  var x=document.forms["myForm"]["email"].value;  var atpos=x.indexOf("@");  var dotpos=x.lastIndexOf(".");  if (atpos<1 || dotpos<atpos+2 || dotpos+2>=x.length){    alert("不是一个有效的 e-mail 地址");    return false;  } }
下面是连同 HTML 表单的完整代码：
<form name="myForm" action="demo-form.php" onsubmit="return validateForm();" method="post">    Email: <input type="text" name="email">    <input type="submit" value="提交"> </form>
[»](https://www.runoob.com/try/try.php?filename=tryjs_form_validate_email)
验证API
### JavaScript 验证 API
------
### 约束验证 DOM 方法
| Property            | Description                                                  |
| :------------------ | :----------------------------------------------------------- |
| checkValidity()     | 如果 input 元素中的数据是合法的返回 true，否则返回 false。   |
| setCustomValidity() | 设置 input 元素的 validationMessage 属性，用于自定义错误提示信息的方法。使用 setCustomValidity 设置了自定义提示后，validity.customError 就会变成true，则 checkValidity 总是会返回false。如果要重新判断需要取消自定义提示，方式如下：`setCustomValidity('')  setCustomValidity(null)  setCustomValidity(undefined)` |
以下实例如果输入信息不合法，则返回错误信息：
### checkValidity() 方法
<input id="id1" type="number" min="100" max="300" required> <button onclick="myFunction()">验证</button>  <p id="demo"></p>  <script>
function myFunction() {    var inpObj = document.getElementById("id1");    if (inpObj.checkValidity() == false) {        document.getElementById("demo").innerHTML = inpObj.validationMessage;    } }
</script>

[»](https://www.runoob.com/try/try.php?filename=tryjs_validation_check)

### 约束验证 DOM 属性
| 属性              | 描述                                  |
| :---------------- | :------------------------------------ |
| validity          | 布尔属性值，返回 input 输入值是否合法 |
| validationMessage | 浏览器错误提示信息                    |
| willValidate      | 指定 input 是否需要验证               |
------
### Validity 属性
input 元素的 **validity 属性**包含一系列关于 validity 数据属性:
| 属性            | 描述                                                       |
| :-------------- | :--------------------------------------------------------- |
| customError     | 设置为 true, 如果设置了自定义的 validity 信息。            |
| patternMismatch | 设置为 true, 如果元素的值不匹配它的模式属性。              |
| rangeOverflow   | 设置为 true, 如果元素的值大于设置的最大值。                |
| rangeUnderflow  | 设置为 true, 如果元素的值小于它的最小值。                  |
| stepMismatch    | 设置为 true, 如果元素的值不是按照规定的 step 属性设置。    |
| tooLong         | 设置为 true, 如果元素的值超过了 maxLength 属性设置的长度。 |
| typeMismatch    | 设置为 true, 如果元素的值不是预期相匹配的类型。            |
| valueMissing    | 设置为 true，如果元素 (required 属性) 没有值。             |
| valid           | 设置为 true，如果元素的值是合法的。                        |
##
如果输入的值大于 100，显示一个信息：
### rangeOverflow 属性
<input id="id1" type="number" max="100"> <button onclick="myFunction()">验证</button>  <p id="demo"></p>  <script>
function myFunction() {    var txt = "";    if (document.getElementById("id1").validity.rangeOverflow) {       txt = "输入的值太大了";    }    document.getElementById("demo").innerHTML = txt; }
</script>
[»](https://www.runoob.com/try/try.php?filename=tryjs_validation_rangeOverflow)
如果输入的值小于 100，显示一个信息：
### rangeUnderflow 属性
<input id="id1" type="number" min="100" required> <button onclick="myFunction()">OK</button>  <p id="demo"></p>  <script>
function myFunction() {    var txt = "";    var inpObj = document.getElementById("id1");    if(!isNumeric(inpObj.value)) {        txt = "你输入的不是数字";    } else if (inpObj.validity.rangeUnderflow) {        txt = "输入的值太小了";    } else {        txt = "输入正确";    }    document.getElementById("demo").innerHTML = txt; }  // 判断输入是否为数字 function isNumeric(n) {    return !isNaN(parseFloat(n)) && isFinite(n); }
</script>
保留关键字

在 JavaScript 中，一些标识符是保留关键字，不能用作变量名或函数名。

##### JavaScript JSON(JavaScript Object Notation)`存储和传输的格式、用于服务端向网页传送数据`
##### `JSON数据（键值对<、JSON对象{}<、JSON数组[]`
- JSON是用于存储和传输的格式
- JSON通常用于服务端向网页传送数据
- JSON是一种轻量级的数据交换格式
- JSON是独立的语言
- JSON易于理解
- JSON 使用JavaScript语法，但是JSON格式仅仅是一个文本
- 文本可以被任何编程语言读取及作为数据格式传递
```json
{
"sites":[
	{"name":"你的名字","url":"www.name.com"},
	{"name":"天气之子","url":"www.weather.com"},
	{"name":"言叶之庭","url":"www.leaf.com"}
]
}
```
JSON语法规则
- 数据为键/值对
- 数据由逗号分隔
- `大括号保持对象`
- `方括号保存数组`
JSON数据 `键值对`
JSON 数据格式为键值对，就像JavaScript对象属性。
键/值对包括字段名称（在双引号中），后面一个冒号，然后是值：
```json
”name“:"你的名字"
```
JSON对象
JSON 对象保存在大括号内。
就像在 JavaScript 中, 对象可以保存多个 键/值 对：
```json
{"name":"你的名字", "url":"www.name.com"}
```
JSON数组
JSON 数组保存在中括号内。
就像在 JavaScript 中, 数组可以包含对象：
```
{
"sites":[
	{"name":"你的名字","url":"www.name.com"},
	{"name":"天气之子","url":"www.weather.com"},
	{"name":"言叶之庭","url":"www.leaf.com"}
]
}
```
对象 "sites" 是一个数组，包含了三个对象。
每个对象为站点的信息（网站名和网站地址）。
JSON格式化后为JavaScript对象	
JSON 格式在语法上与创建 JavaScript 对象代码是相同的。
由于它们很相似，所以 JavaScript 程序可以很容易的将 JSON 数据转换为 JavaScript 对象。
 JavaScript JSON.stringify()
JSON.stringify() 方法用于将 JavaScript 值转换为 JSON 字符串。
```
JSON.stringify(value[, replacer[, space]])
value:
必需， 要转换的 JavaScript 值（通常为对象或数组）。
replacer:
可选。用于转换结果的函数或数组。
如果 replacer 为函数，则 JSON.stringify 将调用该函数，并传入每个成员的键和值。使用返回值而不是原始值。如果此函数返回 undefined，则排除成员。根对象的键是一个空字符串：""。
如果 replacer 是一个数组，则仅转换该数组中具有键值的成员。成员的转换顺序与键在数组中的顺序一样。
space:
可选，文本添加缩进、空格和换行符，如果 space 是一个数字，则返回值文本在每个级别缩进指定数目的空格，如果 space 大于 10，则文本缩进 10 个空格。space 也可以使用非数字，如：\t。
返回值：
返回包含 JSON 文本的字符串。
```
```
var str = {"name":"菜鸟教程", "site":"http://www.runoob.com"}
str_pretty1 = JSON.stringify(str)
document.write( "只有一个参数情况：" );
document.write( "<br>" );
document.write("<pre>" + str_pretty1 + "</pre>" );
document.write( "<br>" );
str_pretty2 = JSON.stringify(str, null, 4) //使用四个空格缩进
document.write( "使用参数情况：" );
document.write( "<br>" );
document.write("<pre>" + str_pretty2 + "</pre>" ); // pre 用于格式化输出
```
JSON字符串转换为JavaScript对象  `JSON parse()`
```json
JSON.parse(text[, reviver])
text:必需， 一个有效的 JSON 字符串。
reviver: 可选，一个转换结果的函数， 将为对象的每个成员调用此函数。
```
通常我们从服务器中读取 JSON 数据，并在网页中显示数据。
简单起见，我们网页中直接设置 JSON 字符串 (你还可以阅读我们的 [JSON 教程](https://www.runoob.com/json/json-tutorial.html)):
首先，创建 JavaScript 字符串，字符串为 JSON 格式的数据：
```json
var text = '{ "sites" : [' +
'{ "name":"Runoob" , "url":"www.runoob.com" },' +
'{ "name":"Google" , "url":"www.google.com" },' +
'{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
var text = '{ "sites" : [' +
    '{ "name":"Runoob" , "url":"www.runoob.com" },' +
    '{ "name":"Google" , "url":"www.google.com" },' +
    '{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
obj = JSON.parse(text);
document.getElementById("demo").innerHTML = obj.sites[1].name + " " + obj.sites[1].url;
// [1]的值为sites数组的下标值
```
然后，使用 JavaScript 内置函数 JSON.parse() 将字符串转换为 JavaScript 对象:
```
var obj = JSON.parse(text);
```
相关函数
| 函数             | 描述                                                         |
| ---------------- | ------------------------------------------------------------ |
| JSON parse()     | 用于将一个JSON字符串转换为JavaScript对象`JSON字符串 => Javascript对象` |
| JSON stringify() | 用于将一个JavaSript值装换为JSON字符串 `JavaScript值=>JSON字符串` |
##### JavaScript void ``javascript:void(0)死链接 void该操作符指定要计算一个表达式但是不返回值`
`javascript:void(0) 中最关键的是 void 关键字， void 是 JavaScript 中非常重要的关键字，该操作符指定要计算一个表达式但是不返回值。`
```
<a href="javascript:void(0)">单击此处什么也不会发生</a>
//创建了一个超级链接，当用户点击以后不会发生任何事。
<a href="javascript:void(alert('Warning!!!'))">点我!</a>
//在用户点击链接后显示警告信息：
```
```
a = void ( b = 5, c = 7 ); // a undefined
void func()
javascript:void func()
或者
void(func())
javascript:void(func())
```
##### href="#"与href="javascript:void(0)"的区别
**#** 包含了一个位置信息，默认的锚是**#top** 也就是网页的上端。
而javascript:void(0), 仅仅表示一个死链接。
在页面很长的时候会使用 **#** 来定位页面的具体位置，格式为：**# + id**。
如果你要定义一个死链接请使用 javascript:void(0) 。
```js
<a href="javascript:void(0);">点我没有反应的!</a>
<a href="#pos">点我定位到指定位置!</a>
<br>
...
<br>
<p id="pos">尾部定位点</p>
```
### 代码规范
1. 变量名驼峰法，除第一个单词之外，其他单词首字母大写（ **lowerCamelCase**）
2. 全局变量为大写 (**UPPERCASE** )
3. 常量 (如 PI) 为大写 (**UPPERCASE** ) `const 定义`
4. 变量名不要以 $ 作为开始标记，会与很多 JavaScript 库冲突。
5. 空格、代码缩进
6. 分号结尾
7. 为了便于阅读每行字符建议小于数 80 个。
8. 使用小写文件名
9. data-  横杠(-)字符通常在 JavaScript 中被认为是减法，所以不允许使用。
10. js 可以使用下划线使用下划线
### 作用域
- 作用域是可访问变量的集合。
- 在 JavaScript 中, 对象和函数同样也是变量。
- **在 JavaScript 中, 作用域为可访问变量，对象，函数的集合。**
- JavaScript 函数作用域: 作用域在函数内修改。
#### 全局作用域
#### 函数作用域
变量在函数内声明，变量为函数作用域
局部变量：只能在函数内部访问
#### 块级作用域

## 定时器

### setTimeout clearTimeout

```js
setTimeout(characterTime, 1000);
setTimeout(方法,时间)
```

### setInterval clearInterval

```js
var time = setInterval(characterTime, 1000);
setInterval(方法,时间)
clearInterval(time)清除的是setInterval的值而不是方法的
```

## 高级技巧

继承、原型链、this指向、设计模式、call, apply, bind,



new实现、防抖节流、let, var, const 区别、暂时性死区、event、loop；



promise使用及实现、promise并行执行和顺序执行；



async/await的优缺点；



闭包、垃圾回收和内存泄漏、数组方法、数组乱序, 数组扁平化、事件委托、事件监听、事件模型



### 三元运算符

语法：

三元运算符是`if`语句的快捷方式。它由三个操作数组成；一个问号、一个条件和一个在条件为真时执行的表达式，后跟一个冒号和另一个在条件为假时执行的表达式

- `A : B ? A > B`
- ` A > B ? A : B`
- `let C = (A > B) ? A : B`
- `条件 ? A(true):B(false)`

```js
let Name = (length >= 5) ? 'MIKER' : 'MIKE' 
console.log(Name)
```



### 箭头函数



### 闭包







### 防抖



### 节流





### 深浅拷贝



### 数组扁平化

数组扁平化是指将一个多维数组变为一个一维数组

```js
const arr = [[1,2,3,4],[4,[5,6,7,7,[3]]],[4]]
// 多维数组 => 一维数组  
```

- flat() 

```js
const res = arr.flat(Infinity)
// [
       1, 2, 3, 4, 4,
       5, 6, 7, 7, 3,
       4
   ]
```

- 正则
	- JSON.stringify()
	- JSON.parse()

```js
const res = JSON.stringify(arr).replace(/\[|\]/g, '').split(',');


```

- reduce

```js
const fla = arr =>{
	return arr.reduce((pre,cur)) => { 
    
    }
}
```

- 函数递归
- 

### 数组去重

原生

```

```

Set方法

```
const res1 = Array.from(new Set(arr)); 
```

两层for 循环 + splice



indexOf

```

```

include

```js
const unique = arr => {
	const res = [];
    
}
```

filter

```js
const unique = arr =>{
	return arr.filter((item,index) =>{
        return arr.indexOf(item) == index
    });
}
```

利用map







类数组转化为数组





### 原型、原型链和原型继承

Array.prototype.filter()



Array.prototype.map()



Array.prototype.forEach()



Array.prototype.reduce()



### Promise



Promise.all



Promise.reace







### 乱序



### 函数柯里化

指的是将一个接受多个参数的函数 变为 接受一个参数返回一个函数的固定形式，这样便于再次调用，例如f(1)(2)

```js
function add() {
    const _args = [...arguments];
    function fn() {
        _args.push(...arguments);
        return fn;
    }
    fn.toString = function () {
        return _args.reduce((sum, cur) => sum + cur);
    }
    return fn;
}

let num = add(1)(2)(3)(4)
console.log(num.toString())
console.log(add(1)(1, 2, 3)(2).toString())
```





### 图片懒加载





### 滚动加载



### 事件模式





### 继承



### 高阶函数



### Generator 







## 错误处理和调试

常用写法

`document.bgColor ='red'`	不能省略引号，变换的是整个页面的背景颜色。
`div.style.backgroundColor='pink'`是改变div的背景颜色。
`btn.onclick = methods`  onclick是一个点击事件，不是一个函数，不用加括号  methods 是一个函数，不用加括号，如果加了括号，表示事件立刻执行。 
`window.onload = function () {}` 文档加载事件
`     document.getElementsByTagName("element")[0]`与 `document.getElementsByClassName("element")[0]`表示选取多个元素，要在后面加上[index]值，表示找到相应的元素。
`element.textContent = '这是内容，`  
`var boxs = document.getElementById('box');`  两个变量的名字不能一样

获取input文本框值

```js
function readtext() {
    // 方法一
    var name = document.getElementById("name").value;
    alert(name);
    // 方法二
    name = form1.name.value;
    alert(name);
    // 方法三 jquery
    name = $("#name").val();
    alert(name);
    // 方法四 jquery
    name =  $("input[id='name']").val();
    alert(name);
    // 方法五 jquery
    name = $("#name").attr("value");
    alert(name);
    // 方法六 jquery
    name = $("input[id='name']").attr("value");
    alert(name);
    <input type="text" name="" id="" placeholder="请输入第一个数" id="inp_num1">
}                    
```
`Uncaught TypeError: Cannot set property 'onfocus' of null at attribute.html:10`·
未捕获的类型错误:无法设置null的属性“onfocus”
==页面没有加载onfocus方法，没有在页面HTML页面加载完成后，加载JS文件==
解决方法：

```js
window.onload = function(){}
```



# 内置对象

## 内置对象

`9种 Number Array String prototype Object Date Boolearn Math Error 全局属性/函数`
数据类型

- 基本数据类型：Number、Boolean、String、Null、Undefined、Symbol
- 引用数据类型：Array、Object、function

| 内置对象  | 描述   |
| --------- | ------ |
| Array     | 数组   |
| Boolean   | 布尔值 |
| Math      | 数学   |
| Number    | 数字   |
| String    | 字符串 |
| Date      | 日期   |
| Object    | 对象   |
|           |        |
| RegExp    | 正则   |
| prototype | 原型   |

## Array对象

> [JS数组方法](https://juejin.cn/post/6844903591149322248)
>
> [js 数组详细操作方法及解析合集](https://juejin.cn/post/6844903614918459406)

- 数组对象的作用是：使用单独的变量名来存储一系列的值
- 数组是一种线性表数据结构。它用一组连续的内存空间，来存储一组具有相同类型的数据。

### 创建数组

```js
 // 1. 字面量方式
 var arr = ["Hello","World","JavaScript"]
 // 2. 构造函数方式
 var arr = new Array("Hello","World","JavaScript")
 var arr = new Array();
 arr[0] = "Hello"
 arr[1] = "World"
 arr[2] = "JavaScript"
 // 构造器 实际上 new Array === Array, new 关键字是可省略的
 var arr = Array("Hello","World","JavaScript")
 // 3. Array.of()方法（ES6新增）
 // 方法的作用是将一组值（即传进来的参数）转换为数组。这个方法弥补了构造函数创建数组的不足。可以实现创建只有一个number类型元素的数组。
let arr = Array.of(6,10); // arr = [6,10]
let arr1 = Array.of(6,10,'a', true, null, undefined, {name: "zhangsan"}, [45]); // arr = [ 6, 10,'a', true, null, undefined, { name: 'zhangsan' }, [ 45 ] ]

// 单维数组 
var obj = [元素1,元素2]
// 多维数组
var obj = [[],[],[]]
```

- 访问：数组下标从0**开始访问 ** 
  创建自定义的数组方法

```js
Array.prototype.myUcase = function(){
     for(i = 0;i < this.length;i++){
         this[i] = this[i].toUpperCase();
     }
 }
//  arr.myUcase()
 // 格式
 Array.prototype.方法名 = function(){
     // 函数体;
 }
 // 使用方法:数组.方法名()
```

基本操作

- 存放数组  
  - 单维数组  数组名[下标索引]
  - 多维数组 
- 增加数组 [] 新下标
- 删除数组 dekete 数组下标
- 遍历数组  for(var 数组元素变量 in 数组)

### 数组属性 `3`

| 属性                                                         | 描述                             |
| :----------------------------------------------------------- | :------------------------------- |
| [length](https://www.runoob.com/jsref/jsref-length-array.html) | 设置或返回数组元素的个数。       |
| [constructor](https://www.runoob.com/jsref/jsref-constructor-array.html) | 返回创建数组对象的原型函数。     |
| [prototype](https://www.runoob.com/jsref/jsref-prototype-array.html) | 允许你向数组对象添加属性或方法。 |

### 数组方法 `30`

#### 常用数组方法

数组方法可以分为

- 数组原型的方法
- 构造函数的方法（ES6新增）
  - Array.from()
- unshift、shift  &&  push、pop

> ES5
>
> - length (长度、增加和删除数组项)
>
>   - 可以通过指定数组增加或删除数组元素
>
> - join & split
>
>   - join 数组转字符串
>     - join
>     - toLocaleString() 数组转字符串
>     - toString() 数组转字符串 不推荐
>   - split 
>
> - 数组添加删除 头部或尾部（ push()、pop()、unshift()、shift() ）
>
>   - (数组末尾)push & pop
>   - push 数组结尾添加一项项或多项，返回添加元素数组后的长度
>   - pop  删除数组最后一项，返回删除的那一项
>   - (数组开头) unshift & shift 
>
>   - unshift 向数组开头添加一项或者多项
>   - shift 删除数组第一项，返回删除的那一项 
>
> - reverse & sort
>
>   - reverse 翻转原数组，返回翻转后的数组
>   - sort 数组排序
>
> - concat，slice & splice
>
>   - concat 拼接数组
>   - slice  基于当前数组的一项或多项创建一个新的数组（裁剪数组、赋值数组）
>   - splice  添加/删除数组元素
>
> - indexOf & lastIndexOf  元素查找索引位置
>
>   -  indexOf： 从数组开头查找元素在数组中的索引位置
>   -  lastIndexOf： 从数组结尾查找元素在数组中的索引位置
>
> - every, filter, forEach, map & some 迭代方法
>
>   - every  对数组中的每一项运行给定函数，如果该函数对每一项都返回true,则返回true
>   - filter
>   - forEach(item,index,array)  对数组中的每一项运行给定函数。无返回值
>   - map
>   - some
>
> - reduce & reduceRight 缩小方法
>
>   - reduce 从数组的第一项开始，逐步遍历到最后，迭代数组的所有项
>   - reduceRight 从数组的最后一项开始，逐步遍历到第一项，迭代数组的所有项
>
> - toString & Array.isArray(数组)[判断是不是数组]  数组的检测
>
>   - toString
>   - Array,isArray
>
> ES6
>
> - 数组拓展运算符`...`
>   - 数组的扩展运算符可以将数组转化为以逗号分割的参数序列
> - Array.from() & Array.of()
> - copyWithin(target,start=0,end=this.length) 拷贝，将数组指定位置（start到end）的元素复制到当前数组的其他位置（target开始），这种复制会替换原位置的元素（ES6新增）
> - fill
>   - 数组填充
> - find & findIndex
> - entries() 、keys() & values()
>   - entries()
>   - keys()
>   - values()
>
> ES7
>
> - includes 查找数组是否包含某个元素
>
> ES10
>
> - flat & flatMap

```js
let sumArr = []
let arrNum = [3,6,9,3,5,7,2,9];
let chArr = ['c','e','t','f','x','a','y'];
// 数组的属性
console.log(arrNum.length);
sumArr.concat(arrNum);
sumArr.concat(arrNum,chArr);
// 数组的检测
Object.prototype.toString.call([]) === "[object Array]"; // true 利用对象的toString方法
Array.isArray(arrNum); // Array.isArray(数组名):
// 数组排序 sort() 排序方式 默认自小到大
let temp = arrNum.sort((a,b) => {
    // 排序方式 小 => 大
    return a - b; 
})
console.log(arrNum,temp)
// every()
// 数组裁剪或数组复制 slice()
let temp = arrNum.slice(2,5)
console.log(arrNum,temp)
// 元素查找索引位置 indexOf() lastIndexOf()
let temp = arrNum.indexOf(3) // 3是元素值，返回索引值 
let temp = arrNum.LastIndexOf(3)
// 构造函数的方法
Array.from() // 将类数组转化为数组
// 数组扩展运算符
// 1. 将数组通过扩展运算符转化为参数序列直接传参，无需使用apply转化了
ler arrNew = [1,2,3,4,5]
// apply 写法
Math.min.apply(null,arr)
// 扩展运算符
Math.min(...arr)
// 2. 复制和拼接数组
console.log(...arrNum,...arrNew);
// 3. 将字符串分解为真正的数组 字符串转数组
[...'hello'] // [ 'h', 'e', 'l', 'l', 'o' ]
```

| 方法                                                         | 描述                                                   |
| :----------------------------------------------------------- | :----------------------------------------------------- |
| [concat()](https://www.runoob.com/jsref/jsref-concat-array.html) | `连接`两个或更多的数组，并返回结果。                   |
| [copyWithin()](https://www.runoob.com/jsref/jsref-copywithin.html) | 从数组的指定位置``拷贝``元素到数组的另一个指定位置中。 |
| [entries()](https://www.runoob.com/jsref/jsref-entries.html) | 返回数组的可迭代对象。                                 |
| [every()](https://www.runoob.com/jsref/jsref-every.html)     | 检测数值元素的每个元素是否都符合条件。                 |
| [fill()](https://www.runoob.com/jsref/jsref-fill.html)       | 使用一个固定值来``填充``数组。                         |
| [filter()](https://www.runoob.com/jsref/jsref-filter.html)   | 检测数值元素，并返回符合条件所有元素的数组。           |
| [find()](https://www.runoob.com/jsref/jsref-find.html)       | 返回符合传入测试（函数）条件的数组元素。               |
| [findIndex()](https://www.runoob.com/jsref/jsref-findindex.html) | 返回符合传入测试（函数）条件的数组元素索引。           |
| [forEach()](https://www.runoob.com/jsref/jsref-foreach.html) | 数组每个元素都执行一次回调函数。                       |
| [from()](https://www.runoob.com/jsref/jsref-from.html)       | 通过给定的对象中创建一个数组。                         |
| [includes()](https://www.runoob.com/jsref/jsref-includes.html) | 判断一个数组是否包含一个指定的值。                     |
| 位置方法                                                     |                                                        |
| [indexOf()](https://www.runoob.com/jsref/jsref-indexof-array.html) | 搜索数组中的元素，并返回它所在的位置。                 |
| [lastIndexOf()](https://www.runoob.com/jsref/jsref-lastindexof-array.html) | 搜索数组中的元素，并返回它最后出现的位置。             |
|                                                              |                                                        |
| [isArray()](https://www.runoob.com/jsref/jsref-isarray.html) | 判断对象``是否为数组``。                               |
| [join()](https://www.runoob.com/jsref/jsref-join.html)       | 把数组的所有元素放入一个字符串。                       |
| [keys()](https://www.runoob.com/jsref/jsref-keys.html)       | 返回数组的可迭代对象，包含原始数组的键(key)。          |
| [map()](https://www.runoob.com/jsref/jsref-map.html)         | 通过指定函数处理数组的每个元素，并返回处理后的数组。   |
| 数组后端                                                     |                                                        |
| [pop()](https://www.runoob.com/jsref/jsref-pop.html)         | 删除数组的最后一个元素并返回删除的元素。               |
| [push()](https://www.runoob.com/jsref/jsref-push.html)       | 向数组的末尾添加一个或更多元素，并返回新的长度。       |
|                                                              |                                                        |
| [reduce()](https://www.runoob.com/jsref/jsref-reduce.html)   | 将数组元素计算为一个值（从左到右）。                   |
| [reduceRight()](https://www.runoob.com/jsref/jsref-reduceright.html) | 将数组元素计算为一个值（从右到左）。                   |
|                                                              |                                                        |
| [reverse()](https://www.runoob.com/jsref/jsref-reverse.html) | `反转`数组的元素顺序。                                 |
| [sort()](https://www.runoob.com/jsref/jsref-sort.html)       | 对数组的元素进行``排序``。                             |
| 数组前端                                                     |                                                        |
| [shift()](https://www.runoob.com/jsref/jsref-shift.html)     | 删除并返回数组的第一个元素。                           |
| [unshift()](https://www.runoob.com/jsref/jsref-unshift.html) | 向数组的开头添加一个或更多元素，并返回新的长度。       |
| 数组任意位置                                                 |                                                        |
| [slice()](https://www.runoob.com/jsref/jsref-slice-array.html) | 选取数组的的一部分，并返回一个新数组。                 |
| [splice()](https://www.runoob.com/jsref/jsref-splice.html)   | 从数组中添加或删除元素。                               |
|                                                              |                                                        |
| [some()](https://www.runoob.com/jsref/jsref-some.html)       | 检测数组元素中是否有元素符合指定条件。                 |
| [toString()](https://www.runoob.com/jsref/jsref-tostring-array.html) | 把数组转换为字符串，并返回结果。                       |
| toLoccleString                                               | 转换为本地格式字符串并返回                             |
| [valueOf()](https://www.runoob.com/jsref/jsref-valueof-array.html) | 返回数组对象的原始值。                                 |

### 数组的遍历`9`

> [数组遍历](https://juejin.cn/post/6844903607645503496)
>
> - ES5：    forEach、every 、some、 filter、map、reduce、reduceRight、- ES6：    find、findIndex、keys、values、entries

1. for 循环
2. forEach(function(item,index){},that) 循环

   - 实际操作的函数function
   - 参数that是改变this指向的
   - that和index均可不写不用,
   - 缺点：forEach循环不支持return
3. for in 循环

   - 基本不会用来遍历数组
   - 缺点：数组的私有属性也会遍历。默认遍历的是数组的key值，所以会是string类型
4. for of循环

   - 弥补了forEach和for in循环的弊端。既有return，而且不会遍历数组的私有属性。
   - 缺点：for of循环不能遍历对象
5. filter 过滤器

   - 遍历一个数组并返回一个新的数组，所以并不会影响原数组。遍历数组每一项，回调函数返回了true，就把这一项添加到新数组。其中回调函数有两个参数(item,index)，item是每一项，index是下标。index可以不写不用出处。
6. map 映射

   - 遍历数组的每一项，但是不会操作改变原数组，同filter一样会返回一个新的数组。回调函数返回的是什么，对应的新数组的那一项就会是什么
7. include 和 find
8. some 和 every

   - some和every是两个作用截然相反的方法。some遍历数组，找到true，即返回true，否则返回false；every则是找到false返回false，否则返回true
9. reduce

   - reduce是es5的方法，从数组的第一项开始逐步迭代至最后一项。reduce的参数可以有两个，第一个是一个回调函数（必需），函数参数可包括四个：prev，cur，index，arr。其中，prev是前一个迭代的值，cur是当前迭代的一项，index是当前一项的下标，arr则是迭代的原数组；reduce的第二个参数是传入的基础值，可不用。如果不用，迭代将从数组的第一项开始。

```js
// 
let arr = [1,2,3,4,5];
for(let i = 0;i < arr.length;i++){ 
    // do someing 
}
// 数组.forEach(function(item,index){},that)    
arr.forEach(function(item,index){
    // console.log(arr[i]);
},that);
// for in
arr.a = "key" // 数组添加使用属性
// arr = [1, 2, 3, 4, 5, a: "key"]
for(let key in arr){
    // do someing...
    console.log(typeof key)
    // 6个string
}    
// for of
for(let val of arr){
    console.log(val)
}
// filter 过滤
let newArr = [];
arr.a = "key"
let newArr = arr.filter(item => item>3); // es6
let newArr = arr.filter(item=> console.log(item))
let newArr = arr.filter(function(item,index){ // es5
    return item > 3;
})
let newArr = arr.filter(function(item,index){
    console.log(item)
})
console.log(newArr)
// map 映射
let newArr = arr.map(item=> console.log(item)) // es6
let newArr = arr.map(function(item){ // es5
    console.log(item)
})
// include(包含)和find
let res = arr.find(function(item,index){
    return item.toString().indexof(5) > -1
    console.log)(item)
})
console.log(res);
// some和every 遍历数组
// some 找值找到 true 返回 true
// every 找值找到 false 返回 false 
let sResult = arr.some(item=>item > 3);
// true 
let sArr = arr.some(item=> console.log(item))
console.log(sResult);
let eResult = arr.every(item => item > 0){
    console.log(eResult);
    // false
}
// reduce
```

#### 数组的奇特方法

## Boolean对象

`constructor prototype toString() valueOf()`
Boolean对象用于转换一个不是Boolearn类型的值转换为Boolean类型值（true）或（false）

### 新建Boolean对象

```js
var bool = new Boolearn(1)
var bool = new Boolearn(0)
```

对象属性

#### constructor `返回对创建此对象的 Boolean 函数的引用`

- boolean.constructor
- constructor   n. 构造函数；构造器；建造者

```js
var bool = new Boolean(0);
var x = bool.constructor;
console.log(x);
ƒ Boolean() { [native code] }
```

#### prototype `使您有能力向对象添加属性和方法。`

- 当构造一个原型，所有的布尔对象默认都添加了属性或方法。
- 定义：Boolean.prototype.name=value（function(){}）
- 使用：boolean.name()

```js
Boolean.prototype.myColor = function(){
     if(this.valueOf() == true){
            this.color = 'green';
      }
      else{
            this.color = 'red';
       }
}
var a = new Boolean(1);
a.myColor();
console.log(a.color);
```

对象方法`toSting() 转为字符串 valueOf() 返回原始值`

#### toString() 布尔值转为字符串，并返回结果

- boolean.toString()
- 数据类型是字符串

```js
var bool2 = new Boolean(0);
var myvar2 = bool2.toString();
console.log(myvar2);
console.log(typeof(myvar2));
```

#### valueOf() 返回 Boolean 对象的原始值

- boolean.valueOf()
- 数据类型还是布尔值

```js
 var bool = new Boolean(1);
var myvar = bool.valueOf();
console.log(myvar);
console.log(typeof (myvar));
```

### Boolean对象属性 `2`

| 属性                                                         | 描述                                  |
| :----------------------------------------------------------- | :------------------------------------ |
| [constructor](https://www.runoob.com/jsref/jsref-constructor-boolean.html) | 返回对创建此对象的 Boolean 函数的引用 |
| [prototype](https://www.runoob.com/jsref/jsref-prototype-boolean.html) | 使您有能力向对象添加属性和方法。      |

### Boolean对象方法 `2`

| 方法                                                         | 描述                               |
| :----------------------------------------------------------- | :--------------------------------- |
| [toString()](https://www.runoob.com/jsref/jsref-tostring-boolean.html) | 把布尔值转换为字符串，并返回结果。 |
| [valueOf()](https://www.runoob.com/jsref/jsref-valueof-boolean.html) | 返回 Boolean 对象的原始值。        |

## Date 对象

Date 对象用于处理日期与时间。

### 创建 Date 对象

以下四种方法同样可以创建 Date 对象：

```js
var d = new Date();
var d = new Date(milliseconds);
var d = new Date(dateString);
var d = new Date(year, month, day, hours, minutes, seconds, milliseconds);
```

### Date 对象属性

| 属性                                                         | 描述                                 |
| :----------------------------------------------------------- | :----------------------------------- |
| [constructor](https://www.runoob.com/jsref/jsref-constructor-date.html) | 返回对创建此对象的 Date 函数的引用。 |
| [prototype](https://www.runoob.com/jsref/jsref-prototype-date.html) | 使您有能力向对象添加属性和方法。     |

### Date 对象方法

> - 年月日时分秒：getFullYear()、Month()、Day()、Hours()、Minutes()、Seconds()、MilliSeconds()
>
> | 方法                                                         | 描述                                                         |
> | :----------------------------------------------------------- | :----------------------------------------------------------- |
> | [getDate()](https://www.runoob.com/jsref/jsref-getdate.html) | 从 Date 对象返回一个月中的某一天 (1 ~ 31)。                  |
> |                                                              |                                                              |
> | [getFullYear()](https://www.runoob.com/jsref/jsref-getfullyear.html) | 从 Date 对象以四位数字返回年份。                             |
> | [getMonth()](https://www.runoob.com/jsref/jsref-getmonth.html) | 从 Date 对象返回月份 (0 ~ 11)。                              |
> | [getDay()](https://www.runoob.com/jsref/jsref-getday.html)   | 从 Date 对象返回一周中的某一天 (0 ~ 6)。                     |
> | [getHours()](https://www.runoob.com/jsref/jsref-gethours.html) | 返回 Date 对象的小时 (0 ~ 23)。                              |
> | [getMinutes()](https://www.runoob.com/jsref/jsref-getminutes.html) | 返回 Date 对象的分钟 (0 ~ 59)。                              |
> | [getSeconds()](https://www.runoob.com/jsref/jsref-getseconds.html) | 返回 Date 对象的秒数 (0 ~ 59)。                              |
> | [getMilliseconds()](https://www.runoob.com/jsref/jsref-getmilliseconds.html) | 返回 Date 对象的毫秒(0 ~ 999)。                              |
> |                                                              |                                                              |
> | [getTime()](https://www.runoob.com/jsref/jsref-gettime.html) | 返回 1970 年 1 月 1 日至今的毫秒数。                         |
> |                                                              |                                                              |
> | [getTimezoneOffset()](https://www.runoob.com/jsref/jsref-gettimezoneoffset.html) | 返回本地时间与格林威治标准时间 (GMT) 的分钟差。              |
> |                                                              |                                                              |
> | [getUTCDate()](https://www.runoob.com/jsref/jsref-getutcdate.html) | 根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。              |
> | [getUTCFullYear()](https://www.runoob.com/jsref/jsref-getutcfullyear.html) | 根据世界时从 Date 对象返回四位数的年份。                     |
> | [getUTCMonth()](https://www.runoob.com/jsref/jsref-getutcmonth.html) | 根据世界时从 Date 对象返回月份 (0 ~ 11)。                    |
> | [getUTCDay()](https://www.runoob.com/jsref/jsref-getutcday.html) | 根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。               |
> | [getUTCHours()](https://www.runoob.com/jsref/jsref-getutchours.html) | 根据世界时返回 Date 对象的小时 (0 ~ 23)。                    |
> | [getUTCMinutes()](https://www.runoob.com/jsref/jsref-getutcminutes.html) | 根据世界时返回 Date 对象的分钟 (0 ~ 59)。                    |
> | [getUTCSeconds()](https://www.runoob.com/jsref/jsref-getutcseconds.html) | 根据世界时返回 Date 对象的秒钟 (0 ~ 59)。                    |
> | [getUTCMilliseconds()](https://www.runoob.com/jsref/jsref-getutcmilliseconds.html) | 根据世界时返回 Date 对象的毫秒(0 ~ 999)。                    |
> |                                                              |                                                              |
> | getYear()                                                    | 已废弃。 请使用 getFullYear() 方法代替。                     |
> | [parse()](https://www.runoob.com/jsref/jsref-parse.html)     | 返回1970年1月1日午夜到指定日期（字符串）的毫秒数。           |
> | [setDate()](https://www.runoob.com/jsref/jsref-setdate.html) | 设置 Date 对象中月的某一天 (1 ~ 31)。                        |
> | [setFullYear()](https://www.runoob.com/jsref/jsref-setfullyear.html) | 设置 Date 对象中的年份（四位数字）。                         |
> | [setHours()](https://www.runoob.com/jsref/jsref-sethours.html) | 设置 Date 对象中的小时 (0 ~ 23)。                            |
> | [setMilliseconds()](https://www.runoob.com/jsref/jsref-setmilliseconds.html) | 设置 Date 对象中的毫秒 (0 ~ 999)。                           |
> | [setMinutes()](https://www.runoob.com/jsref/jsref-setminutes.html) | 设置 Date 对象中的分钟 (0 ~ 59)。                            |
> | [setMonth()](https://www.runoob.com/jsref/jsref-setmonth.html) | 设置 Date 对象中月份 (0 ~ 11)。                              |
> | [setSeconds()](https://www.runoob.com/jsref/jsref-setseconds.html) | 设置 Date 对象中的秒钟 (0 ~ 59)。                            |
> | [setTime()](https://www.runoob.com/jsref/jsref-settime.html) | setTime() 方法以毫秒设置 Date 对象。                         |
> | [setUTCDate()](https://www.runoob.com/jsref/jsref-setutcdate.html) | 根据世界时设置 Date 对象中月份的一天 (1 ~ 31)。              |
> | [setUTCFullYear()](https://www.runoob.com/jsref/jsref-setutcfullyear.html) | 根据世界时设置 Date 对象中的年份（四位数字）。               |
> | [setUTCHours()](https://www.runoob.com/jsref/jsref-setutchours.html) | 根据世界时设置 Date 对象中的小时 (0 ~ 23)。                  |
> | [setUTCMilliseconds()](https://www.runoob.com/jsref/jsref-setutcmilliseconds.html) | 根据世界时设置 Date 对象中的毫秒 (0 ~ 999)。                 |
> | [setUTCMinutes()](https://www.runoob.com/jsref/jsref-setutcminutes.html) | 根据世界时设置 Date 对象中的分钟 (0 ~ 59)。                  |
> | [setUTCMonth()](https://www.runoob.com/jsref/jsref-setutcmonth.html) | 根据世界时设置 Date 对象中的月份 (0 ~ 11)。                  |
> | [setUTCSeconds()](https://www.runoob.com/jsref/jsref-setutcseconds.html) | setUTCSeconds() 方法用于根据世界时 (UTC) 设置指定时间的秒字段。 |
> | setYear()                                                    | 已废弃。请使用 setFullYear() 方法代替。                      |
> | [toDateString()](https://www.runoob.com/jsref/jsref-todatestring.html) | 把 Date 对象的日期部分转换为字符串。                         |
> | toGMTString()                                                | 已废弃。请使用 toUTCString() 方法代替。                      |
> | [toISOString()](https://www.runoob.com/jsref/jsref-toisostring.html) | 使用 ISO 标准返回字符串的日期格式。                          |
> | [toJSON()](https://www.runoob.com/jsref/jsref-tojson.html)   | 以 JSON 数据格式返回日期字符串。                             |
> | [toLocaleDateString()](https://www.runoob.com/jsref/jsref-tolocaledatestring.html) | 根据本地时间格式，把 Date 对象的日期部分转换为字符串。       |
> | [toLocaleTimeString()](https://www.runoob.com/jsref/jsref-tolocaletimestring.html) | 根据本地时间格式，把 Date 对象的时间部分转换为字符串。       |
> | [toLocaleString()](https://www.runoob.com/jsref/jsref-tolocalestring.html) | 据本地时间格式，把 Date 对象转换为字符串。                   |
> | [toString()](https://www.runoob.com/jsref/jsref-tostring-date.html) | 把 Date 对象转换为字符串。                                   |
> | [toTimeString()](https://www.runoob.com/jsref/jsref-totimestring.html) | 把 Date 对象的时间部分转换为字符串。                         |
> | [toUTCString()](https://www.runoob.com/jsref/jsref-toutcstring.html) | 根据世界时，把 Date 对象转换为字符串。实例：`var today = new Date(); var UTCstring = today.toUTCString();` |
> | [UTC()](https://www.runoob.com/jsref/jsref-utc.html)         | 根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。        |
> | [valueOf()](https://www.runoob.com/jsref/jsref-valueof-date.html) | 返回 Date 对象的原始值。                                     |

## Math对象

Math对象用于执行数学任务

### Math 对象属性

| 属性                                                       | 描述                                                    |
| :--------------------------------------------------------- | :------------------------------------------------------ |
| [E](https://www.runoob.com/jsref/jsref-e.html)             | 返回算术常量 e，即自然对数的底数（约等于2.718）。       |
| [LN2](https://www.runoob.com/jsref/jsref-ln2.html)         | 返回 2 的自然对数（约等于0.693）。                      |
| [LN10](https://www.runoob.com/jsref/jsref-ln10.html)       | 返回 10 的自然对数（约等于2.302）。                     |
| [LOG2E](https://www.runoob.com/jsref/jsref-log2e.html)     | 返回以 2 为底的 e 的对数（约等于 1.4426950408889634）。 |
| [LOG10E](https://www.runoob.com/jsref/jsref-log10e.html)   | 返回以 10 为底的 e 的对数（约等于0.434）。              |
| [PI](https://www.runoob.com/jsref/jsref-pi.html)           | 返回圆周率（约等于3.14159）。                           |
| [SQRT1_2](https://www.runoob.com/jsref/jsref-sqrt1-2.html) | 返回 2 的平方根的倒数（约等于 0.707）。                 |
| [SQRT2](https://www.runoob.com/jsref/jsref-sqrt2.html)     | 返回 2 的平方根（约等于 1.414）。                       |

### Math 对象方法

> - max()、min()
> - random() 
> - floor 向下舍入 ceil  向上舍入 round 四舍五入
>
> | 方法                                                         | 描述                                                         |
> | :----------------------------------------------------------- | :----------------------------------------------------------- |
> | [abs(x)](https://www.runoob.com/jsref/jsref-abs.html)        | 返回 x 的绝对值。                                            |
> | [acos(x)](https://www.runoob.com/jsref/jsref-acos.html)      | 返回 x 的反余弦值。                                          |
> | [asin(x)](https://www.runoob.com/jsref/jsref-asin.html)      | 返回 x 的反正弦值。                                          |
> | [atan(x)](https://www.runoob.com/jsref/jsref-atan.html)      | 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。     |
> | [atan2(y,x)](https://www.runoob.com/jsref/jsref-atan2.html)  | 返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。 |
> |                                                              |                                                              |
> | [ceil(x)](https://www.runoob.com/jsref/jsref-ceil.html)      | 对数进行上舍入。                                             |
> | [cos(x)](https://www.runoob.com/jsref/jsref-cos.html)        | 返回数的余弦。                                               |
> | [exp(x)](https://www.runoob.com/jsref/jsref-exp.html)        | 返回 Ex 的指数。                                             |
> | [floor(x)](https://www.runoob.com/jsref/jsref-floor.html)    | 对 x 进行下舍入。                                            |
> | [log(x)](https://www.runoob.com/jsref/jsref-log.html)        | 返回数的自然对数（底为e）。                                  |
> | [max(x,y,z,...,n)](https://www.runoob.com/jsref/jsref-max.html) | 返回 x,y,z,...,n 中的最高值。                                |
> | [min(x,y,z,...,n)](https://www.runoob.com/jsref/jsref-min.html) | 返回 x,y,z,...,n中的最低值。                                 |
> | [pow(x,y)](https://www.runoob.com/jsref/jsref-pow.html)      | 返回 x 的 y 次幂。                                           |
> | [random()](https://www.runoob.com/jsref/jsref-random.html)   | 返回 0 ~ 1 之间的随机数。                                    |
> | [round(x)](https://www.runoob.com/jsref/jsref-round.html)    | 四舍五入。                                                   |
> | [sin(x)](https://www.runoob.com/jsref/jsref-sin.html)        | 返回数的正弦。                                               |
> | [sqrt(x)](https://www.runoob.com/jsref/jsref-sqrt.html)      | 返回数的平方根。                                             |
> | [tan(x)](https://www.runoob.com/jsref/jsref-tan.html)        | 返回角的正切。                                               |

## Number对象

### Number `浮点型类型`

### JavaScript 只有一种数字类型

不使用小数点可以，使用小数点可以

```js
 const num = 123
 const num = 123.1223
```

极大或极小数的数字可通过科学（指数）计数法

```js
 const num = 123e5; //12300000
 const num = 123e-5;0.00123
```

### JavaScript数字为64位 `在JavaScript中，数字不分为整数类型和浮点型类型，所有的数字都是由 浮点型类型。`

JavaScript 不是类型语言。与许多其他编程语言不同，JavaScript 不定义不同类型的数字，比如整数、短、长、浮点等等。
在JavaScript中，数字不分为整数类型和浮点型类型，所有的数字都是由 浮点型类型。

### 精度

整数（不使用小数点或指数计数法）最多为 15 位。

```js
 var x = 999999999999999; //15  // x 为 999999999999999  15位
 var y = 9999999999999999;//16  // y 为 10000000000000000  17位
```

小数的最大位数是 17，但是浮点运算并不总是 100% 准确：

```js
 var x = 0.2+0.1; // 输出结果为 0.30000000000000004
```

### 特殊值

#### 无穷大（infinity）`是一个数字  -infinity 负无穷大`

当数字运算结果超过了JavaScript所能表示的数字上限（溢出），结果为一个特殊的无穷大（infinity）值
当负数的值超过了JavaScript所能表示的负数范围，结果为负无穷大

#### 非数字值（NaN）`true =>不是数字 false =>是数字`

```js
isNaN（是不是数字） 全局函数判断一个值是否是NaN值（即使数字）是数字返回false 不是数字返回true
 console.log(isNaN(999/0)); // 返回false 是一个数字 除以0是无穷大，无穷大是一个数字:
 console.log(isNaN(-999/0)); // 返回false 是一个数字 除以0是无穷大，负无穷大是一个数字: -Infinity
```

### 进制

二进制、八进制、十进制、十六进制

```js
使用 toString() 方法 输出16进制、8进制、2进制 toString(要装换的进制数)
 const num = 12
 console.log(num.toString(2))
 console.log(num.toString(8))
 console.log(num.toString(10))
 console.log(num.toString(16))
```

### 创建Number 对象

Number 对象是原始数值的包装对象。
Number 创建方式 new Number()。

```
var num = new Number(value);
```

**注意：** 如果一个参数值不能转换为一个数字将返回 NaN (非数字值)。

### Number 对象属性

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [constructor](https://www.runoob.com/jsref/jsref-constructor-number.html) | 返回对创建此对象的 Number 函数的引用。                       |
| [MAX_VALUE](https://www.runoob.com/jsref/jsref-max-value.html) | 可表示的最大的数。                                           |
| [MIN_VALUE](https://www.runoob.com/jsref/jsref-min-value.html) | 可表示的最小的数。                                           |
| [NEGATIVE_INFINITY](https://www.runoob.com/jsref/jsref-negative-infinity.html) | 负无穷大，溢出时返回该值。                                   |
| [NaN](https://www.runoob.com/jsref/jsref-number-nan.html)    | 非数字值。                                                   |
| [POSITIVE_INFINITY](https://www.runoob.com/jsref/jsref-positive-infinity.html) | 正无穷大，溢出时返回该值。                                   |
| [prototype](https://www.runoob.com/jsref/jsref-prototype-num.html) | 允许您可以向对象添加属性和方法。                             |
|                                                              |                                                              |
| ES6新增                                                      |                                                              |
| EPSILON                                                      | 表示 1 和比最接近 1 且大于 1 的最小 Number 之间的差别        |
| MIN_SAFE_INTEGER/MAX_SAFE_INTEGER                            | 表示在 JavaScript中最小的安全的 integer 型数字 (`-(253 - 1)`)。// 表示在 JavaScript 中最大的安全整数（`253 - 1`） |

### Number 对象方法

| 方法                                                         | 描述                                                 |
| :----------------------------------------------------------- | :--------------------------------------------------- |
| [isFinite](https://www.runoob.com/jsref/jsref-isfinite-number.html) | 检测指定参数是否为无穷大。                           |
|                                                              |                                                      |
| [toExponential(x)](https://www.runoob.com/jsref/jsref-toexponential.html) | 把对象的值转换为指数计数法。                         |
| [toFixed(x)](https://www.runoob.com/jsref/jsref-tofixed.html) | 把数字转换为字符串，结果的小数点后有指定位数的数字。 |
| [toPrecision(x)](https://www.runoob.com/jsref/jsref-toprecision.html) | 把数字格式化为指定的长度。                           |
| [toString()](https://www.runoob.com/jsref/jsref-tostring-number.html) | 把数字转换为字符串，使用指定的基数。                 |
| [valueOf()](https://www.runoob.com/jsref/jsref-valueof-number.html) | 返回一个 Number 对象的基本数字值。                   |
|                                                              |                                                      |
| ES6新增                                                      |                                                      |
| isInterger()                                                 | 用来判断给定的参数是否为整数。                       |
| isSafeInteger()                                              | 判断传入的参数值是否是一个"安全整数"                 |

> var x = Number.EPSILON;  var y = Number.MIN_SAFE_INTEGER;  var z = Number.MAX_SAFE_INTEGER;
>
> Number.isInteger() 在参数是整数时返回 true。
>
> Number.isInteger(10);        // 返回 true Number.isInteger(10.5);      // 返回 false
>
> Number.isSafeInteger()判断传入的参数值是否是一个"安全整数"。
>
> 安全整数范围为 `-(253 - 1)到` `253 - 1 `之间的整数，包含 `-(253 - 1)和` `253 - 1`。
>
> Number.isSafeInteger(10);    // 返回 true Number.isSafeInteger(12345678901234567890);  // 返回 false

## String对象

字符串属性

| 属性                | 描述                                                         |
| :------------------ | :----------------------------------------------------------- |
| constructor         | 返回创建字符串属性的函数                                     |
| length              | 返回字符串的长度                                             |
| prototype           | 允许您向对象添加属性和方法                                   |
| 字符串方法          |                                                              |
| 方法                | 描述                                                         |
| :------------------ | :----------------------------------------------------------- |
| charAt()            | 返回指定索引位置的字符                                       |
| charCodeAt()        | 返回指定索引位置字符的 Unicode 值                            |
| concat()            | 连接两个或多个字符串，返回连接后的字符串                     |
| fromCharCode()      | 将 Unicode 转换为字符串                                      |
| indexOf()           | 返回字符串中检索指定字符第一次出现的位置                     |
| lastIndexOf()       | 返回字符串中检索指定字符最后一次出现的位置                   |
| localeCompare()     | 用本地特定的顺序来比较两个字符串                             |
| match()             | 找到一个或多个正则表达式的匹配                               |
| replace()           | 替换与正则表达式匹配的子串                                   |
| search()            | 检索与正则表达式相匹配的值                                   |
| slice()             | 提取字符串的片断，并在新的字符串中返回被提取的部分           |
| split()             | 把字符串分割为子字符串数组                                   |
| substr()            | 从起始索引号提取字符串中指定数目的字符                       |
| substring()         | 提取字符串中两个指定的索引号之间的字符                       |
| toLocaleLowerCase() | 根据主机的语言环境把字符串转换为小写，只有几种语言（如土耳其语）具有地方特有的大小写映射 |
| toLocaleUpperCase() | 根据主机的语言环境把字符串转换为大写，只有几种语言（如土耳其语）具有地方特有的大小写映射 |
| toLowerCase()       | 把字符串转换为小写                                           |
| toString()          | 返回字符串对象值                                             |
| toUpperCase()       | 把字符串转换为大写                                           |
| trim()              | 移除字符串首尾空白                                           |
| valueOf()           | 返回某个字符串对象的原始值                                   |

## RegExp对象

正则表达式是描述字符模式的对象
正则表达式用于对字符串模式匹配及检索替换，是对字符串执行模式匹配的强大工具

### 正则表达式

修饰符
方括号
元字符
量词

### RegExp 对象方法

### RegExp 对象属性

支持正则表达式的string 对象的方法

### 全局属性/函数

JavaScript 全局属性和方法可用于创建Javascript对象。
JavaScript 全局属性

| 属性                                                         | 描述                                               |
| :----------------------------------------------------------- | :------------------------------------------------- |
| [Infinity](https://www.runoob.com/jsref/jsref-infinity.html) | 代表正的无穷大的数值。                             |
| [NaN](https://www.runoob.com/jsref/jsref-nan.html)           | 指示某个值是不是数字值。                           |
| [undefined](https://www.runoob.com/jsref/jsref-undefined.html) | 指示未定义的值。                                   |
| JavaScript 全局函数                                          |                                                    |
| 函数                                                         | 描述                                               |
| :----------------------------------------------------------- | :------------------------------------------------- |
| [decodeURI()](https://www.runoob.com/jsref/jsref-decodeuri.html) | 解码某个编码的 URI。                               |
| [decodeURIComponent()](https://www.runoob.com/jsref/jsref-decodeuricomponent.html) | 解码一个编码的 URI 组件。                          |
| [encodeURI()](https://www.runoob.com/jsref/jsref-encodeuri.html) | 把字符串编码为 URI。                               |
| [encodeURIComponent()](https://www.runoob.com/jsref/jsref-encodeuricomponent.html) | 把字符串编码为 URI 组件。                          |
| [escape()](https://www.runoob.com/jsref/jsref-escape.html)   | 对字符串进行编码。                                 |
| [eval()](https://www.runoob.com/jsref/jsref-eval.html)       | 计算 JavaScript 字符串，并把它作为脚本代码来执行。 |
| [isFinite()](https://www.runoob.com/jsref/jsref-isfinite.html) | 检查某个值是否为有穷大的数。                       |
| [isNaN()](https://www.runoob.com/jsref/jsref-isnan.html)     | 检查某个值是否是数字。                             |
| [Number()](https://www.runoob.com/jsref/jsref-number.html)   | 把对象的值转换为数字。                             |
| [parseFloat()](https://www.runoob.com/jsref/jsref-parsefloat.html) | 解析一个字符串并返回一个浮点数。                   |
| [parseInt()](https://www.runoob.com/jsref/jsref-parseint.html) | 解析一个字符串并返回一个整数。                     |
| [String()](https://www.runoob.com/jsref/jsref-string.html)   | 把对象的值转换为字符串。                           |
| [unescape()](https://www.runoob.com/jsref/jsref-unescape.html) | 对由 escape() 编码的字符串进行解码。               |

## Error 对象

Error对象在错误发生时提供了错误的提示信息
JavaScript 错误：throw、try、catch

### Error 对象属性

| 属性                                                         | 描述                           |
| :----------------------------------------------------------- | :----------------------------- |
| [name](https://www.runoob.com/jsref/prop-error-name.html)    | 设置或返回一个错误名           |
| [message](https://www.runoob.com/jsref/prop-error-message.html) | 设置或返回一个错误信息(字符串) |

## JSON对象



## 全局属性/函数

JavaScript 全局属性和方法可用于创建Javascript对象。

### 全局属性

| 属性                                                         | 描述                     |
| :----------------------------------------------------------- | :----------------------- |
| [Infinity](https://www.runoob.com/jsref/jsref-infinity.html) | 代表正的无穷大的数值。   |
| [NaN](https://www.runoob.com/jsref/jsref-nan.html)           | 指示某个值是不是数字值。 |
| [undefined](https://www.runoob.com/jsref/jsref-undefined.html) | 指示未定义的值。         |

### 全局函数

| 函数                                                         | 描述                                               |
| :----------------------------------------------------------- | :------------------------------------------------- |
| [decodeURI()](https://www.runoob.com/jsref/jsref-decodeuri.html) | 解码某个编码的 URI。                               |
| [decodeURIComponent()](https://www.runoob.com/jsref/jsref-decodeuricomponent.html) | 解码一个编码的 URI 组件。                          |
| [encodeURI()](https://www.runoob.com/jsref/jsref-encodeuri.html) | 把字符串编码为 URI。                               |
| [encodeURIComponent()](https://www.runoob.com/jsref/jsref-encodeuricomponent.html) | 把字符串编码为 URI 组件。                          |
| [escape()](https://www.runoob.com/jsref/jsref-escape.html)   | 对字符串进行编码。                                 |
| [eval()](https://www.runoob.com/jsref/jsref-eval.html)       | 计算 JavaScript 字符串，并把它作为脚本代码来执行。 |
| [isFinite()](https://www.runoob.com/jsref/jsref-isfinite.html) | 检查某个值是否为有穷大的数。                       |
| [isNaN()](https://www.runoob.com/jsref/jsref-isnan.html)     | 检查某个值是否是数字。                             |
| [Number()](https://www.runoob.com/jsref/jsref-number.html)   | 把对象的值转换为数字。                             |
| [parseFloat()](https://www.runoob.com/jsref/jsref-parsefloat.html) | 解析一个字符串并返回一个浮点数。                   |
| [parseInt()](https://www.runoob.com/jsref/jsref-parseint.html) | 解析一个字符串并返回一个整数。                     |
| [String()](https://www.runoob.com/jsref/jsref-string.html)   | 把对象的值转换为字符串。                           |
| [unescape()](https://www.runoob.com/jsref/jsref-unescape.html) | 对由 escape() 编码的字符串进行解码。               |

# DOM

DOM(Document Object Model) 文档对象模型

作用

- 改变页面中的所有HTML元素（innerHTML）
- 改变页面中的所有HTML 属性
- 改变页面中所有CSS样式
- 对页面中的HTML DOM事件做出反应
- 添加、修改或删除HTML元素

节点类型

- Document：顶层节点
- DocumentType：`doctype`标签
- Element：HTML标签 （元素节点）
- Attr：元素的属性（ 属性节点）
- Text：标签中的文本 （文本节点）
- Comment：注释  （注释节点）
- DocumentFragment：（文档片段）

节点树

- 第一个：文档类型节点`<!doctype html>`
- 第二个：顶层容器标签`<html>` 树结构的根节点（root node）

除了根节点，其他节点都有三种层级关系

- 父节点关系（parentNode）：直接的那个上级节点
- 子节点关系（childNodes）：直接的下级节点
  - `firstChild` 第一个子节点
  - `lastChilid` 最后一个子节点
- 同级节点关系（sibling）：拥有同一个父节点的节点
  - `nextSibling` 紧邻在后的同级节点
  - `previousSibling` 紧邻在前的那个同级节点

## DOM HTML



DOM查找方法

```js
// id 查找
document.getElementById("id")
// name属性获取节点
document.getElementByName('name')
// 标签名查找
document.getElementsByTagName("p")
// 使用 document.getElementsByTagName("p")[数组下标值]
// 类名查找
docuement.getElementsByClassName("class")
```

改变 HTML 元素的内容

- 改变HTML输出流 `document.write()`
- 改变HTML内容 `document.getElementById(id).innerHTML=新的HTML`
- 改变HTML属性 `document.getElementById(id).attribute=新属性值`
- 更改类名`className`

```html
 <h1 class="one" onclick="style.color='red'">Hello 你好</h1>
document.getElementsByTagName('html')[0].innerHTML ="Hell world"
```

### Document 节点

| 属性 / 方法                                                  | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| document.doctype                                             | 返回与文档相关的文档类型声明 (DTD)。                         |
| document.body                                                | 返回文档的body元素                                           |
| document.baseURI                                             | 返回文档的绝对基础 URI                                       |
| [document.documentURI](https://www.runoob.com/jsref/prop-document-documenturi.html) | 设置或返回文档的位置                                         |
| document.URL                                                 | 返回文档完整的URL                                            |
| document.cookie                                              | 设置或返回与当前文档有关的所有 cookie。                      |
| document.title                                               | 返回当前文档的标题。                                         |
| document.close()                                             | 关闭用 document.open() 方法打开的输出流，并显示选定的数据。  |
| document.write()                                             | 向文档写 HTML 表达式 或 JavaScript 代码。                    |
| document.writeln()                                           | 等同于 write() 方法，不同的是在每个表达式之后写一个换行符。  |
| [document.links](https://www.runoob.com/jsref/coll-doc-links.html) | 返回对文档中所有 Area 和 Link 对象引用。                     |
| [document.scripts](https://www.runoob.com/jsref/coll-doc-scripts.html) | 返回页面中所有脚本的集合。                                   |
| [document.open()](https://www.runoob.com/jsref/met-doc-open.html) | 打开一个流，以收集来自任何 document.write() 或 document.writeln() 方法的输出。 |
| document.lastModified                                        | 返回文档被最后修改的日期和时间。                             |
| [document.images](https://www.runoob.com/jsref/coll-doc-images.html) | 返回对文档中所有 Image 对象引用。                            |
| [document.domain](https://www.runoob.com/jsref/prop-doc-domain.html) | 返回当前文档的域名。                                         |
| [document.documentElement](https://www.runoob.com/jsref/prop-document-documentelement.html) | 返回文档的根节点                                             |
| [document.referrer](https://www.runoob.com/jsref/prop-doc-referrer.html) | 返回载入当前文档的文档的 URL。                               |
|                                                              |                                                              |
| document.addEventListener()                                  | 向文档添加句柄                                               |
| document.removeEventListener()                               | 移除文档中的事件句柄(由 addEventListener() 方法添加)         |

#### 创建DOM

| 属性 / 方法                                                  | 描述                                           |
| :----------------------------------------------------------- | :--------------------------------------------- |
| [document.createAttribute()](https://www.runoob.com/jsref/met-document-createattribute.html) | 创建一个属性节点                               |
| [document.createComment()](https://www.runoob.com/jsref/met-document-createcomment.html) | createComment() 方法可创建注释节点。           |
| [document.createDocumentFragment()](https://www.runoob.com/jsref/met-document-createdocumentfragment.html) | 创建空的 DocumentFragment 对象，并返回此对象。 |
| [document.createElement()](https://www.runoob.com/jsref/met-document-createelement.html) | 创建元素节点。                                 |
| [document.createTextNode()](https://www.runoob.com/jsref/met-document-createtextnode.html) | 创建文本节点。                                 |

#### 选择DOM

| 属性 / 方法                                                  | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| document.getElementById()                                    | 返回对拥有指定 id 的第一个对象的引用。                       |
| [document.getElementsByName()](https://www.runoob.com/jsref/met-doc-getelementsbyname.html) | 返回带有指定名称的对象集合。                                 |
| [document.getElementsByClassName()](https://www.runoob.com/jsref/met-document-getelementsbyclassname.html) | 返回文档中所有指定类名的元素集合，作为 NodeList 对象。       |
| [document.getElementsByTagName()](https://www.runoob.com/jsref/met-document-getelementsbytagname.html) | 返回带有指定标签名的对象集合。                               |
| [document.querySelector()](https://www.runoob.com/jsref/met-document-queryselector.html) | 返回文档中匹配指定的CSS选择器的第一元素                      |
| [document.querySelectorAll()](https://www.runoob.com/jsref/met-document-queryselectorall.html) | document.querySelectorAll() 是 HTML5中引入的新方法，返回文档中匹配的CSS选择器的所有元素节点列表 |

#### 其他DOM

| 属性 / 方法                                                  | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [document.implementation](https://www.runoob.com/jsref/prop-document-implementation.html) | 返回处理该文档的 DOMImplementation 对象。                    |
| [document.importNode()](https://www.runoob.com/jsref/met-document-importnode.html) | 把一个节点从另一个文档复制到该文档以便应用。                 |
| [document.inputEncoding](https://www.runoob.com/jsref/prop-document-inputencoding.html) | 返回用于文档的编码方式（在解析时）。                         |
|                                                              |                                                              |
|                                                              |                                                              |
| [document.normalize()](https://www.runoob.com/jsref/met-document-normalize.html) | 删除空文本节点，并连接相邻节点                               |
| [document.normalizeDocument()](https://www.runoob.com/jsref/met-document-normalizedocument.html) | 删除空文本节点，并连接相邻节点的                             |
|                                                              |                                                              |
| [document.readyState](https://www.runoob.com/jsref/prop-doc-readystate.html) | 返回文档状态 (载入中……)                                      |
|                                                              |                                                              |
| [document.renameNode()](https://www.runoob.com/jsref/met-document-renamenode.html) | 重命名元素或者属性节点。                                     |
|                                                              |                                                              |
| [document.documentMode](https://www.runoob.com/jsref/prop-doc-documentmode.html) | 返回用于通过浏览器渲染文档的模式                             |
| [document.activeElement](https://www.runoob.com/jsref/prop-document-activeelement.html) | 返回当前获取焦点元素                                         |
| [document.adoptNode(node)](https://www.runoob.com/jsref/met-document-adoptnode.html) | 从另外一个文档返回 adapded 节点到当前文档。                  |
| [document.anchors](https://www.runoob.com/jsref/coll-doc-anchors.html) | 返回对文档中所有 Anchor 对象的引用。                         |
| document.applets                                             | 返回对文档中所有 Applet 对象的引用。**注意:** HTML5 已不支持 <applet> 元素。 |
| [document.strictErrorChecking](https://www.runoob.com/jsref/prop-document-stricterrorchecking.html) | 设置或返回是否强制进行错误检查。                             |
| document.domConfig                                           | **已废弃**。返回 normalizeDocument() 被调用时所使用的配置。  |
| [document.embeds](https://www.runoob.com/jsref/coll-doc-embeds.html) | 返回文档中所有嵌入的内容（embed）集合                        |
| [document.forms](https://www.runoob.com/jsref/coll-doc-forms.html) | 返回对文档中所有 Form 对象引用。                             |

## DOM CSS

HTML DOM 允许 JavaScript 改变 CSS 

HTML DOM 允许我们通过触发事件来执行代码

- 元素被点击。
- 页面加载完成。
- 输入框被修改。

```html
document.getElementById(id).style.property=新样式
<h1 class="one">Hello 你好</h1>
<button type="button" onclick="document.getElementsByClassName('one')[0].style.color='red'">按钮</button>
document.getElementsByClassName('one')[0].style.display='none'
```

#### CSSStyleDeclaration

CSS 样式声明对象()
CSSStyleDeclaration 对象
CSSStyleDeclaration 对象表示一个 CSS 属性-值（property-value）对的集合。
CSSStyleDeclaration 对象属性

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [cssText](https://www.runoob.com/jsref/prop-cssstyle-csstext.html) | 设置或返回样式声明文本，cssText 对应的是 HTML 元素的 style 属性。 |
| [length](https://www.runoob.com/jsref/prop-cssstyle-length.html) | 返回样式中包含多少条声明。                                   |
| [parentRule](https://www.runoob.com/jsref/prop-cssstyle-parentrule.html) | 返回包含当前规则的规则。                                     |
| CSSStyleDeclaration 对象方法                                 |                                                              |
| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :------------------------------------------------            |
| [getPropertyPriority()](https://www.runoob.com/jsref/met-cssstyle-getpropertypriority.html) | 返回指定的 CSS 属性是否设置了 "important!" 属性。            |
| [getPropertyValue()](https://www.runoob.com/jsref/met-cssstyle-getpropertyvalue.html) | 返回指定的 CSS 属性值。                                      |
| [item()](https://www.runoob.com/jsref/met-cssstyle-item.html) | 通过索引方式返回 CSS 声明中的 CSS 属性名。                   |
| [removeProperty()](https://www.runoob.com/jsref/met-cssstyle-removeproperty.html) | 移除 CSS 声明中的 CSS 属性。                                 |
| [setProperty()](https://www.runoob.com/jsref/met-cssstyle-setproperty.html) | 在 CSS 声明块中新建或者修改 CSS 属性。                       |
| DOM CSS `Element.style.property=新样式`                      |                                                              |

```js
document.getElementById(id).style.property = 新样式
```

## DOM Element

- createElement\TextNode\DocumentFragment\Comment()
  - el.appendChild()
  - el.insertBefore()
- el.inner/out HTML/Text(‘html内容’)
- removeChild()



### DOM 增删改查

#### 添加节点

##### document.write()

```js
document.write("内容");
document.write("<h1>内容</h1>");		
```

##### create()

Element\TextNode\DocumentFragment\Comment()

|              create方法               | 功能                         | 参数     |
| :-----------------------------------: | ---------------------------- | -------- |
|     **document.createElement()**      | 创建``标签元素``             | 标签     |
|       document.createTextNode()       | 创建``文本节点``（添加文本） | 文本内容 |
| document.create**DocumentFragment()** | 创建``文档片段``             | 无       |
|     document.create**Comment()**      | 创建`注释节点`(很少动态创建) | 文本     |

##### appendChild()

方法，属性值没有双引号 装填到DOM树上

```js
<ul id="mylist"> </ul>
var ul = document.getElementById("mylist");
var li = document.createElement("li"); //创建标签元素
ul.appendChild(li); //appendChild() 属性值没有双引号
var txt = document.createTextNode("传递进去的文本"); //创建文本节点（添加文本）
li.appendChild(txt);

var ul = document.getElementById("mylist");
var fragment = document.createDocumentFragment(); //创建文档片段
var li = null;
for(var i = 0; i < 3;i++ ){
    li = document.createElement("li");
    li.appendChild(document.createTextNode("Item " + (i+1)));
    fragement.appendChild(li);
}
ul.appendChild(fragment);
var ul = document.getElementById("box");
var fragment = document.createDocumentFragment();
var comment = document.createComment("A comment"); //创建注释节点
var li = null;
for (var i = 0; i < 3; i++) {
    li = document.createElement("li");
    li.appendChild(document.createTextNode("Item " + (i + 1)));
    fragment.appendChild(li);
}
ul.appendChild(fragment);
document.body.insertBefore(comment, document.body.firstChild);
```

##### insertBefor()

(插入的节点，插入的位置）

```js
document.body.insertBefore(commert,document.body.firstChild);
```

```js
扩展：**document.createElement()**还能支持创建当前浏览器不支持的标签名，在IE6-8下，这是一个著名的hack。
// 立即调用的函数表达式，让代码在当前作用域下执行，不污染window环境
// IE不支持 html5元素 ，解决方案document.createElement()
(function(){
	if(！
     /*@cc_on!@*/  //如果是IE浏览器执行中间的代码，其他浏览器不执行 IE浏览器 ！！0 假 
      0) return;  //IE的功能 条件编译语句 其他浏览器 ！0 真 
    var e = "abbr,article,aside,audio,canvas,datalist,details,dialog,eventsource,figure,footer,header,hgroup,mark,menu,meter,nav,output,progress,section,time,video".split(', ');
    var i = e.length;
    while(i--){
        document.createElement(e[i]);
    }
})();
```

##### inner/out HTML/Text

（高效创建节点的方法 ）

| 方法      | 功能                                                         |      |
| --------- | ------------------------------------------------------------ | ---- |
| innerHTML | 用来设置或获取当前标签的起始和结束里面的内容**（html->DOM节点）** |      |
| outerHTML | 返回调用它的元素及所有子节点的HTML标签**(输出HMTL的内容)**   |      |
| innerText | 设置或获取位于对象起始和结束标签内的文本**(获取标签内的文本)** |      |
| outerText | 在标签内添加内容                                             |      |

- innerHTML 

```js
var content = document.getElement("content");
var str = "<h1>标题h1</h1>"
		+"<ul>"
		+"<li>li1</li>"
        +"<li>li2</li>"
        +"<li>li3</li>"
        +"<li>li4</li>"
		+"</ul>";
content.innerHTML = str;	

使用innerHTML的限制

字符串的最左边不能出现空白，IE6-8会自动移除掉它，chrome保存空格

大多数浏览器不**会对script标签进行脚本执行操作**，通过innerHTML插入html不会执行其脚本
//解决方法(大多数浏览器不支持，IE8及更早版本支持)
//1、为script标签添加defer属性
//2、script标签要在有作用域的元素之后 前面插入有作用域的元素（文本节点，元素节点）
// script(无作用域的元素) 
var str2 = "<script>alert("hello")<\/script>"; //需要转义字符
var str = "<input type=\"hidden\"><script defer>alert('hello');<\/script>"; //需要转义字符 alert要单引号，分号  type=\"hidden\" defer
不能单独创建meta、style、link等元素，一定要在前面加上一些字符
var content = document.getElement("content");
//innerHTML创建style
var str = "_<style type=\"text/css\">body{background:red;}</style>";
//IE8以及以前版本 
content.removeChild(content.firstChild); //删除有作用域的节点
```

- outerHTML

```js
content.outerHTML = "<p>HTML</p>" //写会覆盖原本的HTML DOM内容
```

- innerText //textContent()  某个标签元素添加内容 

```js
console.log(content.innerText) //打印Text文本
content.innerText = "<p>HTML</p>" //写会覆盖原本的HTML 直接输出<p>HTML</p>
// 火狐浏览器不支持innerText 支持textContent()
console.log(content,textContent);
content.textContent =  "<p>HTML</p>" //写会覆盖原本的HTML 直接输出<p>HTML</p>

// 通用方法(兼容所有浏览器)

var content = document.getElement("content");
// 读取
function getInnerText(element){
	return (typeof element.textContent == ”string“)?element.textContent:element.innerText;
}
// 写入
function setInnerText(element,text){
	if(typeof element.textContent == "string"){
		element.textContent = text;
	}else{
		element.innerText = text;
	}
}
setInnerText(content,"Hello World"); //写入
console.log(getInnerText(content));
```

- outerText (不建议使用该属性，会导致调用它的元素不存在)
  读取内容与innerText一样

```js
console.log(content.outerText());
content.outerText = "<p>HTML</p>"; //写入内容 会把原本的元素调用它的元素取消
```

#### 删除节点

- **removeChild()  删除某个节点中指定的子节点**
- removeNode()  ：IE的私有实现、将目标节点从文档中删除，返回目标节点、参数是布尔值，默认值是false
- innerHTML()
- deleteContents()
- textContent()

```js
<ul id="myUl">
    <li>1</li>
    <li>2</li>	
    <li>3</li>
</ul>    
//removeChild()  删除某个节点中指定的子节点
var myUl - document.getElementById("myUl");
var secondChild = myUl.removeChild(myUl.childNodes[1]);
console.log(secondChild);
var removedNode = myUl.removeNode(); // flase删除父节点 true删除包含父子元素
console.log(removedNode.outerHTML);
```

removerChild（） 与innerHTML（）比较

```js
<ul id="myUl">
	<li>1</li>
	<li>2</li>
	<li>3</li>
	<li>4</li>
</ul>
//removeChild()
var div = document.createELement("div");
console.log(div.parentNode); //null
document.body.removeChild(document.body.appendChild(div));
console.log(div.parentNode); //null
//innerHTML
document.body.innerHTML = "";
console.log(myUl.parentNode); //null
```

#### 查找节点

父节点查找子节点**
firstChild
lastClild
childNodes[1] 第二个节点
childNodes.item(1)

*子节点查找父节点**
parentNode

**兄弟节点**
nextSibling   //下一个
previousSibling //前一个

**子节点查找祖先节点 **
ownerDocument

**祖先节点查找子节点**

**判断是不有一个子节点**
hasChildNodes()
获取文本节点的个数
childNodes.length
head与body之间的空格也是一个文本节点
属性
**document.documentElement; 获取属性可返回文档的根节点 HTML元素**
document节点是文档的根节点
**tagName 属性返回元素的标签名**

```js
<p id="p">文本节点</p>
var oHTML = document,documentElement;
console.log(oHTML.tagName)
var p = document.getElementById("p");
var txt = p.childNodes[0];
console.log(p.ownerDocumen == document); //true
console.log(p.hasChildNodes()); //true 有文本叶子节点
console.log(txt.hasChildNodes()); //false
//一个节点（元素）内有文字是一个文本节点
```

```js
//遍历HTML树
window.onload = function(){
}
var s = "";
function travel(space,node){
	if(node.tagName){ //如果当前节点是标签，不是空的，就拼接字符串
		s += space + node.tagName + "</br>";
	}
	var len = node.childNodes.length; //保存当前节点的子节点
	for(var i = 0;i < len;i++){ //遍历节点的子节点
		travel(space + "|-",node.childNodes[i]);
	}
}
travel("",document);
document.write(s);
/*
输出结果
|-HTML
|-|-HEAD
|-|-|-META
|-|-|-META
|-|-|-TITLE
|-|-|-SCRIPT
|-|-BODY
|-|-|-DIV
|-|-|-|-P
|-|-|-SCRIPT
*/
```

空白的文本节点影响节点的内容 输出 #text
解决空白的文本节点纳入到子节点的计算范围内中（过滤文本节点）

```js
var box = doucment.getElementById("box");
for(var i = 0;i < box.childNodes.length;i < len;i++){
	console.log(box.childNodes[i]);
	//方法一
	if(box.childNodes[i].nodeType == 1){
		console.log(box.childNodes[i]);
	}
}
```

第二套api IE8以下不支持 IE9以上 火狐3.5以上 safari4以上 chrome opera10以上
![image-20200311122817471](C:\Users\Administrator\Desktop\StudyNote\blogphoto\image-20200311122817471.png)
firstElementChild
lastElementChild
children[0]
children[1]
nextElementSibling
previousElementSibling
childElementCount 数量个数

```js
//方法二
var box = doucment.getElementById("box");
for(var i = 0;i < box.childElementCount;i < len;i++){
	console.log(box.children[i]);
}
```

创建 `appendChild()添加新元素到尾部 和 insertBefore()将新元素添加到开始位置`

appendChild()  ==createElement('HTML元素')  + creatTextNode('文本内容') + 创建的HMTL元素.appendChild('文本内容')==

```
var p = createElement('h1'); // 创建一个
```

insertBefore()

```

```

删除 `removeChild()`

#### 修改节点

- appendChild() 为指定元素节点的最后一个子节点之后添加节点。该方法返回新的子节点。
- insertBefore(插入节点，位置)  在指定的已有子节点之前插入新的子节点
- replaceChild() 替换节点
- cloneChild()  创建节点的拷贝，并返回该副本
- normalize() 合并相邻的文本节点
- splitText() 按照指定的位置把文本节点分隔成为两个节点

```js
<ul id="myUl">
	<li>1</li>
	<li>2</li>
	<li>3</li>
</ul>
//appendChild()
var myUl = document.createELement("myUl");
var txt = document.createTextNode("4");
var li = document.createElement ("li");
li.appendChild(txt);
myUl.appendChild(li);
//i
```

#### 替换节点

replaceChild() 父元素.replaceChild(创建的元素（替换元素），被替换的元素)

>innerText 与 innerHTML的区别
>
>innerText 只是插入值
>
>innerHTML 插入HTML标签和值

3. 改变HTML属性 解释 html标签中属性，这种方法更改不了自定义的属性 `.attribute=新属性`

```js
docuemnt.getElementById(id).attribute=新属性
document.getElementById("image").src="landscape.jpg";
```

## DOM Console

Console 对象提供了访问浏览器调试模式的信息到控制台。

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [log()](https://www.runoob.com/jsref/met-console-log.html)   | 控制台输出一条信息                                           |
| [assert()](https://www.runoob.com/jsref/met-console-assert.html) | 如果断言为 false，则在信息到控制台输出错误信息。             |
| [clear()](https://www.runoob.com/jsref/met-console-clear.html) | 清除控制台上的信息。                                         |
| [count()](https://www.runoob.com/jsref/met-console-count.html) | 记录 count() 调用次数，一般用于计数。                        |
| [error()](https://www.runoob.com/jsref/met-console-error.html) | 输出错误信息到控制台                                         |
| [group()](https://www.runoob.com/jsref/met-console-group.html) | 在控制台创建一个信息分组。 一个完整的信息分组以 console.group() 开始，console.groupEnd() 结束 |
| [groupCollapsed()](https://www.runoob.com/jsref/met-console-groupcollapsed.html) | 在控制台创建一个信息分组。 类似 console.group() ，但它默认是折叠的。 |
| [groupEnd()](https://www.runoob.com/jsref/met-console-groupend.html) | 设置当前信息分组结束                                         |
| [info()](https://www.runoob.com/jsref/met-console-info.html) | 控制台输出一条信息                                           |
| [table()](https://www.runoob.com/jsref/met-console-table.html) | 以表格形式显示数据                                           |
| [time()](https://www.runoob.com/jsref/met-console-time.html) | 计时器，开始计时间，与 timeEnd() 联合使用，用于算出一个操作所花费的准确时间。 |
| [timeEnd()](https://www.runoob.com/jsref/met-console-timeend.html) | 计时结束                                                     |
| [trace()](https://www.runoob.com/jsref/met-console-trace.html) | 显示当前执行的代码在堆栈中的调用路径。                       |
| [warn()](https://www.runoob.com/jsref/met-console-warn.html) | 输出警告信息，信息最前面加一个黄色三角，表示警告             |

### 输出

| console.info  | 控制台输出一条信息                               |
| ------------- | ------------------------------------------------ |
| console.log   | 控制台输出一条信息                               |
| console.debug |                                                  |
| console.warm  | 输出警告信息，信息最前面加一个黄色三角，表示警告 |
| console.error | 输出错误信息到控制台                             |
| console.table | 以表格形式显示数据                               |

```js
console.table() 用于在控制台输出表格信息
第一个参数是必需的，且对象类型需要是对象或数组，对应的数据会填充到表格中。
console.table(tabledata, tablecolumns)
//一个值
默认index值为0~index-1
使用数组作为输出的信息：
console.table(["Google", "Runoob", "Taobao"]);
自定义index值为name和site 使用对象作为输出的信息：
console.table({ name : "菜鸟教程", site : "www.runoob.com" });
多列值  使用对象数组：
默认值index
var site1 = { name : "Runoob", site : "www.runoob.com" }
var site2 = { name : "Google", site : "www.google.com" }
var site3 = { name : "Taobao", site : "www.taobao.com" }
console.table([site1, site2, site3]);
指定表格表头标题名，参数只能是对应的键名：
var site1 = { name : "Runoob", site : "www.runoob.com" }
var site2 = { name : "Google", site : "www.google.com" }
var site3 = { name : "Taobao", site : "www.taobao.com" }
console.table([site1, site2, site3], ["site"]);
//可以调换标题栏的列的位置
var site1 = { name : "Runoob", site : "www.runoob.com" }
var site2 = { name : "Google", site : "www.google.com" }
var site3 = { name : "Taobao", site : "www.taobao.com" }
console.table([site1, site2, site3], ["name","site"]);
console.table([site1, site2, site3], ["site","name"]);
参数	类型	描述
tabledata	Array 或 Object	必需，填充到表格中的数据。 [] { }
tablecolumns	Array	可选，一个数组，表格标题栏的名称。[]
```

### 清除

```js
clear() //清除控制台上的信息
```

### 计数、计时

```js
time()  //计时器，开始计时间，与 timeEnd() 联合使用，用于算出一个操作所花费的准确时间。 计时器的起始方法
console.time(label)
参数说明
参数	类型	描述
label	String	可选，用于给计算器设置标签。
tablecolumns	Array	可选，一个数组，表格标题栏的名称。
label的作用是标记,计算
timeEnd() // 计时结束 计算器的结束方法
console.timeEnd(label)
console.time();
for (i = 0; i < 10; i++) {
  // 代码部分
}
console.timeEnd();
default: 0.009033203125ms
var i;
console.time("for 循环测试");
for (i = 0; i < 100000; i++) {
  // 代码部分
}
console.timeEnd("for 循环测试");
i = 0;
console.time("while 循环测试");
while (i < 1000000) {
  i++
}
console.timeEnd("while 循环测试");
VM1724:6 for 循环测试: 2.264892578125ms
VM1724:13 while 循环测试: 3.275146484375ms
count() //记录 count() 调用次数，一般用于计数。
console.count() 在调用时会将数字（调用次数）写入到控制台。
console.count() 方法可以添加标签。
带标签
console.count(label)
console.count("Runoob");
console.count("Runoob");
console.count("Runoob2");
Runoob: 1
Runoob: 2
Runoob2: 1
for (i = 0; i < 2; i++) {
    console.count("r");
    console.count("a");
}
r: 1
a: 1
r: 2
a: 2
for (i = 0; i < 3; i++) {
    console.count();
}
default: 1
default: 2
default: 3
参数	类型	描述
label	String	可选，如果有指定，则会在控制台上输出标签，该标签显示在调用次数之前。
```

### 信息分组  `group() `

```js
group()	//在控制台创建一个信息分组。 一个完整的信息分组以 console.group() 开始，
设置分组信息的起始位置，该位置之后的所有信息将写入分组。
console.group(label)
为信息分组设置标签：
console.log("Runoob");
console.group("RunoobLabel");
console.log("我在指定标签分组里。");
console.groupEnd() 结束 跳出分组
console.log("Runoob");
console.group();
console.log("Runoob，这个在分组里面。");
VM2594:1 Runoob
VM2594:2 console.group
VM2594:3 Runoob，这个在分组里面。
groupCollapsed()	//在控制台创建一个信息分组。 类似 console.group() ，但它默认是折叠的。  隐藏分组信息。、折叠分组信息：
console.groupCollapsed(label)
参数	类型	描述
label	String	可选，分组标签。
为信息分组设置标签：
console.log("Runoob");
console.groupCollapsed("RunoobLabel");
console.log("我在指定标签分组里。");
groupEnd()	//设置当前信息分组结束 结束当前的分组。
```

### 其他

```js
assert()	//如果断言为 false，则在信息到控制台输出错误信息。
console.assert(document.getElementById("demo"), "没有 ID 为 'demo' 的元素");
Assertion failed: 没有 ID 为 'demo' 的元素
console.assert() 方法在第一个参数为 false 的情况下会在控制台输出信息。
console.assert(expression, message)
参数	类型	描述
表达式	布尔值表达式	必需。布尔表达式，返回 true 或 false。
信息	字符串或对象	必需。 要写到控制台的信息或对象。
console.assert(true,'这个的值是真')
console.assert(false,'这个的值是假')
Assertion failed: 这个的值是假
trace()	//显示当前执行的代码在堆栈中的调用路径。
console.trace(label)
function myFunction() {
  myOtherFunction();
}
function myOtherFunction() {
  console.trace();
}
myFunction();
console.trace
myOtherFunction @ VM2401:6
myFunction @ VM2401:2
(anonymous) @ VM2401:8
```

### Console.log  

添加样式 `%c 样式 %s 信息`

https://juejin.im/post/5bfd4e9de51d457edf4095c7

```jsp
console.log('%cHello', 'color: green; background: yellow: font-size: 30px');
```

log语句由三部分组成： **%c** + message + **style** 其中标 识符后紧跟message, 第二个参数为样式 最后输出的message的效果就如样式所定义的一致。

```js
console.log('%cconsole.log', 'color: green;');
console.info('%cconsole.info', 'color: green;');
console.debug('%cconsole.debug', 'color: green;');
console.warn('%cconsole.warn', 'color: green;');
console.error('%cconsole.error', 'color: green;');
```

```js
// 1. 将css样式内容放入数组
const styles = [
  'color: green', 
  'background: yellow', 
  'font-size: 30px',
  'border: 1px solid red',
  'text-shadow: 2px 2px black',
  'padding: 10px',
].join(';'); 
// 2. 利用join方法讲各项以分号连接成一串字符串
// 3. 传入styles变量
console.log('%cHello There', styles);
```

把需要输出的message也抽离出来，保存在变量中

```js
const styles = ['color: green', 'background: yellow'].join(';');
const message = 'Some Important Message Here';
// 3. 传入styles和message变量
console.log('%c%s', styles, message);
```

## 接口和节点

### 接口

#### Node 接口

属性

|                       |      |
| --------------------- | ---- |
| nodeType              |      |
| nodeName              |      |
| nodeValue             |      |
| textContent           |      |
| baseURI               |      |
| ownerDocument         |      |
| nextSibling           |      |
| previousSibling       |      |
| parentNode            |      |
| parentElement         |      |
| firstChild、lastChild |      |
| childNodes            |      |
| isConnected           |      |

方法

|                           |      |
| ------------------------- | ---- |
| appendChild()             |      |
| hasChildNodes             |      |
| cloneNode()               |      |
| insertBefore()            |      |
| removeChild()             |      |
| replaceChild()            |      |
| contains()                |      |
| compareDocumentPosition() |      |
|                           |      |
|                           |      |

#### NodeList 接口

NodeList实例是一个类似数组的对象，它的成员是节点对象，可以包含各种类型的节点

搜索方法

- Node.childNodes
- document.querySelectorAll()

```

```

| 函数                      | 作用               |
| ------------------------- | ------------------ |
| length                    | 节点数列           |
| forEach                   | 遍历NodeList的所有 |
| item                      |                    |
| keys() values() entries() |                    |

`NodeList 对象是一个从文档中获取的节点列表 (集合) 。`

- NodeList 对象是一个从文档中获取的节点列表（集合）
- 节点列表不是一个数组，但是可以使用索引来获取元素，无法使用数组的方法
- length属性定义了节点列表中元素的数量
- length 属性常用于遍历节点列表
  一些旧版本浏览器中的方法（如：**getElementsByClassName()**）返回的是 NodeList 对象，而不是 HTMLCollection 对象。
  所有浏览器的 **childNodes** 属性返回的是 NodeList 对象。
  大部分浏览器的 **querySelectorAll()** 返回 NodeList 对象。

```js
document.querySelector("body").childNodes
var myNodeList = document.querySelectorAll('p')
y = myNodeList[1];
length = myNodeList.length
```

修改节点列表中所有 `<p>` 元素的背景颜色

```js
var myNodelist = document.querySelectorAll("p");
for (var i = 0; i < myNodelist.length; i++) {
    myNodelist[i].style.backgroundColor = "red";
}
var myNodeList = document.querySelectorAll('a')
for(var i = 0;i < myNodeList.length;i++){
    myNodeList[i].style.backgroundColor = 'pink'
}
```

 Nodelist对象的特点

- NodeList是一种**类数组对象**，用来保存一组有序的节点
- 可以通过方括号语法来访问NodeList的值，有**item方法与length属性**
- 它并不是Array的实例，**没有数组对象的方法**

```js
var box = doucument.getElementById("box");
var nodes = box.childNodes;
console.log(nodes);
console.log(nodes[1]); console.log(nodes.item[1]);
//  nodelist ---->array
function makeArray(nodeList){
    try{
        return Array.prototype.slice.call(nodeList); //解决IE浏览器不兼容的方法
    }catch(e){
        var arr = new Array();
        for(var i = 0,len = nodeList.length;i < len;i++){
            arr.push(nodeList[i]);
        }
        return arr;
    }   
}
var newNodeList = makeArray(nodes);
newNodeList.push("<li>节点四</li>");
console.log(newNodeList)
```

类数组对象HTMLCollection

- Ele.getElementsByTagName()
- document.script //script
- document.link //a标签
- document.images //images
- document.forms //forms表单
- tr.cells //td
- select.options //选项

```
console.log();
console.log();
console.log();
console.log();
console.log();
```

**类数组对象NamedNodeMap**
**Ele.attributes //获取元素的属性**

```js
<ul id="box" data-url="index.html" node-action="submit">
	<li><节点一/li>
	<li>节点二</li>
	<li>节点三</li>
</ul>
var box = document.getElementById("box");
var attrs = box.attributes;
console.log(attrs);
console.log(attrs.length);  //3个属性
console.log(attrs[0]);  //id
console.log(attrs.item(1)); //data-url
```

**类数组对象的动态性**

- NodeList、HTMLCollection、NamedNodeMap三个集合都是动态的，是有生命、有呼吸的对象
- 它们实际上是基于DOM结构动态执行查询的结果，因此DOM结构的变化能自动反映这些对象中
- 每当文档结构发生变化时，它们都会得到更新。因此，它们始终都会保持着最新、最准确的信息

```js
<div></div>
<div></div>
<div></div>
// HTMLCollection类数组对象的动态性造成的，每次在循环的时候会重新计算div的个数 divs会和i一起递增
var divs = document.getElementByTagName("div");
var i = 0;
while(i < divs.length){
	document.body.appendChild(document.createElement("div"));
	i++;
}
//解决方法
// 创建多三个div
var divs = document.getElementByTagName("div");
var length = divs.length;
var i = 0;
while(i < length){
	document.body.appendChild(document.createElement("div"));
	i++;
}
```

| 对象       |                                 | 定义           | 相同点                                                       | 不同点               |                    |
| ---------- | ------------------------------- | -------------- | ------------------------------------------------------------ | -------------------- | ------------------ |
| Array      |                                 | 数组           |                                                              |                      |                    |
| Collection | getElementsByTagName()          | HTML元素的集合 | 与数组对象类似（不是一个数组，不能使用数组的方法），使用索引、length 属性、collection[] | name、id或索引来获取 |                    |
| NodeList   | child8Nodes、querySelectorAll() | 文档节点的集合 | 与数组对象类似（不是一个数组，不能使用数组的方法），使用索引、length属性  nodelist[] | 只能通过索引获取     | 属性节点和文本节点 |







#### HTMLCollection 接口

|             |      |
| ----------- | ---- |
| length      |      |
| item        |      |
| namedItem() |      |



`getElementsByTagName()方法 不是一个数组！`
向文档添加和移除元素（节点）
HTML Collection对象类似包含HTML元素的一个数组
`length属性`

```js
var myCollection = document.getElementsByTagName("p");
var i;
for (i = 0; i < myCollection.length; i++) {
    myCollection[i].style.backgroundColor = "red";
}
```

- HTML元素的集合
- HTMLCollection 对象类似包含 HTML 元素的一个数组

```js
var x = docuemnt.getElementsByTagName('p');
console.log(x[1])
console.log(x.length)
```

修改所有 <p> 元素的背景颜色:

```js
var myCollection = document.getElementsByTagName("p");
for (var i = 0; i < myCollection.length; i++) {
    myCollection[i].style.backgroundColor = "red";
}
```



#### parentNode接口 

|                     |      |
| ------------------- | ---- |
| ParentNode.children |      |
| firsetElementChild  |      |
| lastElementChild    |      |
| childELementCount   |      |
| append()、prepend() |      |

#### ChildNode接口

|               |      |
| ------------- | ---- |
| remove()      |      |
| before()      |      |
| after()       |      |
| replaceWith() |      |

### 节点

#### Document节点

#### Element节点

|      |      |
| ---- | ---- |
|      |      |
|      |      |
|      |      |
|      |      |

#### Text节点

|                                             |      |
| ------------------------------------------- | ---- |
| data                                        |      |
| wholeText                                   |      |
| length                                      |      |
| nextElementSibling 、previousElementSibling |      |
| appendData()                                |      |
|                                             |      |

#### DoucumentFrag节点

HTMLCollection 与 NodeList

- [HTMLCollection](https://www.runoob.com/js/js-htmldom-collections.html) 是 HTML 元素的集合。
- NodeList 是一个文档节点的集合。
- NodeList 与 HTMLCollection 有很多类似的地方。
- NodeList 与 HTMLCollection 都与数组对象有点类似，可以使用索引 (0, 1, 2, 3, 4, ...) 来获取元素。
- NodeList 与 HTMLCollection 都有 length 属性。
- HTMLCollection 元素可以通过 name，id 或索引来获取。
- NodeList 只能通过索引来获取。
- 只有 NodeList 对象有包含属性节点和文本节点。

#### Text 和 DocumentFragment节点

#### Mutation Observer API

# BOM

## Window

- 浏览器对象模型(BOM)使JavaScript有能力与浏览器对话。
- 所有浏览器都支持window对象。它表示浏览器窗口
- window 对象表示浏览器中打开的窗口

> 如果文档包含框架（`<frame>` 或 `<iframe>` 标签），浏览器会为 HTML 文档创建一个 window 对象，并为每个框架创建一个额外的 window 对象。

### Window 对象属性 `27`

> - BOM 浏览器对象模型  
>   - window  浏览器中打开的窗口
>     - navigator  有关浏览器的信息
>     - screen  有关客户端 显示屏幕的信息
>     - history  用户（在浏览器窗口中）访问过的 URL
>     - location  有关当前 URL 的信息。
> - DOM  文档对象模型
>   - document  
>
> | window尺寸的方法                                             | 功能                                                         |
> | ------------------------------------------------------------ | ------------------------------------------------------------ |
> | window.innerHeight/ window.innerWidth                        | 对于Internet Explorer、Chrome、Firefox、Opera 以及 Safari：<br />浏览器窗口的内部高度/宽度（包括滚动条） |
> | document.documentElement.clientHeight/clientWidth<br />document.body.clientHeight/clientWidth | 对于 Internet Explorer 8、7、6、5（不包括滚动条）            |
> | 属性                                                         | 描述                                                         |
> | :----------------------------------------------------------- | :----------------------------------------------------------- |
> | [document](https://www.runoob.com/jsref/dom-obj-document.html) | 对 Document 对象的只读引用。(请参阅[对象](https://www.runoob.com/jsref/dom-obj-document.html)) |
> | [navigator](https://www.runoob.com/jsref/obj-navigator.html) | 对 Navigator 对象的只读引用。请参数 [Navigator 对象](https://www.runoob.com/jsref/obj-navigator.html)。 |
> | [screen](https://www.runoob.com/jsref/obj-screen.html)       | 对 Screen 对象的只读引用。请参数 [Screen 对象](https://www.runoob.com/jsref/obj-screen.html)。 |
> | [history](https://www.runoob.com/jsref/obj-history.html)     | 对 History 对象的只读引用。请参数 [History 对象](https://www.runoob.com/jsref/obj-history.html)。 |
> | [location](https://www.runoob.com/jsref/obj-location.html)   | 用于窗口或框架的 Location 对象。请参阅 [Location 对象](https://www.runoob.com/jsref/obj-location.html)。 |
> |                                                              |                                                              |
> | [innerWidth](https://www.runoob.com/jsref/prop-win-innerheight.html)，[innerHeight](https://www.runoob.com/jsref/prop-win-innerheight.html) | 返回窗口的文档显示区的宽度、高度。                           |
> | [outerWidth](https://www.runoob.com/jsref/prop-win-outerheight.html)、[outerHeight](https://www.runoob.com/jsref/prop-win-outerheight.html) | 返回窗口的外部宽度、高度，包含工具条与滚动条。               |
> | clientHeight/clientWidth                                     |                                                              |
> | [screenLeft](https://www.runoob.com/jsref/prop-win-screenleft.html)、[screenTop](https://www.runoob.com/jsref/prop-win-screenleft.html) | 返回相对于屏幕窗口的x、y坐标                                 |
> | [screenX](https://www.runoob.com/jsref/prop-win-screenx.html)、[screenY](https://www.runoob.com/jsref/prop-win-screenx.html) | 返回相对于屏幕窗口的x、y坐标                                 |
> | [pageXOffset](https://www.runoob.com/jsref/prop-win-pagexoffset.html)、[pageYOffset](https://www.runoob.com/jsref/prop-win-pagexoffset.html) | 设置或返回当前页面相对于窗口显示区左上角的 X 、Y位置。       |
> |                                                              |                                                              |
> | [localStorage](https://www.runoob.com/jsref/prop-win-localstorage.html)、[sessionStorage](https://www.runoob.com/jsref/prop-win-sessionstorage.html) | 在浏览器中存储 key/value 对。没有过期时间。在浏览器中存储 key/value 对。 在关闭窗口或标签页之后将会删除这些数据。 |
> |                                                              |                                                              |
> | [length](https://www.runoob.com/jsref/prop-win-length.html)  | 设置或返回窗口中的框架数量。                                 |
> | [name](https://www.runoob.com/jsref/prop-win-name.html)      | 设置或返回窗口的名称。                                       |
> | [closed](https://www.runoob.com/jsref/prop-win-closed.html)  | 返回窗口是否已被关闭。                                       |
> | [frames](https://www.runoob.com/jsref/prop-win-frames.html)  | 返回窗口中所有命名的框架。该集合是 Window 对象的数组，每个 Window 对象在窗口中含有一个框架。 |
> | [parent](https://www.runoob.com/jsref/prop-win-parent.html)  | 返回父窗口。                                                 |
> | [self](https://www.runoob.com/jsref/prop-win-self.html)      | 返回对当前窗口的引用。等价于 Window 属性。                   |
> | [top](https://www.runoob.com/jsref/prop-win-top.html)        | 返回最顶层的父窗口。                                         |
> | [status](https://www.runoob.com/jsref/prop-win-status.html)  | 设置窗口状态栏的文本。                                       |
> | [opener](https://www.runoob.com/jsref/prop-win-opener.html)  | 返回对创建此窗口的窗口的引用。                               |
> | [defaultStatus](https://www.runoob.com/jsref/prop-win-defaultstatus.html) | 设置或返回窗口状态栏中的默认文本。                           |

### Window 对象方法 `26`

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [open()](https://www.runoob.com/jsref/met-win-open.html)     | 打开一个新的浏览器窗口或查找一个已命名的窗口。               |
| [close()](https://www.runoob.com/jsref/met-win-close.html)   | 关闭浏览器窗口。                                             |
| [alert()](https://www.runoob.com/jsref/met-win-alert.html)   | 显示带有一段消息和一个确认按钮的警告框。                     |
| [prompt()](https://www.runoob.com/jsref/met-win-prompt.html) | 显示可提示用户输入的对话框。                                 |
| [confirm()](https://www.runoob.com/jsref/met-win-confirm.html) | 显示带有一段消息以及确认按钮和取消按钮的对话框。             |
| [moveTo()](https://www.runoob.com/jsref/met-win-moveto.html) | 把窗口的左上角移动到一个指定的坐标。                         |
| [print()](https://www.runoob.com/jsref/met-win-print.html)   | 打印当前窗口的内容。打印功能                                 |
| [resizeTo()](https://www.runoob.com/jsref/met-win-resizeto.html) | 把窗口的大小调整到指定的宽度和高度。                         |
| [stop()](https://www.runoob.com/jsref/met-win-stop.html)     | 停止页面载入。                                               |
|                                                              |                                                              |
| [atob()](https://www.runoob.com/jsref/met-win-atob.html)     | 解码一个 base-64 编码的字符串。                              |
| [btoa()](https://www.runoob.com/jsref/met-win-btoa.html)     | 创建一个 base-64 编码的字符串。                              |
|                                                              |                                                              |
| [blur()](https://www.runoob.com/jsref/met-win-blur.html)     | 把键盘焦点从顶层窗口移开。                                   |
| [clearInterval()](https://www.runoob.com/jsref/met-win-clearinterval.html) | 取消由 setInterval() 设置的 timeout。                        |
| [clearTimeout()](https://www.runoob.com/jsref/met-win-cleartimeout.html) | 取消由 setTimeout() 方法设置的 timeout。                     |
| [createPopup()](https://www.runoob.com/jsref/met-win-createpopup.html) | 创建一个 pop-up 窗口。只有 IE 浏览器支持 createPopup() 方法，其他浏览器都不支持。 |
| [focus()](https://www.runoob.com/jsref/met-win-focus.html)   | 把键盘焦点给予一个窗口。                                     |
| getSelection()                                               | 返回一个 Selection 对象，表示用户选择的文本范围或光标的当前位置。 |
| [getComputedStyle()](https://www.runoob.com/jsref/jsref-getcomputedstyle.html) | 获取指定元素的 CSS 样式。                                    |
| [matchMedia()](https://www.runoob.com/jsref/met-win-matchmedia.html) | 该方法用来检查 media query 语句，它返回一个 MediaQueryList对象。 |
| [moveBy()](https://www.runoob.com/jsref/met-win-moveby.html) | 可相对窗口的当前坐标把它移动指定的像素。                     |
| [resizeBy()](https://www.runoob.com/jsref/met-win-resizeby.html) | 按照指定的像素调整窗口的大小。                               |
| scroll()                                                     | 已废弃。 该方法已经使用了 [scrollTo()](https://www.runoob.com/jsref/met-win-scrollto.html) 方法来替代。 |
| [scrollBy()](https://www.runoob.com/jsref/met-win-scrollby.html) | 按照指定的像素值来滚动内容。                                 |
| [scrollTo()](https://www.runoob.com/jsref/met-win-scrollto.html) | 把内容滚动到指定的坐标。                                     |
| [setInterval()](https://www.runoob.com/jsref/met-win-setinterval.html)、[setTimeout()](https://www.runoob.com/jsref/met-win-settimeout.html) | 按照指定的周期（以毫秒计）来调用函数或计算表达式。           |
|                                                              | 在指定的毫秒数后调用函数或计算表达式。                       |

## Navigator

Navigator 对象包含有关浏览器的信息

> ###### 警告!：**来自 navigator 对象的信息具有误导性，不应该被用于检测浏览器版本**，这是因为：
>
> - navigator 数据可被浏览器使用者更改
> - 一些浏览器对测试站点会识别错误
> - 浏览器无法报告晚于浏览器发布的新操作系统
>
> ###### 浏览器检测
>
> 由于 navigator 可误导浏览器检测，使用对象检测可用来嗅探不同的浏览器。
>
> 由于不同的浏览器支持不同的对象，您可以使用对象来检测浏览器。例如，由于只有 Opera 支持属性 "window.opera"，您可以据此识别出 Opera。
>
> 例子：if (window.opera) {...some action...}

```js
if(window.chrome){
    // some action
    // window.chrome 
    // 判断浏览器
}
```

### Navigator 对象属性 `6`

| 属性                                                         | 说明                                                    |
| :----------------------------------------------------------- | :------------------------------------------------------ |
| [appCodeName](https://www.runoob.com/jsref/prop-nav-appcodename.html) | （浏览器代号）返回浏览器的代码名                        |
| [appName](https://www.runoob.com/jsref/prop-nav-appname.html) | （浏览器名称）返回浏览器的名称                          |
| [appVersion](https://www.runoob.com/jsref/prop-nav-appversion.html) | （浏览器版本）返回浏览器的平台和版本信息                |
| [cookieEnabled](https://www.runoob.com/jsref/prop-nav-cookieenabled.html) | 返回指明浏览器中是否启用 cookie 的布尔值                |
| [platform](https://www.runoob.com/jsref/prop-nav-platform.html) | （硬件平台）返回运行浏览器的操作系统平台                |
| [userAgent](https://www.runoob.com/jsref/prop-nav-useragent.html) | （用户代理）返回由客户机发送服务器的user-agent 头部的值 |

```js
navigator.appName 
// "Netscape" 浏览器名称
navigator.appVesion 
// "5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36"  平台和版本信息
navigator.appCodeName
// "Mozilla" 浏览器代码号
navigator.userAgent // 重点
// "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36"
navigator.platform
// "Win32" 浏览器的操作系统平台
navigator.cookieEnabled
// true 是否启用 cookie 的布尔值
```

### Navigator 对象方法 `2`

| 方法                                                         | 描述                                      |
| :----------------------------------------------------------- | :---------------------------------------- |
| [javaEnabled()](https://www.runoob.com/jsref/met-nav-javaenabled.html) | 指定是否在浏览器中启用Java                |
| [taintEnabled()](https://www.runoob.com/jsref/met-nav-taintenabled.html) | 规定浏览器是否启用数据污点(data tainting) |

```js
navigator.javaEnabled()
// 是否在浏览器中启用Java
navigator.taintEnabled()
// 启用数据污点(data tainting)
// 目前只有 Internet Explorer 和 Opera 浏览器支持 taintEnabled() 方法
```

## Screen

screen 对象包含有关客户端 显示屏幕的信息

> window和window Screen的区别
>
> window窗体的尺寸大小 随窗口的缩放而改变 innerXXX/clientXXX
>
> window  Srreen 屏幕的可用宽度或者高度 固定，不随窗口的缩放而改变 screen.availWidth/screen.availHeight
>
> screen.availWidth 属性返回访问者**屏幕的宽度，**以像素计，减去界面特性，比如窗口任务栏。
>
> screen.availHeight 属性返回访问者**屏幕的高度**，以像素计，减去界面特性，比如窗口任务栏。
>
> ### Screen 对象属性  `6`
>
> | 属性                                                         | 说明                                                       |
> | :----------------------------------------------------------- | :--------------------------------------------------------- |
> | [availWidth](https://www.runoob.com/jsref/prop-screen-availwidth.html)、[availHeight](https://www.runoob.com/jsref/prop-screen-availheight.html) | 返回屏幕的宽度、高度（不包括Windows任务栏） 可用屏幕的宽度 |
> | [width](https://www.runoob.com/jsref/prop-screen-width.html)、[height](https://www.runoob.com/jsref/prop-screen-height.html) | 返回屏幕的总宽度、总高度                                   |
> | [colorDepth](https://www.runoob.com/jsref/prop-screen-colordepth.html) | 返回目标设备或缓冲器上的调色板的比特深度                   |
> | [pixelDepth](https://www.runoob.com/jsref/prop-screen-pixeldepth.html) | 返回屏幕的颜色分辨率（每像素的位数）                       |

```js
screen.availWidth/availHeight
window.screen
Screen {availWidth: 2048, availHeight: 1113, width: 2048, height: 1153, colorDepth: 24, …}
availHeight: 1113
availLeft: 1536
availTop: -287
availWidth: 2048
colorDepth: 24 // 目标设备或缓冲器上的调色板的比特深度
height: 1153
width: 2048
pixelDepth: 24  //屏幕的颜色分辨率（每像素的位数
__proto__: Screen
```

## History

History 对象包含用户（在浏览器窗口中）访问过的 URL

```js
History {length: 11, scrollRestoration: "auto", state: null}
length: 11
scrollRestoration: "auto"
state: null
__proto__: History
```

### History 对象属性 `1`

| 属性                                                        | 说明                                     |
| :---------------------------------------------------------- | :--------------------------------------- |
| [length](https://www.runoob.com/jsref/prop-his-length.html) | 返回历史列表中的网址数`当前网站的子网站` |

### History 对象方法 `2`

| 方法                                                         | 说明                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [back()](https://www.runoob.com/jsref/met-his-back.html)     | 在浏览器点击后退按钮相同，加载 history 列表中的前一个 URL    |
| [forward()](https://www.runoob.com/jsref/met-his-forward.html) | 在浏览器中点击向前按钮相同，加载 history 列表中的下一个 URL  |
| [go()](https://www.runoob.com/jsref/met-his-go.html)         | 历史记录的数量、go() 方法可加载历史列表中的某个具体的页面，加载 history 列表中的某个具体页面，history.go(*number*） history.go(-2) |

## Location

- Location 对象包含有关当前 URL 的信息。
- 获取当前页面的地址，重定向到新的页面.

### Location 对象属性 `8`

> `href = protocol://hostname:port/pathname`
>
> host(主机名和端口) = hostname(主机名) + port(端口号)
>
> - location.href URL = 域名+路径
>
> - location.hostname 域名
>
> - location.pathname 路径和文件名
>
>
> [location.href、location.assign和location.replace的区别](https://www.cnblogs.com/liu-l/p/3835714.html)
>
> window.location.assign(url) ：  能返回原来的页面
>
> 加载 URL 指定的新的 HTML 文档。 就相当于一个链接，跳转到指定的url，当前页面会转为新页面内容，可以点击后退返回上一个页面。
>
> window.location.replace(url) ：  返回不了原来的页面
>
> 通过加载 URL 指定的文档来替换当前文档 ，这个方法是替换当前窗口页面，前后两个页面共用一个窗口，所以是没有后退返回上一页的
>
> 在写跳转页面的时候遇到个有意思的问题，RT的三个均能用来写跳转，总结了下它们之间的区别。
>
> 1、window.location.href=“url”;    改变url地址。
>
> 　　location.href是一个属性，要这样写：location.href="url"
>
> 2、window.location.assign("url")  加载新的文档，效果与location.href相当。 
>
> 3、window.location.replace  将地址替换成新url，该方法通过指定URL替换当前缓存在历史里（客户端）的项目。
>
> 与以上两者的区别在于：在replace之后，浏览历史就被清空了（href与assign方法会产生历史记录）。
>
> 因此若**使用replace页面跳转后是不能后退**的。
>
> | 属性                                                         | 描述                                                         |
> | :----------------------------------------------------------- | :----------------------------------------------------------- |
> | [hash](https://www.runoob.com/jsref/prop-loc-hash.html)      | 返回一个URL的锚部分，hash 属性是一个可读可写的字符串，该字符串是 URL 的锚部分（从 # 号开始的部分）http://www.runoob.com/test.htm＃PART2  hash 是 ``#PART2` |
> |                                                              |                                                              |
> | [href](https://www.runoob.com/jsref/prop-loc-href.html)      | 返回``完整的URL`                                             |
> | [protocol](https://www.runoob.com/jsref/prop-loc-protocol.html) | 返回一个URL`协议`                                            |
> | [hostname](https://www.runoob.com/jsref/prop-loc-hostname.html) | 返回URL的主机名                                              |
> | [port](https://www.runoob.com/jsref/prop-loc-port.html)      | 返回一个URL服务器使用的端口号                                |
> | [pathname](https://www.runoob.com/jsref/prop-loc-pathname.html) | 返回的URL路径名。                                            |
> | [host](https://www.runoob.com/jsref/prop-loc-host.html)      | 返回一个URL的主机名和端口                                    |
> |                                                              |                                                              |
> | [search](https://www.runoob.com/jsref/prop-loc-search.html)  | 返回一个URL的查询部分，search 属性是一个可读可写的字符串，可设置或返回当前 URL 的查询部分（问号 ? 之后的部分） 如http://www.runoob.com/submit.htm?email=someone@ example.com 输出结果`?email=someone@ example.com` |

### Location 对象方法 `3`

| 方法                                                         | 说明                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [assign()](https://www.runoob.com/jsref/met-loc-assign.html) | 载入一个新的文档                                             |
| [reload()](https://www.runoob.com/jsref/met-loc-reload.html) | 重新载入当前文档(刷新) 重新加载页面                          |
| [replace()](https://www.runoob.com/jsref/met-loc-replace.html) | 用新的文档替换当前文档 location.replace(*newURL*) 加载新的文档 |

```js
location.assign('https://heweiliang.gitee.io/')
location.reload()
location.replace('https://heweiliang.gitee.io/')
// 定时刷新页面
setInterval(function(){
    location.reload()
},1000)
Location {href: "https://heweiliang.gitee.io/", ancestorOrigins: DOMStringList, origin: "https://heweiliang.gitee.io", protocol: "https:", host: "heweiliang.gitee.io", …}
ancestorOrigins: DOMStringList {length: 0}
assign: ƒ assign()
fragmentDirective: FragmentDirective {}
hash: ""
host: "heweiliang.gitee.io"
hostname: "heweiliang.gitee.io"
href: "https://heweiliang.gitee.io/"
origin: "https://heweiliang.gitee.io"
pathname: "/"
port: ""
protocol: "https:"
reload: ƒ reload()
replace: ƒ replace()
search: ""
toString: ƒ toString()
valueOf: ƒ valueOf()
Symbol(Symbol.toPrimitive): undefined
__proto__: Location
```

### 刷新页面

> - reload() 方法;
>
>   reload()方法用于刷新当前文档。
>
>   reload() 方法类似于你浏览器上的刷新页面按钮。
>
>   `location.reload();`
>
> - replace() 方法;
>
>   **replace() 方法**可用一个新文档取代当前文档。
>
>   `window.location.replace("url")`
>
> - 页面自动刷新;
>
>   页面自动刷新：把如下代码加入``<head>``区域中
>
>   `<meta http-equiv="refresh" content="5">`

### 浏览器重定向

- `port portocol reload() replace() assign() `
- `href = hostname + pathname`
- location.reload() 
- window.location.replace("url") 
- `<meta http-equiv="refresh" content="5">`

## 存储对象

存储

- cookie
- token
- sessionStorage 和 localStorage
- Indexed DB
- Web SQL
  缓存
- Cache Storage
- Application Cache
  Web 存储 API 提供了 sessionStorage （会话存储） 和 localStorage（本地存储）两个存储对象来对网页的数据进行添加、删除、修改、查询操作。
- localStorage 用于长久保存整个网站的数据，保存的数据没有过期时间，直到手动去除。
- sessionStorage 用于临时保存同一窗口(或标签页)的数据，在关闭窗口或标签页之后将会删除这些数据。

### 存储对象属性 `1`

| 属性   | 描述                           |
| :----- | :----------------------------- |
| length | 返回存储对象中包含多少条数据。 |

```js
localStorage.length
sessionStorage.length
```

### 存储对象方法 `5`

| 方法                        | 描述                                               |
| :-------------------------- | :------------------------------------------------- |
| key(*n*)                    | 返回存储对象中第 *n* 个键的名称                    |
| getItem(*keyname*)          | 返回指定键的值                                     |
| setItem(*keyname*, *value*) | 添加键和值，如果对应的值存在，则更新该键对应的值。 |
| removeItem(*keyname*)       | 移除键                                             |
| clear()                     | 清除存储对象中所有的键                             |

### Web 存储 API `2`

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [window.localStorage](https://www.runoob.com/jsref/prop-win-localstorage.html) | 在浏览器中存储 key/value 对。没有过期时间。                  |
| [window.sessionStorage](https://www.runoob.com/jsref/prop-win-sessionstorage.html) | 在浏览器中存储 key/value 对。 在关闭窗口或标签页之后将会删除这些数据。 |

### Cookie	

`Cookie用于存储web页面的用户信息 创建 读取 修改 删除`
JavaScript可以使用document。cookie==属性创建，读取，及删除== 

#### 1. 创建三部曲 

==username 用户名 expires cookie过期时间 path = / cookie参数设置路径==

```js
username 用户名
document.cookie = "username = John Doe";
expires = 时间 为 cookie 添加一个过期时间（以 UTC 或 GMT 时间）
path=/ 默认情况，cookie当前页面 
document.cookie="username=John Doe; expires=Thu, 18 Dec 2043 12:00:00 GMT; path=/";
```

#### 2. 读取

```js
var cookie = document.cookie;
```

document.cookie 将以字符串的方式返回所有的 cookie，类型格式： cookie1=value; cookie2=value; cookie3=value;

#### 3. 修改  

==修改 cookie 类似于创建 cookie 修改expires过期时间 旧的 cookie 将被覆盖==

```js
//当前系统时间
document.cookie="username=John Smith; expires=Thu, 18 Dec 2043 12:00:00 GMT; path=/";
```

#### 4. 删除

==expires =设置时间==
删除cookie只需要设置expires参数为以前的时间即可，设置为`Thu,01 Jan 1970:00:00:00 GMT`

```js
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT";
```

删除Cookie时不必指定cookie的值

#### 5. Cookie实例

```js
//设置cookie值的函数
function setCookie(cname,cvalue,exdays){
    var d = new Date(); //Mon Apr 13 2020 14:38:03 GMT+0800 (中国标准时间)
    d.setTime(d.getTime()+(exdays*24*60*60*1000));
    //Thu, 01 Jan 1970 00:00:00 GMT
    //document.cookie="username=John Smith; expires=Thu, 18 Dec 2043 12:00:00 GMT; path=/";
    var expires = "expires="+d.toGMTString(); //Mon, 13 Apr 2020 06:38:03 GMT
    document.cookie = cname+"="+cvalue+"; "+expires;
}
//获取cookie值的函数
//username=123; _ga=GA1.2.1390342908.1574751797; _gid=GA1.2.1758365235.1586703146; Hm_lvt_3eec0b7da6548cf07db3bc477ea905ee=1586661337,1586678516,1586701261,1586734558; SERVERID=3a4d90ce271dac423615bd00bfd9dc97|1586760084|1586759163; Hm_lpvt_3eec0b7da6548cf07db3bc477ea905ee=1586760086; _gat_gtag_UA_84264393_2=1
function getCookie(cname){
    var name = cname + "=";
    var ca = document.cookie.split(';');
    for(var i=0; i<ca.length; i++) {
        var c = ca[i].trim();
        if (c.indexOf(name)==0) { return c.substring(name.length,c.length); }
    }
    return "";
}
// 检测cookie值的函数
function checkCookie(){
    var user=getCookie("username");
    if (user!=""){
        alert("欢迎 " + user + " 再次访问");
    }
    else {
        user = prompt("请输入你的名字:","");
          if (user!="" && user!=null){
            setCookie("username",user,30);
        }
    }
}
```

### sessionStorage 和 localStorage



### indexDB

## 弹窗

 `alert() confirm() prompt() `
JavaScript 中创建三种消息框：警告框、确定框、提示框

### 警告框 `只有确定按钮`

警告框经常用于确保用户可以得到某些信息。

```js
window.alert('');
```

### 确定框	`确定和取消按钮，确定返回true 取消false`

确认框通常用于验证是否接受用户操作。

```js
window.confirm('');
var r=confirm("按下按钮");
if (r==true)
{
    x="你按下了\"确定\"按钮!";
}
else
{
    x="你按下了\"取消\"按钮!";
}
```

### 提示框	`用户输入`

提示框经常用于提示用户在进入页面前输入某个值。
当提示框出现后，用户需要输入某个值，然后点击确认或取消按钮才能继续操纵。
如果用户点击确认，那么返回值为输入的值。如果用户点击取消，那么返回值为 null。

```js
window.prompt("sometext","defaultvalue"); //第一个提示词 第二个默认值
var person=prompt("请输入你的名字","Harry Potter");
if (person!=null && person!="")
{
    x="你好 " + person + "! 今天感觉如何?";
    document.getElementById("demo").innerHTML=x;
}
```

### 换行

弹窗使用 反斜杠 + "n"(\n) 来设置换行。

```js
alert("Hello\nHow are you?");
```

# 事件

HTML DOM 使 JavaScript 有能力对 HTML 事件做出反应。
如需在用户点击某个元素时执行代码，请向一个 HTML 事件属性添加 JavaScript 代码：

### 常用事件

| 鼠标事件                              | 描述                                                         |
| ------------------------------------- | ------------------------------------------------------------ |
|                                       |                                                              |
| `onmousedown`、`onclick`、`onmouseup` | 点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件 |
| `onload` 和 `onunload`                | onload 和 onunload 事件会在用户进入或离开页面时被触发，onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。 |
| `onchange`                            | onload 和 onunload 事件可用于处理 cookieonchange 事件常结合对输入字段的验证来使用 |
| `onmouseover` 和`onmouseout`          | 鼠标移入、鼠标移出                                           |
| `onfocus`                             | 当输入字段获得焦点时，改变其背景色                           |
|                                       |                                                              |
| 键盘事件                              | 描述                                                         |
|                                       |                                                              |

> nmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分**。首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。
>
> onload 和 onunload 事件会在用户进入或离开页面时被触发。
>
> onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。
>
> onload 和 onunload 事件可用于处理 cookie。
>
> onload 和 onunload 绑定在 body 上

### 事件绑定方法

#### 一、HTML绑定

```js
<button onclick="alert('Hello')"></button>
<button onclick="eventHandler()"></button>
// 括号
function eventHandler(){
	alert('Hello');
}
```

#### 二、Javascript绑定

```json
<button id="btn-click"></button>
var btn = doucument.querySelector('#btn-click');
//方法名带括号表示直接执行
btn.onclick = function(){
	alert('Hello');
}
```

当一个按钮绑定多个事件时只会执行，最后一个会取代前面的，解决方法第三种。

#### 三、addEventListener()

通过addEventListener()方法 增加一个事件监听器到某个物体,可以绑定多个事件

```js
var btn = doucument.querySelector('#btn-click')
btn.addEventListener('click'，sayHello);
//不需要（）
btn.addEventListener('click'，sayYourName);
function sayHello(){
 alert('Hello!!!');
}
function sayYourName(){
 alert('Hello!!!');
}
//.addEventListener(监听的事件类型，事件处理函数);
```

- 向原元素添加事件句柄
- 同一个元素添加多个事件句柄(向同个元素添加多个同类型的事件句柄)
- 向window对象添加事件句柄(任何 DOM 对象添加事件监听)

```js
element.addEventListener(event, function, useCapture);
```

第一个参数是事件的类型 (如 "click" 或 "mousedown").
第二个参数是事件触发后调用的函数。
第三个参数是个布尔值用于描述事件是冒泡(false 默认)还是捕获（true）。该参数是可选的。

> :不要使用 "on" 前缀。 例如，使用 "click" ,而不是使用 "onclick"

#### removeEventListener() 方法

removeEventListener() 方法移除由 addEventListener() 方法添加的事件句柄:

```js
element.removeEventListener("mousemove", myFunction);
```

### 事件冒泡或事件捕获

事件冒泡( false 里到外，默认冒泡)或事件捕获(外到里)
事件传递有两种方式：冒泡与捕获

- 在冒泡中，内部元素的事件会被先发生，然后再触发外部元素（冒泡，由内到外，水波冒泡，false）
- 在捕获中，外部元素的事件会先触发，然后才会触发内部元素的事件（捕获，由外到内，true）
  addEvenListener() 方法可以指定`"useCapture"` 参数来设置传递类型

```js
addEventListener(event,function,useCapture)
```

默认值为false，即是冒泡，当值为true时，事件使用捕获传递

```js
document.getElementById("myDiv").addEventListener("click", myFunction, true);
```

### 阻止冒泡

 `e.stopPropagation() 与 e.canceBubble = true`

w3c的方法是`e.stopPropagation()`  、IE则是使用``e.canceBubble = true`
stopPropagation也是事件对象(Event)的一个方法，作用是阻止目标元素的冒泡事件，但是会不阻止默认行为。

```js
window.event?window.event.cancelBubble = true:e.stopPropagation()
function stopBubble(e) { 
//如果提供了事件对象，则这是一个非IE浏览器 
if ( e && e.stopPropagation ) 
    //因此它支持W3C的stopPropagation()方法 
    e.stopPropagation(); 
else 
    //否则，我们需要使用IE的方式来取消事件冒泡 
    window.event.cancelBubble = true; 
}
```

[javascript常用代码大全-前端开发博客](http://caibaojian.com/288.html)

### 取消默认事件 

`e.preventDefault() e.returnValue = false`

w3c的方法是`e.preventDefault()`，IE则是使用`e.returnValue = false`;
preventDefault它是事件对象(Event)的一个方法，作用是取消一个目标元素的默认行为。既然是说默认行为，当然是元素必须有默认行为才能被取消，如果元素本身就没有默认行为，调用当然就无效了。
什么元素有默认行为呢？如链接<a>，提交按钮<input type="submit">等。当Event 对象的 cancelable为false时，表示没有默认行为，这时即使有默认行为，调用preventDefault也是不会起作用的。

```js
//假定有链接<a href="http://caibaojian.com/" id="testA" >caibaojian.com</a>
var a = document.getElementById("testA");
a.onclick =function(e){
if(e.preventDefault){
e.preventDefault();
}else{
window.event.returnValue == false;
}
}
//阻止浏览器的默认行为 
function stopDefault( e ) { 
    //阻止默认浏览器动作(W3C) 
    if ( e && e.preventDefault ) 
        e.preventDefault(); 
    //IE中阻止函数器默认动作的方式 
    else 
        window.event.returnValue = false; 
    return false; 
}
```

###

### 浏览器支持

表格中的数字表示支持该方法的第一个浏览器的版本号。

| 方法                  | 谷歌 | IE   | 火狐 | Safari | opera |
| :-------------------- | ---- | ---- | ---- | ------ | ----- |
| addEventListener()    | 1.0  | 9.0  | 1.0  | 1.0    | 7.0   |
| removeEventListener() | 1.0  | 9.0  | 1.0  | 1.0    | 7.0   |

**注意：** IE 8 及更早 IE 版本，Opera 7.0及其更早版本不支持 addEventListener() 和 removeEventListener() 方法。但是，对于这类浏览器版本可以使用 detachEvent() 方法来移除事件句柄:

```js
*element.attachEvent(event, function);
element.detachEvent(event, function);*
```

```js
/*
 * 参数：
 *     obj：要绑定事件的对象
 *     eventStr：事件(注意：这里不要on)
 *      callback：回调函数
 */
function bind(obj , eventStr , callback){
    if(obj.addEventListener){
        //大部分浏览器
        obj.addEventListener(eventStr , callback , false);
    }else{
        //IE8及以下
        obj.attachEvent("on"+eventStr , function(){
            //在匿名函数中调用回调函数
            callback.call(obj);
        });
    }
} 
```

> 事件
>
> - 鼠标
> - 键盘
> - 表单
> - 剪贴板
> - 打印
> - 拖动
> - 多媒体
> - 动画
> - 过渡

### HTML DOM 事件

HTML DOM 事件允许Javascript在HTML文档元素中注册不同事件处理程序。
事件通常与函数结合使用，函数不会在事件发生前被执行！ (如用户点击按钮)。
**提示：** 在 W3C 2 级 DOM 事件中规范了事件模型。
**DOM：** 指明使用的 DOM 属性级别。

## 鼠标事件

> 点击：onclick （单击）、ondbclick（双击）、onmousedown（被按下） ==>   onclick  ==> onmouseup（被松开）
>
> 移动：onmousemove、
>
> | 属性          | 描述                                   | DOM  |
> | :------------ | :------------------------------------- | :--- |
> | onclick       | 当用户点击某个对象时调用的事件句柄。   | 2    |
> | oncontextmenu | 在用户点击鼠标右键打开上下文菜单时触发 |      |
> | ondblclick    | 当用户双击某个对象时调用的事件句柄。   | 2    |
> | onmousedown   | 鼠标按钮被按下。                       | 2    |
> | onmouseenter  | 当鼠标指针移动到元素上时触发。         | 2    |
> | onmouseleave  | 当鼠标指针移出元素时触发               | 2    |
> | onmousemove   | 鼠标被移动。                           | 2    |
> | onmouseover   | 鼠标移到某元素之上。                   | 2    |
> | onmouseout    | 鼠标从某元素移开。                     | 2    |
> | onmouseup     | 鼠标按键被松开。                       | 2    |

## 键盘事件

| 属性                                                         | 描述                       | DOM  |
| :----------------------------------------------------------- | :------------------------- | :--- |
| [onkeydown](https://www.runoob.com/jsref/event-onkeydown.html) | 某个键盘按键被按下。       | 2    |
| [onkeypress](https://www.runoob.com/jsref/event-onkeypress.html) | 某个键盘按键被按下并松开。 | 2    |
| [onkeyup](https://www.runoob.com/jsref/event-onkeyup.html)   | 某个键盘按键被松开。       | 2    |

### 框架/对象（Frame/Object）事件

| 属性                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [onabort](https://www.runoob.com/jsref/event-onabort.html)   | 图像的加载被中断。 ( <object>)                               | 2    |
| [onbeforeunload](https://www.runoob.com/jsref/event-onbeforeunload.html) | 该事件在即将离开页面（刷新或关闭）时触发                     | 2    |
| [onerror](https://www.runoob.com/jsref/event-onerror.html)   | 在加载文档或图像时发生错误。 ( <object>, <body>和 <frameset>) |      |
| [onhashchange](https://www.runoob.com/jsref/event-onhashchange.html) | 该事件在当前 URL 的锚部分发生修改时触发。                    |      |
| [onload](https://www.runoob.com/jsref/event-onload.html)     | 一张页面或一幅图像完成加载。                                 | 2    |
| [onpageshow](https://www.runoob.com/jsref/event-onpageshow.html) | 该事件在用户访问页面时触发                                   |      |
| [onpagehide](https://www.runoob.com/jsref/event-onpagehide.html) | 该事件在用户离开当前网页跳转到另外一个页面时触发             |      |
| [onresize](https://www.runoob.com/jsref/event-onresize.html) | 窗口或框架被重新调整大小。                                   | 2    |
| [onscroll](https://www.runoob.com/jsref/event-onscroll.html) | 当文档被滚动时发生的事件。                                   | 2    |
| [onunload](https://www.runoob.com/jsref/event-onunload.html) | 用户退出页面。 ( <body> 和 <frameset>)                       | 2    |

## 表单事件

| 属性                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [onblur](https://www.runoob.com/jsref/event-onblur.html)     | 元素失去焦点时触发                                           | 2    |
| [onchange](https://www.runoob.com/jsref/event-onchange.html) | 该事件在表单元素的内容改变时触发( <input>, <keygen>, <select>, 和 <textarea>) | 2    |
| [onfocus](https://www.runoob.com/jsref/event-onfocus.html)   | 元素获取焦点时触发                                           | 2    |
| [onfocusin](https://www.runoob.com/jsref/event-onfocusin.html) | 元素即将获取焦点时触发                                       | 2    |
| [onfocusout](https://www.runoob.com/jsref/event-onfocusout.html) | 元素即将失去焦点时触发                                       | 2    |
| [oninput](https://www.runoob.com/jsref/event-oninput.html)   | 元素获取用户输入时触发                                       | 3    |
| [onreset](https://www.runoob.com/jsref/event-onreset.html)   | 表单重置时触发                                               | 2    |
| [onsearch](https://www.runoob.com/jsref/event-onsearch.html) | 用户向搜索域输入文本时触发 ( <input="search">)               |      |
| [onselect](https://www.runoob.com/jsref/event-onselect.html) | 用户选取文本时触发 ( <input> 和 <textarea>)                  | 2    |
| [onsubmit](https://www.runoob.com/jsref/event-onsubmit.html) | 表单提交时触发                                               | 2    |

### 剪贴板事件

| 属性                                                       | 描述                           | DOM  |
| :--------------------------------------------------------- | :----------------------------- | :--- |
| [oncopy](https://www.runoob.com/jsref/event-oncopy.html)   | 该事件在用户拷贝元素内容时触发 |      |
| [oncut](https://www.runoob.com/jsref/event-oncut.html)     | 该事件在用户剪切元素内容时触发 |      |
| [onpaste](https://www.runoob.com/jsref/event-onpaste.html) | 该事件在用户粘贴元素内容时触发 |      |

### 打印事件

| 属性                                                         | 描述                                                 | DOM  |
| :----------------------------------------------------------- | :--------------------------------------------------- | :--- |
| [onafterprint](https://www.runoob.com/jsref/event-onafterprint.html) | 该事件在页面已经开始打印，或者打印窗口已经关闭时触发 |      |
| [onbeforeprint](https://www.runoob.com/jsref/event-onbeforeprint.html) | 该事件在页面即将开始打印时触发                       |      |

### 拖动事件

| 事件                                                         | 描述                                 | DOM  |
| :----------------------------------------------------------- | :----------------------------------- | :--- |
| [ondrag](https://www.runoob.com/jsref/event-ondrag.html)     | 该事件在元素正在拖动时触发           |      |
| [ondragend](https://www.runoob.com/jsref/event-ondragend.html) | 该事件在用户完成元素的拖动时触发     |      |
| [ondragenter](https://www.runoob.com/jsref/event-ondragenter.html) | 该事件在拖动的元素进入放置目标时触发 |      |
| [ondragleave](https://www.runoob.com/jsref/event-ondragleave.html) | 该事件在拖动元素离开放置目标时触发   |      |
| [ondragover](https://www.runoob.com/jsref/event-ondragover.html) | 该事件在拖动元素在放置目标上时触发   |      |
| [ondragstart](https://www.runoob.com/jsref/event-ondragstart.html) | 该事件在用户开始拖动元素时触发       |      |
| [ondrop](https://www.runoob.com/jsref/event-ondrop.html)     | 该事件在拖动元素放置在目标区域时触发 |      |

### 多媒体（Media）事件

| 事件                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [onabort](https://www.runoob.com/jsref/event-onabort-media.html) | 事件在视频/音频（audio/video）终止加载时触发。               |      |
| [oncanplay](https://www.runoob.com/jsref/event-oncanplay.html) | 事件在用户可以开始播放视频/音频（audio/video）时触发。       |      |
| [oncanplaythrough](https://www.runoob.com/jsref/event-oncanplaythrough.html) | 事件在视频/音频（audio/video）可以正常播放且无需停顿和缓冲时触发。 |      |
| [ondurationchange](https://www.runoob.com/jsref/event-ondurationchange.html) | 事件在视频/音频（audio/video）的时长发生变化时触发。         |      |
| onemptied                                                    | 当期播放列表为空时触发                                       |      |
| [onended](https://www.runoob.com/jsref/event-onended.html)   | 事件在视频/音频（audio/video）播放结束时触发。               |      |
| [onerror](https://www.runoob.com/jsref/event-onerror-media.html) | 事件在视频/音频（audio/video）数据加载期间发生错误时触发。   |      |
| [onloadeddata](https://www.runoob.com/jsref/event-onloadeddata.html) | 事件在浏览器加载视频/音频（audio/video）当前帧时触发触发。   |      |
| [onloadedmetadata](https://www.runoob.com/jsref/event-onloadedmetadata.html) | 事件在指定视频/音频（audio/video）的元数据加载后触发。       |      |
| [onloadstart](https://www.runoob.com/jsref/event-onloadstart.html) | 事件在浏览器开始寻找指定视频/音频（audio/video）触发。       |      |
| [onpause](https://www.runoob.com/jsref/event-onpause.html)   | 事件在视频/音频（audio/video）暂停时触发。                   |      |
| [onplay](https://www.runoob.com/jsref/event-onplay.html)     | 事件在视频/音频（audio/video）开始播放时触发。               |      |
| [onplaying](https://www.runoob.com/jsref/event-onplaying.html) | 事件在视频/音频（audio/video）暂停或者在缓冲后准备重新开始播放时触发。 |      |
| [onprogress](https://www.runoob.com/jsref/event-onprogress.html) | 事件在浏览器下载指定的视频/音频（audio/video）时触发。       |      |
| [onratechange](https://www.runoob.com/jsref/event-onratechange.html) | 事件在视频/音频（audio/video）的播放速度发送改变时触发。     |      |
| [onseeked](https://www.runoob.com/jsref/event-onseeked.html) | 事件在用户重新定位视频/音频（audio/video）的播放位置后触发。 |      |
| [onseeking](https://www.runoob.com/jsref/event-onseeking.html) | 事件在用户开始重新定位视频/音频（audio/video）时触发。       |      |
| [onstalled](https://www.runoob.com/jsref/event-onstalled.html) | 事件在浏览器获取媒体数据，但媒体数据不可用时触发。           |      |
| [onsuspend](https://www.runoob.com/jsref/event-onsuspend.html) | 事件在浏览器读取媒体数据中止时触发。                         |      |
| [ontimeupdate](https://www.runoob.com/jsref/event-ontimeupdate.html) | 事件在当前的播放位置发送改变时触发。                         |      |
| [onvolumechange](https://www.runoob.com/jsref/event-onvolumechange.html) | 事件在音量发生改变时触发。                                   |      |
| [onwaiting](https://www.runoob.com/jsref/event-onwaiting.html) | 事件在视频由于要播放下一帧而需要缓冲时触发。                 |      |

### 动画事件

| 事件                                                         | 描述                            | DOM  |
| :----------------------------------------------------------- | :------------------------------ | :--- |
| [animationend](https://www.runoob.com/jsref/event-animationend.html) | 该事件在 CSS 动画结束播放时触发 |      |
| [animationiteration](https://www.runoob.com/jsref/event-animationiteration.html) | 该事件在 CSS 动画重复播放时触发 |      |
| [animationstart](https://www.runoob.com/jsref/event-animationstart.html) | 该事件在 CSS 动画开始播放时触发 |      |

### 过渡事件

| 事件                                                         | 描述                          | DOM  |
| :----------------------------------------------------------- | :---------------------------- | :--- |
| [transitionend](https://www.runoob.com/jsref/event-transitionend.html) | 该事件在 CSS 完成过渡后触发。 |      |

### 其他事件

| 事件                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| onmessage                                                    | 该事件通过或者从对象(WebSocket, Web Worker, Event Source 或者子 frame 或父窗口)接收到消息时触发 |      |
| onmousewheel                                                 | 已废弃。 使用 [onwheel](https://www.runoob.com/jsref/event-onwheel.html) 事件替代 |      |
| [ononline](https://www.runoob.com/jsref/event-ononline.html) | 该事件在浏览器开始在线工作时触发。                           |      |
| [onoffline](https://www.runoob.com/jsref/event-onoffline.html) | 该事件在浏览器开始离线工作时触发。                           |      |
| onpopstate                                                   | 该事件在窗口的浏览历史（history 对象）发生改变时触发。       |      |
| [onshow](https://www.runoob.com/jsref/event-onshow.html)     | 该事件当 <menu> 元素在上下文菜单显示时触发                   |      |
| onstorage                                                    | 该事件在 Web Storage(HTML 5 Web 存储)更新时触发              |      |
| [ontoggle](https://www.runoob.com/jsref/event-ontoggle.html) | 该事件在用户打开或关闭 <details> 元素时触发                  |      |
| [onwheel](https://www.runoob.com/jsref/event-onwheel.html)   | 该事件在鼠标滚轮在元素上下滚动时触发                         |      |

### 事件对象

#### 常量

| 静态变量        | 描述                                 | DOM  |
| :-------------- | :----------------------------------- | :--- |
| CAPTURING-PHASE | 当前事件阶段为捕获阶段(1)            | 1    |
| AT-TARGET       | 当前事件是目标阶段,在评估目标事件(1) | 2    |
| BUBBLING-PHASE  | 当前的事件为冒泡阶段 (3)             | 3    |

#### 属性

| 属性                                                         | 描述                                           | DOM  |
| :----------------------------------------------------------- | :--------------------------------------------- | :--- |
| [bubbles](https://www.runoob.com/jsref/event-bubbles.html)   | 返回布尔值，指示事件是否是起泡事件类型。       | 2    |
| [cancelable](https://www.runoob.com/jsref/event-cancelable.html) | 返回布尔值，指示事件是否可拥可取消的默认动作。 | 2    |
| [currentTarget](https://www.runoob.com/jsref/event-currenttarget.html) | 返回其事件监听器触发该事件的元素。             | 2    |
| eventPhase                                                   | 返回事件传播的当前阶段。                       | 2    |
| [target](https://www.runoob.com/jsref/event-target.html)     | 返回触发此事件的元素（事件的目标节点）。       | 2    |
| [timeStamp](https://www.runoob.com/jsref/event-timestamp.html) | 返回事件生成的日期和时间。                     | 2    |
| [type](https://www.runoob.com/jsref/event-type.html)         | 返回当前 Event 对象表示的事件的名称。          | 2    |

#### 方法

| 方法              | 描述                                     | DOM  |
| :---------------- | :--------------------------------------- | :--- |
| initEvent()       | 初始化新创建的 Event 对象的属性。        | 2    |
| preventDefault()  | 通知浏览器不要执行与事件关联的默认动作。 | 2    |
| stopPropagation() | 不再派发事件。                           | 2    |

### 目标事件对象

#### 方法

| 方法                  | 描述                                                    | DOM  |
| :-------------------- | :------------------------------------------------------ | :--- |
| addEventListener()    | 允许在目标事件中注册监听事件(IE8 = attachEvent())       | 2    |
| dispatchEvent()       | 允许发送事件到监听器上 (IE8 = fireEvent())              | 2    |
| removeEventListener() | 运行一次注册在事件目标上的监听事件(IE8 = detachEvent()) | 2    |

### 事件监听对象

#### 方法

| 方法          | 描述                         | DOM  |
| :------------ | :--------------------------- | :--- |
| handleEvent() | 把任意对象注册为事件处理程序 | 2    |

### 文档事件对象

#### 方法

| 方法          | 描述 | DOM  |
| :------------ | :--- | :--- |
| createEvent() |      | 2    |

### 鼠标/键盘事件对象

#### 属性

| 属性                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [altKey](https://www.runoob.com/jsref/event-altkey.html)     | 返回当事件被触发时，"ALT" 是否被按下。                       | 2    |
| [button](https://www.runoob.com/jsref/event-button.html)     | 返回当事件被触发时，哪个鼠标按钮被点击。                     | 2    |
| [clientX](https://www.runoob.com/jsref/event-clientx.html)   | 返回当事件被触发时，鼠标指针的水平坐标。                     | 2    |
| [clientY](https://www.runoob.com/jsref/event-clienty.html)   | 返回当事件被触发时，鼠标指针的垂直坐标。                     | 2    |
| [ctrlKey](https://www.runoob.com/jsref/event-ctrlkey.html)   | 返回当事件被触发时，"CTRL" 键是否被按下。                    | 2    |
| [Location](https://www.runoob.com/jsref/event-key-location.html) | 返回按键在设备上的位置                                       | 3    |
| [charCode](https://www.runoob.com/jsref/event-key-charcode.html) | 返回onkeypress事件触发键值的字母代码。                       | 2    |
| [key](https://www.runoob.com/jsref/event-key-key.html)       | 在按下按键时返回按键的标识符。                               | 3    |
| [keyCode](https://www.runoob.com/jsref/event-key-keycode.html) | 返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码。 | 2    |
| [which](https://www.runoob.com/jsref/event-key-which.html)   | 返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码。 | 2    |
| [metaKey](https://www.runoob.com/jsref/event-metakey.html)   | 返回当事件被触发时，"meta" 键是否被按下。                    | 2    |
| [relatedTarget](https://www.runoob.com/jsref/event-relatedtarget.html) | 返回与事件的目标节点相关的节点。                             | 2    |
| [screenX](https://www.runoob.com/jsref/event-screenx.html)   | 返回当某个事件被触发时，鼠标指针的水平坐标。                 | 2    |
| [screenY](https://www.runoob.com/jsref/event-screeny.html)   | 返回当某个事件被触发时，鼠标指针的垂直坐标。                 | 2    |
| [shiftKey](https://www.runoob.com/jsref/event-shiftkey.html) | 返回当事件被触发时，"SHIFT" 键是否被按下。                   | 2    |

#### 方法

| 方法                | 描述                   | W3C  |
| :------------------ | :--------------------- | :--- |
| initMouseEvent()    | 初始化鼠标事件对象的值 | 2    |
| initKeyboardEvent() | 初始化键盘事件对象的值 | 3    |

HTML DOM 使 JavaScript 有能力对 HTML 事件做出反应。
如需在用户点击某个元素时执行代码，请向一个 HTML 事件属性添加 JavaScript 代码：

```
onclick=JavaScript
```

| 事件名称 |                                                              |      |
| :------: | ------------------------------------------------------------ | ---- |
| 鼠标事件 | `onmousedown(点击鼠标按钮)、onmouseup(释放鼠标按钮) 以及 onclick 事件`<br>`onmouseover（鼠标移入）与onmouseout（鼠标移出）` |      |
| 键盘事件 |                                                              |      |
| 滚动事件 |                                                              |      |
| 表单事件 | `onfocus(当输入字段获得焦点时)`                              |      |
| 页面加载 | `onload 和 onunload 事件`                                    |      |

**onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分**。首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。
onload 和 onunload 事件会在用户进入或离开页面时被触发。
onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。
onload 和 onunload 事件可用于处理 cookie。
事件加载方法一：HTML 事件属性

```
<button onclick="displayDate()">点这里</button>
```

### DOM EventListener  `addEventListener() 和 removerEventListener()`

---

### addEventListener()方法

- addEventListener()方法用于向指定元素添加事件句柄、
- 添加的事件句柄不会覆盖已存在的事件句柄、
- 可以向一个元素添加多个事件句柄、
- 可以向同个元素添加多个同类型的事件句柄、
- 可以向任何 DOM 对象添加事件监听，不仅仅是 HTML 元素。如： window 对象。
- ==addEventListener() 方法可以更简单的控制事件（冒泡与捕获）==

```js
element.addEventListener(event, function, useCapture);
element.addEventListener("click",displayDate);
elemnet.addEventListener("click",function(){	});
//不要使用 "on" 前缀。 例如，使用 "click" ,而不是使用 "onclick"。
```

- 第一个参数是事件的类型 (如 "click" 或 "mousedown").
- 第二个参数是事件触发后调用的函数。
- `第三个参数是个布尔值用于描述事件是冒泡还是捕获。该参数是可选的。`

##### 传递参数

当传递参数值时，使用"匿名函数"调用带参数的函数：

##### 实例

```
element.addEventListener("click", function(){ myFunction(p1, p2); });
```

### removerEventListener()方法

```
element.removeEventListener("mousemove", myFunction);
element.attachEvent(event, function);
element.detachEvent(event, function);
注意： IE 8 及更早 IE 版本，Opera 7.0及其更早版本不支持 addEventListener() 和 removeEventListener() 方法。但是，对于这类浏览器版本可以使用 detachEvent() 方法来移除事件句柄:
```

跨浏览器解决方法:

```
var x = document.getElementById("myBtn");
if (x.addEventListener) {          // 所有主流浏览器，除了 IE 8 及更早版本
  x.addEventListener("click", myFunction);
} else if (x.attachEvent) {         // IE 8 及更早版本
  x.attachEvent("onclick", myFunction);
}
```

### 事件冒泡( false 里到外，默认冒泡)或事件捕获(外到里)

`事件传递有两种方式：冒泡与捕获。`
事件传递定义了元素事件触发的顺序。 如果你将 <p> 元素插入到 <div> 元素中，用户点击 <p> 元素, 哪个元素的 "click" 事件先被触发呢？
在 *冒泡* 中，内部元素的事件会先被触发，然后再触发外部元素，即： <p> 元素的点击事件先触发，然后会触发 <div> 元素的点击事件。
在 *捕获* 中，外部元素的事件会先被触发，然后才会触发内部元素的事件，即： <div> 元素的点击事件先触发 ，然后再触发 <p> 元素的点击事件。
addEventListener() 方法可以指定 "useCapture" 参数来设置传递类型：

```
addEventListener(event, function, useCapture);
```

`默认值为 false, 即冒泡传递，当值为 true 时, 事件使用捕获传递。`

```
document.getElementById("myDiv").addEventListener("click", myFunction, true);
```

> 设置父元素为true，
> [JS阻止冒泡和取消默认事件(默认行为)-前端开发博客](http://caibaojian.com/javascript-stoppropagation-preventdefault.html)

### 阻止冒泡 `e.stopPropagation() 与 e.canceBubble = true`

w3c的方法是`e.stopPropagation()`  、IE则是使用``e.canceBubble = true`
stopPropagation也是事件对象(Event)的一个方法，作用是阻止目标元素的冒泡事件，但是会不阻止默认行为。

```js
window.event?window.event.cancelBubble = true:e.stopPropagation()
function stopBubble(e) { 
//如果提供了事件对象，则这是一个非IE浏览器 
if ( e && e.stopPropagation ) 
    //因此它支持W3C的stopPropagation()方法 
    e.stopPropagation(); 
else 
    //否则，我们需要使用IE的方式来取消事件冒泡 
    window.event.cancelBubble = true; 
}
```

[javascript常用代码大全-前端开发博客](http://caibaojian.com/288.html)

### 取消默认事件 `e.preventDefault() e.returnValue = false`

w3c的方法是`e.preventDefault()`，IE则是使用`e.returnValue = false`;
preventDefault它是事件对象(Event)的一个方法，作用是取消一个目标元素的默认行为。既然是说默认行为，当然是元素必须有默认行为才能被取消，如果元素本身就没有默认行为，调用当然就无效了。
什么元素有默认行为呢？如链接<a>，提交按钮<input type="submit">等。当Event 对象的 cancelable为false时，表示没有默认行为，这时即使有默认行为，调用preventDefault也是不会起作用的。

```js
//假定有链接<a href="http://caibaojian.com/" id="testA" >caibaojian.com</a>
var a = document.getElementById("testA");
a.onclick =function(e){
if(e.preventDefault){
e.preventDefault();
}else{
window.event.returnValue == false;
}
}
//阻止浏览器的默认行为 
function stopDefault( e ) { 
    //阻止默认浏览器动作(W3C) 
    if ( e && e.preventDefault ) 
        e.preventDefault(); 
    //IE中阻止函数器默认动作的方式 
    else 
        window.event.returnValue = false; 
    return false; 
}
```

### 使用[jQuery](http://caibaojian.com/t/jquery)，既阻止默认行为又停止冒泡

```html
<div id='div'  onclick='alert("div");'>
<ul  onclick='alert("ul");'>
<li id='ul-a' onclick='alert("li");'><a href="http://caibaojian.com/"id="testC">caibaojian.com</a></li>
</ul>
</div>
$("#testC").on('click',function(){
return false;
});
```

# 计时器

``setInterval()/clearInterval() 不停的执行 setTimeout()/clearTimeout()执行一次``
---

<font color="red" size="3" style="background:#F8F8F8">JavaScript做到在一个设定的时间间隔之后来执行代码，而不是在函数被调用后立即执行，这就是计时事件</font>

|                             属性                             | 功能                                   |
| :----------------------------------------------------------: | -------------------------------------- |
| `setInterval("javascript function",milliseconds)/clearInterval(intervalVariable)` | 间隔毫秒数不停的执行指定的代码不停执行 |
| `setTimeout("javascript function",milliseconds)/clearTimeout(intervalVariable)` | 在指定的好毫秒数后执行指定的代码一个   |

> setInterval() 和 setTimeout() 是 HTML DOM Window对象的两个方法。
>
> **window.setInterval()** 方法可以不使用 window 前缀，直接使用函数 **setInterval()**。
>
> setInterval() 第一个参数是函数（function）。
>
> 第二个参数间隔的毫秒数
>
> 两者的区别：
>
> `setInterval() 不停的执行code`
>
> `setTimeout() 只执行 code 一次`。如果要多次调用，请使用 setInterval() 或者让 code 自身再次调用 setTimeout()。
>
> 业务场景
>
> - setTimeout用于延迟执行某方法或功能
>
> - setInterval则一般用于刷新表单，对于一些表单的假实时指定时间刷新同步

# 代码技巧

[loverajoel/jstips: This is about useful JS tips!](https://github.com/loverajoel/jstips/)、



## 数组

> [数组遍历 - 搜索](https://juejin.cn/search?query=%E6%95%B0%E7%BB%84%E9%81%8D%E5%8E%86&type=all)

### 遍历

```js
let arr = [1,2,3,4,5,7]
```

- for 循环、while循环

```js
for(let index = 0;index < arr.length;index++){
 	console.log(arr[index])
}

let i = 0;
while(i < arr.length){
    console.log(arr[i])
    i++
}
```

- for in

```js
for(let i in arr){
	console.log(arr[i])
}	
```

- for of 循环

```js

```

- forEarh

```js
arr.forEarh((item,index) =>{
	console.log(arr[index])
})
```

- map

```

```

- filter

```

```

- some

```

```

- every

```

```

- reduce

```

```

- reduceRight

```

```

- find

```

```

### 去重





### 浅拷贝





### 合并





### 取交集













## 拷贝 

```js
document.querSelector('#input').select()
document.execCommand('copy')
```



# 数据结构



# 设计模式





外观模式



代理模式









工厂模式





单例模式





策略模式



迭代器模式





观察者模式



中介者模式





访问者模式

