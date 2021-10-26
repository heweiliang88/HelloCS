---
title: 原生数据请求的方式ajax
categories:
  - 前端
tags:
  - JavaScript
  - AJAX
  - 前端
abbrlink: 19417
---
# 原生 AJAX

> AJAX ==  <b style="color:red;font-size:20px">A</b>synchronous <b style="color:red;font-size:20px">J</b>avascript <b style="color:red;font-size:20px">A</b>nd <b style="color:red;font-size:20px">X</b>ML 异步的JavaScript和XML
>
> AJAX不是新的编程语言，而是一种使用现有标准的新的方法
>
> AJAX 是一种在无需重新加载整个网页的情况下，能够更新部分网页的技术
## AJAX基础
![image-20200503211444689](https://i.loli.net/2020/05/03/GFHqEOcxSp718Tg.png)
### 三件套
- `html(html5)` 主要用来实现页面得排版布局
- `css (css3)`主要用来实现页面得样式美化
- `JavaScript(JQuery)` 主要用来实现前端功能特效
### 网站
- 网站由一系列页面组成（页面由js、css、图片、html标签….. 所有的这些文件都被称为资源），网站分为动态网站和静态网站
### 概念
- ajax最早产生于2005年
- AJAX ==  <b style="color:red;font-size:20px">A</b>synchronous <b style="color:red;font-size:20px">J</b>avascript <b style="color:red;font-size:20px">A</b>nd <b style="color:red;font-size:20px">X</b>ML 异步的JavaScript和XML
- 传统的网页（不使用AJAX） 如果需要更新内容，必需重载整个网页，AJAX 是一种用于创建快速动态网页的技术，通过在后台与服务器进行少量数据交互，AJAX可以使网页实现异步更新，这意味着可以在不重新在加载整个网页的情况下，对网页的某一部分进行更新
- AJAX不是新的编程语言，而是``一种使用现有标准的新方法``，AJAX它不是像HTML、JavaScript或CSS 这样的一种“正式的”技术，它是表示 ==一些技术的混合交互==的一个术语(JavaScript 、Web 浏览器、Web服务器) ，它使我们可以获取和显示新的内容，而不必载入一个新的Web页面。增强用户体验，更有桌面程序的感觉。
#### AJAX是基于现有的Internet标准
- XMLHttpRequest 对象（异步的与服务器交换数据）
- JavaScript/DOM (信息显示/交互)
- CSS(给数据定义样式)
- XML(作为转换数据的格式)
### 作用
- 显示新的HTML内容而不用载入整个页面
- 提交一个表单并且立即显示结果
- 登录而不用跳转到新的页面
- 星级评定组件
- 遍历数据库信息加载更多而不刷新页面
### AJAX代码
```js
var xmlhttp;
if(window.XMLHttpRequest){
	xmlhttp = new XMLHttpRequest();
}else{
	xmlhttp = new AcitveXObject("Microsoft.XMLHTTP");
}
xmlhttp.onreadystatechange = function(){
    if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
       document.getElementById("mydiv").innerHTML = xmlhttp.responseText;
    }
}
xmlhttp.open("GET","请求文件的路径名如 /my/hello.json  /my/hello.txt",true) 
// http://mobilecdnbj.kugou.com/api/v3/tag/recommend?showtype=3&apiver=2&plat=0
xmlhttp.send();
注意点： readyState status responseText 请求文件的路径名如 要从根目录开始
onreadystatechage xmlhttp.responseText
```
## AJAX XHR
### 创建 => 请求 =>响应 => readyState函数
### XHR 创建对象
XMLHttpRequest是AJAX的基础
#### XMLHttpRequest对象
- 所有现代浏览器均支持 XMLHttpRequest 对象（IE5 和 IE6 使用 ActiveXObject）
- `XMLHttpRequest 用于在后台与服务器交换数据。这意味着可以在不重新加载整个网页的情况下，对网页的某部分进行更新`
#### 创建XMLHttpRequest对象
所有现代浏览器（IE7+、Firefox、Chrome、Safari 以及 Opera）均内建 XMLHttpRequest 对象。
- 创建DMLHttpRequest对象的语法：
```js
variable = new XMLHttpRequest();
```
- IE5、IE6(老版本的 Internet Explorer)使用 ActiveX 对象
```js
variable = new ActiveXObject("Microsoft.XMLHTTP")
```
- 兼容所有浏览器
```js
var xmlhttp;
if(window.XMLHttpRequest){
	//code for IE7+, Firefox, Chrome, Opera, Safari
	xmlhttp = new XMLHttpRequest();
}else{
	//// code for IE6, IE5
	xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
}
```
### XHR 请求 `xmlhttp.open()`
----
XMLHttpRequest 对象用于和服务器交换数据
#### 向服务器发送请求
```js
xmlhttp.open("GET","test.txt","true");
xmlhttp.send();
```
| 方法                         | 描述                                                         |
| :--------------------------- | :----------------------------------------------------------- |
| open(*method*,*url*,*async*) | 规定请求的类型、URL 以及是否异步处理请求。*method*：请求的类型；GET 或 POST*url*：文件在服务器上的位置*async*：true（异步）或 false（同步） |
| send(*string*)               | `将请求发送到服务器`。*string*：仅用于 POST 请求             |
#### GET 还是 POST的区别
GET：GET 更简单也更快，并且在大部分情况下都能用。
POST：以下情况中，请使用 POST 请求：
- 无法使用缓存文件（更新服务器上的文件或数据库）
- 向服务器发送大量数据（POST 没有数据量限制）
- 发送包含未知字符的用户输入时，POST 比 GET 更稳定也更可靠
##### Get请求
```js
xmlhttp.open("GET","demo_get.asp",true);
xmlhttp.send();
```
在上面的例子中，您可能得到的是缓存的结果。
为了避免这种情况，请向 URL 添加一个唯一的 ID：
```js
xlhttp.open("GET","demo_get.asp?t="+ Math.random(),true);
xhhttp.send();
```
##### Post请求
```js
xmlhttp.open("POST","demo_post.asp",true);
xmlhttp.send();
```
如果需要像 HTML 表单那样 POST 数据，请使用 setRequestHeader() 来添加 HTTP 头。然后在 send() 方法中规定您希望发送的数据：
```js
xlhttp.open("POST","ajax_test.asp",true);
xlhttp.setRequestHeader("Content-type","application/x-www-form-unclencoded");
xhhttp.send("fname=Bill&name=Gates");
```
| 方法                               | 描述                                                         |
| :--------------------------------- | :----------------------------------------------------------- |
| setRequestHeader(*header*,*value*) | 向请求添加 HTTP 头。*header*: 规定头的名称*value*: 规定头的值 |
#### url-服务器上的文件
open() 方法的 *url* 参数是服务器上文件的地址：
```js
xmlhttp.open("GET","ajax_test.asp",true);
```
该文件可以是任何类型的文件，比如 .txt 和 .xml，或者服务器脚本文件，比如 .asp 和 .php （在传回响应之前，能够在服务器上执行任务）。
#### 异步 - True 或 False？
AJAX 指的是异步 JavaScript 和 XML（Asynchronous JavaScript and XML）。
`XMLHttpRequest 对象如果要用于 AJAX 的话，其 open() 方法的 async 参数必须设置为 true：`
```
xmlhttp.open("GET","ajax_test.asp",true);
```
对于 web 开发人员来说，发送异步请求是一个巨大的进步。很多在服务器执行的任务都相当费时。AJAX 出现之前，这可能会引起应用程序挂起或停止。
通过 AJAX，JavaScript 无需等待服务器的响应，而是：
- 在等待服务器响应时执行其他脚本
- 当响应就绪后对响应进行处理
##### Async = true
`当使用async=true时，请规定在响应处于onreadystatechange事件中的就绪状态时执行的函数：`
```js
xmlhttp.onreadystatechage= function(){
	if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
	document.getElementById("myDiv").innerHTML = xmlhttp.responseText;
	}
xmlhttp.open("GET","test1.txt",true);
xmlhttp.send();
```
##### Async = false JavaScript 会等到服务器响应就绪才继续执行。如果服务器繁忙或缓慢，应用程序会挂起或停止。
如需使用 async=false，请将 open() 方法中的第三个参数改为 false：
```js
xmlhttp.open("GET","test1.txt",false);
```
我们不推荐使用 async=false，但是对于一些小型的请求，也是可以的。
请记住，JavaScript 会等到服务器响应就绪才继续执行。如果服务器繁忙或缓慢，应用程序会挂起或停止。
**注释：**当您使用 async=false 时，请不要编写 onreadystatechange 函数 - 把代码放到 send() 语句后面即可：
```js
xmlhttp.open("GET","test1.txt",false);
xmlhttp.send();
document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
```
### XHR 响应
----
#### 服务器响应
解析 responseXML(.xml) 和 responseText(.txt) 文件
使用 XMLHttpRequest 对象的 responseText 或 responseXML 属性
| 属性         | 描述                       |
| :----------- | :------------------------- |
| responseText | 获得字符串形式的响应数据。 |
| responseXML  | 获得 XML 形式的响应数据。  |
#### responseText 属性
如果来自服务器的响应并非 XML，请使用 responseText 属性。
responseText 属性返回字符串形式的响应
```js
document.getElementById("mydiv").innerHTML = xmlhttp.responseText;
```
#### responseXML 属性
如果来自服务器的响应是 XML，而且需要作为 XML 对象进行解析
```js
function loadXMLDoc(){
	var xmlhttp;
	var txt,x,i;
	if(window.XMLHttpRequest){
		xmlhttp = new XMLHttpRequest();	
	}else{
		xmlhttp = new AvtiveXObject("Microsoft.XMLHTTP");
	}
	xmlhttp.onreadystatechage = function(){
		if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
			xmlDoc = xmlhttp.responseXML;
			txt = "";
			x=xmlDoc.getElementsByTagName("ARTIST"); // 获取标签 ARTIST
            for (i=0;i<x.length;i++)
            {
                txt= xt + x[i].childNodes[0].nodeValue + "<br>";
            }
            document.getElementById("myDiv").innerHTML=txt;
		}
	}
	xmlhttp.open("GET","xml文件位置","true");
	xmlhttp.send();
}
```
### XHR readyState == 4 status == 200
--------
#### onreadystatechange 事件
当请求被发送到服务器时，我们需要执行一些基于响应的任务。
每当 readyState 改变时，就会触发 onreadystatechange 事件。
readyState 属性存有 XMLHttpRequest 的状态信息。
下面是 XMLHttpRequest 对象的三个重要的属性：
| 属性               | 描述                                                         |
| :----------------- | :----------------------------------------------------------- |
| onreadystatechange | 存储函数（或函数名），每当 readyState 属性改变时，就会调用该函数。 |
| readyState         | 存有 XMLHttpRequest 的状态。从 0 到 4 发生变化。0: 请求未初始化1: 服务器连接已建立2: 请求已接收3: 请求处理中4: 请求已完成，且响应已就绪 |
| status             | 200: "OK" 404: 未找到页面                                    |
> **注意：** onreadystatechange 事件被触发 4 次（0 - 4）, 分别是： 0-1、1-2、2-3、3-4，对应着 readyState 的每个变化。
```js
xmlhttp.onreadystatechange-function(){
	if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
	//在 onreadystatechange 事件中，我们规定当服务器响应已做好被处理的准备时所执行的任务。
	//当 readyState 等于 4 且状态(status)为 200 时，表示响应已就绪：
		document.getElementById()
	}
}
```
#### 使用 Callback 回调函数
回调函数是一种以参数形式传递给另一个函数的函数。
如果您的网站上存在多个 AJAX 任务，那么您应该为创建 XMLHttpRequest 对象编写一个*标准*的函数，并为每个 AJAX 任务调用该函数。
该函数调用应该包含 URL 以及发生 onreadystatechange 事件时执行的任务（每次调用可能不尽相同）
```js
var xmlhttp;
function loadXMLDoc(url,cfunc){
    if(window.XMLHttpRequest){
      	xmlhttp = new XMLHttpRequest(); 
    }else{
        xmlhttp = new ActiveXObject('Microsoft.XMLHTTP');
    }
    xmlhttp.onreadystatechange = cfunc;
    xmlhttp.open("GET",url,true);
    xmlhttp.send();
}
function myFunction(){
 	loadXMLDoc("/try/ajax/ajax_info.txt",function()
    {
        if (xmlhttp.readyState==4 && xmlhttp.status==200)
        {
            document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
        }
    });
}
<div id="myDiv"><h2>使用 AJAX 修改文本内容</h2></div>
<button type="button" onclick="myFunction()">修改内容</button>
```
## 原生Ajax
### 隐藏帧iframe方式实现页面局 同步
```js
<div>
        <form action="./iframe.php" method="post" target="myframe">
            用户名：<input type="text" name="username"><span id="info"></span><br>
            密码：<input type="text" name="password">
            <input type="submit" value="登录">
        </form>
    </div>
    <iframe width="0" height="0"  frameborder="0" name="myframe"></iframe>
    <?php 
$uname = $_POST['username'];
$pw = $_POST['password'];
// if($uname == 'admin' && $pw == '123'){
//     echo '登录成功';
// }
if($uname == 'admin' && $pw == '123'){
?>
    <script type="text/javascript">
        parent.document.getElementById('info').innerHTML = '登录成功';
    </script>
<?php }else{ ?>
    <script type="text/javascript">
        parent.document.getElementById('info').innerHTML = '登录失败';
    </script>
<?php } ?>
```
### 实现页面局部更新
使用Ajax发送请求需要如下几步：
```js
get
//创建XMLHttpRequest 对象
var xhr = null
if(window.XMLHttpRequest){
	xhr = new XMLHttpRequest(); // 标准浏览器
}else{
	xhr = new ActiveXObject("Microsoft") // IE老版本 IE6 
}
准备发送
参数一：请求方式（get获取数据；post提交数据）
参数二：请求地址
参数三：同步或者异步标志位，默认是true表示异步，false表示同步
如果是get 请求那么请求参数必须在url中传递
encodeURI() 用来对中文参数进行编码。防止乱码
var param = 'username='+uname+'&password'
xhr.open('get','02get.php?+encodeURI(param)'+pw,true);
执行发送动作
xhr.send(null); //get请求这里需要添加null参数
指定回调函数
xhr.onreadystatechange = function(){
	if(xhr.readyState == 4 && xhr.status == 200){
		cosole.log(xhr.responseText)
	}
}
post
var xhr = null
if(window.XMLHttpRequest){
	xhr = new XMLHttpRequest(); // 标准浏览器
}else{
	xhr = new ActiveXObject("Microsoft") // IE老版本 IE6 
}
//readyState = 0表示xhr对象创建完成
准备发送
参数一：请求方式（get获取数据；post提交数据）
参数二：请求地址
参数三：同步或者异步标志位，默认是true表示异步，false表示同步
如果是get 请求那么请求参数必须在url中传递
post请求参数通过send传递，不需要通过encodeURI()转码必须设置请求头信息
var param = 'username='+uname+'&password'
xhr.o pen('post','02get.php'+pw,true);
xhr.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
执行发送动作
xhr.send(param); //post请求在这里传递，并且不需要转码
指定回调函数 
// readyState = 1表示已经发生了请求
// 该函数调用的条件就是readyState状态发生变化(不包括从0变为1)
xhr.onreadystatechange = function(){
	/*
	readyState:
	2 浏览器已经收到了服务器响应的数据
	3 正在解析数据
	4 数据已经解析完成，可以使用了，但是数据不一定是正常的
	*/
	if(xhr.readyState == 4 && xhr.status == 200){
	// 200 状态码 响应成功  404 没有找到请求的资源 500 服务器端错误
	// responseText
		cosole.log(xhr.responseText)
		//var data = xhr.responseXML; xml
	}
}
```
onreadysatechange
xhr.readyState
- 0 xhr对象初始化
- 1 执行发送动作
- 2 服务器端数据已经全部返回
- 3 数据正在解析
- 4 数据解析完成，可以使用了
xhr.status 
- 200 数据相应正常
- 404 没有找到资源
- 500 服务器端错误
## 跨域
[(...) 不要再问我跨域的问题了 - 个人文章 - SegmentFault 思否](https://segmentfault.com/a/1190000015597029)
# AJAX 数据库
AJAX 与数据库进行动态通信
```js
function showCustomer(str)
{
  var xmlhttp;    
  if (str=="")
  {
    document.getElementById("txtHint").innerHTML="";
    return;
  }
  if (window.XMLHttpRequest)
  {
    // IE7+, Firefox, Chrome, Opera, Safari 浏览器执行代码
    xmlhttp=new XMLHttpRequest();
  }
  else
  {
    // IE6, IE5 浏览器执行代码
    xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
  }
  xmlhttp.onreadystatechange=function()
  {
    if (xmlhttp.readyState==4 && xmlhttp.status==200)
    {
      document.getElementById("txtHint").innerHTML=xmlhttp.responseText;
    }
  }
  xmlhttp.open("GET","/try/ajax/getcustomer.php?q="+str,true);
  xmlhttp.send();
}
```
# AJAX XML文件
```js
function loadXMLDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     	myFunction(this);
    }
  };
  xhttp.open("GET", "cd_catalog.xml", true);
  xhttp.send();
}
function myFunction(xml) {
  var i;
  var xmlDoc = xml.responseXML;
  var table="<tr><th>Artist</th><th>Title</th></tr>";
  var x = xmlDoc.getElementsByTagName("CD");
  for (i = 0; i <x.length; i++) { 
    table += "<tr><td>" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}
```
# AJAX JQuery
ajax() 方法通过 HTTP 请求加载远程数据。
该方法是 jQuery 底层 AJAX 实现。简单易用的高层实现见 $.get, $.post 等。$.ajax() 返回其创建的 XMLHttpRequest 对象。大多数情况下你无需直接操作该函数，除非你需要操作不常用的选项，以获得更多的灵活性。
最简单的情况下，$.ajax() 可以不带任何参数直接使用。
**注意：**所有的选项都可以通过 $.ajaxSetup() 函数来全局设置。
```js
$(document).ready(function(){
	$("#b01").click(function(){
		 htmlpbj = $.ajax({url:'文件名.txt',async:false});
		 $("#myDiv").html(htmlobj.responseText);	 
	});
});
<div id="myDiv"><h2>通过 AJAX 改变文本</h2></div>
<button id="b01" type="button">改变内容</button>
```
# AJAX Vue
# AJAX Node
# AJAX PHP
## JSONP
跨域请求
**同源策略**
AJAX之所以需要“跨域”，罪魁祸首就是浏览器的`同源策略`。即，一个页面的AJAX只能获取这个页面相同源或者相同域的数据。 如何叫“同源”或者“同域”呢？——`协议、域名、端口号都必须相同`。例如：
```
http://example.com  和  https://example.com 不同，因为协议不同；   
http://localhost:8080  和  http://localhost:1000 不同，因为端口不同；   
http://localhost:8080  和  https://example.com 不同，协议、域名、端口号都不同，根本不是一家的。
```
当跨域请求时，一般都会看到这个错误：
```
XMLHttpRequest cannot load http://ghmagical.com/article/?intro=jsonp%E8%AF%B7%E6%B1%82&v=5520. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'http://localhost' is therefore not allowed access.
```
那如何跨域请求呢？这时，**JSONP**就登场了！
**JSONP(JSON with Padding)** 是一种跨域请求方式。主要原理是利用了`script `标签可以跨域请求的特性，由其 `src` 属性发送请求到服务器，服务器返回 `JavaScript `代码，浏览器接受响应，然后就直接执行了，这和通过 `script` 标签引用外部文件的原理是一样的。
**JSONP**由两部分组成：`回调函数`和`数据`，回调函数一般是在浏览器控制，作为参数发往服务器端（当然，你也可以固定回调函数的名字，但客户端和服务器端的名称一定要一致）。当服务器响应时，服务器端就会把该函数和数据拼成字符串返回。
**JSONP**的请求过程：
- 请求阶段：浏览器创建一个 `script` 标签，并给其`src` 赋值(类似 `http://example.com/api/?callback=jsonpCallback`）。
- 发送请求：当给`script`的`src`赋值时，浏览器就会发起一个请求。
- 数据响应：服务端将要返回的`数据`作为参数和`函数名称`拼接在一起(格式类似”`jsonpCallback({name: 'abc'})`”)返回。当浏览器接收到了响应数据，由于发起请求的是 `script`，所以相当于直接调用 `jsonpCallback` 方法，并且传入了一个参数。
对于`JQuery`的**JSONP**请求，这里就不多讲了，之前也写过一篇文章《[JQuery的Ajax请求跨域问题](http://ghmagical.com/article/page/id/e90VjjV5dX3K)》。
在这里讲解一下用原生`JavaScript`如何实现。
依旧是`ajax()`方法里添加**JSONP**，后面会将两者整合在一起，**JSONP**的配置参数主要多了一个`jsonp`参数，它就是你的回调函数名。
```
function ajax(params) {   
  params = params || {};   
  params.data = params.data || {};   
  var json = params.jsonp ? jsonp(params) : json(params);      
  // jsonp请求   
  function jsonp(params) {   
    //创建script标签并加入到页面中   
    var callbackName = params.jsonp;   
    var head = document.getElementsByTagName('head')[0];   
    // 设置传递给后台的回调参数名   
    params.data['callback'] = callbackName;   
    var data = formatParams(params.data);   
    var script = document.createElement('script');   
    head.appendChild(script);    
    //创建jsonp回调函数   
    window[callbackName] = function(json) {   
      head.removeChild(script);   
      clearTimeout(script.timer);   
      window[callbackName] = null;   
      params.success && params.success(json);   
    };    
    //发送请求   
    script.src = params.url + '?' + data;    
    //为了得知此次请求是否成功，设置超时处理   
    if(params.time) {   
     script.timer = setTimeout(function() {   
       window[callbackName] = null;   
       head.removeChild(script);   
       params.error && params.error({   
         message: '超时'   
       });   
     }, time);   
    }   
  };    
  //格式化参数   
  function formatParams(data) {   
    var arr = [];   
    for(var name in data) {   
      arr.push(encodeURIComponent(name) + '=' + encodeURIComponent(data[name]));   
    };   
    // 添加一个随机数，防止缓存   
    arr.push('v=' + random());   
    return arr.join('&');   
  }   
  // 获取随机数   
  function random() {   
    return Math.floor(Math.random() * 10000 + 500);   
  } }
著作权归作者所有。
商业转载请联系作者获得授权,非商业转载请注明出处。
原文: https://laixiazheteng.com/article/page/id/AASiankfBJWp © ghmagical.com
```
注意：因为 `script` 标签的` src` 属性只在第一次设置的时候起作用，导致 `script` 标签没法重用，所以每次完成操作之后要移除；
使用实例：
```
ajax({   
  url: 'test.php',    // 请求地址
  jsonp: 'jsonpCallback',  // 采用jsonp请求，且回调函数名为"jsonpCallbak"，可以设置为合法的字符串
  data: {'b': '异步请求'},   // 传输数据
  success:function(res){   // 请求成功的回调函数
    console.log(res);   
  },
  error: function(error) {}   // 请求失败的回调函数
});
著作权归作者所有。
商业转载请联系作者获得授权,非商业转载请注明出处。
原文: https://laixiazheteng.com/article/page/id/AASiankfBJWp © ghmagical.com
```
在这里后台使用PHP处理：
```
<?php
   $data = array('type'=>'jsonp');
   $callback = isset($_GET['callback']) ? trim($_GET['callback']) : '';  
   echo $callback.'('.json_encode($data).')';
```
注意：别漏了用函数名与数据拼接返回。
当然，前面也说过，你可以给定固定回调函数名：
```
<?php
   $data = array('type'=>'jsonp');
   $callback = isset($_GET['callback']) ? trim($_GET['callback']) : '';  
   echo $callback.'('.json_encode($data).')';
```
# 原生 AJAX
> AJAX ==  <b style="color:red;font-size:20px">A</b>synchronous <b style="color:red;font-size:20px">J</b>avascript <b style="color:red;font-size:20px">A</b>nd <b style="color:red;font-size:20px">X</b>ML 异步的JavaScript和XML
>
> AJAX不是新的编程语言，而是一种使用现有标准的新的方法
>
> AJAX 是一种在无需重新加载整个网页的情况下，能够更新部分网页的技术
## AJAX基础
![image-20200503211444689](https://i.loli.net/2020/05/03/GFHqEOcxSp718Tg.png)
### 三件套
- `html(html5)` 主要用来实现页面得排版布局
- `css (css3)`主要用来实现页面得样式美化
- `JavaScript(JQuery)` 主要用来实现前端功能特效
### 网站
- 网站由一系列页面组成（页面由js、css、图片、html标签….. 所有的这些文件都被称为资源），网站分为动态网站和静态网站
### 概念
- ajax最早产生于2005年
- AJAX ==  <b style="color:red;font-size:20px">A</b>synchronous <b style="color:red;font-size:20px">J</b>avascript <b style="color:red;font-size:20px">A</b>nd <b style="color:red;font-size:20px">X</b>ML 异步的JavaScript和XML
- 传统的网页（不使用AJAX） 如果需要更新内容，必需重载整个网页，AJAX 是一种用于创建快速动态网页的技术，通过在后台与服务器进行少量数据交互，AJAX可以使网页实现异步更新，这意味着可以在不重新在加载整个网页的情况下，对网页的某一部分进行更新
- AJAX不是新的编程语言，而是``一种使用现有标准的新方法``，AJAX它不是像HTML、JavaScript或CSS 这样的一种“正式的”技术，它是表示 ==一些技术的混合交互==的一个术语(JavaScript 、Web 浏览器、Web服务器) ，它使我们可以获取和显示新的内容，而不必载入一个新的Web页面。增强用户体验，更有桌面程序的感觉。
#### AJAX是基于现有的Internet标准
- XMLHttpRequest 对象（异步的与服务器交换数据）
- JavaScript/DOM (信息显示/交互)
- CSS(给数据定义样式)
- XML(作为转换数据的格式)
### 作用
- 显示新的HTML内容而不用载入整个页面
- 提交一个表单并且立即显示结果
- 登录而不用跳转到新的页面
- 星级评定组件
- 遍历数据库信息加载更多而不刷新页面
### AJAX代码
```js
var xmlhttp;
if(window.XMLHttpRequest){
	xmlhttp = new XMLHttpRequest();
}else{
	xmlhttp = new AcitveXObject("Microsoft.XMLHTTP");
}
xmlhttp.onreadystatechange = function(){
    if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
       document.getElementById("mydiv").innerHTML = xmlhttp.responseText;
    }
}
xmlhttp.open("GET","请求文件的路径名如 /my/hello.json  /my/hello.txt",true) 
// http://mobilecdnbj.kugou.com/api/v3/tag/recommend?showtype=3&apiver=2&plat=0
xmlhttp.send();
注意点： readyState status responseText 请求文件的路径名如 要从根目录开始
onreadystatechage xmlhttp.responseText
```
## AJAX XHR
### 创建 => 请求 =>响应 => readyState函数
### XHR 创建对象
XMLHttpRequest是AJAX的基础
#### XMLHttpRequest对象
- 所有现代浏览器均支持 XMLHttpRequest 对象（IE5 和 IE6 使用 ActiveXObject）
- `XMLHttpRequest 用于在后台与服务器交换数据。这意味着可以在不重新加载整个网页的情况下，对网页的某部分进行更新`
#### 创建XMLHttpRequest对象
所有现代浏览器（IE7+、Firefox、Chrome、Safari 以及 Opera）均内建 XMLHttpRequest 对象。
- 创建DMLHttpRequest对象的语法：
```js
variable = new XMLHttpRequest();
```
- IE5、IE6(老版本的 Internet Explorer)使用 ActiveX 对象
```js
variable = new ActiveXObject("Microsoft.XMLHTTP")
```
- 兼容所有浏览器
```js
var xmlhttp;
if(window.XMLHttpRequest){
	//code for IE7+, Firefox, Chrome, Opera, Safari
	xmlhttp = new XMLHttpRequest();
}else{
	//// code for IE6, IE5
	xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
}
```
### XHR 请求 `xmlhttp.open()`
----
XMLHttpRequest 对象用于和服务器交换数据
#### 向服务器发送请求
```js
xmlhttp.open("GET","test.txt","true");
xmlhttp.send();
```
| 方法                         | 描述                                                         |
| :--------------------------- | :----------------------------------------------------------- |
| open(*method*,*url*,*async*) | 规定请求的类型、URL 以及是否异步处理请求。*method*：请求的类型；GET 或 POST*url*：文件在服务器上的位置*async*：true（异步）或 false（同步） |
| send(*string*)               | `将请求发送到服务器`。*string*：仅用于 POST 请求             |
#### GET 还是 POST的区别
GET：GET 更简单也更快，并且在大部分情况下都能用。
POST：以下情况中，请使用 POST 请求：
- 无法使用缓存文件（更新服务器上的文件或数据库）
- 向服务器发送大量数据（POST 没有数据量限制）
- 发送包含未知字符的用户输入时，POST 比 GET 更稳定也更可靠
##### Get请求
```js
xmlhttp.open("GET","demo_get.asp",true);
xmlhttp.send();
```
在上面的例子中，您可能得到的是缓存的结果。
为了避免这种情况，请向 URL 添加一个唯一的 ID：
```js
xlhttp.open("GET","demo_get.asp?t="+ Math.random(),true);
xhhttp.send();
```
##### Post请求
```js
xmlhttp.open("POST","demo_post.asp",true);
xmlhttp.send();
```
如果需要像 HTML 表单那样 POST 数据，请使用 setRequestHeader() 来添加 HTTP 头。然后在 send() 方法中规定您希望发送的数据：
```js
xlhttp.open("POST","ajax_test.asp",true);
xlhttp.setRequestHeader("Content-type","application/x-www-form-unclencoded");
xhhttp.send("fname=Bill&name=Gates");
```
| 方法                               | 描述                                                         |
| :--------------------------------- | :----------------------------------------------------------- |
| setRequestHeader(*header*,*value*) | 向请求添加 HTTP 头。*header*: 规定头的名称*value*: 规定头的值 |
#### url-服务器上的文件
open() 方法的 *url* 参数是服务器上文件的地址：
```js
xmlhttp.open("GET","ajax_test.asp",true);
```
该文件可以是任何类型的文件，比如 .txt 和 .xml，或者服务器脚本文件，比如 .asp 和 .php （在传回响应之前，能够在服务器上执行任务）。
#### 异步 - True 或 False？
AJAX 指的是异步 JavaScript 和 XML（Asynchronous JavaScript and XML）。
`XMLHttpRequest 对象如果要用于 AJAX 的话，其 open() 方法的 async 参数必须设置为 true：`
```
xmlhttp.open("GET","ajax_test.asp",true);
```
对于 web 开发人员来说，发送异步请求是一个巨大的进步。很多在服务器执行的任务都相当费时。AJAX 出现之前，这可能会引起应用程序挂起或停止。
通过 AJAX，JavaScript 无需等待服务器的响应，而是：
- 在等待服务器响应时执行其他脚本
- 当响应就绪后对响应进行处理
##### Async = true
`当使用async=true时，请规定在响应处于onreadystatechange事件中的就绪状态时执行的函数：`
```js
xmlhttp.onreadystatechage= function(){
	if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
	document.getElementById("myDiv").innerHTML = xmlhttp.responseText;
	}
xmlhttp.open("GET","test1.txt",true);
xmlhttp.send();
```
##### Async = false JavaScript 会等到服务器响应就绪才继续执行。如果服务器繁忙或缓慢，应用程序会挂起或停止。
如需使用 async=false，请将 open() 方法中的第三个参数改为 false：
```js
xmlhttp.open("GET","test1.txt",false);
```
我们不推荐使用 async=false，但是对于一些小型的请求，也是可以的。
请记住，JavaScript 会等到服务器响应就绪才继续执行。如果服务器繁忙或缓慢，应用程序会挂起或停止。
**注释：**当您使用 async=false 时，请不要编写 onreadystatechange 函数 - 把代码放到 send() 语句后面即可：
```js
xmlhttp.open("GET","test1.txt",false);
xmlhttp.send();
document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
```
### XHR 响应
----
#### 服务器响应
解析 responseXML(.xml) 和 responseText(.txt) 文件
使用 XMLHttpRequest 对象的 responseText 或 responseXML 属性
| 属性         | 描述                       |
| :----------- | :------------------------- |
| responseText | 获得字符串形式的响应数据。 |
| responseXML  | 获得 XML 形式的响应数据。  |
#### responseText 属性
如果来自服务器的响应并非 XML，请使用 responseText 属性。
responseText 属性返回字符串形式的响应
```js
document.getElementById("mydiv").innerHTML = xmlhttp.responseText;
```
#### responseXML 属性
如果来自服务器的响应是 XML，而且需要作为 XML 对象进行解析
```js
function loadXMLDoc(){
	var xmlhttp;
	var txt,x,i;
	if(window.XMLHttpRequest){
		xmlhttp = new XMLHttpRequest();	
	}else{
		xmlhttp = new AvtiveXObject("Microsoft.XMLHTTP");
	}
	xmlhttp.onreadystatechage = function(){
		if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
			xmlDoc = xmlhttp.responseXML;
			txt = "";
			x=xmlDoc.getElementsByTagName("ARTIST"); // 获取标签 ARTIST
            for (i=0;i<x.length;i++)
            {
                txt= xt + x[i].childNodes[0].nodeValue + "<br>";
            }
            document.getElementById("myDiv").innerHTML=txt;
		}
	}
	xmlhttp.open("GET","xml文件位置","true");
	xmlhttp.send();
}
```
### XHR readyState == 4 status == 200
--------
#### onreadystatechange 事件
当请求被发送到服务器时，我们需要执行一些基于响应的任务。
每当 readyState 改变时，就会触发 onreadystatechange 事件。
readyState 属性存有 XMLHttpRequest 的状态信息。
下面是 XMLHttpRequest 对象的三个重要的属性：
| 属性               | 描述                                                         |
| :----------------- | :----------------------------------------------------------- |
| onreadystatechange | 存储函数（或函数名），每当 readyState 属性改变时，就会调用该函数。 |
| readyState         | 存有 XMLHttpRequest 的状态。从 0 到 4 发生变化。0: 请求未初始化1: 服务器连接已建立2: 请求已接收3: 请求处理中4: 请求已完成，且响应已就绪 |
| status             | 200: "OK" 404: 未找到页面                                    |
> **注意：** onreadystatechange 事件被触发 4 次（0 - 4）, 分别是： 0-1、1-2、2-3、3-4，对应着 readyState 的每个变化。
```js
xmlhttp.onreadystatechange-function(){
	if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
	//在 onreadystatechange 事件中，我们规定当服务器响应已做好被处理的准备时所执行的任务。
	//当 readyState 等于 4 且状态(status)为 200 时，表示响应已就绪：
		document.getElementById()
	}
}
```
#### 使用 Callback 回调函数
回调函数是一种以参数形式传递给另一个函数的函数。
如果您的网站上存在多个 AJAX 任务，那么您应该为创建 XMLHttpRequest 对象编写一个*标准*的函数，并为每个 AJAX 任务调用该函数。
该函数调用应该包含 URL 以及发生 onreadystatechange 事件时执行的任务（每次调用可能不尽相同）
```js
var xmlhttp;
function loadXMLDoc(url,cfunc){
    if(window.XMLHttpRequest){
      	xmlhttp = new XMLHttpRequest(); 
    }else{
        xmlhttp = new ActiveXObject('Microsoft.XMLHTTP');
    }
    xmlhttp.onreadystatechange = cfunc;
    xmlhttp.open("GET",url,true);
    xmlhttp.send();
}
function myFunction(){
 	loadXMLDoc("/try/ajax/ajax_info.txt",function()
    {
        if (xmlhttp.readyState==4 && xmlhttp.status==200)
        {
            document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
        }
    });
}
<div id="myDiv"><h2>使用 AJAX 修改文本内容</h2></div>
<button type="button" onclick="myFunction()">修改内容</button>
```
## 原生Ajax
### 隐藏帧iframe方式实现页面局 同步
```js
<div>
        <form action="./iframe.php" method="post" target="myframe">
            用户名：<input type="text" name="username"><span id="info"></span><br>
            密码：<input type="text" name="password">
            <input type="submit" value="登录">
        </form>
    </div>
    <iframe width="0" height="0"  frameborder="0" name="myframe"></iframe>
    <?php 
$uname = $_POST['username'];
$pw = $_POST['password'];
// if($uname == 'admin' && $pw == '123'){
//     echo '登录成功';
// }
if($uname == 'admin' && $pw == '123'){
?>
    <script type="text/javascript">
        parent.document.getElementById('info').innerHTML = '登录成功';
    </script>
<?php }else{ ?>
    <script type="text/javascript">
        parent.document.getElementById('info').innerHTML = '登录失败';
    </script>
<?php } ?>
```
### 实现页面局部更新
使用Ajax发送请求需要如下几步：
```js
get
//创建XMLHttpRequest 对象
var xhr = null
if(window.XMLHttpRequest){
	xhr = new XMLHttpRequest(); // 标准浏览器
}else{
	xhr = new ActiveXObject("Microsoft") // IE老版本 IE6 
}
准备发送
参数一：请求方式（get获取数据；post提交数据）
参数二：请求地址
参数三：同步或者异步标志位，默认是true表示异步，false表示同步
如果是get 请求那么请求参数必须在url中传递
encodeURI() 用来对中文参数进行编码。防止乱码
var param = 'username='+uname+'&password'
xhr.open('get','02get.php?+encodeURI(param)'+pw,true);
执行发送动作
xhr.send(null); //get请求这里需要添加null参数
指定回调函数
xhr.onreadystatechange = function(){
	if(xhr.readyState == 4 && xhr.status == 200){
		cosole.log(xhr.responseText)
	}
}
post
var xhr = null
if(window.XMLHttpRequest){
	xhr = new XMLHttpRequest(); // 标准浏览器
}else{
	xhr = new ActiveXObject("Microsoft") // IE老版本 IE6 
}
//readyState = 0表示xhr对象创建完成
准备发送
参数一：请求方式（get获取数据；post提交数据）
参数二：请求地址
参数三：同步或者异步标志位，默认是true表示异步，false表示同步
如果是get 请求那么请求参数必须在url中传递
post请求参数通过send传递，不需要通过encodeURI()转码必须设置请求头信息
var param = 'username='+uname+'&password'
xhr.o pen('post','02get.php'+pw,true);
xhr.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
执行发送动作
xhr.send(param); //post请求在这里传递，并且不需要转码
指定回调函数 
// readyState = 1表示已经发生了请求
// 该函数调用的条件就是readyState状态发生变化(不包括从0变为1)
xhr.onreadystatechange = function(){
	/*
	readyState:
	2 浏览器已经收到了服务器响应的数据
	3 正在解析数据
	4 数据已经解析完成，可以使用了，但是数据不一定是正常的
	*/
	if(xhr.readyState == 4 && xhr.status == 200){
	// 200 状态码 响应成功  404 没有找到请求的资源 500 服务器端错误
	// responseText
		cosole.log(xhr.responseText)
		//var data = xhr.responseXML; xml
	}
}
```
onreadysatechange
xhr.readyState
- 0 xhr对象初始化
- 1 执行发送动作
- 2 服务器端数据已经全部返回
- 3 数据正在解析
- 4 数据解析完成，可以使用了
xhr.status 
- 200 数据相应正常
- 404 没有找到资源
- 500 服务器端错误
## 跨域
[(...) 不要再问我跨域的问题了 - 个人文章 - SegmentFault 思否](https://segmentfault.com/a/1190000015597029)
[Ajax 知识体系大梳理 - 掘金](https://juejin.im/post/58c883ecb123db005311861a#heading-67)
[coffe1891/frontend-hard-mode-interview: 《前端内参》，有关于JavaScript、编程范式、设计模式、软件开发的艺术等大前端范畴内的知识分享，旨在帮助前端工程师们夯实技术基础以通过一线互联网企业技术面试。](https://github.com/coffe1891/frontend-hard-mode-interview)
### 什么是跨域
- 域名不同
- 域名相同，端口不同
只有域名相同，端口相同时，才可以访问数据
### 跨域的产生
浏览器同源策略限制了从同一个源加载的文档或脚本如何与来自另一个源的资源进行交互。这是一个用于隔离潜在恶意文件的重要安全机制。
### 没有同源策略限制的两大危险场景
据我了解，浏览器是从两个方面去做这个同源策略的，
一是针对接口的请求，
二是针对Dom的查询。
试想一下没有这样的限制上述两种动作有什么危险。
#### 没有同源策略限制的接口请求
有一个小小的东西叫cookie大家应该知道，一般用来处理登录等场景，目的是让服务端知道谁发出的这次请求。如果你请求了接口进行登录，服务端验证通过后会在响应头加入Set-Cookie字段，然后下次再发请求的时候，浏览器会自动将cookie附加在HTTP请求的头字段Cookie中，服务端就能知道这个用户已经登录过了。知道这个之后，我们来看场景：
1.你准备去清空你的购物车，于是打开了买买买网站www.maimaimai.com，然后登录成功，一看，购物车东西这么少，不行，还得买多点。
2.你在看有什么东西买的过程中，你的好基友发给你一个链接www.nidongde.com，一脸yin笑地跟你说：“你懂的”，你毫不犹豫打开了。
3.你饶有兴致地浏览着www.nidongde.com，谁知这个网站暗地里做了些不可描述的事情！由于没有同源策略的限制，它向www.maimaimai.com发起了请求！聪明的你一定想到上面的话“服务端验证通过后会在响应头加入Set-Cookie字段，然后下次再发请求的时候，浏览器会自动将cookie附加在HTTP请求的头字段Cookie中”，这样一来，这个不法网站就相当于登录了你的账号，可以为所欲为了！如果这不是一个买买买账号，而是你的银行账号，那……
这就是传说中的CSRF攻击[浅谈CSRF攻击方式](http://www.cnblogs.com/hyddd/archive/2009/04/09/1432744.html)。
看了这波CSRF攻击我在想，即使有了同源策略限制，但cookie是明文的，还不是一样能拿下来。于是我看了一些cookie相关的文章[聊一聊 cookie](https://segmentfault.com/a/1190000004556040#articleHeader6)、[Cookie/Session的机制与安全](https://harttle.land/2015/08/10/cookie-session.html)，知道了服务端可以设置httpOnly，使得前端无法操作cookie，如果没有这样的设置，像XSS攻击就可以去获取到cookie[Web安全测试之XSS](https://www.cnblogs.com/TankXiao/archive/2012/03/21/2337194.html)；设置secure，则保证在https的加密通信中传输以防截获。
#### 没有同源策略限制的Dom查询
1.有一天你刚睡醒，收到一封邮件，说是你的银行账号有风险，赶紧点进www.yinghang.com改密码。你吓尿了，赶紧点进去，还是熟悉的银行登录界面，你果断输入你的账号密码，登录进去看看钱有没有少了。
2.睡眼朦胧的你没看清楚，平时访问的银行网站是www.yinhang.com，而现在访问的是www.yinghang.com，这个钓鱼网站做了什么呢？
```
// HTML
<iframe name="yinhang" src="www.yinhang.com"></iframe>
// JS
// 由于没有同源策略的限制，钓鱼网站可以直接拿到别的网站的Dom
const iframe = window.frames['yinhang']
const node = iframe.document.getElementById('你输入账号密码的Input')
console.log(`拿到了这个${node}，我还拿不到你刚刚输入的账号密码吗`)
```
由此我们知道，同源策略确实能规避一些危险，不是说有了同源策略就安全，只是说同源策略是一种浏览器最基本的安全机制，毕竟能提高一点攻击的成本。其实没有刺不穿的盾，只是攻击的成本和攻击成功后获得的利益成不成正比。
# AJAX 数据库
AJAX 与数据库进行动态通信
```js
function showCustomer(str)
{
  var xmlhttp;    
  if (str=="")
  {
    document.getElementById("txtHint").innerHTML="";
    return;
  }
  if (window.XMLHttpRequest)
  {
    // IE7+, Firefox, Chrome, Opera, Safari 浏览器执行代码
    xmlhttp=new XMLHttpRequest();
  }
  else
  {
    // IE6, IE5 浏览器执行代码
    xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
  }
  xmlhttp.onreadystatechange=function()
  {
    if (xmlhttp.readyState==4 && xmlhttp.status==200)
    {
      document.getElementById("txtHint").innerHTML=xmlhttp.responseText;
    }
  }
  xmlhttp.open("GET","/try/ajax/getcustomer.php?q="+str,true);
  xmlhttp.send();
}
```
# AJAX XML文件
```js
function loadXMLDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     	myFunction(this);
    }
  };
  xhttp.open("GET", "cd_catalog.xml", true);
  xhttp.send();
}
function myFunction(xml) {
  var i;
  var xmlDoc = xml.responseXML;
  var table="<tr><th>Artist</th><th>Title</th></tr>";
  var x = xmlDoc.getElementsByTagName("CD");
  for (i = 0; i <x.length; i++) { 
    table += "<tr><td>" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}
```
# AJAX JQuery
AJAX 是一种与服务器交换数据的技术，可以在不重新载入整个页面的情况下更新网页的一部分。
ajax() 方法通过 HTTP 请求加载远程数据。
该方法是 jQuery 底层 AJAX 实现。简单易用的高层实现见 $.get, $.post 等。$.ajax() 返回其创建的 XMLHttpRequest 对象。大多数情况下你无需直接操作该函数，除非你需要操作不常用的选项，以获得更多的灵活性。
最简单的情况下，$.ajax() 可以不带任何参数直接使用。
**注意：**所有的选项都可以通过 $.ajaxSetup() 函数来全局设置。
```js
$(document).ready(function(){
	$("#b01").click(function(){
		 htmlpbj = $.ajax({url:'文件名.txt',async:false});
		 $("#myDiv").html(htmlobj.responseText);	 
	});
});
<div id="myDiv"><h2>通过 AJAX 改变文本</h2></div>
<button id="b01" type="button">改变内容</button>
```
# AJAX Vue
axios
# AJAX Node
# AJAX PHP
### 跨域
[解决ajax跨域问题【5种解决方案】](https://blog.csdn.net/itcats_cn/article/details/82318092)
什么是跨域
解决跨域的方法
# 原生 AJAX
> AJAX ==  <b style="color:red;font-size:20px">A</b>synchronous <b style="color:red;font-size:20px">J</b>avascript <b style="color:red;font-size:20px">A</b>nd <b style="color:red;font-size:20px">X</b>ML 异步的JavaScript和XML
>
> AJAX不是新的编程语言，而是一种使用现有标准的新的方法
>
> AJAX 是一种在无需重新加载整个网页的情况下，能够更新部分网页的技术
## AJAX基础
![image-20200503211444689](https://i.loli.net/2020/05/03/GFHqEOcxSp718Tg.png)
### 三件套
- `html(html5)` 主要用来实现页面得排版布局
- `css (css3)`主要用来实现页面得样式美化
- `JavaScript(JQuery)` 主要用来实现前端功能特效
### 网站
- 网站由一系列页面组成（页面由js、css、图片、html标签….. 所有的这些文件都被称为资源），网站分为动态网站和静态网站
### 概念
- ajax最早产生于2005年
- AJAX ==  <b style="color:red;font-size:20px">A</b>synchronous <b style="color:red;font-size:20px">J</b>avascript <b style="color:red;font-size:20px">A</b>nd <b style="color:red;font-size:20px">X</b>ML 异步的JavaScript和XML
- 传统的网页（不使用AJAX） 如果需要更新内容，必需重载整个网页，AJAX 是一种用于创建快速动态网页的技术，通过在后台与服务器进行少量数据交互，AJAX可以使网页实现异步更新，这意味着可以在不重新在加载整个网页的情况下，对网页的某一部分进行更新
- AJAX不是新的编程语言，而是``一种使用现有标准的新方法``，AJAX它不是像HTML、JavaScript或CSS 这样的一种“正式的”技术，它是表示 ==一些技术的混合交互==的一个术语(JavaScript 、Web 浏览器、Web服务器) ，它使我们可以获取和显示新的内容，而不必载入一个新的Web页面。增强用户体验，更有桌面程序的感觉。
#### AJAX是基于现有的Internet标准
- XMLHttpRequest 对象（异步的与服务器交换数据）
- JavaScript/DOM (信息显示/交互)
- CSS(给数据定义样式)
- XML(作为转换数据的格式)
### 作用
- 显示新的HTML内容而不用载入整个页面
- 提交一个表单并且立即显示结果
- 登录而不用跳转到新的页面
- 星级评定组件
- 遍历数据库信息加载更多而不刷新页面
### AJAX代码
```js
var xmlhttp;
if(window.XMLHttpRequest){
	xmlhttp = new XMLHttpRequest();
}else{
	xmlhttp = new AcitveXObject("Microsoft.XMLHTTP");
}
xmlhttp.onreadystatechange = function(){
    if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
       document.getElementById("mydiv").innerHTML = xmlhttp.responseText;
    }
}
xmlhttp.open("GET","请求文件的路径名如 /my/hello.json  /my/hello.txt",true) 
// http://mobilecdnbj.kugou.com/api/v3/tag/recommend?showtype=3&apiver=2&plat=0
xmlhttp.send();
注意点： readyState status responseText 请求文件的路径名如 要从根目录开始
onreadystatechage xmlhttp.responseText
```
## AJAX XHR
### 创建 => 请求 =>响应 => readyState函数
### XHR 创建对象
XMLHttpRequest是AJAX的基础
#### XMLHttpRequest对象
- 所有现代浏览器均支持 XMLHttpRequest 对象（IE5 和 IE6 使用 ActiveXObject）
- `XMLHttpRequest 用于在后台与服务器交换数据。这意味着可以在不重新加载整个网页的情况下，对网页的某部分进行更新`
#### 创建XMLHttpRequest对象
所有现代浏览器（IE7+、Firefox、Chrome、Safari 以及 Opera）均内建 XMLHttpRequest 对象。
- 创建DMLHttpRequest对象的语法：
```js
variable = new XMLHttpRequest();
```
- IE5、IE6(老版本的 Internet Explorer)使用 ActiveX 对象
```js
variable = new ActiveXObject("Microsoft.XMLHTTP")
```
- 兼容所有浏览器
```js
var xmlhttp;
if(window.XMLHttpRequest){
	//code for IE7+, Firefox, Chrome, Opera, Safari
	xmlhttp = new XMLHttpRequest();
}else{
	//// code for IE6, IE5
	xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
}
```
### XHR 请求 `xmlhttp.open()`
----
XMLHttpRequest 对象用于和服务器交换数据
#### 向服务器发送请求
```js
xmlhttp.open("GET","test.txt","true");
xmlhttp.send();
```
| 方法                         | 描述                                                         |
| :--------------------------- | :----------------------------------------------------------- |
| open(*method*,*url*,*async*) | 规定请求的类型、URL 以及是否异步处理请求。*method*：请求的类型；GET 或 POST*url*：文件在服务器上的位置*async*：true（异步）或 false（同步） |
| send(*string*)               | `将请求发送到服务器`。*string*：仅用于 POST 请求             |
#### GET 还是 POST的区别
GET：GET 更简单也更快，并且在大部分情况下都能用。
POST：以下情况中，请使用 POST 请求：
- 无法使用缓存文件（更新服务器上的文件或数据库）
- 向服务器发送大量数据（POST 没有数据量限制）
- 发送包含未知字符的用户输入时，POST 比 GET 更稳定也更可靠
##### Get请求
```js
xmlhttp.open("GET","demo_get.asp",true);
xmlhttp.send();
```
在上面的例子中，您可能得到的是缓存的结果。
为了避免这种情况，请向 URL 添加一个唯一的 ID：
```js
xlhttp.open("GET","demo_get.asp?t="+ Math.random(),true);
xhhttp.send();
```
##### Post请求
```js
xmlhttp.open("POST","demo_post.asp",true);
xmlhttp.send();
```
如果需要像 HTML 表单那样 POST 数据，请使用 setRequestHeader() 来添加 HTTP 头。然后在 send() 方法中规定您希望发送的数据：
```js
xlhttp.open("POST","ajax_test.asp",true);
xlhttp.setRequestHeader("Content-type","application/x-www-form-unclencoded");
xhhttp.send("fname=Bill&name=Gates");
```
| 方法                               | 描述                                                         |
| :--------------------------------- | :----------------------------------------------------------- |
| setRequestHeader(*header*,*value*) | 向请求添加 HTTP 头。*header*: 规定头的名称*value*: 规定头的值 |
#### url-服务器上的文件
open() 方法的 *url* 参数是服务器上文件的地址：
```js
xmlhttp.open("GET","ajax_test.asp",true);
```
该文件可以是任何类型的文件，比如 .txt 和 .xml，或者服务器脚本文件，比如 .asp 和 .php （在传回响应之前，能够在服务器上执行任务）。
#### 异步 - True 或 False？
AJAX 指的是异步 JavaScript 和 XML（Asynchronous JavaScript and XML）。
`XMLHttpRequest 对象如果要用于 AJAX 的话，其 open() 方法的 async 参数必须设置为 true：`
```
xmlhttp.open("GET","ajax_test.asp",true);
```
对于 web 开发人员来说，发送异步请求是一个巨大的进步。很多在服务器执行的任务都相当费时。AJAX 出现之前，这可能会引起应用程序挂起或停止。
通过 AJAX，JavaScript 无需等待服务器的响应，而是：
- 在等待服务器响应时执行其他脚本
- 当响应就绪后对响应进行处理
##### Async = true
`当使用async=true时，请规定在响应处于onreadystatechange事件中的就绪状态时执行的函数：`
```js
xmlhttp.onreadystatechage= function(){
	if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
	document.getElementById("myDiv").innerHTML = xmlhttp.responseText;
	}
xmlhttp.open("GET","test1.txt",true);
xmlhttp.send();
```
##### Async = false JavaScript 会等到服务器响应就绪才继续执行。如果服务器繁忙或缓慢，应用程序会挂起或停止。
如需使用 async=false，请将 open() 方法中的第三个参数改为 false：
```js
xmlhttp.open("GET","test1.txt",false);
```
我们不推荐使用 async=false，但是对于一些小型的请求，也是可以的。
请记住，JavaScript 会等到服务器响应就绪才继续执行。如果服务器繁忙或缓慢，应用程序会挂起或停止。
**注释：**当您使用 async=false 时，请不要编写 onreadystatechange 函数 - 把代码放到 send() 语句后面即可：
```js
xmlhttp.open("GET","test1.txt",false);
xmlhttp.send();
document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
```
### XHR 响应
----
#### 服务器响应
解析 responseXML(.xml) 和 responseText(.txt) 文件
使用 XMLHttpRequest 对象的 responseText 或 responseXML 属性
| 属性         | 描述                       |
| :----------- | :------------------------- |
| responseText | 获得字符串形式的响应数据。 |
| responseXML  | 获得 XML 形式的响应数据。  |
#### responseText 属性
如果来自服务器的响应并非 XML，请使用 responseText 属性。
responseText 属性返回字符串形式的响应
```js
document.getElementById("mydiv").innerHTML = xmlhttp.responseText;
```
#### responseXML 属性
如果来自服务器的响应是 XML，而且需要作为 XML 对象进行解析
```js
function loadXMLDoc(){
	var xmlhttp;
	var txt,x,i;
	if(window.XMLHttpRequest){
		xmlhttp = new XMLHttpRequest();	
	}else{
		xmlhttp = new AvtiveXObject("Microsoft.XMLHTTP");
	}
	xmlhttp.onreadystatechage = function(){
		if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
			xmlDoc = xmlhttp.responseXML;
			txt = "";
			x=xmlDoc.getElementsByTagName("ARTIST"); // 获取标签 ARTIST
            for (i=0;i<x.length;i++)
            {
                txt= xt + x[i].childNodes[0].nodeValue + "<br>";
            }
            document.getElementById("myDiv").innerHTML=txt;
		}
	}
	xmlhttp.open("GET","xml文件位置","true");
	xmlhttp.send();
}
```
### XHR readyState == 4 status == 200
--------
#### onreadystatechange 事件
当请求被发送到服务器时，我们需要执行一些基于响应的任务。
每当 readyState 改变时，就会触发 onreadystatechange 事件。
readyState 属性存有 XMLHttpRequest 的状态信息。
下面是 XMLHttpRequest 对象的三个重要的属性：
| 属性               | 描述                                                         |
| :----------------- | :----------------------------------------------------------- |
| onreadystatechange | 存储函数（或函数名），每当 readyState 属性改变时，就会调用该函数。 |
| readyState         | 存有 XMLHttpRequest 的状态。从 0 到 4 发生变化。0: 请求未初始化1: 服务器连接已建立2: 请求已接收3: 请求处理中4: 请求已完成，且响应已就绪 |
| status             | 200: "OK" 404: 未找到页面                                    |
> **注意：** onreadystatechange 事件被触发 4 次（0 - 4）, 分别是： 0-1、1-2、2-3、3-4，对应着 readyState 的每个变化。
```js
xmlhttp.onreadystatechange-function(){
	if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
	//在 onreadystatechange 事件中，我们规定当服务器响应已做好被处理的准备时所执行的任务。
	//当 readyState 等于 4 且状态(status)为 200 时，表示响应已就绪：
		document.getElementById()
	}
}
```
#### 使用 Callback 回调函数
回调函数是一种以参数形式传递给另一个函数的函数。
如果您的网站上存在多个 AJAX 任务，那么您应该为创建 XMLHttpRequest 对象编写一个*标准*的函数，并为每个 AJAX 任务调用该函数。
该函数调用应该包含 URL 以及发生 onreadystatechange 事件时执行的任务（每次调用可能不尽相同）
```js
var xmlhttp;
function loadXMLDoc(url,cfunc){
    if(window.XMLHttpRequest){
      	xmlhttp = new XMLHttpRequest(); 
    }else{
        xmlhttp = new ActiveXObject('Microsoft.XMLHTTP');
    }
    xmlhttp.onreadystatechange = cfunc;
    xmlhttp.open("GET",url,true);
    xmlhttp.send();
}
function myFunction(){
 	loadXMLDoc("/try/ajax/ajax_info.txt",function()
    {
        if (xmlhttp.readyState==4 && xmlhttp.status==200)
        {
            document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
        }
    });
}
<div id="myDiv"><h2>使用 AJAX 修改文本内容</h2></div>
<button type="button" onclick="myFunction()">修改内容</button>
```
## 原生Ajax
### 隐藏帧iframe方式实现页面局 同步
```js
<div>
        <form action="./iframe.php" method="post" target="myframe">
            用户名：<input type="text" name="username"><span id="info"></span><br>
            密码：<input type="text" name="password">
            <input type="submit" value="登录">
        </form>
    </div>
    <iframe width="0" height="0"  frameborder="0" name="myframe"></iframe>
    <?php 
$uname = $_POST['username'];
$pw = $_POST['password'];
// if($uname == 'admin' && $pw == '123'){
//     echo '登录成功';
// }
if($uname == 'admin' && $pw == '123'){
?>
    <script type="text/javascript">
        parent.document.getElementById('info').innerHTML = '登录成功';
    </script>
<?php }else{ ?>
    <script type="text/javascript">
        parent.document.getElementById('info').innerHTML = '登录失败';
    </script>
<?php } ?>
```
### 实现页面局部更新
使用Ajax发送请求需要如下几步：
```js
get
//创建XMLHttpRequest 对象
var xhr = null
if(window.XMLHttpRequest){
	xhr = new XMLHttpRequest(); // 标准浏览器
}else{
	xhr = new ActiveXObject("Microsoft") // IE老版本 IE6 
}
准备发送
参数一：请求方式（get获取数据；post提交数据）
参数二：请求地址
参数三：同步或者异步标志位，默认是true表示异步，false表示同步
如果是get 请求那么请求参数必须在url中传递
encodeURI() 用来对中文参数进行编码。防止乱码
var param = 'username='+uname+'&password'
xhr.open('get','02get.php?+encodeURI(param)'+pw,true);
执行发送动作
xhr.send(null); //get请求这里需要添加null参数
指定回调函数
xhr.onreadystatechange = function(){
	if(xhr.readyState == 4 && xhr.status == 200){
		cosole.log(xhr.responseText)
	}
}
post
var xhr = null
if(window.XMLHttpRequest){
	xhr = new XMLHttpRequest(); // 标准浏览器
}else{
	xhr = new ActiveXObject("Microsoft") // IE老版本 IE6 
}
//readyState = 0表示xhr对象创建完成
准备发送
参数一：请求方式（get获取数据；post提交数据）
参数二：请求地址
参数三：同步或者异步标志位，默认是true表示异步，false表示同步
如果是get 请求那么请求参数必须在url中传递
post请求参数通过send传递，不需要通过encodeURI()转码必须设置请求头信息
var param = 'username='+uname+'&password'
xhr.o pen('post','02get.php'+pw,true);
xhr.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
执行发送动作
xhr.send(param); //post请求在这里传递，并且不需要转码
指定回调函数 
// readyState = 1表示已经发生了请求
// 该函数调用的条件就是readyState状态发生变化(不包括从0变为1)
xhr.onreadystatechange = function(){
	/*
	readyState:
	2 浏览器已经收到了服务器响应的数据
	3 正在解析数据
	4 数据已经解析完成，可以使用了，但是数据不一定是正常的
	*/
	if(xhr.readyState == 4 && xhr.status == 200){
	// 200 状态码 响应成功  404 没有找到请求的资源 500 服务器端错误
	// responseText
		cosole.log(xhr.responseText)
		//var data = xhr.responseXML; xml
	}
}
```
onreadysatechange
xhr.readyState
- 0 xhr对象初始化
- 1 执行发送动作
- 2 服务器端数据已经全部返回
- 3 数据正在解析
- 4 数据解析完成，可以使用了
xhr.status 
- 200 数据相应正常
- 404 没有找到资源
- 500 服务器端错误
## 跨域
[(...) 不要再问我跨域的问题了 - 个人文章 - SegmentFault 思否](https://segmentfault.com/a/1190000015597029)
[Ajax 知识体系大梳理 - 掘金](https://juejin.im/post/58c883ecb123db005311861a#heading-67)
[coffe1891/frontend-hard-mode-interview: 《前端内参》，有关于JavaScript、编程范式、设计模式、软件开发的艺术等大前端范畴内的知识分享，旨在帮助前端工程师们夯实技术基础以通过一线互联网企业技术面试。](https://github.com/coffe1891/frontend-hard-mode-interview)
### 什么是跨域
- 域名不同
- 域名相同，端口不同
只有域名相同，端口相同时，才可以访问数据
### 跨域的产生
浏览器同源策略限制了从同一个源加载的文档或脚本如何与来自另一个源的资源进行交互。这是一个用于隔离潜在恶意文件的重要安全机制。
### 没有同源策略限制的两大危险场景
据我了解，浏览器是从两个方面去做这个同源策略的，
一是针对接口的请求，
二是针对Dom的查询。
试想一下没有这样的限制上述两种动作有什么危险。
#### 没有同源策略限制的接口请求
有一个小小的东西叫cookie大家应该知道，一般用来处理登录等场景，目的是让服务端知道谁发出的这次请求。如果你请求了接口进行登录，服务端验证通过后会在响应头加入Set-Cookie字段，然后下次再发请求的时候，浏览器会自动将cookie附加在HTTP请求的头字段Cookie中，服务端就能知道这个用户已经登录过了。知道这个之后，我们来看场景：
1.你准备去清空你的购物车，于是打开了买买买网站www.maimaimai.com，然后登录成功，一看，购物车东西这么少，不行，还得买多点。
2.你在看有什么东西买的过程中，你的好基友发给你一个链接www.nidongde.com，一脸yin笑地跟你说：“你懂的”，你毫不犹豫打开了。
3.你饶有兴致地浏览着www.nidongde.com，谁知这个网站暗地里做了些不可描述的事情！由于没有同源策略的限制，它向www.maimaimai.com发起了请求！聪明的你一定想到上面的话“服务端验证通过后会在响应头加入Set-Cookie字段，然后下次再发请求的时候，浏览器会自动将cookie附加在HTTP请求的头字段Cookie中”，这样一来，这个不法网站就相当于登录了你的账号，可以为所欲为了！如果这不是一个买买买账号，而是你的银行账号，那……
这就是传说中的CSRF攻击[浅谈CSRF攻击方式](http://www.cnblogs.com/hyddd/archive/2009/04/09/1432744.html)。
看了这波CSRF攻击我在想，即使有了同源策略限制，但cookie是明文的，还不是一样能拿下来。于是我看了一些cookie相关的文章[聊一聊 cookie](https://segmentfault.com/a/1190000004556040#articleHeader6)、[Cookie/Session的机制与安全](https://harttle.land/2015/08/10/cookie-session.html)，知道了服务端可以设置httpOnly，使得前端无法操作cookie，如果没有这样的设置，像XSS攻击就可以去获取到cookie[Web安全测试之XSS](https://www.cnblogs.com/TankXiao/archive/2012/03/21/2337194.html)；设置secure，则保证在https的加密通信中传输以防截获。
#### 没有同源策略限制的Dom查询
1.有一天你刚睡醒，收到一封邮件，说是你的银行账号有风险，赶紧点进www.yinghang.com改密码。你吓尿了，赶紧点进去，还是熟悉的银行登录界面，你果断输入你的账号密码，登录进去看看钱有没有少了。
2.睡眼朦胧的你没看清楚，平时访问的银行网站是www.yinhang.com，而现在访问的是www.yinghang.com，这个钓鱼网站做了什么呢？
```
// HTML
<iframe name="yinhang" src="www.yinhang.com"></iframe>
// JS
// 由于没有同源策略的限制，钓鱼网站可以直接拿到别的网站的Dom
const iframe = window.frames['yinhang']
const node = iframe.document.getElementById('你输入账号密码的Input')
console.log(`拿到了这个${node}，我还拿不到你刚刚输入的账号密码吗`)
```
由此我们知道，同源策略确实能规避一些危险，不是说有了同源策略就安全，只是说同源策略是一种浏览器最基本的安全机制，毕竟能提高一点攻击的成本。其实没有刺不穿的盾，只是攻击的成本和攻击成功后获得的利益成不成正比。
# AJAX 数据库
AJAX 与数据库进行动态通信
```js
function showCustomer(str)
{
  var xmlhttp;    
  if (str=="")
  {
    document.getElementById("txtHint").innerHTML="";
    return;
  }
  if (window.XMLHttpRequest)
  {
    // IE7+, Firefox, Chrome, Opera, Safari 浏览器执行代码
    xmlhttp=new XMLHttpRequest();
  }
  else
  {
    // IE6, IE5 浏览器执行代码
    xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
  }
  xmlhttp.onreadystatechange=function()
  {
    if (xmlhttp.readyState==4 && xmlhttp.status==200)
    {
      document.getElementById("txtHint").innerHTML=xmlhttp.responseText;
    }
  }
  xmlhttp.open("GET","/try/ajax/getcustomer.php?q="+str,true);
  xmlhttp.send();
}
```
# AJAX XML文件
```js
function loadXMLDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     	myFunction(this);
    }
  };
  xhttp.open("GET", "cd_catalog.xml", true);
  xhttp.send();
}
function myFunction(xml) {
  var i;
  var xmlDoc = xml.responseXML;
  var table="<tr><th>Artist</th><th>Title</th></tr>";
  var x = xmlDoc.getElementsByTagName("CD");
  for (i = 0; i <x.length; i++) { 
    table += "<tr><td>" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}
```
# AJAX JQuery
AJAX 是一种与服务器交换数据的技术，可以在不重新载入整个页面的情况下更新网页的一部分。
ajax() 方法通过 HTTP 请求加载远程数据。
该方法是 jQuery 底层 AJAX 实现。简单易用的高层实现见 $.get, $.post 等。$.ajax() 返回其创建的 XMLHttpRequest 对象。大多数情况下你无需直接操作该函数，除非你需要操作不常用的选项，以获得更多的灵活性。
最简单的情况下，$.ajax() 可以不带任何参数直接使用。
**注意：**所有的选项都可以通过 $.ajaxSetup() 函数来全局设置。
```js
$(document).ready(function(){
	$("#b01").click(function(){
		 htmlpbj = $.ajax({url:'文件名.txt',async:false});
		 $("#myDiv").html(htmlobj.responseText);	 
	});
});
<div id="myDiv"><h2>通过 AJAX 改变文本</h2></div>
<button id="b01" type="button">改变内容</button>
```
# AJAX Vue
axios
# AJAX Node
# AJAX PHP
### 跨域
[解决ajax跨域问题【5种解决方案】](https://blog.csdn.net/itcats_cn/article/details/82318092)
什么是跨域
解决跨域的方法
