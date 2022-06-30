---
title: dom、bom和对象手册
categories:
- 前端
tags:
- dom&&bom&&对象
abbrlink: 53953
---
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
> 	- 可以通过指定数组增加或删除数组元素
> 	
> - join & split
>
> 	- join 数组转字符串
> 		- join
> 		-  toLocaleString() 数组转字符串
> 		- toString() 数组转字符串 不推荐
> 	- split 
>
> - 数组添加删除 头部或尾部（ push()、pop()、unshift()、shift() ）
>
> 	- (数组末尾)push & pop
> 	- push 数组结尾添加一项项或多项，返回添加元素数组后的长度
> 	- pop  删除数组最后一项，返回删除的那一项
> 	- (数组开头) unshift & shift 
>
> 	- unshift 向数组开头添加一项或者多项
> 	- shift 删除数组第一项，返回删除的那一项 
>
> - reverse & sort
>
> 	- reverse 翻转原数组，返回翻转后的数组
> 	- sort 数组排序
>
> - concat，slice & splice
>
> 	- concat 拼接数组
> 	- slice  基于当前数组的一项或多项创建一个新的数组（裁剪数组、赋值数组）
> 	- splice  添加/删除数组元素
>
> - indexOf & lastIndexOf  元素查找索引位置
>
> 	-  indexOf： 从数组开头查找元素在数组中的索引位置
> 	-  lastIndexOf： 从数组结尾查找元素在数组中的索引位置
>
> - every, filter, forEach, map & some 迭代方法
>
> 	- every  对数组中的每一项运行给定函数，如果该函数对每一项都返回true,则返回true
> 	- filter
> 	- forEach(item,index,array)  对数组中的每一项运行给定函数。无返回值
> 	- map
> 	- some
>
> - reduce & reduceRight 缩小方法
>
> 	- reduce 从数组的第一项开始，逐步遍历到最后，迭代数组的所有项
> 	- reduceRight 从数组的最后一项开始，逐步遍历到第一项，迭代数组的所有项
>
> - toString & Array.isArray(数组)[判断是不是数组]  数组的检测
>
> 	- toString
> 	- Array,isArray
>
> ES6
>
> - 数组拓展运算符`...`
> 	- 数组的扩展运算符可以将数组转化为以逗号分割的参数序列
> - Array.from() & Array.of()
> - copyWithin(target,start=0,end=this.length) 拷贝，将数组指定位置（start到end）的元素复制到当前数组的其他位置（target开始），这种复制会替换原位置的元素（ES6新增）
> - fill
> 	- 数组填充
> - find & findIndex
> - entries() 、keys() & values()
> 	- entries()
> 	- keys()
> 	- values()
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
| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [getDate()](https://www.runoob.com/jsref/jsref-getdate.html) | 从 Date 对象返回一个月中的某一天 (1 ~ 31)。                  |
|                                                              |                                                              |
| [getFullYear()](https://www.runoob.com/jsref/jsref-getfullyear.html) | 从 Date 对象以四位数字返回年份。                             |
| [getMonth()](https://www.runoob.com/jsref/jsref-getmonth.html) | 从 Date 对象返回月份 (0 ~ 11)。                              |
| [getDay()](https://www.runoob.com/jsref/jsref-getday.html)   | 从 Date 对象返回一周中的某一天 (0 ~ 6)。                     |
| [getHours()](https://www.runoob.com/jsref/jsref-gethours.html) | 返回 Date 对象的小时 (0 ~ 23)。                              |
| [getMinutes()](https://www.runoob.com/jsref/jsref-getminutes.html) | 返回 Date 对象的分钟 (0 ~ 59)。                              |
| [getSeconds()](https://www.runoob.com/jsref/jsref-getseconds.html) | 返回 Date 对象的秒数 (0 ~ 59)。                              |
| [getMilliseconds()](https://www.runoob.com/jsref/jsref-getmilliseconds.html) | 返回 Date 对象的毫秒(0 ~ 999)。                              |
|                                                              |                                                              |
| [getTime()](https://www.runoob.com/jsref/jsref-gettime.html) | 返回 1970 年 1 月 1 日至今的毫秒数。                         |
|                                                              |                                                              |
| [getTimezoneOffset()](https://www.runoob.com/jsref/jsref-gettimezoneoffset.html) | 返回本地时间与格林威治标准时间 (GMT) 的分钟差。              |
|                                                              |                                                              |
| [getUTCDate()](https://www.runoob.com/jsref/jsref-getutcdate.html) | 根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。              |
| [getUTCFullYear()](https://www.runoob.com/jsref/jsref-getutcfullyear.html) | 根据世界时从 Date 对象返回四位数的年份。                     |
| [getUTCMonth()](https://www.runoob.com/jsref/jsref-getutcmonth.html) | 根据世界时从 Date 对象返回月份 (0 ~ 11)。                    |
| [getUTCDay()](https://www.runoob.com/jsref/jsref-getutcday.html) | 根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。               |
| [getUTCHours()](https://www.runoob.com/jsref/jsref-getutchours.html) | 根据世界时返回 Date 对象的小时 (0 ~ 23)。                    |
| [getUTCMinutes()](https://www.runoob.com/jsref/jsref-getutcminutes.html) | 根据世界时返回 Date 对象的分钟 (0 ~ 59)。                    |
| [getUTCSeconds()](https://www.runoob.com/jsref/jsref-getutcseconds.html) | 根据世界时返回 Date 对象的秒钟 (0 ~ 59)。                    |
| [getUTCMilliseconds()](https://www.runoob.com/jsref/jsref-getutcmilliseconds.html) | 根据世界时返回 Date 对象的毫秒(0 ~ 999)。                    |
|                                                              |                                                              |
| getYear()                                                    | 已废弃。 请使用 getFullYear() 方法代替。                     |
| [parse()](https://www.runoob.com/jsref/jsref-parse.html)     | 返回1970年1月1日午夜到指定日期（字符串）的毫秒数。           |
| [setDate()](https://www.runoob.com/jsref/jsref-setdate.html) | 设置 Date 对象中月的某一天 (1 ~ 31)。                        |
| [setFullYear()](https://www.runoob.com/jsref/jsref-setfullyear.html) | 设置 Date 对象中的年份（四位数字）。                         |
| [setHours()](https://www.runoob.com/jsref/jsref-sethours.html) | 设置 Date 对象中的小时 (0 ~ 23)。                            |
| [setMilliseconds()](https://www.runoob.com/jsref/jsref-setmilliseconds.html) | 设置 Date 对象中的毫秒 (0 ~ 999)。                           |
| [setMinutes()](https://www.runoob.com/jsref/jsref-setminutes.html) | 设置 Date 对象中的分钟 (0 ~ 59)。                            |
| [setMonth()](https://www.runoob.com/jsref/jsref-setmonth.html) | 设置 Date 对象中月份 (0 ~ 11)。                              |
| [setSeconds()](https://www.runoob.com/jsref/jsref-setseconds.html) | 设置 Date 对象中的秒钟 (0 ~ 59)。                            |
| [setTime()](https://www.runoob.com/jsref/jsref-settime.html) | setTime() 方法以毫秒设置 Date 对象。                         |
| [setUTCDate()](https://www.runoob.com/jsref/jsref-setutcdate.html) | 根据世界时设置 Date 对象中月份的一天 (1 ~ 31)。              |
| [setUTCFullYear()](https://www.runoob.com/jsref/jsref-setutcfullyear.html) | 根据世界时设置 Date 对象中的年份（四位数字）。               |
| [setUTCHours()](https://www.runoob.com/jsref/jsref-setutchours.html) | 根据世界时设置 Date 对象中的小时 (0 ~ 23)。                  |
| [setUTCMilliseconds()](https://www.runoob.com/jsref/jsref-setutcmilliseconds.html) | 根据世界时设置 Date 对象中的毫秒 (0 ~ 999)。                 |
| [setUTCMinutes()](https://www.runoob.com/jsref/jsref-setutcminutes.html) | 根据世界时设置 Date 对象中的分钟 (0 ~ 59)。                  |
| [setUTCMonth()](https://www.runoob.com/jsref/jsref-setutcmonth.html) | 根据世界时设置 Date 对象中的月份 (0 ~ 11)。                  |
| [setUTCSeconds()](https://www.runoob.com/jsref/jsref-setutcseconds.html) | setUTCSeconds() 方法用于根据世界时 (UTC) 设置指定时间的秒字段。 |
| setYear()                                                    | 已废弃。请使用 setFullYear() 方法代替。                      |
| [toDateString()](https://www.runoob.com/jsref/jsref-todatestring.html) | 把 Date 对象的日期部分转换为字符串。                         |
| toGMTString()                                                | 已废弃。请使用 toUTCString() 方法代替。                      |
| [toISOString()](https://www.runoob.com/jsref/jsref-toisostring.html) | 使用 ISO 标准返回字符串的日期格式。                          |
| [toJSON()](https://www.runoob.com/jsref/jsref-tojson.html)   | 以 JSON 数据格式返回日期字符串。                             |
| [toLocaleDateString()](https://www.runoob.com/jsref/jsref-tolocaledatestring.html) | 根据本地时间格式，把 Date 对象的日期部分转换为字符串。       |
| [toLocaleTimeString()](https://www.runoob.com/jsref/jsref-tolocaletimestring.html) | 根据本地时间格式，把 Date 对象的时间部分转换为字符串。       |
| [toLocaleString()](https://www.runoob.com/jsref/jsref-tolocalestring.html) | 据本地时间格式，把 Date 对象转换为字符串。                   |
| [toString()](https://www.runoob.com/jsref/jsref-tostring-date.html) | 把 Date 对象转换为字符串。                                   |
| [toTimeString()](https://www.runoob.com/jsref/jsref-totimestring.html) | 把 Date 对象的时间部分转换为字符串。                         |
| [toUTCString()](https://www.runoob.com/jsref/jsref-toutcstring.html) | 根据世界时，把 Date 对象转换为字符串。实例：`var today = new Date(); var UTCstring = today.toUTCString();` |
| [UTC()](https://www.runoob.com/jsref/jsref-utc.html)         | 根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。        |
| [valueOf()](https://www.runoob.com/jsref/jsref-valueof-date.html) | 返回 Date 对象的原始值。                                     |
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
| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [abs(x)](https://www.runoob.com/jsref/jsref-abs.html)        | 返回 x 的绝对值。                                            |
| [acos(x)](https://www.runoob.com/jsref/jsref-acos.html)      | 返回 x 的反余弦值。                                          |
| [asin(x)](https://www.runoob.com/jsref/jsref-asin.html)      | 返回 x 的反正弦值。                                          |
| [atan(x)](https://www.runoob.com/jsref/jsref-atan.html)      | 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。     |
| [atan2(y,x)](https://www.runoob.com/jsref/jsref-atan2.html)  | 返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。 |
|                                                              |                                                              |
| [ceil(x)](https://www.runoob.com/jsref/jsref-ceil.html)      | 对数进行上舍入。                                             |
| [cos(x)](https://www.runoob.com/jsref/jsref-cos.html)        | 返回数的余弦。                                               |
| [exp(x)](https://www.runoob.com/jsref/jsref-exp.html)        | 返回 Ex 的指数。                                             |
| [floor(x)](https://www.runoob.com/jsref/jsref-floor.html)    | 对 x 进行下舍入。                                            |
| [log(x)](https://www.runoob.com/jsref/jsref-log.html)        | 返回数的自然对数（底为e）。                                  |
| [max(x,y,z,...,n)](https://www.runoob.com/jsref/jsref-max.html) | 返回 x,y,z,...,n 中的最高值。                                |
| [min(x,y,z,...,n)](https://www.runoob.com/jsref/jsref-min.html) | 返回 x,y,z,...,n中的最低值。                                 |
| [pow(x,y)](https://www.runoob.com/jsref/jsref-pow.html)      | 返回 x 的 y 次幂。                                           |
| [random()](https://www.runoob.com/jsref/jsref-random.html)   | 返回 0 ~ 1 之间的随机数。                                    |
| [round(x)](https://www.runoob.com/jsref/jsref-round.html)    | 四舍五入。                                                   |
| [sin(x)](https://www.runoob.com/jsref/jsref-sin.html)        | 返回数的正弦。                                               |
| [sqrt(x)](https://www.runoob.com/jsref/jsref-sqrt.html)      | 返回数的平方根。                                             |
| [tan(x)](https://www.runoob.com/jsref/jsref-tan.html)        | 返回角的正切。                                               |
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
| 属性        | 描述                       |
| :---------- | :------------------------- |
| constructor | 返回创建字符串属性的函数   |
| length      | 返回字符串的长度           |
| prototype   | 允许您向对象添加属性和方法 |
字符串方法
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
| 属性                                                         | 描述                     |
| :----------------------------------------------------------- | :----------------------- |
| [Infinity](https://www.runoob.com/jsref/jsref-infinity.html) | 代表正的无穷大的数值。   |
| [NaN](https://www.runoob.com/jsref/jsref-nan.html)           | 指示某个值是不是数字值。 |
| [undefined](https://www.runoob.com/jsref/jsref-undefined.html) | 指示未定义的值。         |
JavaScript 全局函数
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
CSSStyleDeclaration 对象方法
| 方法                                                         | 描述                                              |
| :----------------------------------------------------------- | :------------------------------------------------ |
| [getPropertyPriority()](https://www.runoob.com/jsref/met-cssstyle-getpropertypriority.html) | 返回指定的 CSS 属性是否设置了 "important!" 属性。 |
| [getPropertyValue()](https://www.runoob.com/jsref/met-cssstyle-getpropertyvalue.html) | 返回指定的 CSS 属性值。                           |
| [item()](https://www.runoob.com/jsref/met-cssstyle-item.html) | 通过索引方式返回 CSS 声明中的 CSS 属性名。        |
| [removeProperty()](https://www.runoob.com/jsref/met-cssstyle-removeproperty.html) | 移除 CSS 声明中的 CSS 属性。                      |
| [setProperty()](https://www.runoob.com/jsref/met-cssstyle-setproperty.html) | 在 CSS 声明块中新建或者修改 CSS 属性。            |
DOM CSS `Element.style.property=新样式`

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
> 	- window  浏览器中打开的窗口
> 		- navigator  有关浏览器的信息
> 		- screen  有关客户端 显示屏幕的信息
> 		- history  用户（在浏览器窗口中）访问过的 URL
> 		- location  有关当前 URL 的信息。
> - DOM  文档对象模型
> 	- document  
| window尺寸的方法                                             | 功能                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| window.innerHeight/ window.innerWidth                        | 对于Internet Explorer、Chrome、Firefox、Opera 以及 Safari：<br />浏览器窗口的内部高度/宽度（包括滚动条） |
| document.documentElement.clientHeight/clientWidth<br />document.body.clientHeight/clientWidth | 对于 Internet Explorer 8、7、6、5（不包括滚动条）            |
| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [document](https://www.runoob.com/jsref/dom-obj-document.html) | 对 Document 对象的只读引用。(请参阅[对象](https://www.runoob.com/jsref/dom-obj-document.html)) |
| [navigator](https://www.runoob.com/jsref/obj-navigator.html) | 对 Navigator 对象的只读引用。请参数 [Navigator 对象](https://www.runoob.com/jsref/obj-navigator.html)。 |
| [screen](https://www.runoob.com/jsref/obj-screen.html)       | 对 Screen 对象的只读引用。请参数 [Screen 对象](https://www.runoob.com/jsref/obj-screen.html)。 |
| [history](https://www.runoob.com/jsref/obj-history.html)     | 对 History 对象的只读引用。请参数 [History 对象](https://www.runoob.com/jsref/obj-history.html)。 |
| [location](https://www.runoob.com/jsref/obj-location.html)   | 用于窗口或框架的 Location 对象。请参阅 [Location 对象](https://www.runoob.com/jsref/obj-location.html)。 |
|                                                              |                                                              |
| [innerWidth](https://www.runoob.com/jsref/prop-win-innerheight.html)，[innerHeight](https://www.runoob.com/jsref/prop-win-innerheight.html) | 返回窗口的文档显示区的宽度、高度。                           |
| [outerWidth](https://www.runoob.com/jsref/prop-win-outerheight.html)、[outerHeight](https://www.runoob.com/jsref/prop-win-outerheight.html) | 返回窗口的外部宽度、高度，包含工具条与滚动条。               |
| clientHeight/clientWidth                                     |                                                              |
| [screenLeft](https://www.runoob.com/jsref/prop-win-screenleft.html)、[screenTop](https://www.runoob.com/jsref/prop-win-screenleft.html) | 返回相对于屏幕窗口的x、y坐标                                 |
| [screenX](https://www.runoob.com/jsref/prop-win-screenx.html)、[screenY](https://www.runoob.com/jsref/prop-win-screenx.html) | 返回相对于屏幕窗口的x、y坐标                                 |
| [pageXOffset](https://www.runoob.com/jsref/prop-win-pagexoffset.html)、[pageYOffset](https://www.runoob.com/jsref/prop-win-pagexoffset.html) | 设置或返回当前页面相对于窗口显示区左上角的 X 、Y位置。       |
|                                                              |                                                              |
| [localStorage](https://www.runoob.com/jsref/prop-win-localstorage.html)、[sessionStorage](https://www.runoob.com/jsref/prop-win-sessionstorage.html) | 在浏览器中存储 key/value 对。没有过期时间。在浏览器中存储 key/value 对。 在关闭窗口或标签页之后将会删除这些数据。 |
|                                                              |                                                              |
| [length](https://www.runoob.com/jsref/prop-win-length.html)  | 设置或返回窗口中的框架数量。                                 |
| [name](https://www.runoob.com/jsref/prop-win-name.html)      | 设置或返回窗口的名称。                                       |
| [closed](https://www.runoob.com/jsref/prop-win-closed.html)  | 返回窗口是否已被关闭。                                       |
| [frames](https://www.runoob.com/jsref/prop-win-frames.html)  | 返回窗口中所有命名的框架。该集合是 Window 对象的数组，每个 Window 对象在窗口中含有一个框架。 |
| [parent](https://www.runoob.com/jsref/prop-win-parent.html)  | 返回父窗口。                                                 |
| [self](https://www.runoob.com/jsref/prop-win-self.html)      | 返回对当前窗口的引用。等价于 Window 属性。                   |
| [top](https://www.runoob.com/jsref/prop-win-top.html)        | 返回最顶层的父窗口。                                         |
| [status](https://www.runoob.com/jsref/prop-win-status.html)  | 设置窗口状态栏的文本。                                       |
| [opener](https://www.runoob.com/jsref/prop-win-opener.html)  | 返回对创建此窗口的窗口的引用。                               |
| [defaultStatus](https://www.runoob.com/jsref/prop-win-defaultstatus.html) | 设置或返回窗口状态栏中的默认文本。                           |
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
### Screen 对象属性  `6`
| 属性                                                         | 说明                                                       |
| :----------------------------------------------------------- | :--------------------------------------------------------- |
| [availWidth](https://www.runoob.com/jsref/prop-screen-availwidth.html)、[availHeight](https://www.runoob.com/jsref/prop-screen-availheight.html) | 返回屏幕的宽度、高度（不包括Windows任务栏） 可用屏幕的宽度 |
| [width](https://www.runoob.com/jsref/prop-screen-width.html)、[height](https://www.runoob.com/jsref/prop-screen-height.html) | 返回屏幕的总宽度、总高度                                   |
| [colorDepth](https://www.runoob.com/jsref/prop-screen-colordepth.html) | 返回目标设备或缓冲器上的调色板的比特深度                   |
| [pixelDepth](https://www.runoob.com/jsref/prop-screen-pixeldepth.html) | 返回屏幕的颜色分辨率（每像素的位数）                       |
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
| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [hash](https://www.runoob.com/jsref/prop-loc-hash.html)      | 返回一个URL的锚部分，hash 属性是一个可读可写的字符串，该字符串是 URL 的锚部分（从 # 号开始的部分）http://www.runoob.com/test.htm＃PART2  hash 是 ``#PART2` |
|                                                              |                                                              |
| [href](https://www.runoob.com/jsref/prop-loc-href.html)      | 返回``完整的URL`                                             |
| [protocol](https://www.runoob.com/jsref/prop-loc-protocol.html) | 返回一个URL`协议`                                            |
| [hostname](https://www.runoob.com/jsref/prop-loc-hostname.html) | 返回URL的主机名                                              |
| [port](https://www.runoob.com/jsref/prop-loc-port.html)      | 返回一个URL服务器使用的端口号                                |
| [pathname](https://www.runoob.com/jsref/prop-loc-pathname.html) | 返回的URL路径名。                                            |
| [host](https://www.runoob.com/jsref/prop-loc-host.html)      | 返回一个URL的主机名和端口                                    |
|                                                              |                                                              |
| [search](https://www.runoob.com/jsref/prop-loc-search.html)  | 返回一个URL的查询部分，search 属性是一个可读可写的字符串，可设置或返回当前 URL 的查询部分（问号 ? 之后的部分） 如http://www.runoob.com/submit.htm?email=someone@ example.com 输出结果`?email=someone@ example.com` |
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
> 	reload()方法用于刷新当前文档。
>
> 	reload() 方法类似于你浏览器上的刷新页面按钮。
>
> 	`location.reload();`
>
> - replace() 方法;
>
> 	**replace() 方法**可用一个新文档取代当前文档。
>
> 	`window.location.replace("url")`
>
> - 页面自动刷新;
>
> 	页面自动刷新：把如下代码加入``<head>``区域中
>
> 	`<meta http-equiv="refresh" content="5">`
### 浏览器重定向
- `port portocol reload() replace() assign() `
- `href = hostname + pathname`
- location.reload() 
- window.location.replace("url") 
-  `<meta http-equiv="refresh" content="5">`
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
