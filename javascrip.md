---
title: JavaScript基础
categories:
  - JavaScript
tags:
  - 前端
  - JavaScript
abbrlink: 53226
---
# 基础知识

match

element.src style 

onclick="fuc()"





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

