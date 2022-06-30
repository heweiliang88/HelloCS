---
title: HTML5的隐藏功能
categories:
- 前端
tags:
- HTML5
- 前端
abbrlink: 33960
---

# 学习路线

html

教程

- [ ] [HTML | MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML)
- [ ] [HTML 教程 | 菜鸟教程](https://www.runoob.com/html/html-tutorial.html)
- [ ] [HTML 教程](https://www.w3school.com.cn/html/index.asp)
- [ ] [《图解HTML》第三节 HTML简介 - 掘金](https://juejin.cn/post/6940966600367407141)
- [ ] [HTML与CSS基础总结 - 掘金](https://juejin.cn/post/6844904185163415565)

- [ ] [HTML 教程 ](https://www.runoob.com/html/html-tutorial.html)
- [ ] [HTML（超文本标记语言） | MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML)

面试题

- [ ] [高频前端面试题汇总之HTML篇 ](https://juejin.cn/post/6905294475539513352)
- [ ] [2021 前端面试 | “HTML + CSS + JS”专题 - 掘金](https://juejin.cn/post/6844903848553742350)
- [ ] [html篇--这可能是目前较为全面的html面试知识点了吧](https://juejin.cn/post/6844904180943945742)

html5

教程

- [ ] [HTML5 教程 | 菜鸟教程](https://www.runoob.com/html/html5-intro.html)
- [ ] [HTML5 简介](https://www.w3school.com.cn/html/html5_intro.asp)
- [ ] [CSS3 和 HTML5 新特性一览 - 掘金](https://juejin.cn/post/6844903829679390728)
- [ ] [10个好用的 HTML5 特性 - 掘金](https://juejin.cn/post/6881779044505878542)
- [ ] [学习总结之HTML5剑指前端（建议收藏，图文并茂） - 掘金](https://juejin.cn/post/6844904082629459975)
- [x] [BAT大佬推荐使用的HTML5的十个功能 - 掘金](https://juejin.cn/post/6888507535771631629)
- [ ] [最全的HTML5知识汇总 - 前端技术交流 - 葡萄城产品技术社区](https://gcdn.grapecity.com.cn/showtopic-23856-1-3.html?utm_source=gold.xitu.io&utm_medium=referral&utm_campaign=20161214)
- [ ] [HTML5基础 - 掘金](https://juejin.cn/post/6844903925468889102)

面试题

- [ ] [前端HTML5面试官和应试者一问一答 | 七日打卡 ](https://juejin.cn/post/6917044041863397383)
- [ ] [[秃破前端面试] —— HTML5 - 掘金](https://juejin.cn/post/6844904066926002189)

书籍：

- [ ] Web权威指南

# 知识图谱

HTML

- 基本文档 (Html)： 
- 基本标签（Basic Tag）
- 文本格式化（Formatting）
- 链接（Link）
- 图片（Images）
- 列表（List）: 有序列表、无序列表
- 表格（Table） table 、tr、td、th
- 表单（Form）
- 框架（iframe）
- 实体字符（Entities）
- 颜色（Color）
- 脚本（noscript）

html5

- 新增标签和废弃标签
- 语法与基础标签
- Div布局
- 语义化标签与属性
- 有序、无序、自定义列表
- 超链接、img
- 表单、表格
- 音频、视频、多媒体
- 浏览器内核

css3

- 布局：盒模型、flex布局、两/三栏布局、水平/垂直居中、BFC、清除浮动；
- 动画


# XHTML

XHTML是以XML格式编写的HTML 可扩展超文本标记语言

- 2001.1月 w3C 推荐标准
- 与HTML4.0.1几乎是相同的
- 更严格更纯净的HTML版本
- 以XML应用的方式定义HTML
- 大小写敏感
- 所有主流浏览器的支持文档结构
- XHTML  DOCTYPE 是强制性的
- `<html>`中的XML namespace 属性是强制性的元素语法
- 正确嵌套、始终关闭、必须小写、一个根元素 属性语法
- 属性小写、属性引号包围、属性最小化是禁止的

# HTML

## 快速

- 超文本标记语言
- `<!DOCTYPE html>`   文档声明类型
- head title base link meta script style 
- div span p h1~h5  br  a （target id ）  hr   img(src width height alt  align对齐 )
- (strong)b (em)i code sub sup small  ins(插入字) del  
- code 代码 kbd 键盘 samp 代码样本 var  变量 pre 预格式文本
- abbr 缩写 address 地址 bdo 文字方向 blockquote 长的引用 q 短的引用语  cite 引用 引证 dfn 定义项目 
- 表格 table 
  - caption 表格标题
  - table thead tbody tfoot + tr + td
  - table th 标题栏  tr 行  td 列 
    - border="0"
    - cellspacing 表格单元格之间的空间
    - cellpadding 单元格与单元格内容之间的距离
  - 合并单元格 作用在 td 上
    - colspan 合并列
    - rowspan  合并行
  - colgroup 表格组
  - col 列属性 
- 列表 list
  - 无序列表 ul li
  - 有序列表 ol li
  - 自定义列表 dl dt dd
- 表单 form
  - input 输入框
    -  type text  文本域
    -  password 密码
    -  radio 单选按钮
    -  checkbox 复选按钮
    -  sumbit 提交按钮
  - textarea 文本域 rows cols 
  - fieldset
  - legend
  - select option 下拉列表选项
    - `<option selected="selected">`
  - label  标签
  - button 按钮
  - datalist 输入控件选项列表  keygen  密钥对  output 计算结果
- 符号实体
- iframe src width height  frameborder="0"  class id style title 
  - frameset标签 HTML5 不支持 src 
  - frame
- media 
  - video audio
  - 插件
    - object 插件  插入对象Java 小程序 PDF阅读器 Flash 播放器`object` data type height width usemap name form 
    - embed 
- 属性 class id style title

## 插件

### Emmet

> [Emmet — the essential toolkit for web-developers](https://emmet.io/)

## 类库

### Boilerplate
> [html5-boilerplate](https://github.com/h5bp/html5-boilerplate)
>
> HTML5样板是一个专业的前端模板，用于构建快速、健壮和适应性强的web应用程序或网站。

```cmd
npx create-html5-boilerplate new-site
cd new-site
npm install
npm start
```
## 总结

- 基本文档 (Html)
- 基本标签（Basic Tag）
	- 块级元素  `div、h1-h6、ul、ol、li、dl、table、p、hr、form`
	- 行内元素 `span、a、img、input、span、textarea、label、select `
- 文本格式化（Formatting）
- 链接（Link）
	- a
- 图片（Images）
	- img
- 列表（List）
	- 有序列表 li
	- 无序列表 ul
- 表格（Table） 
	- table 、tr、td、th、
- 表单（Form）
- 框架（Iframe）
- 实体字符（Entities）
- 颜色（Color）
- 脚本（Noscript）

## 结构

#### 概述
- HTML（Hyper Text Markup Language）超文本标记语言，是一种使用结构化Web网页及其内容的标记语言
- 主要是通过HTML标签对网页中的文本、图片、声音等内容进行描述，是用来描述网页的一种语言。
- HTML 不是一种编程语言，而是一种**标记**语言（标记语言是一套标记标签（markup tag），使用标记标签来描述网页）
- HTML 文档（Web页面）包含 HTML标签 及 文本内容
#### HTML标签（HTML tag）与 HTML 元素
> HTML 标签 == HTML 元素

- "HTML 标签" 和 "HTML 元素" 通常都是描述同样的意思，严格来讲, 一个 HTML 元素包含了开始标签与结束标签
- 尖括号包围的关键词
- 成对出现
- HTML标签：第一个标签是开始标签（开放标签）== 起始标签（opening tag），第二个标签是结束标签（闭合标签）
- 单标签：`<br/>` 、`<input /> ` 空元素：没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的
- `<br/>` 在开始标签中添加斜杠，是关闭空元素的正确方法
#### HTML标签的语义化
HTML标签语义化：`所谓标签语义化，就是指标签的含义。`
#### 标签属性
```html
<标签名 属性1="属性值1" 属性2="属性值2" …> 内容 </标签名>  
// 键值对 的格式   key="value"  的格式 
```
#### 版本
| 版本      | 发布时间 |
| :-------- | :------- |
| HTML      | 1991     |
| HTML+     | 1993     |
| HTML 2.0  | 1995     |
| HTML 3.2  | 1997     |
| HTML 4.01 | 1999     |
| XHTML 1.0 | 2000     |
| HTML5     | 2012     |
| XHTML5    | 2013     |
#### HTML与HTML5 是不是编程语言？
>**HTML 是超文本标记语言，不具备图灵完备性，应该不算编程语言。**HTML5感觉更像一个平台，而不是一个语言。html5 包含 html等基础标记，有人也把 css3 划归到html5里面，更具划时代意义的是html5 提供了很多 js 的api，通过 js 调用这些api可以做到很多完备编程语言的事情。
>
>**在可计算性理论里，如果一系列操作数据的规则（如指令集、编程语言、细胞自动机）可以用来模拟单带图灵机，那么它是图灵完备的。**这个词源于引入图灵机概念的数学家艾伦·图灵。虽然图灵机会受到储存能力的物理限制，图灵完全性通常指“具有无限存储能力的通用物理机器或编程语言”。
>
>**HTML5** **是一门编程语言吗？**最基本的一个问题是，编程语言是为了解决一个问题，通过给计算机处理问题的逻辑指令从而得到相应结果的一种人机交互语言，html5是标记语言，其本质是信息载体，并不具备处理问题逻辑的能力，所以不是编程语言。
#### HTML组成
| 组成       | 区域                                 | 标签                                    |
| ---------- | ------------------------------------ | --------------------------------------- |
| <!DOCTYPE> | 文档类型                             | `<!DOCTYPE html>`                       |
| html       | 根节点                               | `<html></html>`                         |
| title      | 文档的标题                           | `<title></title>`                       |
| base       | 定义了页面链接标签的默认链接地址     | `<base></base>`                         |
| meta       | 元数据                               | `<meta>`                                |
| head       | 头部部分(包含了文档的元（meta）数据) | title(标题),meta,base,style,script,link |
| body       | 主体部分                             | p,h,a,b,u,i,s,em,del,ins,strong,img     |
```html
<base> // 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接:
<base href="https://www.baidu.com/" target="_black">
<a href="s?wd=123">123</a> // https://www.baidu.com/s?wd=123
<a href="s?wd=123">123</a>  
// 引入css的方法
<link> 
// 标签定义了文档与外部资源之间的关系。
// 标签通常用于链接到样式表
<link rel="stylesheet" type="text/css" href="mystyle.css">
<style> // 标签定义了HTML文档的样式文件引用地址.
<style>  // 元素中你也可以直接添加样式来渲染 HTML 文档:
<style type="text/css">
    body {background-color:yellow}
    p {color:blue}
</style>
<script>  
// 标签用于加载脚本文件，如： JavaScript。
```
#### 文档类型<!DOCTYPE>
~~~html
<!DOCTYPE html> 
// doctype 声明是不区分大小写的，告诉用户和浏览器我们使用的html版本号。
<!DOCTYPE> 标签位于文档的最前面，用于向浏览器说明当前文档使用哪种 HTML 或 XHTML 标准规范，必需在开头处使用<!DOCTYPE>标签为所有的XHTML文档指定XHTML版本和类型，只有这样浏览器才能按指定的文档类型进行解析。
~~~
#### meta（元数据meta data）

元信息是关于数据的信息
meta提供有关``页面的元信息（meta-information）``，比如``针对搜索引擎和更新频度的描述和关键词``。

必需的属性

| 属性                                                         | 值        | 描述                                       |
| :----------------------------------------------------------- | :-------- | :----------------------------------------- |
| [content](https://www.w3school.com.cn/tags/tag_meta.asp#meta_prop_content) | some_text | 定义与 http-equiv 或 name 属性相关的元信息 |
可选的属性
| 属性                                                         | 值                                                           | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| [http-equiv](https://www.w3school.com.cn/tags/tag_meta.asp#meta_prop_http-equiv) | Content-Type、refresh、text/html;charset=UTF-8               | 把 content 属性``关联到 HTTP 头部``。                        |
| [name](https://www.w3school.com.cn/tags/tag_meta.asp#meta_prop_name) | author 作者 、description 描述、keywords 关键字、viewport  视图 | 把 content 属性``关联到一个名称。``                          |
| charset                                                      | UTF-8                                                        |                                                              |
| [scheme](https://www.w3school.com.cn/tags/tag_meta.asp#meta_prop_scheme) | some_text                                                    | 定义用于``翻译 content 属性值的格式。用于指定要用来翻译属性值的方案。`` |
content 属性始终要和 `name 属性或 http-equiv 属性一起使用`。
```html
// 每30秒钟刷新当前页面:
<meta http-equiv="refresh" content="30">
```
```html
// 模板
<head>
    <meta name="autor" content="">
    <meta name="keywords" content="">
    <meta name="description" content="">
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="refresh" content="0">
</head>
```
```html
<meta name="autor" content="作者名">
//meta:utf
<meta charset="UTF-8">
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8"> 
//  meta:compat
< meta http-equiv = "X-UA-Compatible" content ="IE=edge,chrome=1" />
//标记后面竟然出现了chrome这样的值，难道IE也可以模拟chrome了明白原来不是微软增强了IE，而是谷歌做了个外挂：Google Chrome Frame（谷歌内嵌浏览器框架GCF）。这个插件可以让用户的IE浏览器外观不变，但用户在浏览网页时，实际上使用的是Google Chrome浏览器内核，而且支持IE6、7、8等多个版本的IE浏览器
<meta http-equiv="X-UA-Compatible" content="IE=edge">
//这是个是IE8的专用标记,用来指定IE8浏览器去模拟某个特定版本的IE浏览器的渲染方式（比如人见人烦的IE6），以此来解决部分兼容问题，例如模拟IE7的具体方式如下：  
<meta http-equiv = "X-UA-Compatible" content = "IE=EmulateIE7" />
//让搜索引擎更好的抓取网页
<meta name="keywords" content="HTML,ASP,PHP,SQL">
<meta name="keywords" content="Bilibili,哔哩哔哩,哔哩哔哩动画,哔哩哔哩弹幕网">
// 设置网页的刷新时间 meta:redirect coontent="网页刷新时长"
<meta http-equiv="refresh" content="0">
<meta http-equiv="refresh" content="0; url=http://example.com">
//网页的相关描述
 <meta name="description" content="bilibili是国内知名的视频弹幕网站，这里有最及时的动漫新番，最棒的ACG氛围，最有创意的Up主。大家可以在这里找到许多欢乐。">
// 快捷键 meta:vp 
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
```html
<head>
    <meta charset="utf-8">
    <title>哔哩哔哩 (゜-゜)つロ 干杯~-bilibili</title>
    <meta name="description" content="bilibili是国内知名的视频弹幕网站，这里有最及时的动漫新番，最棒的ACG氛围，最有创意的Up主。大家可以在这里找到许多欢乐。">
    <meta name="keywords" content="Bilibili,哔哩哔哩,哔哩哔哩动画,哔哩哔哩弹幕网">
    <meta name="renderer" content="webkit">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="spm_prefix" content="333.851">
</head>
```
> [关于 < meta http-equiv = X-UA-Compatible content = IE=edge,chrome=1 />](https://blog.csdn.net/ccfxue/article/details/70739646)
字符

```html
<meta charset="UTF-8">
```
| 字符集编码方式 | 作用                                                         |
| -------------- | ------------------------------------------------------------ |
| utf-8          | 目前最常用的字符集编码方式(包含全世界所有国家需要用到的字符)。常用的字符集编码方式还有gbk和gb2312 |
| gb2312         | 简体中文                                                     |
| blg5           | 繁体中文                                                     |
| gbk            | 全部中文字符    是GB2312的扩展，加入对繁体字的支持，兼容GB2312 |
| ascii |  |
|HTML 空元素||

- HTML 空元素即为没有内容的HTML元素
- HTML空元素应该在开始标签中关闭
- 例如 `<br>`没有关闭标签  HTML空源的关闭方法是在开始标签中添加斜杠`<br/>`
- 注意：在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭，即使是空元素。

#### HTML常用标签

| 标签                   | 作用           |
| ---------------------- | -------------- |
| `<h1>~<h6>`            | 标题           |
| `<p>`                  | 段落           |
| `<a> anchor锚点`       | 链接           |
| `<img>`                | 图像           |
| `<hr/>`                | 水平线         |
| `<br/>`                | 换行           |
| 文本格式化标签         |                |
| `<b>、<strong>`        | 加粗、加重语气 |
| `<i>、<em>`            | 斜体、着重文字 |
| `sub` 、`sup`          | 下标、上标     |
| `pre`                  | 预格式文本     |
| `<small> <big>`        | 小号字、大号字 |
| `<ins>`                | 插入字         |
| `<del>`                | 删除字         |
| 计算机输出标签         |                |
| `<code>`               | 计算机代码     |
| `<cite>`               | 定义引用，引证 |
| `<kbd>`                | 键盘码         |
| `<samp>`               | 计算机代码样本 |
| `<var>`                | 变量           |
| `<pre>`                | 预格式文本     |
| 引文, 引用, 及标签定义 |                |
| `<abbr>`               | 缩写           |
| `<address>`            | 地址           |
| `<bdo dir="rtl">`      | 文字方向       |
| `<blockquote>`         | 长的引用       |
| `<q>`                  | 短的引用语     |
| `<cite>`               | 引用、引证     |
| `<dfn>`                | 定义项目       |
| `<kbd>`                | 计算机代码     |
```html
<p><bdo dir="rtl">该段落文字从右到左显示。</bdo></p>
// dir="ltr/rtl"  必需。规定 <bdo> 元素内的文本方向。
```
p 标签 当渲染这些代码的时候，HTML 解释器会将连续出现的空格字符减少为一个单独的空格符。
```html
// 两个代码片段是等价
<p>狗 狗 很 呆 萌。</p>
<p>狗 狗        很
       呆 萌。</p>
```
`b` 和 `strong` 与 `i`和 `em`的区别
> `<strong> `或者 `<em>`意味着你要呈现的文本是重要的，所以要突出显示。现今所有主要浏览器都能渲染各种效果的字体。不过，未来浏览器可能会支持更好的渲染效果。
#### HTML中的H1-H6字体大小
> - h1 { font-size: 24px;}
> - h2 { font-size: 22px;}
> - h3 { font-size: 18px;}
> - h4 { font-size: 16px;}
> - h5 { font-size: 12px;}
> - h6 { font-size: 10px;}
## 区块
> [块级元素和内联元素区别](https://blog.csdn.net/chen_zw/article/details/8713205)

|          | 元素特性                                                     | 主要有                                                       |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 块级元素 | 总 是独占一行，表现为另起一行开始，而且其后的元素也必须另起一行显示; width 、height、padding、margin都可控制; | `div、h1-h6、ul、ol、li、dl、table、p、hr、form`、(address , blockquote , center , dir , div , dl , fieldset , form , h1 , h2 , h3 , h4 , h5 , h6 , hr , isindex , menu , noframes , noscript , ol , p , pre , table , ul , li) |
| 内联元素 | 和相邻的内联元素在同一行; width、height、padding-top/padding-bottom、margin-top/margin-bottom都不可改变，就是里面文字或图片的大小; | `span、a、img、input、textarea、label、select ` 、(a , abbr , acronym , b , bdo , big , br , cite , code , dfn , em , font , i , img , input , kbd , label , q , s , samp , select , small , span , strike , strong , sub , sup ,  textarea , tt , u , var) |
## 链接

链接（hyperlink）是互联网的核心。它允许用户在页面上，从一个网址跳转到另一个网址，从而把所有资源联系在一起。HTML 使用超级链接与网络上的另一个文档相连。几乎可以在所有的网页中找到链接。点击链接可以从一张页面跳转到另一张页面。

URL 是链接指向的地址。链接不仅可以指向另一个网页，也可以指向文本、图像、文件等资源。可以这样说，所有互联网上的资源，都可以通过链接访问

- 一个未访问过的链接显示为蓝色字体并带有下划线。

- 访问过的链接显示为紫色并带有下划线。

- 点击链接时，链接显示为红色并带有下划线。

超链接种类

- 空链接
```html
<a href="#">
<a href="javascript:;">    
```
- 图片链接 
```html
<a href="">
<img  border="10" src="" alt="HTML 教程" width="32" height="32">
</a>
```
- 文字链接
```html
<a href="url">链接文本</a>
```
- 邮件链接 `mailto`
```html
<a href="mailto:someone@example.com?Subject=Hello%20again" target="_top">
<a href="mailto:contact@example.com">联系我们</a>
subject：主题
cc：抄送
bcc：密送
body：邮件内容
```
`a:target:`

`_blank 新窗口`

` _parent 用于从父窗口打开的子窗口 当前窗口 _self  当前窗口 _top 顶层窗口`  

| 属性                                                        | 值                                                           | 描述                                                         |
| ----------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| href                                                        | *URL* :mailto :tel                                           | 规定链接的目标 URL。                                         |
| hreflang                                                    |                                                              | `hreflang`属性给出链接指向的网址所使用的语言，纯粹是提示性的，没有实际功能。 |
| title                                                       |                                                              | 给出链接的说明信息。鼠标悬停在链接上方时，浏览器会将这个属性的值，以提示块的形式显示出来 |
| target                                                      | `_blank(新窗口)`<br/>`_parent`上层窗口打开，这通常用于从父窗口打开的子窗口，或者`<iframe>`里面的链接。如果当前窗口没有上层窗口，这个值等同于`_self`<br/>`_self`(当前窗口 默认值)<br/>`_top`（顶层窗口打开。如果当前窗口就是顶层窗口，这个值等同于`_self`）<br/>*framename* | 使用 target 属性，你可以定义被链接的文档在何处显示。         |
| id                                                          | id 值搭配href                                                | id属性可用于创建在一个HTML文档书签标记。                     |
| download                                                    | filename                                                     | 指定下载链接                                                 |
| [hreflang](https://www.runoob.com/tags/att-a-hreflang.html) | *language_code*                                              | 规定目标 URL 的基准语言。仅在 href 属性存在时使用。          |
| [rel](https://www.runoob.com/tags/att-a-rel.html)           | alternate author bookmark help license next nofollow noreferrer prefetch prev search tag | 规定当前文档与目标 URL 之间的关系。仅在 href 属性存在时使 说明链接与当前页面的关系 |
| type                                                        | *MIME_type*                                                  | 规定目标 URL 的 MIME 类型。仅在 href 属性存在时使用。 注：MIME = Multipurpose Internet Mail Extensions。性给出链接 URL 的 MIME 类型，比如到底是网页，还是图像或文件。它也是纯粹提示性的属性，没有实际功能 |
| ping                                                        |                                                              | 属性指定一个网址，用户点击的时候，会向该网址发出一个 POST 请求，通常用于跟踪用户的行为 |
| referrerpolicy                                              |                                                              | 属性用于精确设定点击链接时，浏览器发送 HTTP 头信息的`Referer`字段的行为。 |
```html
<a href="" title="" target="" id="" download="" rel="" type="" ping=""></a>
```

电话链接 `tel`

```
<a href="tel:13312345678">13312345678</a>
```

HTML5 不支持

| 属性                                                    | 值                       | 描述                                |
| :------------------------------------------------------ | :----------------------- | :---------------------------------- |
| charset                                                 | *char_encoding*          | 规定目标 URL 的字符编码。           |
| [coords](https://www.runoob.com/tags/att-a-coords.html) | *coordinates*            | 规定链接的坐标。                    |
| [name](https://www.runoob.com/tags/att-a-name.html)     | *section_name*           | 规定锚的名称。                      |
| [rev](https://www.runoob.com/tags/att-a-rev.html)       | *text*                   | 规定目标 URL 与当前文档之间的关系。 |
| [shape](https://www.runoob.com/tags/att-a-shape.html)   | default rect circle poly | 规定链接的形状。                    |
a 链接 id 的使用
```html
// 同一页面
<a id="tips">有用的提示部分</a>
<a href="#tips">访问有用的提示部分</a>
// 不同页面
<a id="tips">有用的提示部分</a>
<a href="hello.html#tips">访问有用的提示部分</a>
```
## 样式

HTML 样式标签
| 标签    | 描述             |
| :------ | :--------------- |
| `style` | 定义文本样式     |
| `link`  | 定义资源引用地址 |
```html
<p style="color:blue;margin-left:20px;">这是一个段落。</p>
```
内部样式
```html
<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
</style>
```
外部样式
```html
<link rel="stylesheet" type="text/css" href="mystyle.css">
```


```html
// rel （rel="alternate stylesheet"），默认不生效
<link href="fancy.css" rel="alternate stylesheet" title="Fancy">

// 加载网站的 favicon 图标文件
<link rel="icon" href="/favicon.ico" type="image/x-icon">

// 手机访问时，网站通常需要提供不同分辨率的图标文件。
<link rel="apple-touch-icon-precomposed" sizes="114x114" href="favicon114.png">
<link rel="apple-touch-icon-precomposed" sizes="72x72" href="favicon72.png">

// 文档 文档的 RSS Feed 地址
<link rel="alternate" type="application/atom+xml" href="/blog/news/atom">

// rel属性表示外部资源与当前文档之间的关系，是<link>标签的必需属性。它可以但不限于取以下值。
```

资源的预加载

- `<link rel="preload">`
- `<link rel="prefetch">`
- `<link rel="preconnect">`
- `<link rel="dns-prefetch">`
- `<link rel="prerender">`

media属性

```html
<link href="print.css" rel="stylesheet" media="print">
<link href="mobile.css" rel="stylesheet" media="screen and (max-width: 600px)">
<link rel="preload" as="image" href="map.png" media="(max-width: 600px)">
<link rel="preload" as="script" href="map.js" media="(min-width: 601px)">
```

## 列表

HTML 列表标签
| 标签               | 描述                 |
| :----------------- | :------------------- |
| `<ol>`             | 定义有序列表         |
| `<ul>`             | 定义无序列表         |
| `<li>`             | 定义列表项           |
| `<dl>` list        | 定义列表             |
| `<dt>` title       | 自定义列表项目       |
| `<dd>` description | 定义自定列表项的描述 |
HTML 支持有序、无序和定义列表:
```html
<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>
```
```html
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
```
`dl => list  dd => dd  dt=> title`
<dl> 
<dt>Coffee</dt>
<dd>black hot drink</dd>
<dd>black hot drink</dd>
<dt>Milk</dt>
<dd>white cold drink</dd>
<dd>black hot drink</dd>    
</dl>
```html
<dl> 
<dt>Coffee</dt>
<dd>- black hot drink</dd>
<dt>Milk</dt>
<dd>- white cold drink</dd>
</dl>
```
## 图片
HTML 图像
`<img>` 是空标签，意思是说，它只包含属性，并且没有闭合标签
| 标签 | 描述                       |
| :--- | :------------------------- |
| img  | 定义图像                   |
| map  | 定义图像地图               |
| area | 定义图像地图中的可点击区域 |

| 标签            | 描述                                                         |
| :-------------- | :----------------------------------------------------------- |
| src             | source 源属性的值是图像的 URL 地址                           |
| alt             | 为图像定义一串预备的可替换的文本                             |
| width 和 height | 宽度和高度                                                   |
| align           | 设置图片对齐方式                                             |
| srcset 和 sizes | `srcset`属性和`sizes`属性分别解决了像素密度和屏幕大小的适配  |
| referrerpolicy  | `<img>`导致的图片加载的 HTTP 请求，默认会带有Referer的头信息。referrerpolicy属性对这个行为进行设置。 |
| crossorigin     | 有时，图片和网页属于不同的网站，网页加载图片就会导致跨域请求，对方服务器可能要求跨域认证。`crossorigin`属性用来告诉浏览器，是否采用跨域的形式下载图片，默认是不采用。简单说，只要打开了这个属性，HTTP 请求的头信息里面，就会加入`origin`字段，给出请求发出的域名，不打开这个属性就不加。 |
| loading         | `懒加载` auto 、lazy、eager 浏览器的默认行为是，只要解析到`<img>`标签，就开始加载图片。对于很长的网页，这样做很浪费带宽，因为用户不一定会往下滚动，一直看到网页结束。用户很可能是点开网页，看了一会就关掉了，那些不在视口的图片加载的流量，就都浪费了。`loading`属性改变了这个行为，可以指定图片的懒加载，即图片默认不加载，只有即将滚动进入视口，变成用户可见时才会加载，这样就节省了带宽。 |

```html
<img src="foo.jpg" crossorigin="anonymous">
// crossorigin属性如果省略值的部分，则等同于anonymous。

// anonymous：跨域请求不带有用户凭证（通常是 Cookie）。
// use-credentials：跨域请求带有用户凭证。

<img src="image.png" loading="lazy" alt="…" width="200" height="200">
// loading属性可以取以下三个值。

// auto：浏览器默认行为，等同于不使用loading属性。
// lazy：启用懒加载。
// eager：立即加载资源，无论它在页面上的哪个位置。

// 由于行内图片的懒加载，可能会导致页面布局重排，所以使用这个属性的时候，最好指定图片的高和宽。
```

`figure  figcaption`

`<figure>`标签可以理解为一个图像区块，将图像和相关信息封装在一起。`<figcaption>`是它的可选子元素，表示图像的文本描述，通常用于放置标题，可以出现多个。

```html
<figure>
  <img src="https://example.com/foo.jpg">
  <figcaption>示例图片</figcaption>
</figure>
```

<figure>
  <img src="https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png">
  <figcaption>示例图片</figcaption>
</figure>

图库图片

```html
<img src="https://gitee.com/heweiliang/FigureBed/raw/master/11~20.png">
// 图片默认以原始大小插入网页，width属性和height属性可以指定图片显示时的宽度和高度，单位是像素或百分比。
```
```html
<img src="https://api.sunweihu.com/api/bing1/api.php" width="auto" height="auto">
```
<img src="https://api.sunweihu.com/api/bing1/api.php" width="auto" height="auto" >

<img src="https://api.sunweihu.com/api/bing1/api.php" style="zoom:30%;" >

```html
<img src="https://gitee.com/heweiliang/FigureBed/raw/master/12.png" align="center" width="500px">
```
<img src="https://gitee.com/heweiliang/FigureBed/raw/master/12.png" align="center" width="500px">

压缩方式

- Base64图片
- 图片压缩模式
- 精灵图、雪碧图

使用方法

响应式图片

```html
<img src="foo.jpg">
```

上面代码的弊端

- 体积
- 像素密度：桌面显示器一般是单倍像素密度，而手机的显示屏往往是多倍像素密度
- 视觉风格

解决方法

- `<srcset>属性`：指定``多张图像，适应不同像素密度的屏幕``。它的值是一个逗号分隔的字符串，每个部分都是一张图像的 URL，后面接一个空格，然后是像素密度的描述符。

```html
<img srcset="foo-320w.jpg,
             foo-480w.jpg 1.5x,
             foo-640w.jpg 2x"
     src="foo-640w.jpg">
// 图像 URL 后面的像素密度描述符，格式是像素密度倍数 + 字母x。1x表示单倍像素密度，可以省略。浏览器根据当前设备的像素密度，选择需要加载的图像。
```

- `<sizes>属性`:像素密度的适配，只适合显示区域一样大小的图像。如果希望不同尺寸的屏幕，显示不同大小的图像，`srcset`属性就不够用了，必须搭配`sizes`属性。

```html
<img srcset="foo-160.jpg 160w,
             foo-320.jpg 320w,
             foo-640.jpg 640w,
             foo-1280.jpg 1280w"
     sizes="(max-width: 440px) 100vw,
            (max-width: 900px) 33vw,
            254px"
     src="foo-1280.jpg">
```

- `<picture>`

```html
<picture>
  <source srcset="homepage-person@desktop.png,
                  homepage-person@desktop-2x.png 2x"
          media="(min-width: 990px)">
  <source srcset="homepage-person@tablet.png,
                  homepage-person@tablet-2x.png 2x"
          media="(min-width: 750px)">
  <img srcset="homepage-person@mobile.png,
               homepage-person@mobile-2x.png 2x"
       alt="Shopify Merchant, Corrine Anestopoulos">
</picture>
```

- ​	格式

	```html
	<picture>
	  <source type="image/svg+xml" srcset="logo.xml">
	  <source type="image/webp" srcset="logo.webp"> 
	  <img src="logo.png" alt="ACME Corp">
	</picture>
	```

## 表格

概念
- 标题 `caption`
- 行 `row`
- 列 `col`
- 单元格
- `<colgroup>` 和 `<col>` 设置样式
- `align`对齐方式
- `dir`
| 标签                 | 描述         |
| -------------------- | ------------ |
| `<table>`            | 表格         |
| tr td th             |              |
| `<tr>`               | `row`行      |
| `<td>`               | 表格单元     |
| `<th>`               | `head`表头   |
| thread tbody tfoot   |              |
| `<thread>`           | 表格的页眉   |
| `<tbody>`            | 表格的主体   |
| `<tfoot>`            | 表格的页脚   |
| caption colgroup col |              |
| `<caption>`          | 表格的标题   |
| `<colgroup>`         | 表格列的组   |
| `<col>`              | 表格列的属性 |
表格
- x 为 行 row，y 为列 column
- 没有边框的表格 `<table border="0">` 或者 CSS`table:{border:0;}`
- 水平标题或者垂直标题
	- 水平标题 `<tr><th> + <tr><td>`
	- 垂直标题 `<tr><th><td></tr>`
- 单元格内可以添加其他标签
- 合并单元格 ：跨行`rowspan="跨行数"`或跨列`colspan="跨列数"`的表格单元格 
- 带标题的表格`caption`
- 单元格边距（Cell padding）`cellpadding="0"`  单元格边框与单元格内容之间的空间，（单元格里面的）
- 单元格间距（Cell spacing）`cellspacing="0"`表格单元格之间的空间（单元格与单元格之间的）

```html
<table border="1" cellpadding="0" cellspacing="0">
        <caption>标题</caption>
        <colgroup>
            <col span="2" style="background:pink">
            <col style="background-color:yellow">
        </colgroup>
        <tr>
            <th>1</th>
            <th colspan="2">2</th>
        </tr>
        <tr>
            <td rowspan="3">1</td>
            <td>2</td>
            <td>3</td>
        </tr>
        <tr>
            <td>2</td>
            <td>3</td>
        </tr>
        <tr>
            <td>1</td>
            <td colspan="2">2</td>
        </tr>
        <tr>
            <td>1</td>
            <td>2</td>
            <td>3</td>
        </tr>
    </table>
```

<table border="1" cellpadding="0" cellspacing="0">
        <caption>标题</caption>
        <colgroup>
            <col span="2" style="background:pink">
            <col style="background-color:yellow">
        </colgroup>
        <tr>
            <th>1</th>
            <th colspan="2">2</th>
        </tr>
        <tr>
            <td rowspan="3">1</td>
            <td>2</td>
            <td>3</td>
        </tr>
        <tr>
            <td>2</td>
            <td>3</td>
        </tr>
        <tr>
            <td>1</td>
            <td colspan="2">2</td>
        </tr>
        <tr>
            <td>1</td>
            <td>2</td>
            <td>3</td>
        </tr>
    </table>
```html
<h4>水平标题:</h4>
<table border="1" cellpadding="0"  cellspacing="0">
<caption>标题</caption> //
<tr>
  <th>Name</th>
  <th colspan="2">Telephone</th>
</tr>
<tr>
  <td>Bill Gates</td>
  <td>555 77 854</td>
  <td>555 77 855</td>
</tr>
</table>
<h4>垂直标题:</h4>
<table border="1">
<tr>
  <th>First Name:</th>
  <td>Bill Gates</td> 
  <td>Bill Gates</td>
</tr>
<tr>
  <th rowspan="2">Telephone:</th>
  <td>555 77 854</td>
  <td>555 77 854</td>  
</tr>
<tr>
  <td>555 77 855</td>
   <td>555 77 855</td>
</tr>
</table>
```
> `<thread> 、 <tbody> 和 <tfont>` 表头、主体、页脚
>
> 通过使用这些元素，使浏览器有能力支持独立于表格表头和表格页脚的表格主体滚动。`当包含多个页面的长的表格被打印时，表格的表头和页脚可被打印在包含表格数据的每张页面上`。
```html
<table border="1">
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
    </tr>
  </tbody>
</table>
```
> `<colgroup>` 表格列的组  和 `<col> `表格列的属性
```html
<table border="1">
  <colgroup>
    <col span="2" style="background-color:red">
    <col style="background-color:yellow">
  </colgroup>
  <tr>
    <th>ISBN</th>
    <th>Title</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>3476896</td>
    <td>My first HTML</td>
    <td>$53</td>
  </tr>
</table>
```
HTML 5 不推荐使用`bgcolor`、`background`、`bordercolor`

## 表单

HTML表单用于收集不同类型的用户输入

表单组成

- 表单域 `form`
- 提示信息`label`
- 表单控件（表单元素）`input、select、textarea`
	- 输入框 ``input ``
	- 下拉菜单 `select` 
	- 文本域 `textarea`

| 标签         | 属性                                                         | 描述                                    |
| ------------ | ------------------------------------------------------------ | --------------------------------------- |
| `<form>`     | action=“URL”(规定当提交表单时向何处发送表单数据。)<br/>name(名称)、<br/>method(get、post)(规定用于发送表单数据的 HTTP 方法)、<br/>target（`_black、_self、_parent、_top`）、<br/>enctype （`application/x-www-form-urlencoded、multipart/form-data、text/plain`)(规定在向服务器发送表单数据之前如何对其进行编码。（适用于 method="post" 的情况）)<br/>accept="*MIME_type*"(HTML5 不支持。规定服务器接收到的文件的类型。（文件是通过文件上传提交的）)<br/>navalidate="navalidate"(如果使用该属性，则提交表单时不进行验证。)<br/>accept-charset(规定服务器可处理的表单数据字符集。)<br/>autocomplete="on/off"(规定是否启用表单的自动完成功能。) | 用户输入的表单                          |
| `<input>`    | type="text(文本域)/password(密码)/radio(单选按钮)/checkbox(复选框)/submit(提交按钮)/button(按钮)/reset(重置按钮)/file(文件上传)email(电子邮箱)" | 输入域                                  |
| `<textarea>` | name（名称）、rows="10"(文本区域内可见的行数。)、cols="30"(文本区域内可见的宽度)、maxlength(规定文本区域允许的最大字符数)、disabled="disabled"(规定禁用文本区域)、readonly | 文本域                                  |
| `<label>`    | for="element_id"(规定 label 与哪个表单元素绑定)、<br/>form="form_id"(规定 label 字段所属的一个或多个表单。) | 定义了`input`元素的标签，一般输入为标题 |
| `<filedset>` |                                                              | 一组相关的表单元素，并使用外框包含起来  |
| `<legend>`   |                                                              | `filedset`元素的标题                    |
| `<select>`   | option、optgroup                                             | 下拉选项列表                            |
| `<optgroup>` |                                                              | 选项组                                  |
| `<option>`   |                                                              | 下拉列表中的选项                        |
| `<button>`   | name(名称)、type="button/reset/submit"(按钮类型)、value(按钮的初始值，可由脚本修改) | 定义一个点击按钮                        |
| `<datalist>` |                                                              | 指定一个预先定义的输入控件选项列表      |
| `<keygen>`   | 从web标准中删除                                              | 定义了表单的密钥对生成器字段            |
| `<output>`   |                                                              | 定义一个计算结果                        |


### form

| 属性                                                         | 值                                                           | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| [accept](https://www.runoob.com/tags/att-form-accept.html)   | *MIME_type*                                                  | HTML5 不支持。规定服务器接收到的文件的类型。（文件是通过文件上传提交的） |
| [accept-charset](https://www.runoob.com/tags/att-form-accept-charset.html) | *character_set*                                              | 规定服务器可处理的表单数据字符集。                           |
| [action](https://www.runoob.com/tags/att-form-action.html)   | *URL*                                                        | 规定当提交表单时向何处发送表单数据。                         |
| [autocomplete](https://www.runoob.com/tags/att-form-autocomplete.html)**New** | on off                                                       | 规定是否启用表单的自动完成功能。                             |
| [enctype](https://www.runoob.com/tags/att-form-enctype.html) | application/x-www-form-urlencoded multipart/form-data text/plain | 规定在向服务器发送表单数据之前如何对其进行编码。（适用于 method="post" 的情况） |
| [method](https://www.runoob.com/tags/att-form-method.html)   | get post                                                     | 规定用于发送表单数据的 HTTP 方法。                           |
| [name](https://www.runoob.com/tags/att-form-name.html)       | *text*                                                       | 规定表单的名称。                                             |
| [novalidate](https://www.runoob.com/tags/att-form-novalidate.html)**New** | novalidate                                                   | 如果使用该属性，则提交表单时不进行验证。                     |
| [target](https://www.runoob.com/tags/att-form-target.html)   | _blank _self _parent _top                                    | 规定在何处打开 action URL。                                  |
### input

> - button、checkbox、radio、submit、image
> - text、search、tel、url、password
> - color
> - date 年月日、datetime 年、月、日、时、分、datetime-local、date、time、month 月、week 周
> - emial
> - file
> - number
> - hidden

按钮、时间、颜色、文本域、文件上传

- button（按钮） 、checkbox（复选框） 、radio（单选框） 、reset、submit 、image (图像作为提交按钮)
- color （拾色器）
- date（date 控件（包括年、月、日，不包括时间）） 、datetime （ date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，基于 UTC 时区））、datetime-local （ date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，不带时区））、time（用于输入时间的控件（不带时区）） 、month ( month 和 year 控件（不带时区）)、week( week 和 year 控件（不带时区）)
- email 、search、tel 用于输入电话号码的字段、text 、 url、password 
- file (文件选择字段和 "浏览..." 按钮，供文件上传)
- hidden (隐藏输入字段)
- number (用于输入数字的字段)、range 用于精确值不重要的输入数字的控件（比如 slider 控件） 滑动控件

	- [max](https://www.runoob.com/tags/att-input-max.html) - 规定允许的最大值。
	- [min](https://www.runoob.com/tags/att-input-min.html) - 规定允许的最小值。
	- [step](https://www.runoob.com/tags/att-input-step.html) - 规定合法数字间隔。
	- [value](https://www.runoob.com/tags/att-input-value.html) - 规定默认值。

| 属性                                                         | 值                                                           | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| [accept](https://www.runoob.com/tags/att-input-accept.html)  | audio/* video/* image/* *MIME_type*                          | 规定通过文件上传来提交的文件的类型。 (只针对type="file")     |
| [align](https://www.runoob.com/tags/att-input-align.html)    | left right top middle bottom                                 | HTML5已废弃，不赞成使用。规定图像输入的对齐方式。 (只针对type="image") |
| [alt](https://www.runoob.com/tags/att-input-alt.html)        | *text*                                                       | 定义图像输入的替代文本。 (只针对type="image")                |
| [autocomplete](https://www.runoob.com/tags/att-input-autocomplete.html)**New** | on off                                                       | autocomplete 属性规定 <input> 元素输入字段是否应该启用自动完成功能。 |
| [autofocus](https://www.runoob.com/tags/att-input-autofocus.html)**New** | autofocus                                                    | 属性规定当页面加载时 <input> 元素应该自动获得焦点。          |
| [checked](https://www.runoob.com/tags/att-input-checked.html) | checked                                                      | checked 属性规定在页面加载时应该被预先选定的 <input> 元素。 (只针对 type="checkbox" 或者 type="radio") |
| [disabled](https://www.runoob.com/tags/att-input-disabled.html) | disabled                                                     | disabled 属性规定应该禁用的 <input> 元素。                   |
| [form](https://www.runoob.com/tags/att-input-form.html)**New** | *form_id*                                                    | form 属性规定 <input> 元素所属的一个或多个表单。             |
| [formaction](https://www.runoob.com/tags/att-input-formaction.html)**New** | *URL*                                                        | 属性规定当表单提交时处理输入控件的文件的 URL。(只针对 type="submit" 和 type="image") |
| [formenctype](https://www.runoob.com/tags/att-input-formenctype.html)**New** | application/x-www-form-urlencoded multipart/form-data text/plain | 属性规定当表单数据提交到服务器时如何编码(只适合 type="submit" 和 type="image")。 |
| [formmethod](https://www.runoob.com/tags/att-input-formmethod.html)**New** | get post                                                     | 定义发送表单数据到 action URL 的 HTTP 方法。 (只适合 type="submit" 和 type="image") |
| [formnovalidate](https://www.runoob.com/tags/att-input-formnovalidate.html)**New** | formnovalidate                                               | formnovalidate 属性覆盖 <form> 元素的 novalidate 属性。      |
| [formtarget](https://www.runoob.com/tags/att-input-formtarget.html)**New** | _blank _self _parent _top *framename*                        | 规定表示提交表单后在哪里显示接收到响应的名称或关键词。(只适合 type="submit" 和 type="image") |
| [height](https://www.runoob.com/tags/att-input-height.html)**New** | *pixels*                                                     | 规定 <input>元素的高度。(只针对type="image")                 |
| [list](https://www.runoob.com/tags/att-input-list.html)**New** | *datalist_id*                                                | 属性引用 <datalist> 元素，其中包含 <input> 元素的预定义选项。 |
| [max](https://www.runoob.com/tags/att-input-max.html)**New** | *number date*                                                | 属性规定 <input> 元素的最大值。                              |
| [maxlength](https://www.runoob.com/tags/att-input-maxlength.html) | *number*                                                     | 属性规定 <input> 元素中允许的最大字符数。                    |
| [min](https://www.runoob.com/tags/att-input-min.html)**New** | *number date*                                                | 属性规定 <input>元素的最小值。                               |
| [multiple](https://www.runoob.com/tags/att-input-multiple.html)**New** | multiple                                                     | 属性规定允许用户输入到 <input> 元素的多个值。                |
| [name](https://www.runoob.com/tags/att-input-name.html)      | *text*                                                       | name 属性规定 <input> 元素的名称。                           |
| [pattern](https://www.runoob.com/tags/att-input-pattern.html)**New** | *regexp*                                                     | pattern 属性规定用于验证 <input> 元素的值的正则表达式。      |
| [placeholder](https://www.runoob.com/tags/att-input-placeholder.html)**New** | *text*                                                       | placeholder 属性规定可描述输入 <input> 字段预期值的简短的提示信息 。 |
| [readonly](https://www.runoob.com/tags/att-input-readonly.html) | readonly                                                     | readonly 属性规定输入字段是只读的。                          |
| [required](https://www.runoob.com/tags/att-input-required.html)**New** | required                                                     | 属性规定必需在提交表单之前填写输入字段。                     |
| [size](https://www.runoob.com/tags/att-input-size.html)      | *number*                                                     | size 属性规定以字符数计的 <input> 元素的可见宽度。           |
| [src](https://www.runoob.com/tags/att-input-src.html)        | *URL*                                                        | src 属性规定显示为提交按钮的图像的 URL。 (只针对 type="image") |
| [step](https://www.runoob.com/tags/att-input-step.html)**New** | *number*                                                     | step 属性规定 <input> 元素的合法数字间隔。                   |
| [type](https://www.runoob.com/tags/att-input-type.html)      | button checkbox color date datetime datetime-local email file hidden image month number password radio range reset search submit tel text time url week | type 属性规定要显示的 <input> 元素的类型。                   |
| [value](https://www.runoob.com/tags/att-input-value.html)    | *text*                                                       | 指定 <input> 元素 value 的值。                               |
| [width](https://www.runoob.com/tags/att-input-width.html)**New** | *pixels*                                                     | width 属性规定 <input> 元素的宽度。 (只针对type="image")     |
### textarea
| 属性                                                         | 值        | 描述                                             |
| :----------------------------------------------------------- | :-------- | :----------------------------------------------- |
| [autofocus](https://www.runoob.com/tags/att-textarea-autofocus.html)**New** | autofocus | 规定当页面加载时，文本区域自动获得焦点。         |
| [cols](https://www.runoob.com/tags/att-textarea-cols.html)   | *number*  | 规定文本区域内可见的宽度。                       |
| [disabled](https://www.runoob.com/tags/att-textarea-disabled.html) | disabled  | 规定禁用文本区域。                               |
| [form](https://www.runoob.com/tags/att-textarea-form.html)**New** | *form_id* | 定义文本区域所属的一个或多个表单。               |
| [maxlength](https://www.runoob.com/tags/att-textarea-maxlength.html)**New** | *number*  | 规定文本区域允许的最大字符数。                   |
| [name](https://www.runoob.com/tags/att-textarea-name.html)   | *text*    | 规定文本区域的名称。                             |
| [placeholder](https://www.runoob.com/tags/att-textarea-placeholder.html)**New** | *text*    | 规定一个简短的提示，描述文本区域期望的输入值。   |
| [readonly](https://www.runoob.com/tags/att-textarea-readonly.html) | readonly  | 规定文本区域为只读。                             |
| [required](https://www.runoob.com/tags/att-textarea-required.html)**New** | required  | 规定文本区域是必需的/必填的。                    |
| [rows](https://www.runoob.com/tags/att-textarea-rows.html)   | *number*  | 规定文本区域内可见的行数。                       |
| [wrap](https://www.runoob.com/tags/att-textarea-wrap.html)**New** | hard soft | 规定当提交表单时，文本区域中的文本应该怎样换行。 |
<textarea id="story" name="story"
          rows="5" cols="33">
这是一个很长的故事。
</textarea>

### select、optgroup、option

#### select

| 属性                                                         | 值        | 描述                                               |
| :----------------------------------------------------------- | :-------- | :------------------------------------------------- |
| [autofocus](https://www.runoob.com/tags/att-select-autofocus.html)**New** | autofocus | 规定在页面加载时下拉列表自动获得焦点。             |
| [disabled](https://www.runoob.com/tags/att-select-disabled.html) | disabled  | 当该属性为 true 时，会禁用下拉列表。               |
| [form](https://www.runoob.com/tags/att-select-form.html)**New** | *form_id* | 定义 select 字段所属的一个或多个表单。             |
| [multiple](https://www.runoob.com/tags/att-select-multiple.html) | multiple  | 当该属性为 true 时，可选择多个选项。               |
| [name](https://www.runoob.com/tags/att-select-name.html)     | *text*    | 定义下拉列表的名称。                               |
| [required](https://www.runoob.com/tags/att-select-required.html)**New** | required  | 规定用户在提交表单前必须选择一个下拉列表中的选项。 |
| [size](https://www.runoob.com/tags/att-select-size.html)     | *number*  | 规定下拉列表中可见选项的数目。                     |
#### optgroup

| 属性                                                         | 值       | 描述               |
| :----------------------------------------------------------- | :------- | :----------------- |
| [disabled](https://www.runoob.com/tags/att-optgroup-disabled.html) | disabled | 规定禁用该选项组。 |
| [label](https://www.runoob.com/tags/att-optgroup-label.html) | *text*   | 为选项组规定描述。 |
#### option

| 属性                                                         | 值       | 描述                                             |
| :----------------------------------------------------------- | :------- | :----------------------------------------------- |
| [disabled](https://www.runoob.com/tags/att-option-disabled.html) | disabled | 规定此选项应在首次加载时被禁用。                 |
| [label](https://www.runoob.com/tags/att-option-label.html)   | *text*   | 定义当使用 <optgroup> 时所使用的标注。           |
| [selected](https://www.runoob.com/tags/att-option-selected.html) | selected | 规定选项（在首次显示在列表中时）表现为选中状态。 |
| [value](https://www.runoob.com/tags/att-option-value.html)   | *text*   | 定义送往服务器的选项值。                         |
### button

| 属性                                                         | 值                                                           | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| [autofocus](https://www.runoob.com/tags/att-button-autofocus.html)**New** | autofocus                                                    | 规定当页面加载时按钮应当自动地获得焦点。                     |
| [disabled](https://www.runoob.com/tags/att-button-disabled.html) | disabled                                                     | 规定应该禁用该按钮。                                         |
| [form](https://www.runoob.com/tags/att-button-form.html)**New** | *form_id*                                                    | 规定按钮属于一个或多个表单。                                 |
| [formaction](https://www.runoob.com/tags/att-button-formaction.html)**New** | *URL*                                                        | 规定当提交表单时向何处发送表单数据。覆盖 form 元素的 action 属性。该属性与 type="submit" 配合使用。 |
| [formenctype](https://www.runoob.com/tags/att-button-formenctype.html)**New** | application/x-www-form-urlencoded multipart/form-data text/plain | 规定在向服务器发送表单数据之前如何对其进行编码。覆盖 form 元素的 enctype 属性。该属性与 type="submit" 配合使用。 |
| [formmethod](https://www.runoob.com/tags/att-button-formmethod.html)**New** | get post                                                     | 规定用于发送表单数据的 HTTP 方法。覆盖 form 元素的 method 属性。该属性与 type="submit" 配合使用。 |
| [formnovalidate](https://www.runoob.com/tags/att-button-formnovalidate.html)**New** | formnovalidate                                               | 如果使用该属性，则提交表单时不进行验证。覆盖 form 元素的 novalidate 属性。该属性与 type="submit" 配合使用。 |
| [formtarget](https://www.runoob.com/tags/att-button-formtarget.html)**New** | _blank _self _parent _top *framename*                        | 规定在何处打开 action URL。覆盖 form 元素的 target 属性。该属性与 type="submit" 配合使用。 |
| [name](https://www.runoob.com/tags/att-button-name.html)     | *name*                                                       | 规定按钮的名称。                                             |
| [type](https://www.runoob.com/tags/att-button-type.html)     | button reset submit                                          | 规定按钮的类型。                                             |
| [value](https://www.runoob.com/tags/att-button-value.html)   | *text*                                                       | 规定按钮的初始值。可由脚本进行修改。                         |
```html
// 单选按钮 和 复选框 都要设置相同的 name 和 value就是传递选中的值
通过name 分组不同的单选按钮组 或者 多选按钮组
单选按钮(Radio Buttons) 
<form>
<input type="radio" name="sex" value="male">Male<br>
<input type="radio" name="sex" value="female">Female
</form>
// 复选框(Checkboxes)
<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car
</form>
// 定义提交按钮(Submit Button) 当用户单击确定按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的数据进行。
<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>
下拉菜单 select option
<form action="">
<select name="cars">
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
    <option value="fiat" selected>Fiat</option>
    <option value="audi">Audi</option>
</select>
</form>
label 的使用
<form action="demo_form.php">
  <label for="male">Male</label>
  <input type="radio" name="sex" id="male" value="male"><br>
  <label for="female">Female</label>
  <input type="radio" name="sex" id="female" value="female"><br><br>
  <input type="submit" value="提交">
</form>
文本域
<textarea rows="10" cols="30">
我是一个文本框。
</textarea>
选项组
<select>
  <optgroup label="Swedish Cars">
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
  </optgroup>
  <optgroup label="German Cars">
    <option value="mercedes">Mercedes</option>
    <option value="audi">Audi</option>
  </optgroup>
</select>
<datalist> 标签规定了 <input> 元素可能的选项列表
<form action="demo-form.php" method="get">
<input list="browsers" name="browser">
<datalist id="browsers">
  <option value="Internet Explorer">
  <option value="Firefox">
  <option value="Chrome">
  <option value="Opera">
  <option value="Safari">
</datalist>
<input type="submit">
</form>
```
> `<button>` 和 `input:button` 和`input:submit`的区别：
>
> `<button> `标签定义一个按钮。
>
> 在 `<button> `元素内部，您可以放置内容，比如文本或图像。这是该元素与使用 `<input> `元素创建的按钮之间的不同之处。
>
> **提示：**请始终为 `<button>` 元素规定 type 属性。不同的浏览器对` <button> `元素的 type 属性使用不同的默认值。
## 框架

`iframe 语法`
- `<iframe> `标签规定一个内联框架。
- 一个内联框架被用来在当前6 HTML 文档中嵌入另一个文档。
<iframe src="https://www.baidu.com/" height="500px" frameborder="0" seamless="seamless"></iframe>
```html
<iframe src="https://www.bing.com/" height="500px" frameborder="0" seamless="seamless"></iframe>
```
<iframe src="https://www.bing.com/" height="500px" frameborder="0" seamless="seamless"></iframe>
```html
<iframe src="URL"></iframe>
```
所有主流浏览器都支持 `<iframe> `标签。
使用`iframe` 来显示目标链接页面
```html
<iframe src="https://www.bing.com/" name="myiframe"></iframe>
<a href="https://www.baidu.com/" target="myiframe">
// iframe中name 和 a中target 属性
```
常用的值
> - name 名字 src 文档的url
> - 设置高度和宽度 `width` 和 `height`
> - 移除边框: `frameborder="0"`
> - `scrolling `  去除滚动条
| 属性            | 值                                                           | 描述                                                         |
| --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| name            | name                                                         | 名称                                                         |
| title           |                                                              |                                                              |
| sandbox         |                                                              | 嵌入的网页默认具有正常权限，比如执行脚本、提交表单、弹出窗口等。如果嵌入的网页是其他网站的页面，你不了解对方会执行什么操作，因此就存在安全风险。为了限制`<iframe>`的风险，HTML 提供了`sandbox`属性，允许设置嵌入的网页的权限，等同于提供了一个隔离层，即“沙箱”。 |
| loading         |                                                              | 懒加载                                                       |
| class           |                                                              |                                                              |
| id              |                                                              |                                                              |
| height 和 width | *pixels*                                                     | 高度和宽度                                                   |
| src             | URL                                                          | 显示的文档的 URL                                             |
| sandbox         | ""<br/>allow-forms<br/>allow-same-origin<br/>allow-scripts<br/>allow-top-navigation | 对 `<iframe> `的内容定义一系列额外的限制。                   |
| seamless        | seamless                                                     | 规定 `<iframe>` 看起来像是父文档中的一部分。                 |

HTML5 不支持

| 属性                      | 值                              | 描述                                                         |
| ------------------------- | ------------------------------- | ------------------------------------------------------------ |
| align                     |                                 | HTML 4.01 已废弃。 规定如何根据周围的元素来对齐 `<iframe>`。 |
| frameborder               | 0、1                            | 是否显示 `<iframe>` 周围的边框。                             |
| longdesc                  | *URL                            | 一个页面，该页面包含了有关 `<iframe> `的较长描述。           |
| marginheight/ marginwidth | *pixels*                        | `<iframe> `的顶部和底部的边距、、规定 `<iframe>` 的顶部和底部的边距 |
| scrolling                 | yes（显示）、no（不显示）、auto | 是否在 `<iframe> `中显示滚动条                               |

`frameset标签` HTML5 不支持
`<frameset>标签`在一个页面中设置一个或多个框架，用`frameset`代替`body`，不能出现在`body`标签中

```html
<frameset> // 建立框架的标记，将在其中定义各个框架
    <frame src="menu.html"> // 指示框架显示内容URL地址
    <frame src="content.html">
</frameset>    
```
- 设置行列比例
- 设置边框
	- frameborder 设置边框
	- framespacing 修改边框粗细
	`frame`  
- 设置名字 name
- 设置滚动 
	- noresize 设置禁止用户拖拉框架大小 不允许用户更改其尺寸
	- scrolling 用于设置滚动条是否显示  设置滚动条是否显示
	`<frame>` 标签中我们使用name属性命名每个框架，而不是内容页面
```html
<frameset rows="20%,*" border="2" frameboder="1" framespacing="2" rows="20%,*">
	<frame name="title" src="title.html" noresize scrolling="no">
	<frameset cols="30%,*" border="4" frameboder="1" framespacing="4" >
    	<frame name="menu" src="menu.html">
        <frame name="content" src="content.html">
    </frameset>
</frameset>    
```
## 颜色
[RGB颜色对照表](https://tool.oschina.net/commons?type=3)
### 颜色的表示方法
- RGB 和 RGBA（Color RGBA）
- HSL 和 HSLA 
- 颜色名
- 颜色值（十六进制颜色(Color HEX)）
- 预定义/跨浏览器颜色名
### 十六进制颜色值（Color HEX）
组成：
范围
每种颜色的最小值是0（十六进制：#00）。最大值是255（十六进制：#FF）。
十六进制：0~F
> #000000  ~ #FFFFFF
>
> - 6位数字或者字母  6位十六进制颜色值
> - 不区分大小写
> - 可以使用3位数字**3位十六进制颜色值**
> - 三位数表示法为：#RGB，转换为6位数表示为：#RRGGBB
### RGBA
颜色 由红（R）、绿（G）、蓝 （B）混合而成
> Red-Green-Blue-Alpha **“alpha”** 通道，运行对颜色值设置透明度。
```css
color: rgba(red, green, blue, alpha);
H：Hue(色调)。0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值来指定颜色。取值为：0 - 360
S：Saturation(饱和度)。取值为：0.0% - 100.0%
L：Lightness(亮度)。取值为：0.0% - 100.0%
A：Alpha透明度。取值0~1之间。
```
### HSLA
```
hsla(hue, saturation, lightness, alpha)
```
常用颜色名和颜色值
| 颜色名 | 颜色名 | 颜色十六进制（Color HEX） | 颜色RGBA(Color RGB) | 颜色HSLA(Color) |
| ------ | ------ | ------------------------- | ------------------- | --------------- |
| 黑色   | black  | #000000                   | rgb(0,0,0)          |                 |
| 红色   | red    | #FF0000                   | rgb(255,0,0)        |                 |
| 绿色   | green  | \#00FF00                  | rgb(0,255,0)        |                 |
| 蓝色   | blue   | \#0000FF                  | rgb(0,0,255)        |                 |
| 黄色   | yellow | #FFFF00                   | rgb(255,255,0)      |                 |
| 青色   | cyan   | \#00FFFF                  | rgb(0,255,255)      |                 |
| 紫色   | purple | \#FF00FF                  | rgb(0,255,255)      |                 |
| 灰色   | gray   | #C0C0C0                   | rgb(192,192,192)    |                 |
| 白色   | white  | #FFFFFF                   | rgb(255,255,255)    |                 |


## 脚本
- `script` 定义JS脚本
- `<noscript> `定义不支持脚本浏览器的文本
```html
<script></script>
<noscript>抱歉，你的浏览器不支持 JavaScript!</noscript>
<script type="text/javascript" src="javascript.js"></script>
```
```js
// 设置ES6模块
<script type="moudle" src="main.js"></script>
<script nomodule src="fallback.js"></script>

async：该属性指定 JavaScript 代码为异步执行，不是造成阻塞效果，JavaScript 代码默认是同步执行。
defer：该属性指定 JavaScript 代码不是立即执行，而是页面解析完成后执行。
crossorigin：如果采用这个属性，就会采用跨域的方式加载外部脚本，即 HTTP 请求的头信息会加上origin字段。
integrity：给出外部脚本的哈希值，防止脚本被篡改。只有哈希值相符的外部脚本，才会执行。
nonce：一个密码随机数，由服务器在 HTTP 头信息里面给出，每次加载脚本都不一样。它相当于给出了内嵌脚本的白名单，只有在白名单内的脚本才能执行。
referrerpolicy：HTTP 请求的Referer字段的处理方法。
```

## 单位

长度单位
| 单位               | 描述         |
| ------------------ | ------------ |
| px                 | 像素         |
| em                 | 相对单位     |
| rem                | 相对根的单位 |
| %                  | 百分比       |
| pt                 |              |
| vh、vw、vmin、vmax | 视口单位     |
## 字符

[HTML特殊符号表](https://tool.chinaz.com/tools/htmlchar.aspx)
HTML 中的预留字符必须被替换为字符实体。
实体名称对大小敏感 

| 示结果 | 描述        | 实体名称            | 实体编号  |
| :----- | :---------- | :------------------ | :-------- |
|        | 空格        | `&nbsp;`            | `&#160;`  |
| <      | 小于号      | `&lt;`              | `&#60;`   |
| >      | 大于号      | `&gt;`              | `&#62;`   |
| &      | 和号        | `&amp;`             | `&#38;`   |
| "      | 引号        | `&quot;`            | `&#34;`   |
| '      | 撇号        | `&apos;` (IE不支持) | `&#39;`   |
| ￠     | 分          | `&cent;`            | `&#162;`  |
| £      | 镑          | `&pound;`           | `&#163;`  |
| ¥      | 人民币/日元 | `&yen;`             | `&#165;`  |
| €      | 欧元        | `&euro;`            | `&#8364;` |
| §      | 小节        | `&sect; `           | `&#167;`  |
| ©      | 版权        | `&copy;`            | `&#169;`  |
| ®      | 注册商标    | `&reg;`             | `&#174; ` |
| ™      | 商标        | `&trade;`           | `&#8482;` |
| ×      | 乘号        | `&times; `          | `&#215; ` |
| ÷      | 除号        | `&divide; `         | `&#247;`  |
## 技巧

```html
// 点击关闭窗口
<a href="javascript:top.window.close();">点击关闭窗口</a>
// 去除主页右面的滚动条
<body scroll="no">
<body style="overflow-y:hidden">    
// 不刷新页面的情况下刷新css    
// 网页自动刷新    
// refresh
<meta http=equive="refesh" content="3">
    <script>
    	function refeshMain(){
            document.location.reload()
        }
        setTimeout(refeshMain,2000)
    </script>    
// 网页标签icon   
<link rel="Shortcut Icon" href="favicon.icon">    
// 收藏夹显示出你的图标
<link rel="Bookmark" href="favicon icon">  
<inputstyle="imemode:disabled"> 关闭输入法    
<body oncontextmenu="window.event.returnVale=false" // 屏蔽鼠标右键
      onselectstart="return false" //取消选取
      onpaste="return false" // 不准粘贴
      oncopy="return false" // 防止复制
      oncut="return false" //防止剪切
      >
// 防止被人frame
if(top.location != self.location) top.location = self.locatio;
    // 网页不能被另存为
    <noscript>
        <iframe src="*.html"></iframe>
    </noscript>   
    // 查看网页源代码
    <input type="button" value="查看网页源代码" onclick="window.location = view-source:"+"http://www.baidu.com"">
// 去掉图片链接点击后,图片周围的虚线
<a href="#" onFocus="this.blur()">
	<img src="logo.jpg" border="0"/>
</a>
// 电子邮件处理提交表单
<form name="form" method="post" action="mailt***@**.com" enctype="text/plain">
<input type="submit">
</form>
//子窗口刷新父窗口
window.opener.location.reload()
// Enter 键可以让光标移动到下一个输入框
<input onkeydown="if(event.keyCode==13)event.keyCode=9">                
```
版权信息规范
`Copyright/© + [dates] + [author/owner]    `
- ©1995-2004 Macromedia, Inc. All rights reserved.
- ©2004 Microsoft Corporation. All rights reserved.
- Copyright © 2004 Adobe Systems Incorporated. All rights reserved.
- ©1995-2004 Eric A. and Kathryn S. Meyer. All Rights Reserved.
```html
<span style="font-family:arial;">Copyright &copy; </span>
```
# HTML5

> HTML 5与CSS 3权威指南 上册

## 基础

- 2012年正式推出 HTML5 (HTML的第五次重大修改) ,目前IE8也兼容HTML5的语法

| 版本      | 年份 |
| :-------- | :--- |
| HTML      | 1991 |
| HTML+     | 1993 |
| HTML 2.0  | 1995 |
| HTML 3.2  | 1997 |
| HTML 4.01 | 1999 |
| XHTML 1.0 | 2000 |
| HTML5     | 2012 |
| XHTML5    | 2013 |

### 新特性

- 完全支持 CSS3 
- 新元素 和 新属性
- 2D/3D 制图`canvas` 和 `svg`
- 多媒体 Video 和 Audio
- 表单元素 和 属性
- 本地存储、SQL数据、应用程序缓存
- Web 应用 （地理位置、拖放、Workers、SSE、WebSocket）

### 文档类型声明

- 文档类型声明，用来声明文件用的XHTML或HTML的版本

- `<!DOCTYPE>` 不是 HTML 标签。它为浏览器提供一项信息（声明），即 HTML 是用什么版本编写的。

#### 文档类型规范分类

> DTD文档类型定义，``是一个xml文档``。如果你不写DTD，哪么浏览器就用自身的方式去解析你的文档，这样在各个浏览器中显示可能会不一样。DTD定义了浏览器是用标准方式解析文档。因为文档类型是有W3C联盟制定的标准，浏览器均支持这些标准。 另外，html版本不同，所支持的标签也有所不同，有些被淘汰，有些新增加。如果不定义正确的DTD声明，你的CSS和有些标识可能不会生效。

| DTD          | 应用                                                         |
| ------------ | ------------------------------------------------------------ |
| Transitional | 要求宽松的DTD,允许使用HTML4.0的标识符但要符合XHTML的书写规范。 |
| Strict       | 不能使用任何表现层的标识和属性。                             |
| Frameset     | 专门针对框架页面使用的。                                     |

##### HTML5

```html
<!DOCTYPE html>
```

##### HTML 4.01

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
```

##### XHTML 1.0

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
```

### 浏览器支持情况

html5shiv 解决方案 兼容浏览器(让IE9以下版本兼容HTML5的方法)

> 使用 Sjoerd Visscher 创建的 "HTML5 Enabling JavaScript", " **shiv**" 来解决该问题

```html
// IE9 以下版本浏览器兼容HTML5的方法，使用本站的静态资源的html5shiv包：
// 代码是一个注释，作用是在 IE 浏览器的版本小于 IE9 时将读取 html5.js 文件，并解析它。
<!--[if lt IE 9]>
    <script src="http://cdn.static.runoob.com/libs/html5shiv/3.7/html5shiv.min.js"></script>
<![endif]-->
// 针对IE浏览器html5shiv 是比较好的解决方案。html5shiv主要解决HTML5提出的新的元素不被IE6-8识别，这些新元素不能作为父节点包裹子元素，并且不能应用CSS样式。载入后,初始化新标签的CSS。HTML5 定了 8 个新的 HTML 语义（semantic） 元素。所有这些元素都是 块级元素。为了能让旧版本的浏览器正确显示这些元素，你可以设置 CSS 的 display 属性值为 block:
<style>
    article,aside,dialog,footer,header,section,nav,figure,menu{
        display:block;
    }
<style>
```

HTML5 可以为添加新的标签元素

```html
 <mytag>这是一段文字</mytag>
// 新建了一个HTML的标签元素
mytag {
    display: block;
    background-color: pink;
    padding: 20px;
    font-size: 30px;
}
```

## 格式

```html
// 扩展符  .html
<!DOCTYPE html>  //HTML5 文档声明对象 DOCTYPE 声明 
<html>
<head>
<meta charset="utf-8"> // 指定字符编码
<title></title>
</head>
<body>
// 文档内容
</body>
<html>
```

## 结构

### 主体结构元素

#### article

- 代表文档、页面或应用程序中独立的、完整的、可以独自被外部引用的内容。它可以是一篇博客或报章杂志中的文章一篇论坛帖子、一段用户评论或一个独立的插件，或者其他任何独立的内容

```html
<article></article>
```

#### section

- section元素用来对页面中的内容进行分块，或者是对文章进行分段 一个section元素通常由内容即及其标题组成

- section元素并非一个普通的容器元素，当一个容器需要直接定义样式或通过脚本定义行为时，推荐使用div元素而非section

- session元素中的内容可以单独存储到数据库中或输出到word文档，标题部分位于它的内部，而不是它的前面 不推荐为没有标题的内容使用section 

section与article 

- 内容首先是一段独立的、完整的内容，因此使用article元素，通过section对文章进行分段它是一篇文章中的一段，因此没有使用article元素。但是，这一段中，可以分为几块独立的内容，因此嵌入几个独立的article元素

section、article与div的区别

- article是一种特殊种类的section元素，比section元素更强调独立性。section元素强调分段或分块，而article强调独立性如果一块内容相对来说比较独立、完整的时候使用article 如果想将一块内容分成几段的时候，应该使用section元素进行分段div元素变成一种容器，当使用css样式的时候，可以对这个容器进行一个总体的css样式套用

```html
<section></section>
```

#### nav

一个可以用来作为页面导航的链接组，其中的导航元素链接到其他页面或当前页面的其他部分。并不是所有的链接组都要放进nav元素，只需要将主要的、基本的链接组放进nav元素即可

一个页面中可以拥有几个部分组成，每个部分都带有链接，最主要的链接放在nav元素中

使用场景

传统导航条、侧边栏导航、页内导航、翻页导航

```html
<nav></nav>
```

#### aside

当前页面或文章的附属信息部分，包含与当前页面或主要内容相关的引用、侧边栏、广告、导航条，以及其他类似的有别于主要内容的部分

两种使用方法

包含在article元素中作为主要内容的附属信息部分，其中的内容可以是与当前文字有关的参考资料

在article之外元素使用，作为页面或站点全局的附属信息部分。侧边栏，其中的内容可以是友情链接、博客中其他文章列表或广告单元

```html
<aside></aside>
```

#### time元素与微格式

微格式，是一种利用HTML的class属性来对网页添加诸如新闻事件发生的日期和时间、个人电话号码、企业邮箱之类的附加信息的方法

time元素代表24小时中的某个日期，表示时刻时允许带时差。他可以定义很多格式的日期和时间

pubdate

一个可选的boolean值，他可以背应用到article元素中的time元素上，意思是time元素代表了文章（article元素的内容）或整个网页的发布日期

pubdate属性表明那个time元素 代表通知的发布日期      

### 非主体结构元素

#### header

一种具有引导和导航作用的结构元素，通常用来放置整个页面或页面内的一个内容区块的标题，但也可以包含其他内容，例如数据表格、搜索表单或相关LOGO图片 

一个网页内并不限制只能有一个header元素，可以拥有多个，可以每个内容区块加一个header元素

```html
<header></header>
```

#### addresss

文档中呈现联系信息,包括文档作者或文档维护者、的网络链接、电子邮箱、真实地址、电话号码等

```html
<address></address>
```

#### main

主要内容 表示网页中的主要内容。主内容区域指与网页标题或应用程序中本页面主要功能直接相关或进行扩展的内容。该区域应该为每一个网页中所特有的内容，不能包含整个网站的导航条、版权信息、网站LOGO，公共搜索表单等整个网站内部的共同内容

每一个网页内部只能放置 一个main元素。不能将main元素放置在任何article、aside、footer、header、nav元素内部

```html
<main></main>
```

#### footer

脚注，页脚 可以作为其上层父级内容区块或一个根区块的脚注。footer通常包括其相关区块的脚注信息，如作者、相关阅读链接以及版权信息语义化的footer

```html
<footer></footer>
```

HTML5网页结构

header

页头

nav

main

footer

页脚

```html
<header>
    <nav></nav>
</header>
<main>
	
</main>
<footer></footer>
```

HTML5中的大纲



HTML网页文档中的大纲只是使用不同结构元素进行表达而已 使用各种结构元素所描述出来的整个网页的层次结构，就是该网页的大纲

不能使用div容器，div元素只能当作容器，用在需要对网页中某个局部使用整体样式时

 

header

 

header元素、footer、nav、aside 没有标题元素，也不用于生成大纲

节根元素

 

大纲的编排规则

内容区块的编排，可以分为显式编排与隐式编排两种方式

显式编排内容区块

显示编排是指明确使用section等元素创建文档结构，每个内容区块内使用标题（h1~h6）

清晰明确、易读

隐式编排内容区块

所谓隐式编排，是指不明确使用section等元素，而是根据页面中所书写的各级标题等自动创建各级内容区块

标题分级

不同的内容区块可以使用相同级别的标题

网页编排实例

新的结构元素使用样式

很多浏览器还未对HTML5中新增的结构元素提供支持，无法知道客户端使用的浏览器是否支持这些元素，所以需要使用除上述追加如下声明，目的是通知浏览器页面中使用的HTML5中新增元素都是以块方式显示的

IE8之前不支持用css的方法对尚未支持的结构元素，IE9以后支持

## 元素

### 新增元素

- 绘画元素  1个
	- canvas 标签定义图形，比如图表和其他图像。该标签基于 JavaScript 的绘图 API
- 多媒体元素 5个
	- audio 定义音频内容
	- video  定义视频（video 或者 movie）
	- source 定义多媒体资源 `<video>` 和`` <audio>``
	- embed 定义嵌入的内容，比如插件。
	- track 为诸如`` <video>`` 和`` <audio>`` 元素之类的媒介规定外部文本轨道。
- 新表单元素 3个
	- datalish 定义选项列表。请与 input 元素配合使用该元素，来定义 input 可能的值。
	- keygen 规定用于表单的密钥对生成器字段。
	- output 定义不同类型的输出，比如脚本的输出。

### `语义元素  `

`(语义化标签)` 21个


无语义`div` 和 `span`
![img](html.assets/uxcoAXn9IkZytL3.jpg)
语义= 意义
语义元素 = 有意义的元素
语义标签提供了新的元素来创建更好的`页面结构`
语义是指一个词或者句子含义的正确解释。html标签具有语义的意义，也就是说元素本身传递了关于标签所包含内容类型的一些信息。
语义元素能够清楚的描述其意义给浏览器和开发者
优点

- 代码结构，使页面没有css的情况下，也能够呈现出很好的内容结构
- 有利于SEO**:** 爬虫依赖标签来确定关键字的权重，因此可以和搜索引擎建立良好的沟通，帮助爬虫抓取更多的有效信息
- 结构清晰，利于维护
- 提升用户体验 例如title、alt可以用于解释名称或者解释图片信息，以及label标签的灵活运用
- 便于团队开发维护 语义化使得代码更具有可读性，让其他开发人员更加理解你的html结构，减少差异化。
- 方便其他设备解析 如屏幕阅读器、盲人阅读器、移动设备等，以有意义的方式来渲染网页。

`<main>` 元素 定义页面的主要内容，一个页面只能使用一次。

| 标签           | 描述                                                         |
| :------------- | :----------------------------------------------------------- |
| `<header>`     | 定义了文档的头部区域`页头`，定义页面的介绍展示区域，通常包括网站logo、主导航、全站链接以及搜索框 |
| `<nav> `       | 定义`导航`链接的部分。页脚再次显示顶级全局导航、或者包含招聘信息等重要链接 |
| `<article>`    | 定义`页面独立的内容区域`、定义的内容本身必须是有意义的且必须是独立于文档的其余部分，专注于单个主题的博客文章，报纸文章或网页文章。 |
| `<aside>`      | 定义页面的侧边栏内容。                                       |
| `<section> `   | 定义文档中的节（section、区段）。长表单文章的章节或主要部分  |
| `<footer>  `   | 定义 section 或 document 的`页脚`。通常包含文档的作者，著作权信息，链接的使用条款，联系信息等 |
|                |                                                              |
| `<figure>`     | 规定独立的流内容（图像、图表、照片、代码等等）。\>元素的内容应该与主内容相关，但如果被删除，则不应对文档流产生影响。 |
| `<figcaption>` | 定义 `<figure>` 元素的标题 `行内元素`                        |
| `<dialog>`     | 定义对话框，比如提示框                                       |
|                |                                                              |
| `<progress> `  | 定义任何类型的任务的进度。 进度条                            |
| `<meter>  `    | 定义度量衡。仅用于已知最大和最小值的度量。                   |
| `<mark>`       | 定义带有记号的文本。 `光亮`                                  |
| `<time> `      | 定义日期或时间。                                             |
|                |                                                              |
| `<details>`    | 用于描述文档或文档某个部分的细节`只有 Chrome 和 Safari 6 支持 <details> 标签` |
| `<summary>`    | 标签包含 details 元素的标题                                  |
|                |                                                              |
| `<bdi>`        | 允许您设置一段文本，使其脱离其父元素的文本方向设置。         |
| `<wbr>`        | 规定在文本中的何处适合添加换行符。                           |
| 注音           |                                                              |
| `<ruby> `      | 定义 ruby 注释（中文注音或字符）。                           |
| `<rt>`         | 定义字符（中文注音或字符）的解释或发音。                     |
| `<rp>`         | 在 ruby 注释中使用，定义不支持 ruby 元素的浏览器所显示的内容。 |
|                |                                                              |
| `<command>`    | 定义命令按钮，比如单选按钮、复选框或按钮 `主流浏览器都不支持 <command> 标签 `sb 元素 IE 9 支持 |

<progress value="50" max="100">
</progress>

汉 (Han)
字 (zi)

汉 (Han)
字 (zi)

汉 (Han)
字 (zi)
<ruby>
汉 <rp>(</rp><rt>Han</rt><rp>)</rp>
字 <rp>(</rp><rt>zi</rt><rp>)</rp>
</ruby>

<details>
<summary>Copyright 1999-2011.</summary>
<p> - by Refsnes Data. All Rights Reserved.</p>
<p>All content and graphics on this web site are the property of the company Refsnes Data.</p>
</details>


  <meter value="2" min="0" max="10">2 out of 10</meter><br>
  <meter value="0.6">60%</meter>

<p>Do not forget to buy <mark>milk</mark> today.</p>

```html
<figure>
  <img src="img_pulpit.jpg" alt="The Pulpit Rock" width="304" height="228">
  <figcaption>Fig.1 - A view of the pulpit rock in Norway.</figcaption>
</figure>
<progress value="22" max="100">
</progress>
<ruby>
  汉 <rp>(</rp><rt>Han</rt><rp>)</rp>
  字 <rp>(</rp><rt>zi</rt><rp>)</rp>
</ruby>
<details>
<summary>Copyright 1999-2011.</summary>
<p> - by Refsnes Data. All Rights Reserved.</p>
<p>All content and graphics on this web site are the property of the company Refsnes Data.</p>
</details>
<meter value="2" min="0" max="10">2 out of 10</meter><br>
<meter value="0.6">60%</meter>
<p>Do not forget to buy <mark>milk</mark> today.</p>
```

### ``移除元素``

（HTML 4.01 元素在HTML5中已经被删除:）11个

- `<acronym>`
- `<applet>`
- `<basefont>`
- `<big>`
- `<center>`
- ` <dir>`
- `<font>`
- `<frame>`
- `<frameset>`
- `<noframes>`
- `<strike>`

## 表单

### input

- color 颜色
- email 邮箱
- tel （电话号码）
- number 数值的输入域
- range  类型显示为滑动条
- search 搜索
- url 网址
- file 文件
- date（日期）、datetime(datetime 类型允许你选择一个日期（UTC 时间）)、datatime-local(允许你选择一个日期和时间 (无时区))、month(月份)、time（时间）、week（周和年）



|                |      |
| -------------- | ---- |
| url            |      |
| email          |      |
| date           |      |
| datetime-local |      |
| month          |      |
| time           |      |
| week           |      |
| number         |      |
| range          |      |
| search         |      |
| tel            |      |
| color          |      |

```html
<input type="range" name="points" min="1" max="10">max - 规定允许的最大值min - 规定允许的最小值step - 规定合法的数字间隔value - 规定默认值<input type="number" name="quantity" min="1" max="5">disabled	规定输入字段是禁用的max	规定允许的最大值maxlength	规定输入字段的最大字符长度min	规定允许的最小值pattern	规定用于验证输入字段的模式readonly	规定输入字段的值无法修改required	规定输入字段的值是必需的size	规定输入字段中的可见字符数step	规定输入字段的合法数字间隔value	规定输入字段的默认值
```

### form

form 新属性

- autocomplete
- novalidate

#### 表单元素

| 标签         | 描述                                                         |
| :----------- | :----------------------------------------------------------- |
| `<datalist>` | 定义选项列表。请与 input 元素配合使用该元素，来定义 input 可能的值。 |
| `<keygen>`   | 规定用于表单的密钥对生成器字段。                             |
| `<output>`   | 定义不同类型的输出，比如脚本的输出。                         |

```html
<input list="browsers"><datalist id="browsers">  <option value="Internet Explorer">  <option value="Firefox">  <option value="Chrome">  <option value="Opera">  <option value="Safari"></datalist><select name="" id="">    <option value="A">A</option>    <option value="B">B</option>    <option value="C">C</option></select><form oninput="x.value=parseInt(a.value)+parseInt(b.value)">0<input type="range" id="a" value="50">100 +<input type="number" id="b" value="50">=<output name="x" for="a b"></output></form>表单属性
```

# Web API

## MathML API

> [MathML | MDN](https://developer.mozilla.org/zh-CN/docs/Web/MathML)

MathML 是数学标记语言（` <math>...</math>` ），是一种基于XML（标准通用标记语言的子集）的标准，用来在互联网上书写数学符号和公式的置标语言。

## Canvas API

使用JavaSript 绘图

- HTML5 `<canvas>` 元素用于图形的绘制，通过脚本 (通常是JavaScript)来完成.
- `<canvas>` 标签只是图形容器，您必须使用脚本来绘制图形。

### 创建画布

 `<canvas>`

```html
<canvas width="500px" height="500px" id="myCanvas" style="border: 1px solid pink;"></canvas>
```

### 使用JavaScript 绘制图形

`canvas 元素本身是没有绘图能力的`。所有的绘制工作必须在 JavaScript 内部完成
canvas 是一个二维网格 ` X 和 Y 坐标`

> getContext("2d") 对象是内建的 HTML5 对象，拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法
>
> fillStyle属性可以是CSS颜色，渐变，或图案。fillStyle 默认设置是#000000（黑色）

```html
<canvas width="500px" height="500px" id="myCanvas" style="border:1px solid pink;"></canvas><script>    var c = document.getElementById('myCanvas');    // 创建 context 对象    var ctx = c.getContext('2d')    ctx.fillStyle = 'red';    ctx.fillRect(0,0,150,350);     // fillReact 正方形 左上角  右下角</script>
```

### 路径画线 

`lineTo(x,y) moveTo(x,y)`

- moveTo(x,y) 定义线条开始坐标
- lineTo(x,y) 定义线条结束坐标

```js
var c = document.getElemnetById("myCanvas");var ctx = c.getContext('2d');ctx.moveTo(0,0);ctx.lineTo(200,100);ctx.stroke(); // 线ctx.strokefill = 'red'; // 边框的颜色
```

### 正方形 

`fillRect(x,y,x,y)`

```html
 var c = document.getElementById('myCanvas'); // 创建 context 对象 var ctx = c.getContext('2d') ctx.fillStyle = 'red'; ctx.fillRect(0,0,150,350);  // fillReact 正方形 左上角  右下角
```

### 圆形 

`arc(x,y,r,start,stop)`

```js
arc(x,y,r,start,stop)var c=document.getElementById("myCanvas");var ctx=c.getContext("2d");ctx.beginPath();ctx.arc(95,50,40,0,2*Math.PI);  ctx.stroke();
```

### 文本

- font - 定义字体
- fillText(*text,x,y*) - 在 canvas 上绘制实心的文本
- strokeText(*text,x,y*) - 在 canvas 上绘制空心的文本（x,y）位置

```js
var c=document.getElementById("myCanvas");var ctx=c.getContext("2d");ctx.font="30px Arial"; // 设置字体大小ctx.strokeText("Hello World",10,50);  // fillText(text,x,y); 设置字体
```

### 绘制渐变图形

线性渐变 和 径向渐变
渐变可以填充在矩形, 圆形, 线条, 文本等等, 各种形状可以自己定义不同的颜色。
以下有两种不同的方式来设置Canvas渐变：

- createLinearGradient(*x,y,x1,y1*) - 创建线条渐变
- createRadialGradient(*x,y,r,x1,y1,r1*) - 创建一个径向/圆渐变
	当我们使用渐变对象，必须使用两种或两种以上的停止颜色。
	addColorStop()方法指定颜色停止，参数使用坐标来描述，可以是0至1.
	使用渐变，设置fillStyle或strokeStyle的值为 渐变，然后绘制形状，如矩形，文本，或一条线。
	使用 createLinearGradient():
	线性渐变

```js
var c=document.getElementById("myCanvas");var ctx=c.getContext("2d");// 创建渐变var grd=ctx.createLinearGradient(0,0,200,0);grd.addColorStop(0,"red");grd.addColorStop(1,"white");// 填充渐变ctx.fillStyle=grd;ctx.fillRect(10,10,150,80);
```

径向渐变

```js
var c=document.getElementById("myCanvas");var ctx=c.getContext("2d");// 创建渐变var grd=ctx.createRadialGradient(75,50,5,90,60,100);grd.addColorStop(0,"red");grd.addColorStop(1,"white");// 填充渐变ctx.fillStyle=grd;ctx.fillRect(10,10,150,80);
```

### 图像 

`drawImage(image,x,y)`

```js
var c=document.getElementById("myCanvas");var ctx=c.getContext("2d");var img=document.getElementById("scream");ctx.drawImage(img,10,10);
```

图形

Canvas与 SVG 的区别

> `<canvas> 与 <svg> 两个标签`
>
> canvas 的绘制代码可以在 `<script>`、js文件
>
> svg 的绘制代码可以在``<style>``、svg文件
>
> | Canvas（Javascript）                                         | SVG(XML)                                                     |
> | :----------------------------------------------------------- | :----------------------------------------------------------- |
> | Canvas 通过 JavaScript 来绘制 2D 图形。<br />依赖分辨率<br />不支持事件处理器<br />弱的文本渲染能力能够以<br /> .png 或 .jpg 格式保存结果图像<br />最适合图像密集型的游戏，其中的许多对象会被频繁重绘 | SVG 是一种使用 XML 描述 2D 图形的语言。<br />不依赖分辨率<br />支持事件处理器<br />最适合带有大型渲染区域的应用程序（比如谷歌地图）<br />复杂度高会减慢渲染速度（任何过度使用 DOM 的应用都不快）<br />不适合游戏应用 |
>
> SVG 基于 XML，这意味着 SVG DOM 中的每个元素都是可用的。您可以为某个元素附加 JavaScript 事件处理器。
> 在 SVG 中，每个被绘制的图形均被视为对象。如果 SVG 对象的属性发生变化，那么浏览器能够自动重现图形。
> Canvas 是逐像素进行渲染的。在 canvas 中，一旦图形被绘制完成，它就不会继续得到浏览器的关注。如果其位置发生变化，那么整个场景也需要重新绘制，包括任何或许已被图形覆盖的对象。
> `canvas 元素本身是没有绘图能力的`。所有的绘制工作必须在 JavaScript 内部完成，而svg可以通过内联样式绘制图画

## SVG API

使用 XML 绘图

### 工具

> [SVG 在线编辑器](https://c.runoob.com/more/svgeditor/)
> [SVG 参考手册 ](https://www.runoob.com/svg/svg-reference.html)

视图  ->  源代码 `ctrl+ U`

### 定义

- SVG 指``可伸缩矢量图形 (Scalable Vector Graphics)``
- SVG 用于定义用于网络的基于矢量的图形
- SVG 使用`` XML 格式定义图形``
- SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
- SVG 是万维网联盟的标准
- 是使用XML来描述二维图形和绘图程序的语言

### 优点

- SVG 图像可通过文本编辑器来创建和修改
- SVG 图像可被搜索、索引、脚本化或压缩
- SVG 是可伸缩的
- SVG 图像可在任何的分辨率下被高质量地打印
- SVG 可在图像质量不下降的情况下被放大
- SVG 文件是纯粹的 XML

### SVG 文件 `.svg 扩展`

```svg
<?xml version="1.0" standalone="no"? >// 第一行包含了 XML 声明。请注意 standalone 属性！该属性规定此 SVG 文件是否是"独立的"，或含有对外部文件的引用。// standalone="no" 意味着 SVG 文档会引用一个外部文件 - 在这里，是 DTD 文件。<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN""http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">//第二和第三行引用了这个外部的 SVG DTD。该 DTD 位于 "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"。该 DTD 位于 W3C，含有所有允许的 SVG 元素。<svg xmlns="http://www.w3.org/2000/svg" version="1.1">// version 属性可定义所使用的 SVG 版本，xmlns 属性可定义 SVG 命名空间。  <circle cx="100" cy="50" r="40" stroke="black"  stroke-width="2" fill="red" /></svg>
```

在HTML页面中 
直接在HTML嵌入SVG代码

```svg
<svg></svg>
```

### 属性

- fill
- stroke[ stroke,stroke-width,stroke-linecap,stroke-dasharray ]
- opacity[ fill-opacity,stroke-opacity  ]

```html
svg 标签 可以添加 到 style 属性中,也可以写到 内置属性，还可以写到 <style> 中// 方法一<svg>	<circle style="fill:;stroke:;stroke-width:;"/></svg>// 方法二<svg>	<circle fill="" stroke="" stroke-width="" /></svg>// 方法三<style>circle{	fillL:;    stroke:;    stroke-width:;}</style>fill // 填充的颜色stroke // 边框的颜色stroke-width // 边框的宽度
```

### 浏览器支持情况

> Internet Explorer 9+, Firefox, Opera, Chrome, 和 Safari 支持内联SVG。

### 使用

```html
<!DOCTYPE html><html><body> // 1<svg xmlns="http://www.w3.org/2000/svg" version="1.1" height="190">  <polygon points="100,10 40,180 190,60 10,60 160,180"  style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;"></svg> // 2 <svg>      <polygon points="100,10 40,180 190,60 10,60 160,180"  style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;"> </svg>    </body></html>
```

SVG 默认的画布 `300 * 150 的默认长方形`

### 形状

---

#### 矩形 `<rect>`

```html
<svg width="500px" height="500px">    <rect x="100" y="100" width="300" height="300" style="fill:red;stroke-width:2;stroke:pink"/></svg><svg width="500px" height="500px">    <rect x="100" y="100" width="300" height="300" style="fill:red;stroke-width:2;stroke:pink;fill-opacity:0.5;stroke-opacity:0.9"/></svg><svg width="500px" height="500px">    <rect x="100" y="100" width="300" height="300" style="fill:red;stroke-width:2;stroke:pink;opacity:0.9"/></svg>// rect 圆形或者椭圆形 <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="500px" height="500px">        <rect x="100" y="20" rx="75" ry="75" width="150" height="150"            style="fill:red;stroke:black;stroke-width:5;" /></svg>// rx ry 为水平方向的坐标  和 竖直方向的坐标  // (x,y) 是图形的第一个点的坐标位置  fill 填充颜色 边框 stroke-width  宽度 stroke 颜色 // fill-opacity 属性定义填充颜色透明度（合法的范围是：0 - 1）// stroke-opacity 属性定义轮廓颜色的透明度（合法的范围是：0 - 1）// opacity 属性用于定义了元素的透明值 (范围: 0 到 1)。
```

#### 圆形 `<circle>`

```html
<svg>    <circle cx="300" cy="300" r="100" style="fill: red;"/></svg>// cx和cy属性定义圆点的x和y坐标。如果省略cx和cy，圆的中心会被设置为(0, 0) r属性定义圆的半径
```

#### 椭圆 `<ellipse>`

```svg
<svg>    <ellipse cx="300" cy="80" rx="100" ry="50" style="fill:yellow;stroke:purple;st"></ellipse></svg>
```

#### 线 `<line>`

##### 直线 `<line />`

`svg-line`

```html
<svg>	 <line x1="0" y1="0" x2="200" y2="0" stroke="blue" stroke-width="5" /></svg>// (x1,y1) 起始坐标点   (x2,y2) 结束坐标点 
```

##### 曲线 `<polyline />`

`svg-polyline`

```html
<svg>    <polyline points="20,20 40,25 60,40 80,120 120,140 200,180" style="fill:none;stroke:black;stroke-width:3" /></svg><svg xmlns="http://www.w3.org/2000/svg" version="1.1">    <polyline points="0,40 40,40 40,80 80,80 80,120 120,120 120,160" style="fill:white;stroke:red;stroke-width:4" /> </svg> // fill 填充颜色  stroke 颜色  stroke-width 线宽度
```

#### 多边形 `<polygon>`

#### 路径 `<path>`

#### 文本 `<text>`

```
<svg>	<text x="100" y="100" fill="red">这是一段文字</text></svg>
```

### 效果

---

#### 滤镜



#### 模糊

#### 阴影

#### 渐变

## 多媒体 API

### 多媒体概念

### HTML 多媒体

多媒体指的是音效、音乐、视频和动画

- 视频格式：`(AVI) .avi`、`(WMV) .wmv`、`(MPEG).mpg 和.mpeg`.、`(QuickTime)`、`(RealVideo).rm 和 .ram`、`(Flash).swf 和 .flv`、`(Mpeg-4) .mp4`
- 音频格式：`(MP3).mp3 和 .mpga` 、`.wma`、`.wav`、`.rm 和 .ram`、`.mid 和 .midi`

### 多媒体标签

| 标签       | 描述                                                         |
| ---------- | ------------------------------------------------------------ |
| `<emby>`   | 定义内嵌对象。HTML4 中不支持，HTML5 中允许。                 |
| `<object>` | 定义内嵌对象。                                               |
| `<param>`  | 定义对象的参数。                                             |
| `<audio>`  | 定义声音内容                                                 |
| `<video>`  | 定义一个视频或者影片                                         |
| `<source>` | 定义了media元素的多媒体资源(<video> 和 <audio>)              |
| `<track>`  | 规定media元素的字幕文件或其他包含文本的文件 (<video> 和<audio>) |

### HTML 插件

浏览器插件是一种扩展浏览器标准功能的小型计算机程序
辅助应用程序（helper application）是由浏览器启动的程序。辅助应用程序也称为插件
辅助程序可用于播放音频和视频（以及其他）。辅助程序是使用 <object> 标签来加载的。
使用辅助程序播放视频和音频的一个优势是，您能够允许用户来控制部分或全部播放设置。
插件可以通过 <object> 标签或者 <embed> 标签添加在页面中。 
大多数辅助应用程序允许对音量设置和播放功能（比如后退、暂停、停止和播放）的手工（或程序的）控制。

| 标签       | 描述                                                         |
| ---------- | ------------------------------------------------------------ |
| `<object>` | 定义了在 HTML 文档中嵌入的对象(嵌入 Java 小程序, PDF 阅读器, Flash 播放器,图片) flash  html 图片 |
| `<embed>`  | 表示一个 HTML Embed 对象，<embed> 元素没有关闭标签。 不能使用替代文本 HTML 图片 |

```html
<object width="400" height="50" data="bookmark.swf"></object><object width="100%" height="500px" data="snippet.html"></object><object data="audi.jpeg"></object><embed width="100%" height="500px" src="snippet.html"><embed src="audi.jpeg">
```

### Video（视频）

| 标签                                                         | 描述               |
| ------------------------------------------------------------ | ------------------ |
| 属性                                                         | 值                 |
| [autoplay](https://www.runoob.com/tags/att-video-autoplay.html)**New** | autoplay           |
| [controls](https://www.runoob.com/tags/att-video-controls.html)**New** | controls           |
| [height](https://www.runoob.com/tags/att-video-height.html)**New** | *pixels*           |
| [loop](https://www.runoob.com/tags/att-video-loop.html)**New** | loop               |
| [muted](https://www.runoob.com/tags/att-video-muted.html)**New** | muted              |
| [poster](https://www.runoob.com/tags/att-video-poster.html)**New** | *URL*              |
| [preload](https://www.runoob.com/tags/att-video-preload.html)**New** | auto metadata none |
| [src](https://www.runoob.com/tags/att-video-src.html)**New** | 视频网址           |
| [width](https://www.runoob.com/tags/att-video-width.html)**New** | *pixels*           |

- 使用`<embed>` 元素
- 使用`<object>` 元素
- 使用HTML5`<audio>` 元素
- 使用超链接
- 最好的HTML解决方法

```html
<embed src="intro.swf" height="200" width="200"><object data="intro.swf" height="200" width="200"></object><video width="320" height="240" controls>  <source src="movie.mp4" type="video/mp4">  <source src="movie.ogg" type="video/ogg">  <source src="movie.webm" type="video/webm">您的浏览器不支持 video 标签。</video><a href="intro.swf">Play a video file</a><video width="320" height="240" controls>  <source src="movie.mp4" type="video/mp4">  <source src="movie.ogg" type="video/ogg">  <source src="movie.webm" type="video/webm">  <object data="movie.mp4" width="320" height="240">    <embed src="movie.swf" width="320" height="240">  </object></video>
```

### Audio（音频）

| 属性                                                         | 值                 | 描述                                                        |
| :----------------------------------------------------------- | :----------------- | :---------------------------------------------------------- |
| [autoplay](https://www.runoob.com/tags/att-audio-autoplay.html)**New** | autoplay           | 如果出现该属性，则音频在就绪后马上播放。                    |
| [controls](https://www.runoob.com/tags/att-audio-controls.html)**New** | controls           | 如果出现该属性，则向用户显示音频控件（比如播放/暂停按钮）。 |
| [loop](https://www.runoob.com/tags/att-audio-loop.html)**New** | loop               | 如果出现该属性，则每当音频结束时重新开始播放。              |
| [muted](https://www.runoob.com/tags/att-audio-muted.html)**New** | muted              | 如果出现该属性，则音频输出为静音。                          |
| [preload](https://www.runoob.com/tags/att-audio-preload.html)**New** | auto metadata none | 规定当网页加载时，音频是否默认被加载以及如何被加载。        |
| [src](https://www.runoob.com/tags/att-audio-src.html)**New** | *URL*              | 规定音频文件的 URL。                                        |
| crossorigin                                                  |                    | 是否使用跨域方式请求                                        |

### track、source、embed、object/param

track:标签用于指定视频的字幕，格式是 WebVTT （`.vtt`文件），放置在`<video>`标签内部。它是一个单独使用的标签，没有结束标签。

- `label`：播放器显示的字幕名称，供用户选择。
- `kind`：字幕的类型，默认是`subtitles`，表示将原始声音成翻译外国文字，比如英文视频提供中文字幕。另一个常见的值是`captions`，表示原始声音的文字描述，通常是视频原始使用的语言，比如英文视频提供英文字幕。
- `src`：vtt 字幕文件的网址。
- `srclang`：字幕的语言，必须是有效的语言代码。
- `default`：是否默认打开，布尔属性。

```
<video controls src="sample.mp4">   <track label="英文" kind="subtitles" src="subtitles_en.vtt" srclang="en">   <track label="中文" kind="subtitles" src="subtitles_cn.vtt" srclang="cn" default></video>
```



source:标签用于`<picture>`、`<video>`、`<audio>`的内部，用于指定一项外部资源。单标签是单独使用的，没有结束标签。

- `type`：指定外部资源的 MIME 类型。
- `src`：指定源文件，用于`<video>`和`<audio>`。
- `srcset`：指定不同条件下加载的图像文件，用于`<picture>`。
- `media`：指定媒体查询表达式，用于`<picture>`。
- `sizes`：指定不同设备的显示大小，用于`<picture>`，必须跟`srcset`搭配使用。

embel:标签用于嵌入外部内容，这个外部内容通常由浏览器插件负责控制。由于浏览器的默认插件都不一致，很可能不是所有浏览器的用户都能访问这部分内容，建议谨慎使用。

- `height`：显示高度，单位为像素，不允许百分比。
- `width`：显示宽度，单位为像素，不允许百分比。
- `src`：嵌入的资源的 URL。
- `type`：嵌入资源的 MIME 类型。

```
<embed type="video/webm"       src="/media/examples/flower.mp4"       width="250"       height="200">       <embed type="video/quicktime" src="movie.mov" width="640" height="480">       <embed src="whoosh.swf" quality="medium"       bgcolor="#ffffff" width="550" height="400"       name="whoosh" align="middle" allowScriptAccess="sameDomain"       allowFullScreen="false" type="application/x-shockwave-flash"       pluginspage="http://www.macromedia.com/go/getflashplayer">
```

object  param:`<object>`标签作用跟`<embed>`相似，也是插入外部资源，由浏览器插件处理。它可以视为`<embed>`的替代品，有标准化行为，只限于插入少数几种通用资源，没有历史遗留问题，因此更推荐使用。

- `data`：嵌入的资源的 URL。
- `form`：当前网页中相关联表单的`id`属性（如果有的话）。
- `height`：资源的显示高度，单位为像素，不能使用百分比。
- `width`：资源的显示宽度，单位为像素，不能使用百分比。
- `type`：资源的 MIME 类型。
- `typemustmatch`：布尔属性，表示`data`属性与`type`属性是否必须匹配。

浏览器安装了 PDF 插件，就会在网页显示 PDF 浏览窗口

```
<object data="movie.swf" type="application/x-shockwave-flash">  <param name="foo" value="bar"></object>
```



- 使用`<embed>` 元素
- 使用`<object>` 元素
- 使用HTML5`<audio>` 元素：
- 使用超链接
- 最好的HTML解决方法

```html
<embed height="50" width="100" src="audio.mp3"><object height="50" width="100" data="horse.mp3"></object><audio controls>  <source src="horse.mp3" type="audio/mpeg">  <source src="horse.ogg" type="audio/ogg">  Your browser does not support this audio format.</audio<a href="horse.mp3">Play the sound</a><audio controls height="100" width="100">  <source src="horse.mp3" type="audio/mpeg">  <source src="horse.ogg" type="audio/ogg">  <embed height="50" width="100" src="horse.mp3"></audio>
```

## History API

### 基本概念

## 本地存储 API

HTML5本地存储的两个重要内容

- Web Storage与本地数据库
	- Web Srorage 存储机制 对HTML4中cookie存储机制的一个改善。由于cookie存储有很多缺点，HTML5不再使用它，转而使用改良后的Web Storage存储机制
	- 本地数据库 使用它可以在客户端本地建立一个数据库，原本必须保存在服务器端数据库中的内容现在可以直接保存到客户端本地，这大大减轻了服务器端的负担，同时也加快了访问数据的速度

Web Storage  vs Cookie

Web Storage 是什么

可以在客户端本地保存数据的Web Storage功能

- sessionStorage
- locationStorage

cookie 的缺点

-  大小被限制在4kb
- 带宽
- 复杂性



数据存储 ===> 浏览器存储  +  服务器存储  +  缓存

> 控制台 Application 
>
> Storage(存储)
>
> - Local Storage
> - Session Storage
> - IndexdDB
> - WebSQL
> - Cookie
>
> Cache （缓存）
>
> - Cache Storage
> - Application Cache

### Web存储

HTML5 Web 存储，一个比cookie更好的本地存储方式
什么是HTML5 Web 存储？
本地存储使用的是 cookie。但是Web 存储需要更加的安全与快速. 
这些数据不会被保存在服务器上，但是这些数据只用于用户请求网站数据上.它也可以存储大量的数据，而不影响网站的性能.
数据以 键/值 对存在, web网页的数据只允许该网页访问使用。
客户端存储数据的两个对象`localStorage 和 sessionStorage`

| 对象           | 作用                                                         |
| -------------- | ------------------------------------------------------------ |
| localStorage   | 用于长久保存整个网站的数据，保存的数据没有过期时间，直到手动去除 |
| sessionStorage | 用于临时保存同一窗口(或标签页)的数据，在关闭窗口或标签页之后将会删除这些数据。 |

检查浏览器是否支持localStorage 和SessionStorage

```js
if(typeof(Storage)!== "undefined"){	//支持localStorage 、sessionStorage 对象}else{	// 不支持}
```

localStorage对象
用于长久保存整个网站的数据，保存的数据没有过期时间，直到手动去除
保存数据

```js
localStorage.setItem(key,value);
```

读取数据

```js
localStorage.getItem(key);
```

删除单个数据

```js
localStorage.removeItem(key);
```

删除所有数据

```js
localStorage.clear();
```

得到某个索引的key

```js
localStorage.key(index);
```

> 键/值对通常以字符串存储，你可以按自己的需要转换该格式。

```js
<button onclick="clickNum('add')">按钮 ++ </button><button onclick="clickNum('del')">按钮 -- </button><p id="result"></p><script>        function clickNum(par) {            if (typeof (Storage) !== 'undefined') {                if (localStorage.clickcount) {                    if (par === 'add') {                        localStorage.clickcount = Number(localStorage.clickcount) + 1;                    } else {                        if (localStorage.clickcount == 0) {                            alert('最小值不能小于0');                            localStorage.clickcount = 0;                        } else {                            localStorage.clickcount = Number(localStorage.clickcount) - 1;                        }                    }                } else {                    localStorage.clickcount = 0;                }            } else {                alert('你的浏览器不支持');            }            document.getElementById("result").innerHTML = " 你已经点击了按钮 " + localStorage.clickcount + " 次 ";        }</script>
```

SessionStorage对象
sessionStorage 方法针对一个 session 进行数据存储。当用户关闭浏览器窗口后，数据会被删除。
保存数据

```js
sessionStorage.setItem(key,value);
```

读取数据

```js
sessionStorage.getItem(key);
```

删除单个数据

```js
sessionStorage.removeItem(key);
```

删除所有数据

```js
sessionStorage.clear();
```

得到某个索引的key

```js
sessionStorage.key(index);localStorage.clickcount=Number(localStorage.clickcount)+1;
```

```js
<script>function clickCounter(){	if(typeof(Storage)!=="undefined")	{		if (sessionStorage.clickcount)		{			sessionStorage.clickcount=Number(sessionStorage.clickcount)+1;		}		else		{			sessionStorage.clickcount=1;		}		document.getElementById("result").innerHTML="在这个会话中你已经点击了该按钮 " + sessionStorage.clickcount + " 次 ";	}	else	{		document.getElementById("result").innerHTML="抱歉，您的浏览器不支持 web 存储";	}}</script></head><body><p><button onclick="clickCounter()" type="button">点我！</button></p><div id="result"></div><p>点击该按钮查看计数器的增加。</p><p>关闭浏览器选项卡(或窗口),重新打开此页面,计数器将重置。</p>
```

实例

```js
<div style="border: 2px dashed #ccc;width:320px;text-align:center;">        <label for="keyname">别名(key):</label>          <input type="text" id="keyname" name="keyname" class="text"/>          <br/>          <label for="sitename">网站名：</label>          <input type="text" id="sitename" name="sitename" class="text"/>          <br/>          <label for="siteurl">网 址：</label>          <input type="text" id="siteurl" name="siteurl"/>          <br/>          <input type="button" onclick="save()" value="新增记录"/>          <hr/>          <label for="search_phone">输入别名(key)：</label>          <input type="text" id="search_site" name="search_site"/>          <input type="button" onclick="find()" value="查找网站"/>          <p id="find_result"><br/></p>   </div><br/>  <div id="list">  </div>  <script>//保存数据  function save(){      var site = new Object;    site.keyname = document.getElementById("keyname").value;    site.sitename = document.getElementById("sitename").value;      site.siteurl = document.getElementById("siteurl").value;    var str = JSON.stringify(site); // 将对象转换为字符串    localStorage.setItem(site.keyname,str);      alert("保存成功");}  //查找数据  function find(){      var search_site = document.getElementById("search_site").value;      var str = localStorage.getItem(search_site);      var find_result = document.getElementById("find_result");    var site = JSON.parse(str);      find_result.innerHTML = search_site + "的网站名是：" + site.sitename + "，网址是：" + site.siteurl;  }  //将所有存储在localStorage中的对象提取出来，并展现到界面上// 确保存储的 keyname 对应的值为转换对象，否则JSON.parse会报错function loadAll(){      var list = document.getElementById("list");      if(localStorage.length>0){          var result = "<table border='1'>";          result += "<tr><td>别名</td><td>网站名</td><td>网址</td></tr>";          for(var i=0;i<localStorage.length;i++){             var keyname = localStorage.key(i);              var str = localStorage.getItem(keyname);              var site = JSON.parse(str);              result += "<tr><td>"+site.keyname+"</td><td>"+site.sitename+"</td><td>"+site.siteurl+"</td></tr>";          }          result += "</table>";          list.innerHTML = result;      }else{          list.innerHTML = "数据为空...";      }  }  </script>
```

### 本地数据库

-  SQL存储

Web SQL 数据库 API 并不是 HTML5 规范的一部分，但是它是一个独立的规范，引入了一组使用 SQL 操作客户端数据库的 APIs。
Web SQL 数据库可以在最新版的 Safari, Chrome 和 Opera 浏览器中工作。
核心方法
以下是规范中定义的三个核心方法：

1. **openDatabase**：这个方法使用现有的数据库或者新建的数据库创建一个数据库对象。
2. **transaction**：这个方法让我们能够控制一个事务，以及基于这种情况执行提交或者回滚。
3. **executeSql**：这个方法用于执行实际的 SQL 查询。

	访问本地文件

### indexedDB数据库

HTML5中新增的数据库，该数据库是一种存储在客户端本地的NoSQL数据库



```

```



## 文件 API

### 基本概念



### FileList对象和file对象

- FileList对象表示用户选择的文件列表
- file

```js
<input type="file"id="file" multiple size="80">
<input type="button" onclick="showFileName()" value="文件上传">

function ShowFileName(){
    var file;
    // document.getElementById('file')
    for(var i = 0; document.getElementById('file').files.length;i++){
        alert(file.name)
    }
}
```



### ArrayBuffer与ArrayBufferView对象

AarrayBuffer对象



AarrayBufferView



DateView对象



### Blob对象





### FileReader对象



### FileSystemAPI





### Base 编码支持





## 通信 API



## 拖放API和通知API


WebRTC通信





## XMLHTTPRequest API



## 离线应用程序API



离线Web应用程序详解



新增本地缓存



本地缓存与浏览器网页缓存的区别



manifest文件





## 应用缓存 API

拖放 `Drag 和 Drop`

在 HTML5 中，拖放是标准的一部分，任何元素都能够拖放。
设置元素为可拖放的 `draggable="true"`

```
<img draggable="true">
```

拖放什么 ` ondragstart 和 setData()`
放在何处 `ondragover`
进行放置 `ondrop`

## Geolocation API

- HTML5 Geolocation API 用于获得用户的地理位置。
- 鉴于该特性可能侵犯用户的隐私，除非用户同意，否则用户位置信息是不可用的

```js
<p id="demo">点击按钮获取您当前坐标（可能需要比较长的时间获取）：</p><button onclick="getLocation()">点我</button>var x=document.getElementById("demo");function getLocation(){	if (navigator.geolocation)	{		navigator.geolocation.getCurrentPosition(showPosition,showError);          // getCurrentPosition() 第一个参数显示地理位置 方法的第二个参数用于处理错误	}	else	{		x.innerHTML="该浏览器不支持定位。";	}}function showPosition(position){	x.innerHTML="纬度: " + position.coords.latitude + 	"<br>经度: " + position.coords.longitude;	}function showError(error){	switch(error.code) 	{		case error.PERMISSION_DENIED:			x.innerHTML="用户拒绝对获取地理位置的请求。"			break;		case error.POSITION_UNAVAILABLE:			x.innerHTML="位置信息是不可用的。"			break;		case error.TIMEOUT:			x.innerHTML="请求用户地理位置超时。"			break;		case error.UNKNOWN_ERROR:			x.innerHTML="未知错误。"			break;	}}
```

错误代码：

- Permission denied - 用户不允许地理定位
- Position unavailable - 无法获取当前位置
- Timeout - 操作超时
	百度获取经纬度的方法

```html
<!DOCTYPE html><html><head>    <meta charset="utf-8" />    <title></title>    <!--引入百度 API，"ak=" 后面一串码是密钥，最好自己申请-->    <script type="text/javascript" src="https://api.map.baidu.com/api?v=2.0&ak=7a6QKaIilZftIMmKGAFLG7QT1GLfIncg"></script></head><body>    <input type="button" onclick="getLocation()" value="确认" />    <div id="position"></div>    <script type="text/javascript">    var x = document.getElementById('position');    function getLocation() {        // 创建百度地理位置实例，代替 navigator.geolocation        var geolocation = new BMap.Geolocation();        geolocation.getCurrentPosition(function(e) {            if(this.getStatus() == BMAP_STATUS_SUCCESS){                // 百度 geolocation 的经纬度属性不同，此处是 point.lat 而不是 coords.latitude                x.innerHTML = '纬度：' + e.point.lat + '<br/>经度：' + e.point.lng;            } else {                x.innerHTML = 'failed' + this.getStatus();            }        });    }    </script></body></html>
```

## WebRTC通信



## SSE API

(Server - Sent Events)

HTML5 服务器发送事件 （server-sent event） 允许网页获得来自服务器的更新

### Server-Sent 事件 -  单向消息传递

- Server -Sent 事件指的是网页自动获取来自服务器的更新
- 以前也可能做到这一点，前提是网页不得不询问是否有可用的更新。通过服务器发送事件，更新能够自动到达
- 所有主流浏览器均支持服务器发送事件，除了 Internet Explorer。

### EventSource对象

| 事件      | 描述                   |
| --------- | ---------------------- |
| onopen    | 通往服务器的连接被打开 |
| onmessage | 接收到消息             |
| onerror   | 发生错误               |

### Server-Sent Event 使用

服务器端代码

```php
sse.phphttps://www.runoob.com/try/demo_source/demo_sse.php<?php    header('Content-Type: text/event-stream');	// 把报头 "Content-Type" 设置为 "text/event-stream"    header('Cache-Control: no-cache');	// 规定不对页面进行缓存    $time = date('r');	// 输出发送日期（始终以 "data: " 开头）    echo "data: The server time is: {$time}\n\n";    flush();	//向网页刷新输出数据?>
```

EventSource对象用于接收服务器发送事件通知

```js
if(typeof(EventSource !== "undefined")){ //  检测 Server-Sent 事件支持	// 浏览器支持 Server-Sent    var source = new EventSoure("sse.php")    source.onmessage = function(event){        document.getElementById("result").innerHTML += event.data + "<br>"    }}else{	// 浏览器不支持 Server-Sent    document.getElementById("result").innerHTML="抱歉，你的浏览器不支持 server-sent 事件...";}
```

## Web workers 处理线程

web worker 是运行在`后台的JavaScript` ，独立于其他脚本,不会影响页面的性能
当在HTML页面中执行脚本时，页面的状态是不可响应的，直到脚本已完成

- 页面刷新，workers 文件也会刷新
	Internet Explorer 10, Firefox, Chrome, Safari 和 Opera 都支持Web workers.
	Web Workers 和 DOM，Web workers 位于外部文件中，无法访问window对象 、document对象和 parent 对象

```js
// 创建 web worker 文件 workers.jsvar i = 0;function timeCount(){    i++;    postMessage(i);    setTimeout("timedCount()",500);}timeCount();
```

```js
<p>计数： <output id="result"></output></p><button onclick="startWorker()">开始工作</button> <button onclick="stopWorker()">停止工作</button>var w;function startWorker(){	if(typeof(Worker) !== "undefined"){ // 检测浏览器是否支持 worker 		if(typeof(w) == "undefined"){			w = new Worker("workers.js");   // 创建 web worker 对象		}		w.onmessage = function(event){			document.getElementsById("result").innerHTML = event.data;		}	}else{		console.log('你的浏览器不支持 Web workers...');	}}function stopWorker(){    w.terminate();  // 终止 web worker     w = underfined;}
```

## WebSocker 通信

WebSocket 是 HTML5 开始提供的一种在单个 TCP 连接上进行全双工通讯的协议

### WebSocket 属性

### WebSocket事件

### WebSocket方法

## 其他API

Page Visiblility API
Fullscreen API
鼠标指针锁定 API
requestAnimateFrame 
Mutation Observer
JavaScript Promise
Beacon API



# 网页结构

- header 页头		
- main 页面主体
- footer 页尾		
- content/container 内容
- container 容器
- nav  导航
  - miannav 主导航
  - subnav 子导航
  - topnav 顶导航
  - sidebar 边导航			
  - leftsidebar 左导航
  - rightsidebar 右导航
- menu 菜单
  - submenu 子菜单
- title 标题
- summary 摘要
- sidebar 侧栏
- column 栏目
- wrapper 页面外围控制
- logo 标志
- banner 广告
- login 登陆
- loginbar 登录条
- register 注册
- search 搜索
- shop 功能区
- title 标题
- left center right 左中右





