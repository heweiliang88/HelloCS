---
title: 过时的jquery，也能焕发光彩
categories:
- 前端
tags:
- jquery
abbrlink: 64469
---
# JQuery

## 常用API

[jQuery API 中文文档 | jQuery 中文网](https://www.jquery123.com/)

[jQuery 参考手册](http://www.w3school.me/jquery/jquery-ref-selectors.html)

```
$.fn.jquery
$(this) == this
```



| 鼠标事件              | 键盘事件             | 表单事件                               | 文档/窗口事件                                                |
| --------------------- | -------------------- | -------------------------------------- | ------------------------------------------------------------ |
| `click`               | `keypress 键被按下`  | `submit 提交`                          | `load 指定的元素已加载`                                      |
| `dbclick`             | `keydown 按下的过程` | `change 元素的值改变,仅适用于表单字段` | `resize 调整浏览器窗口大小`                                  |
| `mouseenter 鼠标进入` | `keyup 键被松开`     | `focus 获得焦点`                       | `scroll 滚动指定的元素`                                      |
| `mouseleave 鼠标离开` |                      | `blur 失去焦点`                        | `unload 方法在 jQuery 版本 1.8 中被废弃，在 3.0 版本被移除。` |
| `mousedown 鼠标按下`  |                      |                                        |                                                              |
| `mouseup 鼠标松开`    |                      |                                        |                                                              |
| `hover`               |                      |                                        |                                                              |

| 显示、隐藏                | 作用               |
| ------------------------- | ------------------ |
| `hide(slow) / hide(time)` | 隐藏               |
| `show`                    | 显示               |
| `toggle`                  | 切换hide()和show() |

| 淡入淡出 fade in out toggle      | 作用                                                         |
| -------------------------------- | ------------------------------------------------------------ |
| `fadeIn(speed,callback)`         | 淡入已隐藏的元素                                             |
| `fadeOut(speed,callback)`        | 淡出可见元素                                                 |
| `fadeToggle(speed,callback)`     | fadeIn() 与 fadeOut() 方法之间进行切换                       |
| `fadeTo(speed,opacity,callback)` | "slow"、"fast" 或毫秒，允许渐变为给定的不透明度（值介于 0 与 1 之间） |

| 滑动元素 slide down up toggle | 作用                                      |
| ----------------------------- | ----------------------------------------- |
| `slideDown(speed,callback)`   | 向下滑动元素                              |
| `slideUp(speed,callback)`     | 向上滑动元素                              |
| `slideToggle(speed,callback)` | slideDown() 与 slideUp() 方法之间进行切换 |

| 动画                              | 作用                                                         |
| --------------------------------- | ------------------------------------------------------------ |
| `animate({params},speed,calback)` | 动画效果（可以操作多个属性，使用相对值，使用预定义的值，使用队列功能） |
| `stop(stopAll,goToEnd)`           | 停止动画                                                     |

| 修改文本 | 作用                               |
| -------- | ---------------------------------- |
| `text()` | 设置或返回所选元素的文本内容       |
| `html()` | 设置或返回所选元素的内容           |
| `val()`  | 设置或返回表单字段的值             |
| `attr()` | HTML 元素我们自己自定义的 DOM 属性 |
| `prop()` | HTML 元素本身就带有的固有属性      |

| 插入内容    | 作用                 |
| ----------- | -------------------- |
| `append()`  | 结尾插入内容         |
| `prepend()` | 元素开头插入内容     |
| `after()`   | 被选元素之后插入内容 |
| `before()`  | 被选元素之前插入内容 |

- append/prepend 是在选择元素内部嵌入。
- after/before 是在元素外面追加。

| 删除元素   | 作用                       |
| ---------- | -------------------------- |
| `remove()` | 删除被选元素（及其子元素） |
| `empty()`  | 从被选元素中删除子元素     |

| 操作css                          | 作用                                |
| -------------------------------- | ----------------------------------- |
| `addClass()`                     | 向被选元素添加一个或多个类          |
| `removeClass()`                  | 从被选元素删除一个或多个类          |
| `toggleClass()`                  | 对被选元素进行添加/删除类的切换操作 |
| `css({"":"","":""})，css("","")` | 设置或返回样式属性                  |

<img src="https://www.runoob.com/images/img_jquerydim.gif" alt="jQuery Dimensions" style="zoom:67%;" />

| 尺寸          | 作用                                                 |
| ------------- | ---------------------------------------------------- |
| width()       | 设置或返回元素的宽度（不包括内边距、边框或外边距     |
| height()      | 设置或返回元素的高度（不包括内边距、边框或外边距     |
| innerWidth()  | 返回元素的宽度（包括内边距） +  padding              |
| innerHeight() | 返回元素的高度（包括内边距）                         |
| outerWidth()  | 返回元素的宽度（包括内边距和边框）+ padding + border |
| outerHeight() | 返回元素的宽度（包括内边距和边框）                   |

| 遍历           | 作用                                                         |
| -------------- | ------------------------------------------------------------ |
| 向上遍历       | parent()                                                     |
| parent()       | 方法返回被选元素的直接父元素                                 |
| parents()      | 方法返回被选元素的所有祖先元素，它一路向上直到文档的根元素 `(<html>)` |
| parentsUntil() | 方法返回介于两个给定元素之间的所有祖先元素``$("span").parentsUntil("div");`` |
| 向下遍历       |                                                              |
| children()     | 方法返回被选元素的所有直接子元素                             |
| find()         | 方法返回被选元素的后代元素，一路向下直到最后一个后代。       |
| 同胞           |                                                              |
| 之前           |                                                              |
| siblings()     | 返回被选元素的所有同胞元素                                   |
| next()         | 返回被选元素的下一个同胞元素                                 |
| nextAll()      | 返回元素的所有跟随的同胞元素                                 |
| nextUnit()     | 返回介于两个给定参数之间的所有跟随的同胞元素                 |
| 之后           |                                                              |
| prev()         | 返回前面的同胞元素                                           |
| prevAll()      | 返回前面所有的同胞元素                                       |
| prevUntil()    | 返回介于两个给定参数之间的所有跟随的同胞元素                 |

| 过滤     |                                                              |
| -------- | ------------------------------------------------------------ |
| first()  | 首个元素                                                     |
| last()   | 最后一个元素                                                 |
| eq()     | 返回被选元素中带有指定索引号的元素                           |
| filter() | 允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回 |
| not()    | 返回不匹配标准的所有元素。                                   |

| Ajax   |                                                              |
| ------ | ------------------------------------------------------------ |
| load() |                                                              |
| get()  | 从服务器获得（取回）数据，从指定的资源请求数据               |
| post() | 也可用于从服务器获取数据。不过，POST 方法不会缓存数据，并且常用于连同请求一起发送数据，向指定的资源提交要处理的数据，`向服务器提交数据` |

```js
// 解决问题 在当前 页面下发送 指定网站的请求 
// 发起ajax请求 load
$('#content > div:nth-child(14) > div').load('http://120.78.149.188:3000/search?keywords=%E6%B5%B7%E9%98%94%E5%A4%A9%E7%A9%BA')

//  $.get(URL,callback);
//  $.post(URL,data,callback);
$.get("http://120.78.149.188:3000/search?keywords=%E6%B5%B7%E9%98%94%E5%A4%A9%E7%A9%BA",function(data,status){
    console.log(data)
})

$.post("http://120.78.149.188:3000/search",{ keywords : "你的名字" },function(data,status){
    console.log(data)
    console.log(data)
})
```

|              |                                      |
| ------------ | ------------------------------------ |
| noConflict() | jQuery 使用 $ 符号作为 jQuery 的简写 |

| JSONP |                                                              |
| ----- | ------------------------------------------------------------ |
| JSONP | Jsonp(JSON with Padding) 是 json 的一种"使用模式"，可以让网页从别的域名（网站）那获取资料，即跨域读取数据 |

```js
// 需要服务器端配合
$.getJSOP('https://www.runoob.com/try/ajax/jsonp.php?jsoncallback=?',function(data){

});
```

## 介绍

> [jQuery CDN](https://code.jquery.com/)
### 定义
- jQuery 是一个JavaScript库
- jQuery是一个轻量级的"写的少，做的多"的JavaScript库
### 常见的js库
- Prototype、YUI（网络反响一般）、Dojo、ExtJS、jQuery等
- 这些库对JavaScript进行了封装，简化了开发。
### 为什么要学习JQuery
- DOM中一个简单的功能需要大量的代码、兼容的问题很多、代码的容错性很差、window.onload也只能有一个。
### 特点
- 写的少，做的多
- 很好的解决了不同浏览器的兼容问题（IE 6.0+，FF 2+，Safari 3.0+，Opera 9.0+，Chrome）css还是有问题的对于不同控件具有统--的操作方式
- 体积小（几十KB）、使用简单方便
- 链式编程`$("#div1").draggble().show().hide().fly()`
- 隐式迭代
- 插件丰富、开源、免费
- jQuery兼容于所有主流浏览器, 包括Internet Explorer 6!
### 安装
#### CDN
- 普通版 开发环境
- 压缩版 min.js 生产环境
```js
<script src="https://cdn.bootcdn.net/ajax/libs/jquery/3.5.1/jquery.js"></script>
<script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js">
```
查看jquery版本
```js
console.log($.fn.jquery);
```
#### NPM

```bash
npm install jquery
```
使用
```js
var jq = require('jquery');
console.log(jq);
```
### 顶级对象
- DOM中的顶级对象：docuemnt---页面中的顶级对象 (docuemnt中的属性和方法)
- BOM中的顶级对象：window---浏览器中的项级对象 (window是浏览器中的属性和方法)  window.document 
- jQuery的项级对象：jQuery---  ($点出来的是jQuery中的方法 )
```js
//Javascript
window.onload = function () { }
jQuery的代码---和DOM中的window.onload事件相同的
//页面中所有的内容加载完毕后才触发，标签，图片文字内容....
$(window).load(function(){
	console.log("123");
});
$(window).load(function(){
	console.log("456 ");
});
//第二种页面加载的事件的写法---都是方法了
//页面中的基本的标签加载完毕后就可以触发了
$(document).ready == $
$(document).ready(function(){
	console.log("456");
});

jQuery(function(){
})

$(function(){
})
```
### Jquery对象和DOM对象互转
DOM对象转jQuery对象操作方便，毕竟JQuery中方法都是封装好了的，而且兼容问题解决的很好，代码少，方便。Jquery对象转DOM对象，因为JQuery中文件--直在更新，很多东西都是随着使用而进行封装和升级，不太可能把所有dom中用到的进行封装，还有很多未知的兼容问题没有封装进去，所以，有的时候JQuery中不能解决的问题，还需要原生的js代码来解决，所以，jquery对象有的时候需要转成dom对象来进行操作

- DOM对象转jQuery对象

```js
// $（DOM的对象）---->jQuery对象
window.onload = function () {
    var btnObj = document.getElementById('btn');
    $(btnObj).click(function () {
        // $(this)
        $(this).css("backgroundColor", "red");
    });
};
```
- jQuery对象转DOM对象

```js
//$（"#btn"）[0]--->DOM对象
//$（"#btn"）.get（0）---DOM对象
var btnObj = document.getElementById('btn'); //DOM对象
var obj = $(btnObj).get(0) //DOM对象
var obj = $(btnObj)[0] //DOM对象
$(function(){
    $("#btn").click(function(){
        $(this).css("backgroundColor","yellow");
    });
});
$(function(){
    $("#btn")[0].onclick(function(){
        $(this).css("backgroundColor","yellow");
    });
});
```

```js
// window.onload = function () {
var btn = document.getElementById('btn');
//     btn.onclick = function () {
//         this.style.backgroundColor = "red";
//     }
// }
$(function(){
    $('#btn').click(function(){
        $(this).css("backgroundColor","red");
    });
});
```
```js
<script>
    // Js
    window.onload = function () {
    var btn = document.getElementById('btn')
    btn.onclick = function () {
        if (btn.value == "关灯") {
            document.body.style.backgroundColor = "black"
            btn.value = "开灯"
        } else {
            document.body.style.backgroundColor = "white"
            btn.value = "关灯"
        }
    }
}
<script>
    $(function () {
    $("#btn").click(function () {
        if ($(this).val() == "关灯") {
            $("body").css("backgroundColor", "black")
            $(this).val("开灯")
        } else {
            $("body").css("backgroundColor", "white")
            $(this).val("关灯")
        }
    });
});
</script>
```
**document.body.style.backgroundColor = "white"**
```js
.val()方法--->获取按钮的value属性的值
.val("内容"); 是设置按钮的value属性的值
$(this)
```
## 选择器
### JavaScript选择器

```js
// 根据id获取元素
document.getElementById("id的值");
// 根据标签的名字获取元素多个
document.getElementByTagName(“标签的名字”);
// 根据name属性的值获取元素
document.getElementsByName(“name属性的值");
// 根据的是类样式的名字来获取元素，                           
document.getElementsByClassName("类样式的名字")，
```
### 选择器

|                       符号                        |                       选择器                        |
| :-----------------------------------------------: | :-------------------------------------------------: |
|                     `$("*")`                      |                    选取所有元素                     |
|                   `$(".class")`                   |                      类选择器                       |
|                    `$("#id")`                     |                      id选择器                       |
|                    `$("tag")`                     |                     标签选择器                      |
|             `$(li.cls)、$("p.intro")`             |   标签+类选择器(选取 class 为 intro 的 <p> 元素)    |
|                 `$(span,li,div)`                  |                    多条件选择器                     |
|           `$("#dv li") 或者$("ul li ")`           | 层次选择器：后代选择器（子元素中元素子，仔仔，孙）. |
| `$("#ul>li") 或者$("div>span") 或者$(".cls>li")`  |        子代选择器（直接的所有子元素，儿子）.        |
|                     `$(this)`                     |                 选取当前 HTML 元素                  |
| `eq() 等于索引`、`gt() 大于索引`、`lt() 小于索引` |             索引选择器`索引值从0开始算`             |
|                     `index()`                     |                     获取索引值                      |
|                `:even()`、`:odd()`                |                     奇数、偶数                      |
## 遍历
### 遍历DOM
jQuery 遍历，用于根据其相对于其他元素的关系来查找（或选取）HTML 元素。以某项选择开始，并沿着这个选择移动，直到抵达您期望的元素为止。
jquery 提供了多种遍历DOM方法
- 遍历方法中最大的种类是树遍历`tree-traversal`
### 祖先：向上遍历DOM树
| 方法名          | 作用                                                         |
| --------------- | ------------------------------------------------------------ |
| `parent()`      | 返回被选元素的直接父元素                                     |
| `parents()`     | 方法返回被选元素的所有祖先元素，它一路向上直到文档的根元素`(<html>)` |
| `parentUntil()` | 返回介于两个给定元素之间的所有祖先元素                       |
`parents()`使用可选参数对过滤祖先元素的搜索
```js
$("span").parents("ul") // 返回所有<span>元素的祖先，并且它是<ul>父元素 
// 选中ul的父元素
```
`parentUntil()`方法返回介于两个给定元素之间的所有祖先元素
```js
$("span").parentUntil("div") // <span> 与 <div>之间的所有祖先元素
```
### 后代：向下遍历DOM树
| 方法名       | 作用                                                 |
| ------------ | ---------------------------------------------------- |
| `children()` | 返回被选元素的所有``直接子元素(一个)``               |
| `find()`     | 返回被选元素的``后代元素``，一路向下直到最后一个后代 |
`children()`使用可选参数来过滤对子元素的搜索
```js
$("div").children("p.1")
```
`find()`找所有的后代元素
返回后代的指定元素`span`
```js
$("div").find("span")
```
返回后代的所有元素`*`
```js
$("div").find("*")
```
### 兄弟：遍历同级元素
| 方法名        | 作用                                                   |
| ------------- | ------------------------------------------------------ |
| `siblings()`  | 当前元素的所有兄弟元素                                 |
| 之后          |                                                        |
| `next()`      | 当前元素之后的紧邻着的第一个兄弟元素（下一个兄弟元素） |
| `nextAll()`   | 当前元素之后的所有兄弟元素                             |
| `nextUntil()` | 返回介于两个给定参数之间的所有跟随的同胞元素。         |
| 之前          |                                                        |
| `prev()`      | 当前元素之前的紧邻着的兄弟元素（上一个兄弟元素）       |
| `prevAll()`   | 当前元素之前的所有兄弟元素                             |
| `PrevUntil()` | 返回介于两个给定参数之间的所有跟随的同胞元素。         |
`silbings()`可以使用可选参数来过滤对兄弟元素的搜索
```js
 $("h2").siblings("p");
// 返回属于 <h2> 的同胞元素的所有 <p> 元素
```
`nextUntil()` 方法返回介于两个给定参数之间的所有跟随的同胞元素
```js
 $("h2").nextUntil("h6");
```
### 过滤：遍历过滤DOM树元素
- not() 方法与 filter() 相反
- eq() `索引编号从0开始`
| 方法名     | 作用                                                         |
| ---------- | ------------------------------------------------------------ |
| `first()`  | 首个元素                                                     |
| `last()`   | 最后一个元素                                                 |
| `eq()`     | 返回被选元素中带有指定索引号的元素`索引编号从0开始`          |
| `filter()` | 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。 |
| `not()`    | 返回不匹配标准的所有元素                                     |
## 方法
|   方法名   | 作用                                                         |
| :--------: | :----------------------------------------------------------- |
| `.text()`  | 获取这个元素中的文字内容.text("内容") 设置值<br />相当于DOM中的innerText相当于DOM中的innerText或者是textContent |
| `.html()`  | 设置标签中间显示其他标签及内容，类似于innerHTML              |
|  `val()`   | 设置input标签中value的值，类似于value                        |
|  `.css()`  | 设置元素的样式，类似于style里面可以直接写键值对的方式        |
|  `show()`  | 显示                                                         |
|  `hide()`  | 隐藏                                                         |
| `toggle()` | 切换 hide() 和 show() 方法                                   |
```js
$("#dv").css({"width":"300px","height":"200px",})
```
- 隐藏/显示

```js
$(selector).hide/show/toggle(speed,callback);
// speed 参数规定隐藏/显示的速度,(slow 、fast、毫秒)
```
## 操作DOM
### 获取内容和属性
#### 获得内容 - text()、html() 以及 val()
| 方法名   | 作用         |
| -------- | ------------ |
| `text()` | `文本内容`   |
| `html()` | ``HTML标签`` |
| `val()`  | ``表单字段`` |
#### 设置属性获取属性 - attr() 和 prop()
| 方法名   | 作用                          |
| -------- | ----------------------------- |
| `attr()` | 属性值(元素自定义的 DOM 属性) |
| `prop()` | (元素本身就带有的固有属性)    |
`attr() vs prop()`
- `prop()`HTML 元素本身就带有的固有属性( IDE 里能够智能提示出的属性，这些就叫做固有属性。)，使用 **prop** 方法。
	- 如果有相应的属性，返回指定属性值。
	- 如果没有相应的属性，返回值是空字符串。
- `attr() `HTML 元素自定义的 DOM 属性，使用 **attr** 方法。
	- 如果有相应的属性，返回指定属性值。
	- 如果没有相应的属性，返回值是 undefined。
- 具有 true 和 false 两个属性的属性，如 checked, selected 或者 disabled 使用prop()
```js
$("#id").attr("href")
```
### 设置内容和属性
#### 设置内容 
| 方法名   | 作用                                           |
| -------- | ---------------------------------------------- |
| `text()` | 设置或返回所选元素的``文本内容``               |
| `html()` | 设置或返回所选``元素的内容（包括 HTML 标记）`` |
| `val()`  | 设置或返回``表单字段``的值                     |
#### 设置属性
| 方法名   | 作用            |
| -------- | --------------- |
| `attr()` | 设置/改变属性值 |
`text()、html()、val()的回调函数`
回调函数有两个参数：
- 被选元素列表中当前元素的下标，
- 原始（旧的）值。然后以函数新值返回您希望使用的字符串。
```js
$("#test1").text/html/val (function(i,origText){
     return "旧文本: " + origText + " 新文本: Hello world! (index: " + i + ")"; 
});
```
`attr()` 允许您同时设置多个属性
```js
$("button").click(function(){
    $("#app").attr({
        "href" : "http://www.baidu.com/jquery",
        "title" : "jQuery 教程"
    });
});
```
### 添加内容
| 方法名               | 作用                     |
| -------------------- | ------------------------ |
| 元素内 `ap/pre-pend` | 当前元素内(标签内)       |
| `append()`           | 在被选元素的结尾插入内容 |
| `prepend()`          | 在被选元素的开头插入内容 |
| 元素外               | 当前元素外(标签外)       |
| `after()`            | 在被选元素之后插入内容   |
| `before()`           | 在被选元素之前插入内容   |
通过`append() 和 prepend()`添加多个HTML元素
```js
var txt1 = "<p>文本一</p>"
// jQuery 创建HTML
var txt2 = $("<p></p>").text("文本二")
// javascript 创建HTML
var txt3 = document.createElement("p");
txt3.innerHTML = "文本三"
$("body").append/prepend(txt1,txt2,txt3)
```
通过 `after() `和`` before() `方法添加若干新元素
```js
var txt1 = "<p>文本一</p>"
// jQuery 创建HTML
var txt2 = $("<p></p>").text("文本二")
// javascript 创建HTML
var txt3 = document.createElement("p");
txt3.innerHTML = "文本三"
$("body").ap/prepend(txt1,txt2,txt3)
```
### 删除元素
| 方法       | 作用                                                 |
| ---------- | ---------------------------------------------------- |
| `remove()` | 删除被选元素（及其子元素）                           |
| `empty()`  | 从被选元素中删除子元素（删除当前元素下的所有子元素） |
`remove()` 方法也可接受一个参数，允许您对被删元素进行过滤。
```js
$('p').remove(".italic")
// 删除p元素下的子元素 .italic 
```


jQuery中创建元素及追加元素

DOM中可以动态创建元素：document.createElement（"标签的名字"）；

jQuery中同样可以创建元素标签并且返回的就是jQuery对象，可以直接调用方法进行使用

append方法用来在元素的**末尾追加元素**（最后一 个子节点）。增加元素末尾（儿子)

prepend，**在元素的开始添加元素（第一个子节点）。增加元素开始儿子）**

after，在元素之后添加元素（添加兄弟）增加元素后面兄弟before：在元素之前添加元素（添加兄弟）增加元素前面兄弟）

```js
DOM中创建元素：
doucument.write("标签代码");
缺陷：页面加载后创建元素，把页面中原有的内容全部的干掉
innerHTML 
document.createElement("标签的名字")
JQuery中创建元素的方式
$("标签的代码")
对象.html("标签的代码")
// 当前元素的里面（子元素）
append(obj)
用来在元素的末尾追加元素(最后一个子节点)。增加
appendTo()
把pObj对象主动的加到div中
append()与appendTo()的区别
$("#dv").append(pObj);
pObj.appendTo($("#dv"));
prepend()
after()
把元素添加到当前元素的后面(兄弟元素来添加)
before()
把元素添加到当前元素的前面(兄弟元素来添加)
```

```js
var pObj = $("<p></p>");
pObj.text("文字");
.html()
```

```js
 var obj = [{ name: "何伟亮", age: "18", sex: "男" }, { name: "伟亮", age: "28", sex: "男" }, { name: "亮", age: "34", sex: "男" }];
        $(function () {
            $("input").click(function () {
                for (var i = 0; i < obj.length; i++) {
                    var arr = [];
                    var objs = obj[i];
                    arr.push("<tr><td>" + objs.name + "</td><td>" + objs.age + "</td><td>" + objs.sex + "</td></tr>");
                }
                $("tbody").html(arr);
            });
        })
```

```js
// 清空内容
$("div").html("") 空 //清空元素的内容
$("div").emtry() 清空元素中的内容
$("div").remove(); 移除元素自身 --自杀
// 克隆
clone()
```

表单元素的属性
设置和获取表单的value
input标签：文本框，radio,select,textarea(文本域)。checkbox.....常见的表单标签
都可以通过val方法获取和设置value值

```js
// 获取文本域的内容
text()方法
val()方法
val(选中值)
// 可以改变某一项选中
 $("#bu").click(function () {
                $("#selectBox").val(3);
            });
 <select name="" id="selectBox">
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
        </select>
```

设置和获取系统属性值或者自定义属性
attr()方法：可以设置属性值，两个参数：1；属性名字，2 属性值
attr()方法：可以获取属性值，一个参数1；属性名字

```js
$("#dv:checkbox")
type:checkbox
```

设置复选框中（attr设置checkbox的选中问题） prop()与attr用法一样

```js
$("#dv:checkbox").prop("checked","true");
prop("checked","false");
```

设置元素和获取元素的宽高

```js
.css("width");
.css("height");
var width = parseInt($("dv")).css("width");
$("div").width();
$("div").height();
```

位置操作

```js
offset()
// 设置的时候会有pos:relative
// 获取left和top的值 都是数字类型
console.log($("#dv").offset().left);
console.log($("#dv").offset().top);
offset("left":100,"top":100);
设置的时候没有px
```

```js
scrollLeft()和scrollTop()
console.log($(document).scrollLeft());
console.log($(document).scrollTop());
// 用法和之前的offset方法类似
// 获取的是数字
// 设置可以在括号中添加值即可
// 滚动事件
$(window).scroll(function(){
});
```

## 操作CSS

### 类

| 方法            |                                     |
| --------------- | ----------------------------------- |
| `addClass()`    | 向被选元素添加一个或多个类          |
| `removeClass()` | 从被选元素删除一个或多个类          |
| `toggleClass()` | 对被选元素进行添加/删除类的切换操作 |
| `css()`         | 设置或返回样式属性                  |
`addClass()、removerClass()、toggleClass()`
```js
$("div").addClass("blue")
```
`css()`
返回css属性
```js
css("propertyname");
```
设置css属性
```js
// 键,值
css("propertyname","value");
```
设置多个css属性
```js
// {"键":"值","键":"值"}
$('p').css({
	"background-color":"blue",
    "font-size":"30px"
})
```
### 尺寸

处理元素和浏览
<img src="https://www.runoob.com/images/img_jquerydim.gif" alt="jQuery Dimensions" style="zoom: 67%;"/>

| 器窗口的尺寸                    |                       |
| ------------------------------- | --------------------- |
| `width()`、`height()`           |                       |
| `innerWidth()`、`innerHeight()` | 包括padding           |
| `outerWidth()`、`outerHeight()` | 包括padding 和 border |
设置元素样式

```js
.css（"属性"，"属性值"）；
.css（"属性"，"属性值"）.css（"属性"，"属性值"）；
.css（{"属性"："属性值"，"属性"："属性值"}）；
// { }
// 第一种写法
$("ul li").css("background-color","red");
$("ul li").css("background","red");
// 第二种写法
var style = {
"backgroudColor" : "red",
"fontSize":"30px"
}
$("ul>li").css(style);
// 第三种写法
$("ul>li").css("backgroundColor","red").css("fontSize","30px");
获取属性的值,写一个参数即可
console.log($("#ul>li").css("backgroundColor"));
```

添加和移除类设置元素样式

```js
hasClass("cls")
// 检测元素是否应用某个类样式
toggleClass("cls") 
// 切换类样式
addClass();
// 参数：类样式名字，添加样式的同时不会消除原有的样式
addClass("cls").addClass("cls2");
addClass("cls cls2");
removeClass();
// 不写参数移除所有的类样式
removeClass("cls")
// 移除指定的一一个类样式，类样式名字不用点
```

```js
val() 可以获取input值
val("属性") 设置val的值
var index = $(this).index();
$(ul>li:eq("+index+"))
$(ul>li:eq("index")) //index 字符串
```

## 事件

页面对不同访问者的响应叫做事件。



| 鼠标事件              | 键盘事件             | 表单事件                               | 文档/窗口事件                                                |
| --------------------- | -------------------- | -------------------------------------- | ------------------------------------------------------------ |
| `click`               | `keypress 键被按下`  | `submit 提交`                          | `load 指定的元素已加载`                                      |
| `dbclick`             | `keydown 按下的过程` | `change 元素的值改变,仅适用于表单字段` | `resize 调整浏览器窗口大小`                                  |
| `mouseenter 鼠标进入` | `keyup 键被松开`     | `focus 获得焦点`                       | `scroll 滚动指定的元素`                                      |
| `mouseleave 鼠标离开` |                      | `blur 失去焦点`                        | `unload 方法在 jQuery 版本 1.8 中被废弃，在 3.0 版本被移除。` |
| `mousedown 鼠标按下`  |                      |                                        |                                                              |
| `mouseup 鼠标松开`    |                      |                                        |                                                              |
| `hover`               |                      |                                        |                                                              |
` $('选择器').事件(function(){ }`

```js
$('button').click(function(){  
	// 动作触发后执行的代码
})
```
```js
x=0;
$(document).ready(function(){
  $(window).resize(function(){
    $("span").text(x+=1);
  });
});
```
## 动画
| 方法名         | 作用                                                         |
| -------------- | ------------------------------------------------------------ |
| `slideUp()`    | 滑入                                                         |
| `slideDown()`  | 滑出                                                         |
| `slideToggle`  | 切换滑入滑出                                                 |
| `fadeIn()`     | 淡入                                                         |
| `fadeOut()`    | 淡出                                                         |
| `fadeToggle()` | 切换淡入淡出                                                 |
| `animate()`    | 第一个参数：键值对，（数值的属性可以改颜色不能改）<br/>第二个参数：动画的时间<br/>第三个参数：回调函数 |
```js
hide()方法
参数：可以是一个number类型（数字），也可以是字符串类型
number
1000ms 毫秒
字符串
"slow" "normal" "fast"
show()方法
hide(800,function(){
});
argumnets.callee 相当于递归
$("#btn1").click
$("div>img").last("img").hide(800,function(){
	$(this).prev().hide(800,arguments.callee);
})
```
```js
$(function () {
    $("#show").click(function () {
        $("ul > li").last("li").hide(200, function () {
            $(this).prev().hide(200, arguments.callee);
        });
    });
    $("#hide").click(function () {
        $("ul > li").first("li").show(200, function () {
            $(this).next().show(200, arguments.callee);
        });
    });
});
```
可以设置透明度

- 参数1 ： 时间 slow normal fast
- 参数2 ：透明度 .css("opacity",0.1);
- jquery animate()背景色渐变的处理，jquery animate函数不能处理背景色渐变，需要使用要jquery.color插件

```js
<script src="https://cdn.bootcss.com/jquery-color/2.1.2/jquery.color.js"></script>
```
stop()方法停止动画效果
```
$(this).children("ul").stop().show(500);
```
## 链式编程

`对象.方法().方法().方法() `
断链：对象调用方法，返回的不是当前的对象，再调用方法，调用不了
**多行代码合并成一行代码，前提要认清此行代码返回的是不是对象.是对象才能进行链式编程**

```js
.html("val").text("val").css()链式编程，隐式迭代。
链式编程注意：$（"div"）.html（'设置值’）.val（‘设置值’）；这样可以，但是（'div）.html().text（）这样是不对的，因为获取值时返回的是获取的字符串而不是对象本身所以不能链式编程。
html("<h1>这是一个h1<h1>")
$(function(){
	$("li").click(function(){}).moverover().moverenter();
});
```
解决断链：恢复到断链之前的一个效果---修复断链 `end()`
```js
$(this).prevAll().css("backgroundColor","red").end().nextAll().css("backgroundColor","blue");
```
## 绑定和解绑
事件绑定
同一个元素绑定多个事件
绑定事件：bind方法
bind()方法 不推荐
第一个参数是事件名字
第二个参数是事件处理函数-匿名函数
方便：简单，多事件一次绑定参数：键值对（右），空格隔开

```js
$("#btn").bind({"click":function(){
},"moverover“:function(){
}});
$("#btn").bind("click moverover",function(){
});
```
delegate ---->绑定事件 不推荐
参数 
1.要绑定的元素
要绑定的事件的名字
绑定事件的处理函数 --- 匿名函数

```js
$("#dv").delegate("p",click,function(){
	alert()
})
```
on() 推荐
delegate()方法内部也是调用的on方法来绑定事件
on方法：两个参数：1事件的名字，2事件处理函数
on方法：三个参数：1，事件的名字，2.要绑定事件的元素--p，3事件处理函数
on是父级元素调用，目的：为子级元素去绑定事件
```js
$("").on("click",function(){
	$("").on("click","p",function(){
	})
})
```
绑定事件：bind：绑定多个事件
参数：{"事件的类型"：事件处理函数，...}
delegate参数：父级元素.delegate（"子级元素"，"事件类型"，事件处理函数）
on参数：父级元素.on（"事件类型"，"子级元素"，事件处理函数）；
解绑事件
.off()方法可以解绑事件
```js
$().on("click",function(){
	$("#btn1").off("click");
	off参数是要解绑的事件的名字
})
```
unbind事件
```js
$().bind("click",function(){
	$("#btn1").unbind("click");
	// off参数是要解绑的事件的名字
})
```
undelegate()
```js
$("btn2").click(function(){
	$("dv").undelegate("p","click");
})
```
//如果说父级元素和子级元素都是通过正常的方式绑定事件，如果通过off解绑的时候，父级元素的事件解绑了，子级元素的事件没有解绑
//但是：如果子级元素是通过父级元素调用delegate的方式绑定的事件，父级元素使用off方式解绑事件，这个时候父级元素和子级元素的相同的事件都会被解绑
```js
$("#dv").off("click")
下面的代码是把子级元素的点击事件解绑了，父级的点击事件还存在
$("#dv").off("click","**")
```
触发事件
触发事件：触发某个事件的时候在该事件内部调用了其他元素的某个事件方法
第一种方式：直接调用元素的事件方法

```js
$("#btn1").click()
```
第二种方式：使用trigger()方法
```js
$("").trigger("click")
事件名称
```
第三种方式：使用 triggerHandle()方法
trigger()和triggerHandler()区别
前者会触发浏览器的默认行为，并执行事件
后者不会触发浏览器的默认行为，但是会执行事件
获取焦点属于浏览器的默认行为

```js
触发文本框获取焦点的事件
$("txt").focus()
$("txt").trigger("focus")
$("txt").triggerHandler("focus")
//
P
//第一种触发事件的方式和第二种触发事件的方式是相同的，都会触发浏览器默认的事件（光标在文本框中闪烁）
//第三种触发事件的方式不会触发浏览器的默认事件
}）；
```
事件对象
event.delegateTarget 代码绑定的对象
event.currentTarget 绑定事件的对象
event.target 真正触发事件的对象
```js
console.log(arguments.length);
argumnets.length
获取函数在调用的时候，有几个参数
$("#dv").on("click","input",function(event){
	console.log(arguments.length);
	console.log(arguments[0]);
	console.log(event);
	//event.delegateTarget --- >div
	//event.currentTarget ----->input
	//event.target --->input
});
```
按钮改变颜色
```
$(function () {
            $(document).keydown(function (e) {
                // console.log(event);
                var keyCode = e.keyCode;
                switch (keyCode) {
                    case 65: $("#dv").css("background", "red"); break;
                    case 66: $("#dv").css("background", "yellow"); break;
                    case 67: $("#dv").css("background", "green"); break;
                    case 68: $("#dv").css("background", "pink"); break;
                    case 69: $("#dv").css("background", "black"); break;
                }
                console.log(keyCode);
            })
        });
       /*  $(function () {
                 $(document).on("keydown", function (event) {
                     $("#keyCodeSpan").text(event.keyCode);
                     switch (parseInt(event.keyCode(10))) {
                         case 6: changeColor("red"); break;
                         case 7: changeColor("green"); break;
                         case 8: changeColor("blue"); break;
                     }
                 })
                 function changeColor(color) {
                     $("#bgChange").css("backgroundColor", color);
                 }
             }) */
```
取消事件冒泡+取消默认事件
//事件冒泡：元素中有元素，这些元素都有相同的事件，一旦最 里面的元素的事件触发 了，外面的所有的元素的相同的事件都会被触发
//元素A中有一个元素B，A和B都有点击事件，B点击事件触发，A点击事件自动触发
取消事件冒泡
```
最里面的元素设置
return false;俩种作用 取消事件冒泡+取消默认事件
```
e.stoPropagation()
取消默认事件
event.preventDefault()
链式编程原理

```
链式编程原理：内部返回了return this当前对象有些方法设置了值才能返回当前对象，如果没有设置值，是获取属性对应的值，而不是当前对象
```
```
function Student(name){
	this.name = name;
	this.sayHi = function(){
		console.log("我的名字叫"+this.name)
		return this;
		// 把当前对象返回
	}
	this.eat = function(){
		console.log("我就是喜欢吃大蒜")
	}
	var stu = new Student("小黑");
	stu.sayHi().eat();
	传递参数
	.html()
	function Student(name){
	this.name = name;
	this.sayHi = function(name){
		if(name){
			console.log("我的名字叫"+name);
			return this;
		}else{
			console.log("我的名字叫"+this.name);
		}
		//console.log("我的名字叫"+this.name)
		//return this;
		// 把当前对象返回
	}
	this.eat = function(){
		console.log("我就是喜欢吃大蒜")
	}
	var stu = new Student("小黑");
	stu.sayHi("小白").eat();
}
c
```
each方法
 jQuery中有隐式迭代不需要我们再次进行遍历对某些元素进行操作但是，如果涉及到对不同的元素有不同的操作，那么需要进行each遍历
```
//参数：表示每次遍历都要执行的函数
$（"1i"）.each（function（index，ele）{
//index 表示：当前这个元素的索引号从e开始的0-10
var op=（index+1）/10；
$（ele）.css（"opacity"，op）；
}）；
$（"#uu>li"）.each（function（index，element）{
/ /第一个参数是索引第二个参数是对象
//console.Log（arguments[0]+"===="+arguments[1]）；
$（element）.css（"opacity"，（index+1）/10）；
}）；
```
多库共存
```
//i让jQuery释放对$的控制权
$.noConflict（）；
var $="哦买噶"；console.1og（$）；jQuery（function（）{
jQuery（"#btn"）.click（function（）{
alert（"正常的执行"）；
}）；}）；
```
同一个页面不仅引入了jQuery的外部文件，也引入了其他的库文件如果此时其他的库文件中也使用了S符号那么就使用：5.noConfict）解决其他语言中：这个方式叫解决命名空间的冲突也可以这样：var itcastos.noConflict（）；
也可以用jQuery代替 $
## 插件
[jQuery之家-自由分享jQuery、html5、css3的插件库](http://www.htmleaf.com/)
jQueryUI使用
1. 引入jQueryUl的样式文件
2. 引入jQuery
3. .引入jQueryUl的js文件
4. 使用jQueryUI功能
自已制作插件
```
$("input[type=button]").click()
```
```js
$.fn.changeBackgrounColor= function（color）{
    $（".c1s"）.css（"backgroundColor"，color）；
}；
$（function（）{
    //点击每个按钮改变每个div的背景颜色
    $（"input[type=button]"）.click（function（）{
        $（".cls"）.changeBackgrounColor（$（this）.val（））；
        //$（".cls"）.css（"backgroundColor"，$（this）.val（））；
        //changeBackgrounCoLor（$（this）.val（））；
    }）；
}）；
//function changeBackgrounCoLor（color）{
//$（".cls"）.css（"backgroundColor"，color）；
// }
}
```
语法错误
```
box.style.height = "100px"
box.style.backgroundColor = "green"
```
Jquery 滚轮事件
```js
$(function () {
    $(document).scroll(function () {
        var scroH = $(document).scrollTop();  //滚动高度
        var viewH = $(window).height();  //可见高度 
        var contentH = $(document).height();  //内容高度
        if (scroH > 100) {  //距离顶部大于100px时
            alert('asdfsd')
        }
        if (contentH - (scroH + viewH) <= 100) {  //距离底部高度小于100px
        }
        if (contentH = (scroH + viewH)) {  //滚动条滑到底部啦
        }
    });
})
```
## jquery  ajax

### AJAX

AJAX 是与服务器交换数据的技术，它在不重载全部页面的情况下，实现了对部分网页的更新。
AJAX = 异步 JavaScript 和 XML（Asynchronous JavaScript and XML）。
### load()
jQuery load() 方法是简单但强大的 AJAX 方法。
load() 方法从服务器加载数据，并把返回的数据放入被选元素中。
```js
$(selector).load(URL,data,callback);
// 必需的 URL 参数规定您希望加载的 URL。
//
```
```
$('p').load()
```
### get() 、post()
get()
```js
$.get(URL,callback);
```
post()
```js
$.post(URL,data,callback);
```
#### JSONP
