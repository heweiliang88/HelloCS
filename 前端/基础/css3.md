---
title: 你使不知道的CSS3
categories:
- 前端
tags:
  - CSS3
abbrlink: 24989
date: 2020-06-30 16:56:38
---
# css3

## [css&&css3](./basic/css/css&css3.md)

### css&&css3

- 选择器
- 盒子模型
- 定位、浮动、flex布局 、grid布局
- 过渡、动画
- 2D、3D转换
- 边框、圆角
- 背景、渐变
- 媒体查询
- 布局方式

- css 的引入方式

	- 行内式 内嵌 外联 导入
	- css引入方式之外链式和导入式的异同点(面试题)
	- css命名规范及项目文件目录
	- 权重和权重的计算
	- margin的负值使用技巧
	- 可以继承和不可以继承的样式属性

- 清浮动的方法

- clearfix的清浮动的技巧

- :clear的值和特点及伪元素before和after的使用

- 文档流和脱离文档流

- 背景类之背景显示原点

- 

- 背景类之背景裁剪

- 雪碧图的使用和制作技巧

- :overflow的多个作用

- 内联元素和块级元素

- display 和 visibility

- overflow

- 高度塌陷  margin 重叠

	- BFC

- 雪碧图的制作和使用 CSS Sprite

	- 问题：加载图片需要时间，可以将图片整合为一张图片，背景图片无法显示，导致出现闪烁情况
		- 将多张图片整合为一张图片，这样可以同时将多张图片一起制作，就不会出现闪烁情况
		- 将多张图片整合在一张图片，减少了图片的总大小，提高请求的速度，增加了用户的体验
	- 制作
		- 调整画布的大小
	- 使用

	```css
	width:200px;
	height:200px;
	background-image:url('')
	// 设置偏移量 设置负值 将要用的图片移动到右上角
	background-position:;
	```

- 浏览器默认样式

	- 去除浏览器默认样式的库 css reset

- 压缩css代码 

	- 使用对应的压缩工具

- ie6 fixed 失效 固定定位

- overflow 的高级用法

	- 当父子元素两层有 overflow: scroll 形成滚动条 自已的 overflow: scroll 会作用给自已

	- 当只有一个时 作用 给 文档

	- 禁止系统默认滚动条 html overflow hidden 和 body 

		```css
		html,body{
			height:100%;
			overflow:hidden;
		}
		```

	- 使用绝对定位模拟固定定位 移动端

	```
	html{
		height:100%;
		overflow:hidden; // 作用给文档
	}
	
	body{
		overflow:auto; // 作用给自已
		height:100%
	}
	
	position:absolute; 
	```

- 浏览器兼容

	- 

- BFC

	- BFC两列布局
	- margin叠加
	- 清除浮动

- css hack

- 居中

- line-height vs vertiacl-align

	- line-height
		- 顶线、中线、基线、底线
		- 行高是指上下文本行的基线的垂直距离，两条红线间垂直距离
			- 行高 行距 半行距
			- 内容区 行内框 行框
	- vertial-align

- 样式的继承 我们为一个元素设置的样式同时也会应用到它的后代元素上

- 样式的冲突

- 选择器的权重

- 浏览器默认样式 reset.csss normalize.css 两个库 重置样式表

	- reset.css  直接去除浏览器的默认样式
	- normalize.css 对默认样式进行统一
	- 自定义 

	```
	*{
	 	margin:0;
	 	padding:0;
	}
	```

	

css3

- HTML5新增语义化标签，功能标签、
- 新增表单种类
- 3.新增表单功能属性
- .2D/3D转换详解
- 3D变形效果
- 滤镜,遮罩效果
- 渐变效果
- bfc
- flex
	- 
- grid
- 媒体查询

```css
@media 媒体类型 and 媒体属性(max-width) and 媒体属性{
	// 规则
}
@media screen and (max-width=500px){
    
}
```

媒体类型

​	all

screen

print

媒体属性

- width 浏览器窗口尺寸
- device-width 设备尺寸
- device-pixel-ratio  （必须加webkit前缀）像素比
	- 可以加min和max前缀
	- min最小值为谁
	- max最大值为谁
- orientation 
	- portrait 竖屏
	- landscape 横屏

关键字 

- and 连接一条查询规则
- only 处理浏览器兼容问题
- `,`
- not 取反

- 多列布局

## 快捷

> [Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

### html

- 所有未知的缩写都将被转换为标签，例如foo → `<foo></foo>`。

> `> 后代、+ 相邻 、^ 父级兄弟、[] 属性、* 个数 、$ 数字通配符、{} 内容、# id、. class @- 倒序 @3 从3开始 () 分组`

- Child:  >
- Sibling：+
- Climb-up：^ (爬上去)  让连接的元素脱离当前的父元素`^、^^`

```html
div+div>p>span+em^bq  // 一层
<div></div>
<div>
    <p><span></span><em></em></p>
    <blockquote></blockquote>
</div>
div+div>p>span+em^^bq  // 两层
<div></div>
<div>
    <p><span></span><em></em></p>
</div>
<blockquote></blockquote>
```

- Grouping: () 分组

> 分组最后一组不用添加（）

```html
div>(header>ul>li*2>a)+footer>p
<div>
    <header>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
</div>
(div>dl>(dt+dd)*3)+footer>p
<div>
    <dl>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
    </dl>
</div>
<footer>
    <p></p>
</footer>
```

- MultipLication: * 个数
- ltem numberring: $  数字通配符

> 可以生成不同的多个值
>
> - [] 属性
>
> - {} 内容
> - $ 后面 倒序 `@-` `*` 个数
> 	- 从某个数字开始`@3` `@数字`

```html
ul>li.item$*3
//  class .item$ itme1
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
</ul>
ul>li[class=item$]{hello $}*3
<ul>
    <li class="item1">hello 1</li>
    <li class="item2">hello 2</li>
    <li class="item3">hello 3</li>
</ul>
h$[title=item$]{Header $}*3
<h1 title="item1">Header 1</h1>
<h2 title="item2">Header 2</h2>
<h3 title="item3">Header 3</h3>
ul>li.item$$$*5
<ul>
    <li class="item001"></li>
    <li class="item002"></li>
    <li class="item003"></li>
</ul>
// 无效 @- @3
ul>li.item$@-*5 // 倒序的方法 .item$@-*5
<ul>
    <li class="item5"></li>
    <li class="item4"></li>
    <li class="item3"></li>
    <li class="item2"></li>
    <li class="item1"></li>
</ul>
ul>li.item$@3*5
<ul>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
    <li class="item6"></li>
    <li class="item7"></li>
</ul>
```

- ID and CLASS attributes

```html
#header
.title
form#search.wide
p.class1.class2.class3
```

- Custom attributes [] 属性

```html
p[title="Hello world"]
<p title="Hello world"></p>
td[rowspan=2 colspan=3 title]
<td rowspan="2" colspan="3" title=""></td>
[a='value1' b="value2"]
<div a="value1" b="value2"></div>
```

- Text: { } 文本

```html
a{Click me}
<a href="">Click me</a>
p>{Click }+a{here}+{ to continue}
<p>Click <a href="">here</a> to continue</p>
```

- Implicit tag names

```html
.class
<div class="class"></div>
em>.class
<em><span class="class"></span></em>
ul>.class
<ul>
    <li class="class"></li>
</ul>
table>.row>.col
<table>
    <tr class="row">
        <td class="col"></td>
    </tr>
</table>
```

- 内容

```html
h1{hello world}
h${hello $}*3
h$[class=item$]{hello $}*3
<h1>hello world</h1>
<h1>hello 1</h1>
<h2>hello 2</h2>
<h3>hello 3</h3>
<h1 class="item1">hello 1</h1>
<h2 class="item2">hello 2</h2>
<h3 class="item3">hello 3</h3>
```

```html
 table>(th>td*3)+(tr>td*3)*3
<table>
    <th>
        <td></td>
    </th>
    <tr>
        <td></td>
    </tr>
</table>
```

### css

- CSS模块使用模糊搜索来查找未知的缩写，例如ov:h==ov-h==ovh==oh。
	如果未找到缩写，则将其转换为属性名称：foo bar→ 食物吧：|；
	您可以使用连字符作为缩写的前缀，以生成以供应商为前缀的属性：-foo

## 基础

> [CSS 参考 - CSS（层叠样式表） | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference)

### 概念

- CSS是一种层叠样式表（ 级联样式表）（Casscading Style Sheet）、是一种层叠样式语言，定义如何显示HTML元素，用于控制Web页面的外观，告诉浏览器如何渲染你的页面

css与html

- CSS简化HTML相关标签，网页体积小，下载速度快
- 解决内容与表现分离的问题
- 更好地维护网页，提高工作效率

- html是一种标记语言，属于浏览器解释型语言，可以直接由浏览器执行，不需要编译

优点

- 使网站适配更多的设备
- 优化网站的SEO
- 减少开发与维护成本
- 提高页面性能	
- 减少HTTP请求数量，是提升页面加载的速度的最佳方法之一

渐进增强和优雅降级

- 渐进增强  Progressive Enhancement：不是一种技术、而是一种开发的方式、更是一种Web设计理念。先确保低端浏览器能看到站点的内容，然后考虑使用非必要的CSS和JavaScript等增强功能，为当前和未来的浏览器提供更好的支持，给用户带来更好的体验

- 优雅降级：为不同设备的用户设计不同级别的不那么完美的应用，就叫做优雅降级

css hack

- hack是浏览器厂商的一种手法，用来增强自已的竞争

注释

```css
/*  */
```

### 语法

- 声明`Delclaration`：CSS 的核心功能是将 CSS 属性设定为特定的值。一个属性与值的键值对被称为声明
- 声明块：将一个或者多个声明用 {} 包裹起来
- CSS 规则集``CSS ruleset`：常简称为 CSS 规则：声明块如果需要作用到对应的 HTML 元素，那还需要加上选择器。选择器和声明块组成了CSS 规则集
- 属性`Property`
- 值`Value`

<img src="https://i.loli.net/2021/08/08/h59yrL6O1UHJg3F.png" alt="https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/dc35c91eb2d64ca1aa829d2f070a2d6f~tplv-k3u1fbpfcp-zoom-1.image" style="zoom:50%;" />

引用css

行内样式

```html
style="color:red;font-size:12px;"
```

内部样式表

```html
<style type="text/css"></style>
```

外部样式表

```html
<link href="xxx.css" rel="stylesheet" type="text/css"/>
```


导入式

```html
<style type="text/css"> @import url()；</style>
```

CSS样式表优先级

- 行内样式>内部样式>外部样式（就近原则）

CSS选择器

- 选择器{(属性：值)声明（样式分隔符）;
- CSS样式规则：选择器，声明

CSS命名规范

- 小写字母开头，不能以数字和“_”,"-"开头
- 英文、数字、“_”、“-”
- 单字，连字符，下划线和驼峰

### 兼容性

- 检测css属性浏览器兼容性：[Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/)

- 浏览器兼容性测试：[Most Reliable App & Cross Browser Testing Platform | BrowserStack](https://www.browserstack.com/)

- 插件、自动添加前缀 ` -prefix-free`

| PC浏览器版本                                             | 手机浏览器      |
| -------------------------------------------------------- | --------------- |
| IE   版本  6~8 、9~10 、11    `6~11`                     | Safari on iOS   |
| Edge  12~90、91  `12~91`                                 | Opera Mini      |
| Safri  3.1 - 4、5 、5.1 - 6.1、7 - 14、14.1、15   `3~15` | Android Browser |
| Opera  10.1、11.5~76、77  `10~77`                        | Opera手机浏览器 |
| Firefox  3 - 3.6、4 - 49、50 - 88、89、90 - 91  `3~91`   | UC 浏览器       |
| Chrome  4、`5~90`、91、92~94  `4~94`                     | 火狐浏览器      |

| 浏览器分类（内核） | 浏览器                 | 私有属性的前缀 |
| ------------------ | ---------------------- | -------------- |
| Gecko引擎          | Mozilla(FireFox浏览器) | -moz-          |
| Presto引擎         | Opera                  | -o             |
| KHTML引擎          | Konqueror              | -khtml         |
| Trident引擎        | Internet Explorer      | -ms            |
| webkit引擎         | Chrome                 | -webkit        |

### 特性

- 层叠性：css样式冲突采取的原则（后者覆盖前者)
- 继承性：对于部分属性样式会有天生的继承
- 优先级：选择器优先级算法

#### 层叠性

- 屏幕是一个二维平面，然而HTML元素却是排列在三维坐标系中，x为水平位置，y为垂直位置，z为屏幕由内向外方向的位置，我们在看屏幕的时候是沿着z轴方向从外向内的；由此，元素在用户视角就形成了层叠的关系，某个元素可能覆盖了其他元素也可能被其他元素覆盖；

<img src="css&css3.assets/165fc5323852bd61" alt="img" style="zoom:50%;" />

样式层叠

- 一个元素使用多次设置同一个样式，这将使用最后一次设置的属性值

多重样式优先级

- 优先级是浏览器是通过判断哪些属性值与元素最相关以决定并应用到该元素上的。优先级仅由选择器组成的匹配规则决定的。

优先级就是分配给指定的CSS声明的一个权重，它由匹配的选择器中的每一种选择器类型的数值决定。

- (内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式（浏览器缺省数组）

选择器优先级

- 通用选择器（*）< 元素(类型)选择器 < 类选择器 < 属性选择器 <  伪类 < ID 选择器 < 内联样式

选择器优先级权重

优先级就是分配给指定的 CSS 声明的一个权重，它由匹配的选择器中的每一种选择器类型的数值决定。为了记忆，可以把权重分成如下几个等级，数值越大的权重越高：

<img src="css&css3.assets/IQmRwYsETufbMtg.png" alt="img" style="zoom:50%;" />

- 10000：!important；
- 01000：内联样式；
- 00100：ID 选择器；
- 00010：类选择器、伪类选择器、属性选择器；
- 00001：元素选择器、伪元素选择器；
- 00000：通配选择器、层次选择器

CSS 优先级法则

-  A 选择器都有一个权值，权值越大越优先；
-  B 当权值相等时，后出现的样式表设置要优于先出现的样式表设置；
-  C 创作者的规则高于浏览者：即网页编写者设置的CSS 样式的优先权高于浏览器所设置的样式；
-  D 继承的CSS 样式不如后来指定的CSS 样式；
-  E 在同一组属性设置中标有``!important`规则的优先级最大；

```css
#main{
    color:red !important;
}
```

#### 继承性



#### 文档流



#### 盒模型

- outline
- border
- margin
- content
- padding

### 文件组成

- 注释
- CSS规则集
- @规则

@规则

- CSS 规则是样式表的主体，通常样式表会包括大量的规则列表。但有时候也需要在样式表中包括其他的一些信息，比如字符集，导入其它的外部样式表，字体等，这些需要专门的语句表示。 

| 语句       | 规则                                                         |
| ---------- | ------------------------------------------------------------ |
| @namespace | 告诉 CSS 引擎必须考虑XML命名空间。                           |
| @media     | 如果满足媒体查询的条件则条件规则组里的规则生效。             |
| @page      | 描述打印文档时布局的变化.                                    |
| @font-face | 描述将下载的外部的字体。                                     |
| @keyframes | 描述 CSS 动画的关键帧。                                      |
| @document  | 如果文档样式表满足给定条件则条件规则组里的规则生效。 (推延至 CSS Level 4 规范) |
| @charset   | 定义样式表使用的字符集                                       |
| @import    | 告诉 CSS 引擎引入一个外部样式表                              |
| @supports  | 查询特定的 CSS 是否生效                                      |

```css
@charset "UTF-8"
```

- CSS文件 字符编码规则 浏览器有一套识别顺序（优先级由高到低）：
	- 文件开头的 Byte order mark 字符值，不过一般编辑器并不能看到文件头里的 BOM 值；
	- HTTP 响应头里的 content-type 字段包含的 charset 所指定的值，比如：Content-Type: text/css; charset=utf-8
	- CSS 文件头里定义的 @charset 规则里指定的字符编码；
	- `<link>` 标签里的 charset 属性，该条已在 HTML5 中废除；
	- 默认是 UTF-8。

link 和 @import 都能导入一个样式文件，它们有什么区别嘛？

- link 是 HTML 标签，除了能导入 CSS 外，还能导入别的资源，比如图片、脚本和字体等；而 @import 是 CSS 的语法，只能用来导入 CSS；
- link 导入的样式会在页面加载时同时加载，@import 导入的样式需等页面加载完成后再加载；
- link 没有兼容性问题，@import 不兼容 ie5 以下；
- link 可以通过 JS 操作 DOM 动态引入样式表改变样式，而@import不可以。

@support

```css
@support (--foo:blue){
body{
		color:var(--varName)
	}
}
```

## 选择器

`Selector`

五大类选择器 `巧记：基层属两伪`

- 基本选择器	5种
- 层次选择器   3种

- 属性选择器
- 伪类选择器 6 种
- 伪元素   4种

### 基本选择器

基本选择器

| 选择器   | 基本选择器                          | 版本 |
| -------- | ----------------------------------- | ---- |
| `E`      | 元素(标签)选择器                    | 1    |
| `#`      | ID选择器  id 属性不要以数字开卡的id | 1    |
| `.class` | 类选择器 描述一组元素的样式         | 1    |
| `*`      | 通配选择器                          | 2    |

- 滥用使用通配选择符，滥用他会造成一些意向不到的结果。首页就是他会给所有的元素都添加上对应的属性，即使这个元素压根就用不到这个属性，这样就造成了一定的性能浪费。另外一点则是非常容易忽视的地方在于他的优先级，也是我们说的特指度，通用选择器的特指度为0，结合上面的继承来说，继承是没有特指度的，因此你如果用了通用选择符，然后指望元素通过继承获得父元素的继承属性，却会发现不起作用。来看个

- 通配选择符 的优先级 大于 继承

集合选择器

| 集合选择器                     | 选择器      | 说明           | 版本 |
| ------------------------------ | ----------- | -------------- | ---- |
| 分组(群组)选择器（并集选择器） | h1,h2,h3{ } | 多个元素       | 1    |
| 嵌套选择器（交集选择器）       | h1 .red{ }  | 指定类名的元素 | 1    |

### 层次选择器

| 选择器  | 层次选择器           | 说明                  | 版本 |
| ------- | -------------------- | --------------------- | ---- |
| `E  F`  | 后代选择器           | 后代                  | 1    |
| `E > F` | 子选择器             | 子代                  | 2    |
|         | 兄弟选择器           |                       |      |
| `E + F` | 相邻兄弟(同胞)选择器 | 相邻的同胞元素 (一个) | 2    |
| `E ~ F` | 通用兄弟选择器       | 后面的同胞元素(多个)  | 3    |

> 相邻兄弟选择器 与 普通兄弟选择器：
>
> - 相邻兄弟选择器`+`选取，紧跟在另一元素后的元素
> - 普通兄弟选择器`~`，选择多个

### 属性选择器

| 选择器                            | 说明                                         | 版本 |
| --------------------------------- | -------------------------------------------- | ---- |
| `E[attr]` 属性                    | 指定属性的元素                               | 2    |
| `E[attr=val] `属性=值             | 属性等于指定值的元素                         | 2    |
| `E[attr*=val] `包含val 字符串     | 属性以指定值(完整单词)开头的元素(不推荐使用) | 3    |
| `E[attr^=val] `val开头            | 属性以指定值开头的元素                       | 3    |
| `E[attr$=val] `val结尾            | 属性以指定值结尾的元素                       | 3    |
| `E[attr~=val] `包含val 有空格隔开 | 属性包含指定值(完整单词)的元素(不推荐使用)   | 2    |
| `E[attr|=val] `val val-前缀       | 属性以指定值(完整单词)开头的元素(不推荐使用) | 2    |

```css
[title]
{
    color:blue;
}
[title=runoob]
{
    border:5px solid green;
}
[title~=hello] { color:blue; }
[lang|=en] { color:blue; }
input[type="button"]
{
    width:120px;
    margin-left:35px;
    display:block;
}
```

### 伪类选择器

伪类（Pseudo-classes）用来添加一些选择器的特殊效果

> 动态目标语言否定状态结构

#### 动态伪类选择器

（用户行为伪类选择器）active（被激活） hover （停留）focus （获得焦点） （链接伪类选择器）link（未访问）/visited（已访问）

| 伪类选择器         | 作用                                      | 版本 |
| ------------------ | ----------------------------------------- | ---- |
| 链接伪类选择器     |                                           |      |
| `:link`            | 选择所有未访问链接                        |      |
| `:visted`          | 选择所有访问过的链接                      |      |
| 用户行为伪类选择器 |                                           |      |
| `:active`          | 选择正在活动链接                          |      |
| `:hover`           | 把鼠标放在链接上的状态 	鼠标悬浮的元素 |      |
| `:focus`           | 元素输入后具有的焦点                      |      |

#### 状态伪类选择器

E:checked enable disable

| 选择器    | 作用     | 版本 |
| --------- | -------- | ---- |
| E:checkde | 选中状态 |      |
| E:enable  |          |      |
| E:disable | 禁用状态 |      |

#### 结构伪类选择器

- 结构选择器

| 选择器  | 作用                                | 版本 |
| ------- | ----------------------------------- | ---- |
| E:root  | 根元素                              | 3    |
| E:empth | 没有子元素的元素                    | 3    |
| child   | fist/last/nth/nth-last-child()/only |      |
| of-type | fist/last/nth/nth-last-child()/only |      |

搭配

- first last nth nth-last  only 5  *  2
- child of-type

|         | first                           | last                             | nth                                        | nth-last-child()                              | only                                     |
| ------- | ------------------------------- | -------------------------------- | ------------------------------------------ | --------------------------------------------- | ---------------------------------------- |
| child   | first-child                     | last-child                       | nth-child(n)                               | nth-last-child(n)                             | only-child（父元素仅有该元素的元素）     |
| of-type | first-of-type(标签中为首的标签) | last-of-type(	标签中为尾标签) | nth-of-type(n)（标签中指定顺序索引的标签） | nth-last-of-type(n)(标签中指定逆序索引的标签) | only-of-type(	父元素仅有该标签的标签) |

child

- E:first-child  E:last-child  父元素第一个、最后一个
- E F:nth-child(n)  E F:nth-last-child(n) 第几个元素、最后几个元素

of-type

- E:first-of-type 、E:last-of-type、E:nth-of-type(n)、E:nth-last-of-type(n) 指定类型的第一个、最后一个 指定类型第几个元素

only

- E:only-child E:only-of-type-child(n) E:only-child  只包含一个子元素	
- E:only-of-type-child(n) 包含同一类型的子元素

#### 目标伪类选择器 `:target`

| 伪类选择器     | 作用    |
| -------------- | ------- |
| 目标伪类选择器 | :target |

#### 语言伪类选择器 `:lang`

`:lang(it)` 带有指定lang属性开始的元素添加样式

| 伪类选择器     | 作用               | 版本 |
| -------------- | ------------------ | ---- |
| 语言伪类选择器 | 指定标记语言的元素 | 2    |

```css
 E:lang[language]
```

#### 否定伪类选择器 `:not`

| 选择器 | 说明 | 版本 |
| ------ | ---- | ---- |
| :not   |      |      |

```html
p:lang(it){
	background:yellow;
}
<p lang="it">Hello Message</p>
```

### 伪元素

| 伪元素             | 符号                | 版本 |
| ------------------ | ------------------- | ---- |
| 首字               | `::first-letter`    | 1    |
| 首行               | `::first-line`      | 1    |
| 之前/之后          | `::before//::after` | 2    |
| 匹配突出显示的文本 | `::selection`       | 3    |
| 全屏模式的元素     | `::backdrop`        | 4    |
| 表单元素的占位     | `::placeholder`     | 4    |

## 元素

### 链接


链接状态：

- link visted hover active focus
	- a:link - 正常，未访问过的链接
	- a:visited - 用户已访问过的链接
	- a:hover - 当用户鼠标放在链接上时
	- a:active - 链接被点击的那一刻
```css
a:link {color:#000000;}      /* 未访问链接*/
a:visited {color:#00FF00;}  /* 已访问链接 */
a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
a:active {color:#0000FF;}  /* 鼠标点击时 */
// a:hover 在 a:link 和 a:vistited 后面
// a:active 在 a:hover 后面
```
### 列表

CSS列表属性：
- 设置不同的列表项标记为有序列表
- 设置不同的列表项标记为无序列表
- 设置列表项标记为图像
| 属性                                                         | 描述                                               |                                                              |
| :----------------------------------------------------------- | :------------------------------------------------- | ------------------------------------------------------------ |
| [list-style](https://www.runoob.com/cssref/pr-list-style.html) | 简写属性。用于把所有用于列表的属性设置于一个声明中 | none，disc(实心圆)，circle，square（实心方块），decimal（阿拉伯数字），lower-alpha（小英），upper-alpha，lower-roman，upper-roman（大罗） |
| [list-style-image](https://www.runoob.com/cssref/pr-list-style-image.html) | 将图像设置为列表项标志。                           |                                                              |
| [list-style-position](https://www.runoob.com/cssref/pr-list-style-position.html) | 设置列表中列表项标志的位置。                       |                                                              |
| [list-style-type](https://www.runoob.com/cssref/pr-list-style-type.html) | 设置列表项标志的类型。                             |                                                              |
```html
list-style: square url('')  0px 10px;
list-style:list-style-type image position
```
### 表格

- 文字对齐  text-align:
- 垂直对齐属性设置垂直对齐，比如顶部，底部或中间 vertical-align:bottom;
- border-collapse 显示一个表的单个边框

### 图片

- width 属性设置为 100% 图片会比它的原始图片大
- max-width 属性设置为 100%, 图片永远不会大于其原始大小
- background-size 属性设置为 "100% 100%" ，背景图片将延展覆盖整个区域
- background-size 属性设置为 "cover"，则会把背景图像扩展至足够大，以使背景图像完全覆盖背景区域。注意该属性保持了图片的比例因此 背景图像的某些部分无法显示在背景定位区域中

### 视频

- width设置为100% 视频播放器会根据屏幕大小自动调整比例
	max-width属性设置为100% 根据屏幕自动调整   ~d比例，但不会超过其原始大小

## 盒子

### box model

CSS Box Model (盒子模型)

- width | height 
- min-width | max-width min-width | max-width
- magin(外边距) border(边框) padding(内边距) content(内容) outline(轮廓)

### box-sizing

<div style="display:flex">
     <img src="css&css3.assets/172633c783abc1eb" alt="img" style="zoom: 50%;"/>
	 <img src="css&css3.assets/17263443113eb879" alt="img" style="zoom:50%; " />
</div>

盒模型有 2 种：标准盒模型和 IE 盒模型，本别是由 W3C 和 IExplore 制定的标准。

- 标准(W3C)盒模型 content-box 
  - 盒子的实际尺寸 = 内容（设置的宽/高）+ 内边距 + 边框 
  - width、height = content 内容的宽度 不包括border 和 padding
- IE 盒模型 border-box 
  - 盒子的实际尺寸 = 设置的宽/高  =  内容 + 内边距 + 边框
  - width、height包含border和padding，指的是content+padding+border。
  	- width = border + padding + 内容的宽度
  	- height = border + padding + 内容的高度
- 区别： 标准盒子模型盒子的`height`和`width`是`content`（内容）的宽高，而IE盒子模型盒子的宽高则包括`content+padding+border`部分。

> - ie8+浏览器中使用哪个盒模型可以由box-sizing(CSS新增的属性)控制，默认值为content-box，即标准盒模型；如果将box-sizing设为border-box则用的是IE盒模型。
> - 如果在ie6,7,8中DOCTYPE缺失会触发IE模式。
> - 在当前W3C标准中盒模型是可以通过box-sizing自由的进行切换的。

css的盒模型由content(内容)、padding(内边距)、border(边框)、margin(外边距)组成。但盒子的大小由content+padding+border这几部分决定，把margin算进去的那是盒子占据的位置，而不是盒子的大小！

### outline

<img src="https://i.loli.net/2020/08/19/y2E5zwhOoDFIsqT.gif" alt="Outline" style="zoom: 50%;" />

轮廓（outline）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。
轮廓（outline）属性指定元素轮廓的样式、颜色和宽度。

| 属性                                                         | 说明                           | 值                                                           | CSS  |
| :----------------------------------------------------------- | :----------------------------- | :----------------------------------------------------------- | :--- |
| [outline](https://www.runoob.com/cssref/pr-outline.html)     | 在一个声明中设置所有的轮廓属性 | *outline-color outline-style outline-width *inherit          | 2    |
| [outline-color](https://www.runoob.com/cssref/pr-outline-color.html) | 设置轮廓的颜色                 | *color-name hex-number rgb-number *invert inherit            | 2    |
| [outline-style](https://www.runoob.com/cssref/pr-outline-style.html) | 设置轮廓的样式                 | none dotted dashed solid double groove ridge inset outset inherit | 2    |
| [outline-width](https://www.runoob.com/cssref/pr-outline-width.html) | 设置轮廓的宽度                 | thin medium thick *length *inherit                           | 2    |

```css
outline: outline-color outline-style outline-width inherit;
```

### border

| 属性                                                         | 值                                                           | 描述                                                         |
| :----------------------------------------------------------- | ------------------------------------------------------------ | :----------------------------------------------------------- |
| [border](https://www.runoob.com/cssref/pr-border.html)       |                                                              | 简写属性，用于把针对四个边的属性设置在一个声明。             |
| [border-style](https://www.runoob.com/cssref/pr-border-style.html) |                                                              | 用于设置元素所有边框的样式，或者单独地为各边设置边框样式。   |
| [border-width](https://www.runoob.com/cssref/pr-border-width.html) |                                                              | 简写属性，用于为元素的所有边框设置宽度，或者单独地为各边边框设置宽度。 |
| [border-color](https://www.runoob.com/cssref/pr-border-color.html) |                                                              | 简写属性，设置元素的所有边框中可见部分的颜色，或为 4 个边分别设置颜色。 |
| [border-bottom](https://www.runoob.com/cssref/pr-border-bottom.html) |                                                              | 简写属性，用于把下边框的所有属性设置到一个声明中。           |
| [border-bottom-color](https://www.runoob.com/cssref/pr-border-bottom-color.html) |                                                              | 设置元素的下边框的颜色。                                     |
| [border-bottom-style](https://www.runoob.com/cssref/pr-border-bottom-style.html) | dotted(点线框) dashed （虚线框）solid（实线） double groove ridge inset outset | 设置元素的下边框的样式。                                     |
| [border-bottom-width](https://www.runoob.com/cssref/pr-border-bottom-width.html) |                                                              | 设置元素的下边框的宽度。                                     |
| [border-left](https://www.runoob.com/cssref/pr-border-left.html) |                                                              | 简写属性，用于把左边框的所有属性设置到一个声明中。           |
### margin

<img src="https://i.loli.net/2020/08/19/Y6udvWjNsEDSHeB.png" alt="img" style="zoom:50%;" />

| 属性                                                         | 描述                                       |
| :----------------------------------------------------------- | :----------------------------------------- |
| [margin](https://www.runoob.com/cssref/pr-margin.html)       | 简写属性。在一个声明中设置所有外边距属性。 |
| [margin-bottom](https://www.runoob.com/cssref/pr-margin-bottom.html) | 设置元素的下外边距。                       |
| [margin-left](https://www.runoob.com/cssref/pr-margin-left.html) | 设置元素的左外边距。                       |
| [margin-right](https://www.runoob.com/cssref/pr-margin-right.html) | 设置元素的右外边距。                       |
| [margin-top](https://www.runoob.com/cssref/pr-margin-top.html) | 设置元素的上外边距。                       |
- 可以使用负值，重叠内容

### padding
- padding 内边框 填充
| 属性                                                         | 说明                                       |
| :----------------------------------------------------------- | :----------------------------------------- |
| [padding](https://www.runoob.com/cssref/pr-padding.html)     | 使用简写属性设置在一个声明中的所有填充属性 |
| [padding-bottom](https://www.runoob.com/cssref/pr-padding-bottom.html) | 设置元素的底部填充                         |
| [padding-left](https://www.runoob.com/cssref/pr-padding-left.html) | 设置元素的左部填充                         |
| [padding-right](https://www.runoob.com/cssref/pr-padding-right.html) | 设置元素的右部填充                         |
| [padding-top](https://www.runoob.com/cssref/pr-padding-top.html) | 设置元素的顶部填充                         |
### content

## 内容

> [CSS的常用属性速查表](https://juejin.cn/post/6844904033145061389)

### 边框 border

#### border 边框

```css
border:border-width boder-style boder-color
// 边框粗细 边框类型 边框颜色
border-width:
border-style:
border-color:
```

```css
// 设置四边
border-top/right/left/bottom-width/color/style
设置四边
border
上左下右
上下 左右
// 设置单边
border-top
border-right
border-bottom
border-left
```

#### border-radius 圆角

> border-radius 圆形、椭圆形

```css
border-radius: border-top-left-radius border-top-right-radius border-bottom-right-radius border-bottom-left-radius;
```

| 属性          | 描述                                      |
| :------------ | :---------------------------------------- |
| border-radius | 所有四个边角 border-*-*-radius 属性的缩写 |

<div style="width:150px;height:150px;border-radius:50%;background:blue;margin:0 auto"></div>

| 属性          | 说明                                           | CSS  |
| :------------ | :--------------------------------------------- | :--- |
| border-radius | 一个用于设置所有四个边框- *-半径属性的速记属性 | 3    |

```css
border-image:url(border.png) 30 30  round;
border-image属性是速记属性用于设置 border-image-source, border-image-slice, border-image-width, border-image-outset 和border-image-repeat 的值。
```

#### border-image 边框图片

| 属性                                                         | 说明                         | CSS  |
| :----------------------------------------------------------- | :--------------------------- | :--- |
| [border-image](https://www.runoob.com/cssref/css3-pr-border-image.html) | 设置所有边框图像的速记属性。 | 3    |

```

```

####  `box-shadow` 阴影

> box-shadow: *h-shadow v-shadow blur spread color* inset;
>
> box-shadow: 10px 10px 5px red insert(内侧阴影);
>
> box-shadow: 水平阴影位置、垂直阴影位置、模糊距离（blur）、阴影大小(spread)、阴影颜色、内阴影/外阴影（默认值）；

| 值         | 说明                                         |
| :--------- | :------------------------------------------- |
| *h-shadow* | 必需的。水平阴影的位置。允许负值             |
| *v-shadow* | 必需的。垂直阴影的位置。允许负值             |
| *blur*     | 可选。模糊距离                               |
| *spread*   | 可选。阴影的大小                             |
| *color*    | 可选。阴影的颜色。                           |
| inset      | 可选。从外层的阴影（开始时）改变阴影内侧阴影 |

### 背景 `background`

#### background css2.1 5个

> background：color image repeat attachment position;
>
> background: 颜色\图片\重复\固定\位置;
>
> background-color
>
> background-image
>
> background-repeat
>
> background-attachment：scroll 滚动、fixed 固定
>
> background-position

- background-color 背景颜色
- background-image 图像设置为背景
- background-repeat 背景图像是否及如何重复
- background-attachment  背景图像是否固定或者随着页面的其余部分滚动。
- background-position 背景图像的起始位置
	背景- 简写属性
	当使用简写属性时，属性值的顺序为：:
- background-color
- background-image:`url('')`
- background-repeat :`repeat-x  repeat-y  no-repeat`
- background-attachment scroll fixed local
- background-position:`top bottom center left right center`

```css
body {background:#ffffff url('img_tree.png') no-repeat right top;}
background:颜色 color 图片image 重复repeat 位置position(水平，垂直);
background-attachment: 滚动;
```

重点

- background-attachment `scroll（滚动 默认） fixed（背景图像固定） inherit（继承） local（随滚动元素滚动）`
- background-clip 制定背景绘制区域 `border-box(默认值，剪切成边框方框) | padding-box（剪切成距方框） | content-box（剪切成内容方框）`

#### background css3

| 顺序                                                         | 描述                             | CSS  |
| :----------------------------------------------------------- | :------------------------------- | :--- |
| [background-clip](https://www.runoob.com/cssref/css3-pr-background-clip.html) | 规定背景的绘制区域。背景裁剪     | 3    |
| [background-origin](https://www.runoob.com/cssref/css3-pr-background-origin.html) | 规定背景图片的定位区域。背景原点 | 3    |
| [background-size](https://www.runoob.com/cssref/css3-pr-background-size.html) | 规定背景图片的尺寸。背景图片大小 | 3    |

重点：background-size 和 width与height 的区别



### 渐变 `gradients`

CSS3 渐变（gradients）可以让你在两个或多个指定的颜色之间显示平稳的过渡。
以前，你必须使用图像来实现这些效果。但是，通过使用 CSS3 渐变（gradients），你可以减少下载的时间和宽带的使用。此外，渐变效果的元素在放大时看起来效果更好，因为渐变（gradient）是由浏览器生成的。
CSS3 定义了两种类型的渐变（gradients）：

- linear-gradient 
- radial-gradient
- repeating-linear-gradient
- conic-gradient 

#### 线性渐变（Linear Gradients）

- 向下/向上/向左/向右/对角方向**

```css
background-image:linear-gradient([[<angle> | to <side-or-corner>],] ? <color-stop>[,<color-stop>] + )
```



#### 径向渐变（Radial Gradients）

- 由它们的中心定义

```css
background-image:radial-gradient([[<shape> || <size>] [at <position>] ?, | at <position>,  ? color-stop ] [color-stop] +)
```



```css
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

#### 重复渐变

```css
background-color:repeating-linear-gradient()
```

conic-gradient 圆锥渐变

### 滤镜 `filter`

[CSS3 filter(滤镜) 属性 | 菜鸟教程](https://www.runoob.com/cssref/css3-pr-filter.html)

```css
filter: none | blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia() | url();
```

blur：高斯模糊
contrast：对比度
drop-shadow：投影，常用于给不规则形状进行
greyscale：灰度
hue-rotate：色调变换

浏览器兼容情况

| Filter                                             | 描述                   |
| -------------------------------------------------- | ---------------------- |
| none                                               | 默认值，没有效果       |
| blur(px)                                           | 给图像设置高斯模糊     |
| brightness(%)                                      | 设置图片亮度           |
| contrast(%)                                        | 调整图像的对比度       |
| drop-shadow(*h-shadow v-shadow blur spread color*) | 给图像设置一个阴影效果 |
| grayscale(%)                                       | 将图像转换为灰度图像   |
| hue-rotate(deg)                                    | 给图像                 |
| invert(%)                                          |                        |
| opacity(*%*)                                       | 转化图像的透明程度     |
| saturate(*%*)                                      | 转换图像饱和度         |
| sepia(*%*)                                         | 将图像转换成           |
| url()                                              |                        |
| inital                                             | 设置属性默认值         |
| inherit                                            | 父元素继承该属性       |

```



```

<img scr="https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png" width="250px" height="250px" />



### 背景滤镜 backdrop-filter

作用于元素背景的滤镜

### object-fit

处理替换元素（如img）的变形问题

### 文本 `text`

| 属性                                                         | 描述                                                    | CSS  |
| :----------------------------------------------------------- | :------------------------------------------------------ | :--- |
| [hanging-punctuation](https://www.runoob.com/cssref/css3-pr-hanging-punctuation.html) | 规定标点字符是否位于线框之外。                          | 3    |
| [punctuation-trim](https://www.runoob.com/cssref/css3-pr-punctuation-trim.html) | 规定是否对标点字符进行修剪。                            | 3    |
| [text-align-last](https://www.runoob.com/cssref/css3-pr-text-align-last.html) | 设置如何对齐最后一行或紧挨着强制换行符之前的行。        | 3    |
| [text-emphasis](https://www.runoob.com/css3/css3-pr-text-emphasis.html) | 向元素的文本应用重点标记以及重点标记的前景色。          | 3    |
| [text-justify](https://www.runoob.com/cssref/css3-pr-text-justify.html) | 规定当 text-align 设置为 "justify" 时所使用的对齐方法。 | 3    |
| [text-outline](https://www.runoob.com/cssref/css3-pr-text-outline.html) | 规定文本的轮廓。                                        | 3    |
| [text-overflow](https://www.runoob.com/cssref/css3-pr-text-overflow.html) | 规定当文本溢出包含元素时发生的事情。                    | 3    |
| [text-shadow](https://www.runoob.com/cssref/css3-pr-text-shadow.html) | 向文本添加阴影。                                        | 3    |
| [text-wrap](https://www.runoob.com/cssref/css3-pr-text-wrap.html) | 规定文本的换行规则。                                    | 3    |
| [word-break](https://www.runoob.com/cssref/css3-pr-word-break.html) | 规定非中日韩文本的换行规则。                            | 3    |
| [word-wrap](https://www.runoob.com/cssref/css3-pr-word-wrap.html) | 允许对长的不可分割的单词进行分割并换行到下一行。        | 3    |

word-break vs word-wrap vs white-space（overflow-wrap）

[彻底搞懂word-break、word-wrap、white-space](https://juejin.cn/post/6844903667863126030)

|                                |                                                              |                                                      |
| ------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------- |
| white-space                    | normal \|nowrap \|pre \|pre-wrap \|pre-line。因为默认是normal | 用来控制空白字符的显示的，同时还能控制是否自动换行。 |
| word-break                     | normal \|break-all \|keep-all。                              | 控制单词如何被拆分换行的                             |
| word-wrap又叫做overflow-wrap： |                                                              |                                                      |

- color 指定文本的颜色
- text-align 文本排列属性是用来设置文本的水平对齐方式 text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸
	- center、right、left、justify
- text-decoration 属性用来设置或删除文本的装饰。
	- none、overline、line-through、underline
- text-transform 文本转换属性是用来指定在一个文本中的大写和小写字母。
	- uppercase（大写）、lowercase（小写）、capitilize（首字母大写）
- text-indent:50px;  文本缩进属性是用来指定文本的第一行的缩进
- text-overflow 文本超出部分截断

```
.text-clamp {
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}
```

- -webkit-text-stroke 文本描边

| 属性                                                         | 描述                             |
| :----------------------------------------------------------- | :------------------------------- |
| [color](https://www.runoob.com/cssref/pr-text-color.html)    | 设置文本颜色                     |
| [direction](https://www.runoob.com/cssref/pr-text-direction.html) | 设置文本方向。                   |
| [letter-spacing](https://www.runoob.com/cssref/pr-text-letter-spacing.html) | 设置字符间距                     |
| [line-height](https://www.runoob.com/cssref/pr-dim-line-height.html) | 设置行高                         |
| [text-align](https://www.runoob.com/cssref/pr-text-text-align.html) | 对齐元素中的文本                 |
| [text-decoration](https://www.runoob.com/cssref/pr-text-text-decoration.html) | 向文本添加修饰                   |
| [text-indent](https://www.runoob.com/cssref/pr-text-text-indent.html) | 缩进元素中文本的首行             |
| [text-shadow](https://www.runoob.com/cssref/css3-pr-text-shadow.html) | 设置文本阴影                     |
| [text-transform](https://www.runoob.com/cssref/pr-text-text-transform.html) | 控制元素中的字母大小写           |
| [unicode-bidi](https://www.runoob.com/cssref/pr-text-unicode-bidi.html) | 设置或返回文本是否被重写         |
| [vertical-align](https://www.runoob.com/cssref/pr-pos-vertical-align.html) | 设置元素的垂直对齐               |
| [white-space](https://www.runoob.com/cssref/pr-text-white-space.html) | 设置元素中空白的处理方式         |
| [word-spacing](https://www.runoob.com/cssref/pr-text-word-spacing.html) | 设置字间距，改变字之间的标准间距 |

重点

- letter-spacing vs word-spacing
	- letter-spacing  每个汉字（字母）之间的间距
	- word-spacing  每个单词之间的间距，如果是汉字无效
- direction 文本方向调转
	- ltr 默认
	- rtl 右到左
	- inherit 继承父元素
- vertical-align 垂直对齐 vs text-align 水平对齐方式
	- vertical-align 垂直对齐
		- baseline（默认） 
		- sub super 
		- top text-top middle bottom text-bottom 
		- length %（可以是负值） inherit
	- text-align 水平对齐
- white-space
	- normal（默认） pre nowrap pre-wrap pre-line inherit



### 字体 `font`

```
<'font-weight'> || <'font-size'> [ / <'line-height'>] || <'font-family'>
```



#### @font-face

使用以前 CSS 的版本，网页设计师不得不使用用户计算机上已经安装的字体。
使用 **CSS3**，网页设计师可以使用他/她喜欢的任何字体。
当你发现您要使用的字体文件时，只需简单的将字体文件包含在网站中，它会自动下载给需要的用户。
您所选择的字体在新的 **CSS3** 版本有关于 **@font-face** 规则描述。
您"自己的"的字体是在 **CSS3 @font-face** 规则中定义的。

| 描述符        | 值                                                           | 描述                                                         |
| :------------ | :----------------------------------------------------------- | :----------------------------------------------------------- |
| font-family   | *name*                                                       | 必需。规定字体的名称。                                       |
| src           | *URL*                                                        | 必需。定义字体文件的 URL。                                   |
| font-stretch  | normalcondensedultra-condensedextra-condensedsemi-condensedexpandedsemi-expandedextra-expandedultra-expanded | 可选。定义如何拉伸字体。默认是 "normal"。                    |
| font-style    | normalitalicoblique                                          | 可选。定义字体的样式。默认是 "normal"。                      |
| font-weight   | normalbold100200300400500600700800900                        | 可选。定义字体的粗细。默认是 "normal"。                      |
| unicode-range | *unicode-range*                                              | 可选。定义字体支持的 UNICODE 字符范围。默认是 "U+0-10FFFF"。 |
| line-height   |                                                              | 字体行高                                                     |



> [Google Fonts](https://fonts.google.com/)
> CSS字体属性定义 `字体，加粗，大小，文字样式`
> 在CSS中，有两种类型的字体系列名称：

- **通用字体系列** - 拥有相似外观的字体系统组合（如 "Serif" 或 "Monospace"）
- **特定字体系列** - 一个特定的字体系列（如 "Times" 或 "Courier"）
- sans-serif 字体比serif字体容易阅读

| Generic family                                               | 字体系列                             | 说明                                        |
| :----------------------------------------------------------- | :----------------------------------- | :------------------------------------------ |
| Serif（有）                                                  | Times New Roman Georgia              | Serif字体中字符在行的末端拥有额外的装饰(有) |
| Sans-serif(无装饰)                                           | Arial Verdana                        | "Sans"是指无 - 这些字体在末端没有额外的装饰 |
| Monospace                                                    | Courier New Lucida Console           | 所有的等宽字符具有相同的宽度                |
| Cursive                                                      |                                      |                                             |
| Fantasy                                                      |                                      |                                             |
| Property                                                     | 描述                                 |                                             |
| :----------------------------------------------------------- | :----------------------------------- |                                             |
| [font](https://www.runoob.com/cssref/pr-font-font.html)      | 在一个声明中设置所有的字体属性       |                                             |
| [font-family](https://www.runoob.com/cssref/pr-font-font-family.html) | 指定文本的字体系列                   |                                             |
| [font-size](https://www.runoob.com/cssref/pr-font-font-size.html) | 指定文本的字体大小                   |                                             |
| [font-style](https://www.runoob.com/cssref/pr-font-font-style.html) | 指定文本的字体样式                   |                                             |
| [font-variant](https://www.runoob.com/cssref/pr-font-font-variant.html) | 以小型大写字体或者正常字体显示文本。 |                                             |
| [font-weight](https://www.runoob.com/cssref/pr-font-weight.html) | 指定字体的粗细。                     |                                             |

- font-size
	- px 
	- em（1em = 16px） pixvels/父元素宽度(默认16px)=em
	- 百分比 与 em

> Google Font 使用 (wen font)
>
> ```css
> // cdn
> link rel="preconnect" href="https://fonts.gstatic.com">
> <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@500&display=swap" rel="stylesheet">
> 
> <style>
> p {
> font-family: 'Noto Sans SC', sans-serif;
> }
> </style>
> ```

font-family

```
font-family:  包含两种类型值就能明白了，一种是字体名称，一种叫做字体族。 字体族就是所有字体的一个分类
 font-family: -apple-system,system-ui,Segoe UI,Roboto,Ubuntu,Cantarell,Noto Sans,sans-serif,BlinkMacSystemFont,Helvetica Neue,PingFang SC,Hiragino Sans GB,Microsoft YaHei,Arial;
```

字体族

- 衬线字体。指的就是笔画开始、结束处有额外的装饰，并且笔画粗细不同。
- 无衬线字体。就是没有装饰，笔画粗细相同。
- 等宽字体。字形的宽度都相等。
- 草书字体。模仿人类手写的字体。
- 奇幻字体。没有归于以上四类字体的其他字体。

sans-serif、Helvetica指的是字体族，前者是衬线字体，后者是无衬线字体。那么这其中的意思就很明确了，如果系统中有前面的字体，那就使用前面的字体，如果没有的话，尝试使用后面的衬线字体，如果没有，则继续往后面的声明中寻找可用字体。

#### 字体清晰 -webkit-font-smoothing

-moz-osx-font-smoothing: inherit | grayscale;

- 这个属性可以使页面上的字体抗锯齿,使用后字体看起来会更清晰舒服。
- 它被列入标准规范的草案中，后由于某些原因从web标准中被移除了。但是，我们可以用以下两种定义进行抗锯齿渲染

```css
-webkit-font-smoothing:antialiased; // 变得非常平滑
其默认可以支持6个值（如图），暂时我能看到效果的就是三个：
none | subpixel-antialiased | antialiased
none：对低像素的文本比较好
subpixel-antialiased：默认值
antialiased：抗锯齿很好

 -webkit-font-smoothing: antialiased;
 -moz-osx-font-smoothing: grayscale;
```

### 行高 line-height

line-height 作用在行内元素或者行内块级元素，声明在块级框上的line-height实际也是作用在块级框中的内容

line-heiht的值可以是数值、百分比以及长度值。当值为数值或者百分比时，相对计算的是其font-size属性 ，``font-size:16px line-height:2`实际 line-height：32px,百分比也是使用这种计算方法。



### 支柱 strut

在CSS中看不见，但却无处不在，有些书中将之称为空白节点。他是支撑内联文本存在的支柱。可以通过这种方法来看到他：

```
.line{
	line-height:0;
	border:1px solid green;
	font-size:20px;
}
```





### 显示 display

Display(显示) 与 Visibility（可见性）
display属性设置一个元素应如何显示，visibility属性指定一个元素应可见还是隐藏。
隐藏元素 - display:none或visibility:hidden
隐藏一个元素可以通过把display属性设置为"none"，或把visibility属性设置为"hidden"。但是请注意，这两种方法会产生不同的结果。
visibility:hidden可以隐藏某个元素，但隐藏的元素仍需占用与未隐藏之前一样的空间。也就是说，该元素虽然被隐藏了，但仍然会影响布局。
**块级元素(block)特性：**

- 总是独占一行，表现为另起一行开始，而且其后的元素也必须另起一行显示;
- 宽度(width)、高度(height)、内边距(padding)和外边距(margin)都可控制;
	**内联元素(inline)特性：**
- 和相邻的内联元素在同一行;
- 宽度(width)、高度(height)、内边距的top/bottom(padding-top/padding-bottom)和外边距的top/bottom(margin-top/margin-bottom)都不可改变，就是里面文字或图片的大小;
	**块级元素主要有：**
- address , blockquote , center , dir , div , dl , fieldset , form , h1 , h2 , h3 , h4 , h5 , h6 , hr , isindex , menu , noframes , noscript , ol , p , pre , table , ul , li
	**内联元素主要有：**
- a , abbr , acronym , b , bdo , big , br , cite , code , dfn , em , font , i , img , input , kbd , label , q , s , samp , select , small , span , strike , strong , sub , sup ,textarea , tt , u , var
	**可变元素(根据上下文关系确定该元素是块元素还是内联元素)：**
- applet ,button ,del ,iframe , ins ,map ,object , script
	**CSS中块级、内联元素的应用：**
	利用CSS我们可以摆脱上面表格里HTML标签归类的限制，自由地在不同标签/元素上应用我们需要的属性。
	主要用的CSS样式有以下三个：
- display:block -- 显示为块级元素
- display:inline -- 显示为内联元素
- display:inline-block -- 显示为内联块元素，表现为同行显示并可修改宽高内外边距等属性
	我们常将所有<li>元素加上display:inline-block样式，原本垂直的列表就可以水平显示了。
	对于 CSS 里的 **visibility** 属性，通常其值被设置成 **visible** 或 **hidden**。
	**visibility: hidden** 相当于 **display:none**，能把元素隐藏起来，但两者的区别在于：
- 1、**display:none** 元素不再占用空间。
- 2、**visibility: hidden** 使元素在网页上不可见，但仍占用空间。
	然而，visibility 还可能取值为 collapse 。
	当设置元素 **visibility: collapse** 后，一般的元素的表现与 **visibility: hidden** 一样，也即其会占用空间。但如果该元素是与 table 相关的元素，例如 table row、table column、table column group、table column group 等，其表现却跟 **display: none** 一样，也即其占用的空间会释放。
	在不同浏览器下，对 **visibility: collapse** 的处理方式不同：
- 1、**visibility: collapse** 的上述特性仅在 Firefox 下起作用。
- 2、在 IE 即使设置了 **visibility: collapse**，还是会显示元素。
- 3、在 Chrome 下，即使会将元素隐藏，但无论是否是与 table 相关的元素，**visibility: collapse** 与 **visibility: hidden** 没有什么区别，即仍会占用空间。

### currentColor



### 透明 `opacity`

```css
img{
	opacity:0.4;
    filter:alpha(opacity=40);
}
```

### 溢出 overflow

CSS overflow 属性用于控制内容溢出元素框时显示的方式。
CSS overflow 属性可以控制内容溢出元素框时在对应的元素区间内添加滚动条。
overflow属性有以下值：

visible：超出部分可见
hidden：超出部分不可见
scroll：超出部分以滚动条形式显示

| 值      | 描述                                                     |
| :------ | :------------------------------------------------------- |
| visible | 默认值。内容不会被修剪，会呈现在元素框之外。             |
| hidden  | 内容会被修剪，并且其余内容是不可见的。                   |
| scroll  | 内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。 |
| auto    | 如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。 |
| inherit | 规定应该从父元素继承 overflow 属性的值。                 |

**注意:**overflow 属性只工作于指定高度的块元素上。
**注意:** 在 OS X Lion ( Mac 系统) 系统上，滚动条默认是隐藏的，使用的时候才会显示 (设置 "overflow:scroll" 也是一样的)。
overflow: visible
默认情况下，overflow 的值为 visible， 意思是内容溢出元素框：

### 反射 `-webkit-box-reflect`







### 文本的行进方向 writing-mode



### 替代字形 font-variant-numeric



### 不能选中 user-select





### 显示的剪切区域 clip-parh



### 非矩形的形状 shape-outside







### vertical-align

[我对CSS vertical-align的一些理解与认识（一） « 张鑫旭-鑫空间-鑫生活](https://www.zhangxinxu.com/wordpress/2010/05/%E6%88%91%E5%AF%B9css-vertical-align%E7%9A%84%E4%B8%80%E4%BA%9B%E7%90%86%E8%A7%A3%E4%B8%8E%E8%AE%A4%E8%AF%86%EF%BC%88%E4%B8%80%EF%BC%89/)

[CSS深入理解vertical-align和line-height的基友关系 « 张鑫旭-鑫空间-鑫生活](https://www.zhangxinxu.com/wordpress/2015/08/css-deep-understand-vertical-align-and-line-height/)

```
 vertical-aligin:top，middle，bottom 数值，百分数，也可以设置负数值 负数值其实就是向下偏移指定的值，百分数就是相对line-height的值设定。
```



```
 <div class="img-box">
        <img src="https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png" alt="">
   </div>
   
.img-box {
    border: 1px solid red;
}

img {
    background-color: red;
}

```

- 上面代码存在一个问题 图片的下面出现了一点间隙。针对这种情况，vertical-align就可以出场了，只要将vertical-align设置为除默认值之外的位置值就可以了。 除了使用vertical-align以外，还可以设置line-height: 0、font-size: 0都能去解决这个问题。原因就在于上面说到strut， 图片是内联元素，因此其也存在一个看不见的文本节点，相当于这样

### 透明 transparent

- 表示完全透明的颜色，该颜色看上去将是背景色。

三角形

```css
div {
	height:0;
	width:0;
    border-top-color: #ffc107;
    border-right-color: #00bcd4;
    border-bottom-color: #e26b6b;
    border-left-color: #cc7cda;
    border-width: 50px;
    border-style: solid;
}
```

等腰三角形：设置一条边有颜色，然后紧挨着的 2 边是透明，且宽度是有颜色边的一半；直角三角形：设置一条边有颜色，然后紧挨着的任何一边透明即可。

```css
//
border-left:30px solid red;
border-top:15px solid transparent
borer-bottom:15px solid transparent


// 直角三角形
border-left:30px solid red;
border-bottom:30px solid transparent;
```

增大点击区域

常常在移动端的时候点击的按钮的区域特别小，但是由于现实效果又不太好把它做大，所以常用的一个手段就是通过透明的边框来增大按钮的点击区域：

```css
.btn {
    border: 5px solid transparent;
}
```

### 遮罩 Mask

mask 属性允许使用者通过遮罩或者裁切特定区域的图片的方式来隐藏一个元素的部分或者全部可见区域。

[奇妙的 CSS MASK](https://juejin.cn/post/6846687594693001223)

### 缩放元素  zoom



Scroll
scroll-behavior
auto：默认滚动行为
smooth：丝滑滚动行为
scroll-snap-type
定义在滚动容器中的一个临时点（snap point）如何被严格的执行

scroll-snap-align
控制将要聚焦的当前滚动子元素在滚动方向上相对于父容器的对齐方式

-webkit-overflow-scrolling
设置为touch可以恢复移动端的弹性滚动

overscroll-behavior
设置为contain可以禁止连锁滚动效果

Writing Modes
writing-mode
定义了文本水平或垂直排布以及在块级元素中文本的行进方向。

这里我们默认是ltr文本（左对齐文本）

horizontal-tb：从左到右水平流动，是默认值
vertical-lr：从上到下垂直流动，下一垂直行位于上一行右侧
vertical-rl：从上到下垂直流动，下一垂直行位于上一行左侧

### Blending

### mix-blend-mode

常用混合模式

multiply：正片叠底
screen：滤色
difference：插值



### svg 

#### clip-path

裁剪路径，用来裁剪出各种形状

#### mask

蒙版，用于创建镂空效果

#### pointer-events

鼠标事件（通常都设为none，表示消除对象的鼠标事件）

### appearance

元素的默认样式（通常都设为none，表示消除默认外观）

### cursor

光标类型，最常用的是pointer，也就是一只手

### user-select

用户是否能选择文本（通常都设为none，表示用户无法选中此文本）

### Scroll

#### scroll-behavior

auto：默认滚动行为
smooth：丝滑滚动行为

#### scroll-snap-type

定义在滚动容器中的一个临时点（snap point）如何被严格的执行

#### scroll-snap-align

控制将要聚焦的当前滚动子元素在滚动方向上相对于父容器的对齐方式

#### -webkit-overflow-scrolling

设置为touch可以恢复移动端的弹性滚动

#### overscroll-behavior

设置为contain可以禁止连锁滚动效果

Writing Modes
writing-mode
定义了文本水平或垂直排布以及在块级元素中文本的行进方向。

这里我们默认是ltr文本（左对齐文本）

horizontal-tb：从左到右水平流动，是默认值
vertical-lr：从上到下垂直流动，下一垂直行位于上一行右侧
vertical-rl：从上到下垂直流动，下一垂直行位于上一行左侧

### Motion Path

#### offset-path

路径的定义

#### offset-distance

对象在路径上的位置

### Others

#### attr()

获取自定义属性的值作为content生成的内容

#### var()

CSS自定义变量

#### calc()

计算值

### @media

媒体查询，用于适配不同设备

#### -webkit-box-reflect

投影

#### percentage

一些数值型单位具有百分比写法，那么这些百分比相对的对象是什么呢？有2种：父元素和自身。

相对父元素：width、height、top、left、margin、padding

相对自身：translateX、translateY

## 动画

css 动画的组成: transition + transform + animation

### transition

> [CSS3的动画属性 - 掘金](https://juejin.im/post/5a424a796fb9a045023be66c)
> [CSS3动画之3D动画 | Aotu.io「凹凸实验室」](https://aotu.io/notes/2016/05/06/CSS3-3D-Animation/)

> transition  n. 过渡；转变
>
> property 属性
>
> duration n. 持续，持续的时间，期间；音长，音延
>
> timing-function 时间函数
>
> delay v 延期；（使）耽搁；推迟 n. 延迟的时间；延期；延时；延迟器

transition 首尾两个状态 两个帧

允许css的属性值在一定的时间区间内平滑地**过渡**。这种效果可以在鼠标单击、获得焦点、被点击或对元素任何改变中触发，并圆滑地以动画效果改变CSS的属性值。
不是所有的CSS属性都支持`transition`，transition元素支持的属性
`transition`需要明确知道，开始状态和结束状态的具体数值，才能计算出中间状态。
[Animatable: One property, two values, endless possibilities](http://leaverou.github.io/animatable/)

> transition ：transition-property || transition-duration || transition-timing-function || transition-delay;

```css
transition: all 1s ease 0s; 属性 时间 函数 变换延迟时间
```

| 值                            | 参数                                                         | 描述                                                         |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| transition-property           | none \|\| all \|\| property                                  | 变换的属性                                                   |
| transition-duration           | time                                                         | 元素 转换过程的持续时间time为数值，单位为s（秒）或者ms(毫秒)，其默认值是0 |
| transition-timing-function    | linear \|\| ease \|\| ease-in \|\| ease-in-out \|\| cubic-bezier(n,n,n,n) | 在延续时间段，变换的速率变化                                 |
| transition-delay              | time                                                         | 变换延迟时间                                                 |
| 值                            | 描述 Description                                             |                                                              |
| ----------------------------- | ------------------------------------------------------------ |                                                              |
| linear                        | 规定以``相同速度``开始至结束的过渡效果。                     |                                                              |
| ease                          | 规定``慢速开始，然后变快``，然后慢速结束的过渡效果。         |                                                              |
| ease-in                       | 规定以慢速开始的过渡效果。                                   |                                                              |
| ease-out                      | 规定以慢速结束的过渡效果。                                   |                                                              |
| ease-in-out                   | 规定以慢速开始和结束的过渡效果。                             |                                                              |
| cubic-bezier(*n*,*n*,*n*,*n*) | 在 cubic-bezier 函数中定义自己的值。可能的值是 0 至 1 之间的数值。 |                                                              |

> transition-timing-function: 
>
> linear  相同速度
>
> ease || ease-in || ease-out || ease-in-out 慢速开始，然后变快 || 慢速开始 || 慢速结束 || 慢速开始和结束
>
> cubic-bezier(n,n,n,n)
> 重点hover transition 时，属性应该是写在 没有:hover 的元素中

```
// 开始帧#box{ transition属性的位置}// 结束帧#box:hover{}
```

### transform

```css
transform:none || transform-functions
```

| 值               | 属性                                                         | 描述         |
| ---------------- | ------------------------------------------------------------ | ------------ |
| none             | 无                                                           | 没有         |
| translate 移动   | translate(x,y) 2D转换，translate3d(x,y,z) 3D转换，translateX(x) 定义转换，只是用X轴，translateY(y) Y轴 ， translateZ(z) Z 轴 | 移动         |
| rotate 旋转      | rotate(angle) 2D旋转， rotate3d(angle) 3D 旋转， rotateX(angle) X轴的3D旋转，rotateY(angle) Y轴的3D旋转， rotateZ(angle) Z轴的3D旋转 | 旋转         |
| scale 缩放       | scale(x,y) 2D缩放 scale3d(x,y,z) 3D缩放 scaleX(x) X轴缩放 scaleY(y) y轴缩放 scaleZ(z) z轴缩放 | 缩放         |
| skew 扭曲        | shew(x-angle,y-angle)定义X和Y轴的2D倾斜转换，skewX(angle)定义X轴的2D倾斜转换，skewY(angle) 定义Y轴的2D倾斜转换 | 扭曲         |
| transform-origin | transform-origin:X \|\| Y \|\| Z X，Y，Z对应三维坐标         | 元素的中心点 |
| matrix 矩阵变形  |                                                              | 矩阵变形     |

> transform: translate() rotate() skew() scale();
>
> translate() 、scale()、rotate()   `(x,y)  3d(x,y,z) X(x) Y(y) Z(z)` 5个
>
> skew()`(x angle,y angle)、X(angle)、Y(angle)` 3个
>
> transform-origin: X Y Z;
>
> 单位
>
> translate() px
>
> rotate() deg  rotate 是 2D 其余都是3D的
>
> scale() 放大的倍数
>
> skew() deg
>
> 
>
> 注意
>
> skew 的本质就是拉动X轴或者X轴
>
> transform: scale(1.5, 1.5);
>
> transform: translate3d(100px, 100px, 0px);
>
> 只会执行后面的属性

### animation 

定义任意多的关 键帧 + @keyframe

animation

```css
animation: animation-name || animation-duration || animation-timing-function || animation-delay || animation-iteration-count || animation-directionanimation: mykeframe 3s ease 3s infinite normal
```

| 值                        | 属性                                                        | 描述                                                         |
| ------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------ |
| animation-name            |                                                             | 选择器的keyframe名称                                         |
| animation-duration        |                                                             | 动画花费的时间                                               |
| animation-timing-function |                                                             | 动画的速度曲线                                               |
| animation-delay           |                                                             | 延迟时间                                                     |
| animation-iteration-count | n \|\| infinite(无限次)                                     | 播放次数                                                     |
| animation-direction       | normal reverse alternate alternate-reverse initial inherit; | 规定是否应该轮流反向播放动画，默认值是正向                   |
| animation-fill-mode       | animation-fill-mode: none\|\| backwards \|\| both           | 规定当动画不播放时（当动画完成时，或当动画有一个延迟未开始播放时），要应用到元素的样式。 |
| animation-play-state      | animation-play-state:running\|\|paused                      | 指定动画是否正在运行或已暂停。                               |

keyframes
`@keyframes` 让开发者通过指定动画中特定时间点必须展现的关键帧样式（或者说停留点）来控制CSS动画的中间环节。这让开发者能够控制动画中的更多细节而不是全部让浏览器自动处理。
要使用关键帧, 先创建一个带名称的`@keyframes`规则，以便后续使用 `animation-name`这个属性来调用指定的`@keyframes`. 每个`@keyframes` 规则包含多个关键帧，也就是一段样式块语句，每个关键帧有一个百分比值作为名称，代表在动画进行中，在哪个阶段触发这个帧所包含的样式。
关键帧的编写顺序没有要求，最后只会根据百分比按由小到大的顺序触发。

| 值                 | 属性 | 描述                                                         |
| ------------------ | ---- | ------------------------------------------------------------ |
| animationname      |      | 必需。定义动画的名称。                                       |
| keyframes-selector |      | 必需。动画时长的百分比。合法的值：0-100%from（与 0% 相同）to（与 100% 相同） |
| css-style          |      | 必需。一个或多个合法的 CSS 样式属性。                        |

```
@keyframes animationname {keyframes-selector {css-styles;}}@keyframs ky{  0% { top: 0; left: 0px}  50% { top: 30px; left: 20px; }  100% { top: 0; left: 30px;}}
```

JavaScript动画

```css

```

JQuery 动画

```css
$(selector).animate({params},speed,callback);
```

### 转换	`transform`

#### 2D转换

| 属性                                                         | 描述                              | CSS  |
| :----------------------------------------------------------- | :-------------------------------- | :--- |
| [transform](https://www.runoob.com/cssref/css3-pr-transform.html) | 适用于2D或3D转换的元素            | 3    |
| [transform-origin](https://www.runoob.com/cssref/css3-pr-transform-origin.html) | 允许您更改转化元素位置 (变换中心) | 3    |

2D 转换方法

| 函数                            | 描述                                     |
| :------------------------------ | :--------------------------------------- |
| matrix(*n*,*n*,*n*,*n*,*n*,*n*) | 定义 2D 转换，使用六个值的矩阵。         |
| translate(*x*,*y*)              | 定义 2D 转换，沿着 X 和 Y 轴移动元素。   |
| translateX(*n*)                 | 定义 2D 转换，沿着 X 轴移动元素。        |
| translateY(*n*)                 | 定义 2D 转换，沿着 Y 轴移动元素。        |
| scale(*x*,*y*)                  | 定义 2D 缩放转换，改变元素的宽度和高度。 |
| scaleX(*n*)                     | 定义 2D 缩放转换，改变元素的宽度。       |
| scaleY(*n*)                     | 定义 2D 缩放转换，改变元素的高度。       |
| rotate(*angle*)                 | 定义 2D 旋转，在参数中规定角度。         |
| skew(*x-angle*,*y-angle*)       | 定义 2D 倾斜转换，沿着 X 和 Y 轴。       |
| skewX(*angle*)                  | 定义 2D 倾斜转换，沿着 X 轴。            |
| skewY(*angle*)                  | 定义 2D 倾斜转换，沿着 Y 轴。            |

#### 3D转换

转换属性：

| 属性                                                         | 描述                                                         | CSS  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [transform](https://www.runoob.com/cssref/css3-pr-transform.html) | 向元素应用 2D 或 3D 转换。                                   | 3    |
| [transform-origin](https://www.runoob.com/cssref/css3-pr-transform-origin.html) | 允许你改变被转换元素的位置。                                 | 3    |
| [transform-style](https://www.runoob.com/cssref/css3-pr-transform-style.html) | 规定被嵌套元素如何在 3D 空间中显示。 flat：默认 preserve-3d：3d场景 | 3    |
| [perspective](https://www.runoob.com/cssref/css3-pr-perspective.html) | 规定 3D 元素的透视效果。 透视距离                            | 3    |
| [perspective-origin](https://www.runoob.com/cssref/css3-pr-perspective-origin.html) | 规定 3D 元素的底部位置。                                     | 3    |
| [backface-visibility](https://www.runoob.com/cssref/css3-pr-backface-visibility.html) | 定义元素在不面对屏幕时是否可见。 物体后方是否可视            | 3    |

3D 转换方法

| 函数                                                         | 描述                                      |
| :----------------------------------------------------------- | :---------------------------------------- |
| matrix3d(*n*,*n*,*n*,*n*,*n*,*n*, *n*,*n*,*n*,*n*,*n*,*n*,*n*,*n*,*n*,*n*) | 定义 3D 转换，使用 16 个值的 4x4 矩阵。   |
| translate3d(*x*,*y*,*z*)                                     | 定义 3D 转化。                            |
| translateX(*x*)                                              | 定义 3D 转化，仅使用用于 X 轴的值。       |
| translateY(*y*)                                              | 定义 3D 转化，仅使用用于 Y 轴的值。       |
| translateZ(*z*)                                              | 定义 3D 转化，仅使用用于 Z 轴的值。       |
| scale3d(*x*,*y*,*z*)                                         | 定义 3D 缩放转换。                        |
| scaleX(*x*)                                                  | 定义 3D 缩放转换，通过给定一个 X 轴的值。 |
| scaleY(*y*)                                                  | 定义 3D 缩放转换，通过给定一个 Y 轴的值。 |
| scaleZ(*z*)                                                  | 定义 3D 缩放转换，通过给定一个 Z 轴的值。 |
| rotate3d(*x*,*y*,*z*,*angle*)                                | 定义 3D 旋转。                            |
| rotateX(*angle*)                                             | 定义沿 X 轴的 3D 旋转。                   |
| rotateY(*angle*)                                             | 定义沿 Y 轴的 3D 旋转。                   |
| rotateZ(*angle*)                                             | 定义沿 Z 轴的 3D 旋转。                   |
| perspective(*n*)                                             | 定义 3D 转换元素的透视视图。              |

### 过渡	`transition`

| 属性                                                         | 描述                                         | CSS  |
| :----------------------------------------------------------- | :------------------------------------------- | :--- |
| [transition](https://www.runoob.com/cssref/css3-pr-transition.html) | 简写属性，用于在一个属性中设置四个过渡属性。 | 3    |
| [transition-property](https://www.runoob.com/cssref/css3-pr-transition-property.html) | 过渡名称。                                   | 3    |
| [transition-duration](https://www.runoob.com/cssref/css3-pr-transition-duration.html) | 过渡效果花费的时间。默认是 0。               | 3    |
| [transition-timing-function](https://www.runoob.com/cssref/css3-pr-transition-timing-function.html) | 过渡效果的时间曲线。默认是 "ease"。          | 3    |
| [transition-delay](https://www.runoob.com/cssref/css3-pr-transition-delay.html) | 过渡效果何时开始。默认是 0。                 | 3    |

```css
transtion: transition-property duration timing-function delay;
// transtion: 属性 过渡时间 时间曲线 过渡效果结束;

transtion:width .5s ease .2s;
transtion:all .5s;
```

### 动画	`animation keyframes`

| 属性                                                         | 描述                                                         | CSS  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [@keyframes](https://www.runoob.com/cssref/css3-pr-animation-keyframes.html) | 规定动画。                                                   | 3    |
| [animation](https://www.runoob.com/cssref/css3-pr-animation.html) | 所有动画属性的简写属性。                                     | 3    |
| [animation-name](https://www.runoob.com/cssref/css3-pr-animation-name.html) | 规定 @keyframes 动画的名称。                                 | 3    |
| [animation-duration](https://www.runoob.com/cssref/css3-pr-animation-duration.html) | 规定动画完成一个周期所花费的秒或毫秒。默认是 0。             | 3    |
| [animation-timing-function](https://www.runoob.com/cssref/css3-pr-animation-timing-function.html) | 规定动画的速度曲线。默认是 "ease"。                          | 3    |
| [animation-fill-mode](https://www.runoob.com/cssref/css3-pr-animation-fill-mode.html) | 规定当动画不播放时（当动画完成时，或当动画有一个延迟未开始播放时），要应用到元素的样式。 | 3    |
| [animation-delay](https://www.runoob.com/cssref/css3-pr-animation-delay.html) | 规定动画何时开始。默认是 0。                                 | 3    |
| [animation-iteration-count](https://www.runoob.com/cssref/css3-pr-animation-iteration-count.html) | 规定动画被播放的次数。默认是 1。                             | 3    |
| [animation-direction](https://www.runoob.com/cssref/css3-pr-animation-direction.html) | 规定动画是否在下一周期逆向地播放。默认是 "normal"。          | 3    |
| [animation-play-state](https://www.runoob.com/cssref/css3-pr-animation-play-state.html) | 规定动画是否正在运行或暂停。默认是 "running"。               | 3    |

```css
animation:name dutation timing-function fill-modedelay iteration-count direction play-state;
// animation：动画名称，一个周期花费时间，运动曲线（默认ease），动画延迟（默认0），播放次数（默认1），是否反向播放动画（默认normal），是否暂停动画（默认running）

@keyframes 动画名称{
    from:{}
    to:{}
}

@keyframes 动画名称{
    0%:{}
    50%:{}
    100%:{}
}
```

## 高级

### BFC

Box: CSS布局的基本单位
Box 是 CSS 布局的对象和基本单位， 直观点来说，就是一个页面是由很多个 Box 组成的。元素的类型和 display 属性，决定了这个 Box 的类型。 不同类型的 Box， 会参与不同的 Formatting Context（一个决定如何渲染文档的容器），因此Box内的元素会以不同的方式渲染。让我们看看有哪些盒子： block-level box:display 属性为 block, list-item, table 的元素，会生成 block-level box。并且参与 block fomatting context； inline-level box:display 属性为 inline, inline-block, inline-table 的元素，会生成 inline-level box。并且参与 inline formatting context； run-in box: css3 中才有， 这儿先不讲了。



BFC Block Formatting Content 块级格式化上下文

W3C官方解释为：BFC它决定了元素如何对其内容进行定位，以及与其它元素的关系和相互作用，当涉及到可视化布局时，Block Formatting Context提供了一个环境，HTML在这个环境中按照一定的规则进行布局。

 BFC（Block Formatting Context）直译为“块级格式化范围”。是 W3C CSS 2.1 规范中的一个概念，它决定了元素如何对其内容进行定位，以及与其他元素的关系和相互作用 当涉及到可视化布局的时候，Block Formatting Context提供了一个环境，HTML元素在这个环境中按照一定规则进行布局。一个环境中的元素不会影响到其它环境中的布局。比如浮动元素会形成BFC，浮动元素内部子元素的主要受该浮动元素影响，两个浮动元素之间是互不影响的。这里有点类似一个BFC就是一个独立的行政单位的意思。 也可以说BFC就是一个作用范围。可以把它理解成是一个独立的容器，并且这个容器的里box的布局，与这个容器外的毫不相干

- 元素如何对内容定位
- 其他元素的关系和相互作用

BFC是一个完全独立的空间（布局环境），让空间里的子元素不会影响到外面的布局（不受外界影响）。那么怎么使用BFC呢，BFC可以看做是一个CSS元素属性

触发(设置)BFC

- overflow：hidden
- display：inline-block、table-cell 、flex 、table-caption
- position：absolute、fixed
- float的值不能为none

BFC规则

- BFC就是一个块级元素，块级元素会在垂直排列
- BFC就是页面内部容器，不会影响到外部容器的
- 垂直方向的距离由margin决定，属于同一个BFC的两个相邻的标签外边距会发生重叠 与方向无关)
- 计算BFC的高度时，浮动元素也参与计算  
- BFC的区域不会与float的元素区域重叠
- BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面元素，反之亦然
- 每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。

BFC作用

不和浮动元素重叠

如果一个浮动元素后面跟着一个非浮动的元素，那么就会产生一个覆盖的现象

- 生成BFC， 来实现自适应两栏布局

```
    <div class="two-container">
        <div class="left"></div>
        <div class="right"></div>
    </div>
.two-container{
            width: 100vw;
            height: 100vh;
            background-color: palegreen;
        }

        .left{
            width: 200px;
            height: 500px;
            float: left;
            background-color: pink;
        }

        .right{
            height: 700px;
            background-color: yellowgreen;
            // 生成BFC不受外界干扰
            overflow: hidden;
        }
```

清除元素内部浮动

- 计算BFC的高度时，浮动元素也参与计算

```html
  <div class="parent">
        <div class="child"></div>
        <div class="child"></div>
    </div>

     .parent {
            border: 5px solid #fcc;
            overflow: hidden; // 消除子元素的影响
            /* background-color: red; */
            /* overflow: hidden; */
        }

        .child {
            width: 200px;
            height: 200px;
            border: 1px solid gray;
            float: left; // 浮动脱离文档流 出现一个大问题 父元素被影响
        }
```

防止垂直 margin 重叠

- Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠
- 在p外面包裹一层容器，并触发该容器生成一个BFC。那么两个P便不属于同一个BFC，就不会发生margin重叠了。

```
<style>
    .wrap {
        overflow: hidden;
    }
    p {
        color: #f55;
        background: #fcc;
        width: 200px;
        line-height: 100px;
        text-align:center;
        margin: 100px;
    }
</style>
<body>
    <p>Haha</p>
    <div class="wrap">
        <p>Hehe</p>
    </div>
</body>

```

BFC解决什么问题

- 使用float脱离文档流，高度塌陷
	- box设置完float结果脱离文档流，使container高度没有被撑开，从而背景颜色没有颜色出来，解决此问题可以给container触发BFC，上面我们所说到的触发BFC属性都可以设置。

```css
<div class="container">
	<div class="box"</div>	
	<div class="box"</div>
</div>

.box{
	margin:100px;
	weidth:100px;
    height:100px;
    background:red;
    float:left;
}

.container{
    background:green;
    // 设置BFC规则
    display:inline-block;
}
```

- margin边距重叠 margin塌陷问题
	- 盒子的margin外边距设置的是10px，可结果显示两个盒子之间只有10px的距离，这就导致了margin塌陷问题，这时margin边距的结果为最大值，而不是合，为了解决此问题可以使用BFC规则（为元素包裹一个盒子形成一个完全独立的空间，做到里面元素不受外面布局影响），或者简单粗暴方法一个设置margin，一个设置padding。

```html
.box {
    margin: 10px;
    width: 100px;
    height: 100px;
    background: #000;
}

<div class="container">
        <div class="box"></div>
        <p><div class="box"></div></p>
</div>
```

- 两栏布局
	- 第二个div元素为300px宽度，但是被第一个div元素设置Float脱离文档流给覆盖上去了，解决此方法我们可以把第二个div元素设置为一个BFC。

```html
div {
    width: 200px;
    height: 400px;
    border: 1px solid red;
}
.left{
	float: left;
}
.right{
	display: flex;
} 
<div class="left">
       Lorem ipsum dolor sit, amet consectetur adipisicing elit. Modi dolore similique atque voluptas nihil cupiditate laborum nobis, necessitatibus rerum ratione dolores quas, quisquam velit. Soluta natus molestiae nesciunt mollitia harum.
    </div>
    <div class="right">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis aliquam laboriosam dolorem distinctio ipsa? Itaque enim cupiditate similique laudantium ipsam facilis atque est repellendus nam, eius fugiat eaque voluptates nostrum.
    </div>
```

公共类完美解决bfc

```css
.clearfix::before ,.clearfix::after{
    content:' '; 
    display:table;
    clear:both;
}
解决外边距重叠用前两个属性，解决高度塌陷用三个属性。
```

### IFC



### VFM

视觉格式化模型（Visual formatting model）是用来处理和在视觉媒体上显示文档时使用的计算规则。CSS 中一切皆盒子，而视觉格式化模型简单来理解就是规定这些盒子应该怎么样放置到页面中去，这个模型在计算的时候会依赖到很多的因素，比如：盒子尺寸、盒子类型、定位方案（是浮动还是定位）、兄弟元素或者子元素以及一些别的因素。

Formatting context 是 W3C CSS2.1 规范中的一个概念。它是页面中的一块渲染区域，并且有一套渲染规则，它决定了其子元素将如何定位，以及和其他元素的关系和相互作用。最常见的 Formatting context 有 Block fomatting context (简称BFC)和 Inline formatting context (简称IFC)。 CSS2.1 中只有 BFC 和 IFC, CSS3 中还增加了 GFC 和 FFC。

### 浏览器差异



### 格式化上下文





### 层叠上下文

层叠上下文 (堆叠上下文, Stacking Context)、层叠等级 (层叠水平, Stacking Level)、层叠顺序 (层叠次序, 堆叠顺序, Stacking Order)、z-index

可以把他看成是生成了一个独立的空间，内部的任何子元素不管如何设置都无法摆脱父级层叠的限制。也就是说，现在假设有两个元素，一个z-index是100，另外一个是99，两个元素都包含子元素，那么无论这两个元素的子元素设置多大的z-index都是无法覆盖另一兄弟元素的。这么说可能不够直观，来看个





### 变量

> [CSS 变量教程 - 阮一峰的网络日志](http://www.ruanyifeng.com/blog/2017/05/css-variables.html)
>
> [妙用CSS变量，让你的CSS变得更心动](https://juejin.cn/post/6844904084936327182)

css var `--` 变量

sass `$`

less `@`

css变量叫css自定义属性

声明变量的时候，变量名前面要加两根连词线（`--`）。
`var()` 函数读取
全局的变量通常放在根元素`:root`里面，确保任何选择器都可以读取它们。

css变量的优点

- 减少样式代码的重复性
- 增加样式代码的扩展性
- 提高样式代码的灵活性
- 增多一种CSS与JS的通讯方式
- 不用深层遍历DOM改变某个样式

css变量对比Sass和Less的变量

- 浏览器原生特性，无需经过任何转译就可直接运行
- DOM对象一员，极大便利了CSS与JS之间的联系  

声明：--变量名
读取：var(--变量名, 默认值)
类型
普通：只能用作属性值不能用作属性名
字符：与字符串拼接 "Hello, "var(--name)
数值：使用calc()与数值单位连用 var(--width) * 10px
作用域
范围：在当前元素块作用域及其子元素块作用域下有效
优先级别：内联样式 > ID选择器 > 类选择器 = 属性选择器 = 伪类选择器 > 标签选择器 = 伪元素选择器

```css
:root{
  --acolor:red;
  --bgcolor:green;
  --main-color: #4d4e53;
  --main-bg: rgb(255, 255, 255);
  --logo-border-color: rebeccapurple;
  --header-height: 68px;
  --content-padding: 10px 20px;
  --base-line-height: 1.428571429;
  --transition-duration: .35s;
  --external-link: "external link";
  --margin-top: calc(2vh + 20px);
}
```

var 函数用于读取变量

```css
a{
	color:var(--acolor);
	background:var(--bgcolor,purple); // 第二个参数设置默认值,变量不存在，会使用这个默认值
    // 第二个参数不处理内部的逗号或空格，都视作参数的一部分。
    var(--font-stack, "Roboto", "Helvetica");
	var(--pad, 10px 15px 20px);
}
```

`var()`函数还可以用在变量的声明

```css
:root{
	--primary-color:red;
	--logo-text:var(--primary-color)
}
```

注意，``变量值只能用作属性值，不能用作属性名。``

```css
.foo {
  --side: margin-top;
  /* 无效 */
  var(--side): 20px;
}
```

变量值的类型

- 变量可以是一个字符串，可以与其他字符串拼接
- 变量值是数值，不能与数值单位直接连用
- 变量值带有单位，就不能写成字符串

> 重点：数值与单位直接写在一起，这是无效的。必须使用calc()函数，将它们连接。

```css
--bar:'hello';
--foo: var(--bar) 'world'
--num: 100;
margin-top: var(--num)px;
.foo {
  --gap: 20;
  /* 无效 */
  margin-top: var(--gap)px;
}
// 数值与单位直接写在一起，这是无效的。必须使用calc()函数，将它们连接。
.foo {
  --gap: 20;
  margin-top: calc(var(--gap) * 1px);
}
/* 无效 */
.foo {
  --foo: '20px';
  font-size: var(--foo);
}
/* 有效 */
.foo {
  --foo: 20px;
  font-size: var(--foo);
}
```

作用域

> 同一个 CSS 变量，可以在多个选择器内声明。读取的时候，优先级最高的声明生效。这与 CSS 的"层叠"（cascade）规则是一致的。就是在声明的大括号之间有效

```css
<style>
  :root { --color: blue; }
  div { --color: green; }
  #alert { --color: red; }
  * { color: var(--color); }
</style>
<p>蓝色</p>
<div>绿色</div>
<div id="alert">红色</div>  
// 三个选择器都声明了--color变量。不同元素读取这个变量的时候，会采用优先级最高的规则，因此三段文字的颜色是不一样的。
```

响应式布局
兼容性处理

```css
a {
  color: #7F583F;
  color: var(--primary);
}
```

也可以使用`@support`命令进行检测。

```
@supports ( (--a: 0)) {
  /* supported */
}
@supports ( not (--a: 0)) {
  /* not supported */
}
```



### CSS阻塞

## 界面

| 属性                                                         | 说明                                           | CSS  |
| :----------------------------------------------------------- | :--------------------------------------------- | :--- |
| [appearance](https://www.runoob.com/cssref/css3-pr-appearance.html) | 允许您使一个元素的外观像一个标准的用户界面元素 | 3    |
| [box-sizing](https://www.runoob.com/cssref/css3-pr-box-sizing.html) | 允许你以适应区域而用某种方式定义某些元素       | 3    |
| [icon](https://www.runoob.com/cssref/css3-pr-icon.html)      | 为创作者提供了将元素设置为图标等价物的能力。   | 3    |
| [nav-down](https://www.runoob.com/cssref/css3-pr-nav-down.html) | 指定在何处使用箭头向下导航键时进行导航         | 3    |
| [nav-index](https://www.runoob.com/cssref/css3-pr-nav-index.html) | 指定一个元素的Tab的顺序                        | 3    |
| [nav-left](https://www.runoob.com/cssref/css3-pr-nav-left.html) | 指定在何处使用左侧的箭头导航键进行导航         | 3    |
| [nav-right](https://www.runoob.com/cssref/css3-pr-nav-right.html) | 指定在何处使用右侧的箭头导航键进行导航         | 3    |
| [nav-up](https://www.runoob.com/cssref/css3-pr-nav-up.html)  | 指定在何处使用箭头向上导航键时进行导航         | 3    |
| [outline-offset](https://www.runoob.com/cssref/css3-pr-outline-offset.html) | 外轮廓修饰并绘制超出边框的边缘                 | 3    |
| [resize](https://www.runoob.com/cssref/css3-pr-resize.html)  | 指定一个元素是否是由用户调整大小               | 3    |


## 尺寸

CSS 尺寸 (Dimension) 属性允许你控制元素的高度和宽度。同样，它允许你增加行间距。

### 长度

| 属性                                                         | 描述                     |
| :----------------------------------------------------------- | :----------------------- |
| [height](https://www.runoob.com/cssref/pr-dim-height.html)   | 设置元素的高度。         |
| [line-height](https://www.runoob.com/cssref/pr-dim-line-height.html) | 设置行高。               |
| [max-height](https://www.runoob.com/cssref/pr-dim-max-height.html) | 设置元素的``最大高度``。 |
| [max-width](https://www.runoob.com/cssref/pr-dim-max-width.html) | 设置元素的最大宽度。     |
| [min-height](https://www.runoob.com/cssref/pr-dim-min-height.html) | 设置元素的``最小高度``。 |
| [min-width](https://www.runoob.com/cssref/pr-dim-min-width.html) | 设置元素的最小宽度。     |
| [width](https://www.runoob.com/cssref/pr-dim-width.html)     | 设置元素的宽度。         |

- max-width(不大于指定的宽度 不超过指定宽度  ) vs min-width （不小于的指定宽度 不低于指定宽度） vs width （宽度）
- width 不能低于最小宽度（min-width）不能高于最大宽度 (max-width)
- max-height 同理上

```css
div{
	max-width:100px;
    min-width:300px;
    width:200px;
}
 div = min-width:300px;
```

- width和max-width谁的值小，那么就显示为谁的宽度
- width和min-width谁的值大，那么就显示为谁的宽度
- 范围 min-width < x < max-width
- 当三个属性都设置时，相当于取Math.max(min-width, Math.min(width, max-width))

 px em rem vh fr

|          |                                                              |                                                              |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| px       | 像素                                                         | px(pixel)其实应该算是我们最熟悉的长度单位了，是相对屏幕分辨率而言，也是经常被作为其他单位的基准 |
| %        | 百分比                                                       | % 在没有设置 body 高度的情况下，是无法正确获得可视区域的高度的 |
| em       |                                                              |                                                              |
| rem      |                                                              |                                                              |
| 视窗单位 | vw视窗宽度的百分比（1vw 代表视窗的宽度为 1%）<br/>vh视窗高度的百分比<br/>vmin取当前Vw和Vh中较小的那一个值<br/>vmax取当前Vw和Vh中较大的那一个值 |                                                              |
| fr       |                                                              |                                                              |

 calc 属性

vw和vh

有没有一个单位不需要JS和CSS耦合在一起的单位？答案是有的，就是`vw／vh`。

- vw = view width
- vh = view height
- 这两个单位是CSS3引入的，以上称为**视口单位**允许我们更接近浏览器窗口定义大小。

视口单位(Viewport units)

- Q：什么是视口？A：Peter-Paul Koch（”PPK大神”）提出视口的解释是：在桌面端，视口指的是在桌面端，指的是浏览器的可视区域；而在移动端，它涉及3个视口：Layout Viewport（布局视口），Visual Viewport（视觉视口），Ideal Viewport（理想视口）。
- 视口单位中的“视口”，桌面端指的是浏览器的可视区域；移动端指的就是Viewport中的Layout Viewport。

- 比如：浏览器视口尺寸为370px,那么 1vw = 370px * 1% = 6.5px(浏览器会四舍五入向下取7)


#### vh/vw与%区别

> 单位	解释
> vw	1vw = 视口宽度的1%
> vh	1vh = 视口高度的1%
> vmin	选取vw和vh中最小的那个
> vmax	选取vw和vh中最大的那个
>
> vh/vw与%区别在于，
>
> 单位	依赖于
> %	元素的祖先元素
> vh/vw	视口的尺寸

rem



### 颜色

- 颜色关键字
- transparent关键字
- currentColor关键字
- RGB和RGBA
- HSL和HSLA

color 文本 颜色

opacity 颜色透明度

transparent 透明色

currentColor当前元素color的值



#### 256种安全色



#### 颜色模式



#### 色彩模式



#### 颜色关键字

> [CSS 色彩关键字(color keywords)](https://codepen.io/bulandent/pen/gOLovwL)

- css 标准1 16 个颜色 VGA颜色 它们来源于 VGA 显卡所显示的颜色集合而被称为 VGA colors （视频图形阵列色彩）。
- css 标准2  新增orange
- css 标准3  SVG 1.0 是首个正式定义这些关键字的标准（扩展的颜色关键字， X11 颜色或 SVG 颜色）
- css 标准4  新增rebeccapurple
- 目前，CSS 颜色关键字总共有 146 个
- 如果声明的时候的颜色关键字是错误的，浏览器会忽略它



#### RGBA

RGB[A] 颜色是由 R(red)-G(green)-B(blue)-A(alpha) 组成的色彩空间。



#### HSLA

HSL[A] 颜色是由色相(hue)-饱和度(saturation)-亮度(lightness)-不透明度组成的颜色体系。





#### opacity: alphavalue || inherit ( 1不透明 0 完全透明)



#### alpha通道 vs opacity





# 布局

CSS布局方式

- 盒子模型 ：box-sizing/margin/padding/border/width/height
- 表格布局 Table
- 浮动布局  Float  ：float clear
- 定位布局 Position：position/left/right/top/bottom/z-index
- 弹性布局 Flexbox：display：flex /inline-flex
- 网格布局 Grid：display：grid /inline-grid

布局排版指将图形、文本、图像、媒体等可视化信息元素在页面布局上调整位置、尺寸等属性使页面布局变得条理化的过程。

## 文档流布局

按照文档的顺序一个一个显示，块元素独占一行内元素共享一行

## 居中布局

### 水平居中

#### position + transform

此方案兼容至IE9，因为transform兼容性限制

- 高度未知
- transformX:50%;transformY:50%

#### position + margin: 负值

兼容性极佳

- 高度已知
- margin-top: 1/2 子元素高度;margin-left: 1/2 子元素宽度;

#### magin:0 auto wdith 块级元素

#### flex justify-content:center

flex是一个强大的css，生而为布局，它可以轻松的满足各种居中、对其、平分的布局要求，但由于现浏览器兼容性问题，此方案很少被使用，

#### text-center 父 dislplay:inline-block 子 行内元素

text-align:center  inline-block行内元素

```css
.parent{
    text-align: center;
}
.child{
    display: inline-block;
}
```

- text-align 只对行内元素有效 使用 text-align:center 就必须将子元素设置为 display: inline; 或者 display: inline-block;；

#### table  + margin

- 此方案兼容至IE8，可以使用<table/>代替css写法，兼容性良号

```css
.child{
    display: table;
    margin: 0 auto;
}
```



#### grid  grid-template-columns

```css
<div id="box">
    <div></div>
    <div class="two">target item</div>
    <div></div>
</div>

#box {
    width: 300px;
    height: 300px;
    background: #ddd;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}
.two {
    background: orange;
}
```

### 垂直居中

- 垂直居中对齐 - 使用 padding
- 垂直居中 - 使用 line-height
- 垂直居中 - 使用 position 和 transform

设置容器上下 padding 相同实现垂直居中和使用 line-height=height 实现垂直居中仅对单行文本有效，当文本行数超过单行时：

-  **padding**：文本仍然处于容器垂直居中的位置，但是容器的 height 会随着文本行数的增加而增大；
-  **line-height=height**：容器的 height 不变，line-height 是文本的行间距，文本会溢出容器显示；
	多行文本可使用 **vertical-align: middle;** 来实现元素的垂直居中，但是如果子元素的内容体积大于父元素的内容体积时，仍然会溢出，后面需要使用文字溢出处理来解决。

#### flex align-item:center

```css
// 只要设置父元素
display: flex;
flex-direction: column;
justify-content: center; 
```

```css
display:flex;
align-item:center;
```

#### pos + transform

优点：不需要提前知道尺寸
缺点：兼容性一般般

```css
// 不用设置子元素的宽高
position: relative; 

position: absolute;
top: 50%;
// left:50%
transform: translate(0,-50%);
// transform: translate(-50%,-50%);
```

#### pos + margin-top/left 负值 知道尺寸

- 绝对定位和负外边距对块级元素进行垂直居中  pos +  top 、margin-top:-子元素的宽度的一半
- margin-top: -(高度的一半); margin-left: -(宽度的一半);
- 不建议使用绝对定位 absolute，特别是在移动设备上。

```css
position:relative;

// 要设置子元素的宽度和高度
// width height 
position:absolute;
top:50%;
// left:50% 居中
margin-top:-height/2;
// margin-left:-width/2
```

#### pos + magin:auto

- 绝对定位 + margin:auto

```css
position:relative;

width:100px
height:100px
position:absolute;
top:0;
bottom:0;
margin:auto
```

#### padding 

- padding实现子元素的垂直居中
- 缺点：如果高度固定，需要提前计算尺寸（只在某些特定情况适用）

> 给父元素设置相等的上下内边距，子元素自然是垂直居中的，当然这时候父元素是不能设置高度的，要让它自动被填充起来，除非设置了一个正好等于上内边距+子元素高度+下内边距的值，否则无法精确垂直居中。

```css
width:300px
// heihgt:300px
box-sizing:border-box;
padding:50px 0px;

width:100px;
height:100px;
```

#### calc 块级元素

也是个不错的方法。
缺点：需要知道child的尺寸，需要计算，同样的，如果还在使用IE的小伙伴，不推荐。

```
.parent {
    width: 300px;
    height: 300px;
    border: 1px solid red;
    position: relative;
}
.child {
    width: 100px;
    height: 100px;
    background: blue;
    padding: -webkit-calc((100% - 100px) / 2);
    padding: -moz-calc((100% - 100px) / 2);
    padding: -ms-calc((100% - 100px) / 2);
    padding: calc((100% - 100px) / 2);
    background-clip: content-box;
}
```



#### 第三方基准元素

- 设置第三方基准元素 取父元素的50%位置 + margin-top:负数
	- 首先设置一个高度等于父元素高度一半的第三方基准元素，这时该基准元素的底边线就是父元素纵向上的中分线，做完这些之后再给要垂直居中的元素设置一个 margin-top 属性，值的大小是它自身高度的一半取负，则实现垂直居中。

```css
<div id="box">
    <div id="base"></div>
    <div id="child"></div>
</div>


#box {
    width: 300px;
    height: 300px;
    background: #ddd;
}
#base {
    height: 50%;
    background: orange;
}
#child {
    height: 100px;
    background: rgba(131, 224, 245, 0.6); 
    margin-top: -50px;
}

```

#### line-height = height

- line-height  对``单行文本``进行垂直居中

```css
display:inline-block
height:100px;
line-heihgt:100px;
```

- line-height和vertical-align对图片进行垂直居中

```css
height:300px
line-height:300px
// text-align:center;

vertival-aligin:middle;
```

#### 块级元素：伪元素

```css
<div class="parent">
   <span class="child">child</span>
</div>


.parent {
    width: 300px;
    height: 300px;
    border: 1px solid red;
    text-align: center;
}
.child {
    background: blue;
    width: 100px;
    height: 40px;
    display: inline-block;
    vertical-align: middle;
}
.parent::before {
    content: '';
    height: 100%;
    display: inline-block;
    vertical-align: middle;            
}
```



#### table + table-cell + vertical-align:middle

- display:table  和 vertical-align:middle 对容器里的文字进行垂直居中
	- vertical-align 属性只对拥有 valign 特性的 html 元素起作用，例如表格元素中的 <td> <th> 等等，而像 <div> <span> 这样的元素是不行的。
	- valign 属性规定单元格中内容的垂直排列方式

```css
display:table;

display:table-cell;
vertical-align:middle;

.parent {
    width: 600px;
    height: 200px;
    border: 1px solid red;
    display: table;
}
.child {
    display: table-cell;
    vertical-align: middle;
}
```

#### grid

```css
.box>.one+.two+.three 

.box 设置 display:grid
```

#### 块级元素：改成行内块：inline-block + vertical-align: middle;

- 图片和文字垂直居中

```css
<div class="parent">
    <div class="child">child</div>
    <div class="brother">brother</div>
</div>

.child
display: inline-block;
 vertical-align: middle;
```



### 居中对齐

- 水平和垂直居中

```html
<section>
    <div class="box"></div>
</section>    
```

#### table布局

```css
<table>
     <tr>
         <td align="center" valign="middle">content</td> 
     </tr>
 </table>
```

#### 图片居中对齐 pos +   margin: auto;

```css

```

#### 文字对齐 text-aligin height line-height

- 文字  水平居中  子元素`text-align:left/center/right/`
- 文字   垂直居中  父元素`height:100px;line-height:100px 行高`

```css
text-aligin:center
height:100px
line:height:100px
```

#### display:flex与margin:auto

```css
<div class="center-layout">
    <div></div>
</div>
.center-layout {
    display: flex;
    width: 400px;
    height: 400px;
    background-color: #f66;
    div {
        margin: auto;
        width: 100px;
        height: 100px;
        background-color: #66f;
    }
}
```

#### pos + margin: auto

#### position + transform

```css
父元素   
position: relative;
子元素   
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50px, -50px); //w/2 h/2
// transform :translate(-50%,-50%);
```

```css
section {
    height: 100vh;
    background: #7e57c2;
    position: relative;
}
.box{
    width: 100px;
    height: 100px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50px, -50px); //w/2 h/2
    // transform :translate(-50%,-50%);
    background: #4db6ac;
}
```

#### flex justify align center

- 前提设置了宽度和高度设置，要居中 父元素的宽度和高度 父元素 
- display: flex; justify-content: center;align-items: center;

```css
section {    height: 50vh;    width: 50vw;    background: #7e57c2;    display: flex;     justify-content: center;    align-items: center;}.box {    width: 100px;    height: 100px;    background: #4db6ac;}
```

####  grid align-self justify-self center place-self center

```css
父元素  display: grid;子元素  align-self: center; justify-self: center; 
```

```css
section {    height: 50vh;    width: 50vw;    background: #7e57c2;    display: grid;}.box {    width: 100px;    height: 100px;    background: #4db6ac;    align-self: center;     justify-self: center; }
```

####  grid margin:auto 

```css
父元素 display: grid;子元素  margin: auto; 
```

```css
section {
    height: 50vh;
    width: 50vw;
    background: #7e57c2;
    display: grid;
}
.box {
    width: 100px;
    height: 100px;
    background: #4db6ac;
    margin: auto; //
}
```

####  grid place-items: center;

```css
父元素  display: grid;place-items: center;
```

```css
section {
    height: 50vh;
    width: 50vw;
    background: #7e57c2;
    display: grid;
    place-items: center;
}
.box {
    width: 100px;
    height: 100px;
    background: #4db6ac;
}
```

```css
.container{
	display:grid;
	place-item:center;
}
```

```html
place-items:<align-items> <justify-items>;
// align-item 属性控制垂直位置
// justify-items属性控制水平位置。
这两个属性的值一致时，就可以合并写成一个值。所以，place-items: center;等同于place-items: center center;
```

### css布局高度始终为宽度的一半

- vw
	- 点是只需要vw单位就可以实现，缺点是vw单位会包含滚动条宽度

```css
width:100vw;
height:50vw;
```

- vw+var+calc
	- 缺点也是vw单位会包含滚动条宽度，优点是自定义单位可以随意定如何宽度

```css
.box

:root {
    --wwidth: 100vw;
    --hheight: calc(var(--wwidth) / 2);
}
.box {
    width: var(--wwidth);
    height: var(--hheight);
    backgroud:yellow;
    // border: 1px solid red;
    // display: flex;
    // align-items: center;
    // justify-content: center;
    // color: green;
    // font-size: 30px;
}
```

- padding  
	- width:100% padding:50%/2 =25%
	- 优缺点：优点是宽度100%不包含滚动条，缺点是需要两个html标签才能实现

```css
<div class="outer">
	<div class="inner">
        padding
    </div>
</div>

.outer{
	width:100%;
	padding:25% 0;
	position:relative;
// position的作用形成父子元素之间的关系
}

.inner{
	position:absolute;
	left\top\right\bottom:0;
	// display:flex;	
	// aligin-items:center;
	// justify-content:center;
}
```

## List列表布局



## Table 表格布局



## Position 定位布局

position 属性的五个值：

- [static](https://www.runoob.com/css/css-positioning.html#position-static)
- [relative](https://www.runoob.com/css/css-positioning.html#position-relative)
- [fixed](https://www.runoob.com/css/css-positioning.html#position-fixed)
- [absolute](https://www.runoob.com/css/css-positioning.html#position-absolute)
- [sticky](https://www.runoob.com/css/css-positioning.html#position-sticky)
	元素可以使用的顶部，底部，左侧和右侧属性定位。然而，这些属性无法工作，除非是先设定position属性。他们也有不同的工作方式，这取决于定位方法。

| 属性                                                         | 说明                                                         | 值                                                           | CSS  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [bottom](https://www.runoob.com/cssref/pr-pos-bottom.html)   | 定义了定位元素下外边距边界与其包含块下边界之间的偏移。       | auto *length % *inherit                                      | 2    |
| [clip](https://www.runoob.com/cssref/pr-pos-clip.html)       | 剪辑一个绝对定位的元素                                       | *shape *auto inherit                                         | 2    |
| [cursor](https://www.runoob.com/cssref/pr-class-cursor.html) | 显示光标移动到指定的类型                                     | *url* auto crosshair default pointer move e-resize ne-resize nw-resize n-resize se-resize sw-resize s-resize w-resize text wait help | 2    |
| [left](https://www.runoob.com/cssref/pr-pos-left.html)       | 定义了定位元素左外边距边界与其包含块左边界之间的偏移。       | auto *length % *inherit                                      | 2    |
| [overflow](https://www.runoob.com/cssref/pr-pos-overflow.html) | 设置当元素的内容溢出其区域时发生的事情。                     | auto hidden scroll visible inherit                           | 2    |
| [overflow-y](https://www.runoob.com/css/cssref/css3-pr-overflow-y.html) | 指定如何处理顶部/底部边缘的内容溢出元素的内容区域            | auto hidden scroll visible no-display no-content             | 2    |
| [overflow-x](https://www.runoob.com/css/cssref//cssref/css3-pr-overflow-x.html) | 指定如何处理右边/左边边缘的内容溢出元素的内容区域            | auto hidden scroll visible no-display no-content             | 2    |
| [position](https://www.runoob.com/cssref/pr-class-position.html) | 指定元素的定位类型                                           | absolute fixed relative static inherit                       | 2    |
| [right](https://www.runoob.com/cssref/pr-pos-right.html)     | 定义了定位元素右外边距边界与其包含块右边界之间的偏移。       | auto *length % *inherit                                      | 2    |
| [top](https://www.runoob.com/cssref/pr-pos-top.html)         | 定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。 | auto *length % *inherit                                      | 2    |
| [z-index](https://www.runoob.com/cssref/pr-pos-z-index.html) | 设置元素的堆叠顺序,具有高层叠顺序的元素总是在较低的顺序元素之前 | *number *auto inherit                                        | 2    |

## Float  浮动布局

浮动：使元素脱离文档流，浮动起来

| 属性                                                       | 描述                               | 值                           | CSS  |
| :--------------------------------------------------------- | :--------------------------------- | :--------------------------- | :--- |
| [clear](https://www.runoob.com/cssref/pr-class-clear.html) | 指定不允许元素周围有浮动元素。     | left right both none inherit | 1    |
| [float](https://www.runoob.com/cssref/pr-class-float.html) | 指定一个盒子（元素）是否可以浮动。 | left right none inherit      | 1    |

- float 浮动 left 、right、both、none、inherit
- clear 清除浮动：指定元素两侧不能出现浮动元素 left、right、none、inherit

```css
float:right/left;
clear:right/left/both;
```

## Flex伸缩布局

> - [x] [「一劳永逸」48张小图带你领略flex布局之美](https://juejin.cn/post/6866914148387651592)

| flex container                                               | flex itme                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| flex-flow:flex-direction(row row-reverse column column-reverse) flex-wrap(no-wrap wrap wrap-reverse) | flex: flex-grow 拉伸比例 flex-shrink 压缩比例 flex-basis 原始尺寸 |
| justify-content:flex-start flex-end  center space-between space-around | order: number(排列顺序)                                      |
| align-item：flex-start flex-end  center  baseline stretch(默认值) [baseline stretch] | align-self：flex-start flex-end  center space-between space-around  auto  stretch(默认值) [ auto + stretch ] |
| align-content：flex-start flex-end  center space-between space-around  stretch(默认值)  +[justify-content + stretch ] |                                                              |



![flex-父容器属性](css&css3.assets/e2e9733b84e040f296f827ff4148f235~tplv-k3u1fbpfcp-zoom-1.image)

![flex-子容器属性](css&css3.assets/0c5e529f03d345dab4534bf84b1cfd1d~tplv-k3u1fbpfcp-zoom-1.image)

![img](css&css3.assets/0dd26d8e99257ff36443.png)

关于flex 和 inline-flex 的区别

- flex 设置当前元素为块级元素 block-flex  独占一行
- inline-flex 设置当前元素为行内元素 如果兄弟元素为行内元素则 同时 占一行

#### 概念

2009年，W3C 提出了一种新的方案----Flex 布局，可以简便、完整、响应式地实现各种页面布局。目前，它已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。

Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。

FlexBox 由两部分组成：容器（container）和项目（item）

![flex基本概念](https://user-gold-cdn.xitu.io/2017/8/20/7bc6f5073e763bdadba7b3d0b1b4165e?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

- 容器 
	- 父容器  flex container 
	- 子容器 flex item
- 轴 
  -  主轴默认为水平方向，方向向右，交叉轴为主轴顺时针旋转 90°
  - 主轴  main axis  x轴
  - 交叉轴 cross axis y轴

```css
display:flex/inline-flex;
```

- 设为 Flex 布局以后，子元素的 float、clear 和 vertical-align 属性将失效

#### 容器 container 父容器  6个

- flex-flow：flex-direction  ：主轴的方向 flex-wrap 换行
	- flex-direction  4
		- row(默认 左到右) row-reverse（右到左） column（上到下） column-reverse （下到上）
	- flex-wrap 3
		- nowrap(不换行)	wrap (换行)  wrap-reverse(行翻转)
-  jusitfy-content   5 子容器在主轴的排列方向
	- flex-start(默认 左对齐) flex-end （右对齐）
	- center 居中
	- 分散对齐  space-between  （ 两端对齐） 两端对齐，项目之间间隔相等
	- space-around（ 每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。） 均匀排列每个元素，每个元素周围分配相同的空间
- align-item 子容器在交叉轴的排列方向
	- flex-start flex-end 
	- center
	- (重点)baseline  基线对齐 stretch 默认（如果项目未设置高度或设为auto，将占满整个容器的高度）
- align-content  多根轴线的对齐方式
	- 属性同justify-content
	- stretch  延伸 默认值

flex-direction 

- 该元素是主轴的方向 ，如果改变 justify-content 和 align-item 的方向也会改变
	- justify-content 的方向是跟随flex-direction

align-item vs align-content 

- align-item 单根轴线 针对单行元素
- align-content 多根轴线  针对多行元素

justify-content 的 space-around vs pace-between

- space-around  **左右边上有边距**
- space-between **左右边上没有边距**

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [display](https://www.runoob.com/cssref/pr-class-display.html) | 指定 HTML 元素盒子类型。                                     |
| [flex-direction](https://www.runoob.com/cssref/css3-pr-flex-direction.html) | 指定了弹性容器中子元素的``排列方式``                         |
| [justify-content](https://www.runoob.com/cssref/css3-pr-justify-content.html) | 设置弹性盒子元素在``主轴（横轴）方向上的对齐方式。``         |
| [align-items](https://www.runoob.com/cssref/css3-pr-align-items.html) | 设置弹性盒子元素在``侧轴（纵轴）方向上的对齐方式。``         |
| [flex-wrap](https://www.runoob.com/cssref/css3-pr-flex-wrap.html) | 设置弹性盒子的子元素超出父容器时是否``换行``。               |
| [align-content](https://www.runoob.com/cssref/css3-pr-align-content.html) | 修改 flex-wrap 属性的行为，类似 align-items, 但不是设置子元素对齐，而是设置行对齐 |

#### 项目 item 子容器 6个

- flex: flex-grow 拉伸比例flex-shrink 压缩比例 flex-basis 原始尺寸
	- 默认值  0 1 auto
	- 简化
		- flex:1 —> flex:1 1 0%;
		- flex:3 —> flex:3 1 0%;
	- auto 1  1 auto
	- none 0 0 auto 
	- flex-grow 子容器剩余空间的拉伸比例 定义子容器的伸缩比例。按照该比例给子容器分配空间。
	- flex-shrink 子容器超出空间的压缩比例属性定义了子容器弹性收缩的比例。如图，超出的部分按 1:2 的比例从给子容器中减去。此属性要生效，父容器的 flex-wrap 属性要设置为 nowrap
	- flex-basis 子容器在不伸缩情况下的原始尺寸 flex-basis 属性定义了子容器在不伸缩情况下的原始尺寸，主轴为横向时代表宽度，主轴为纵向时代表高度 px 单位
	- flex-grow
		子容器弹性伸展的比例，简单理解，就是把剩余的空间按比例分配给子容器。
	- flex-shrink
		子容器弹性收缩的比例。简单理解，就是当你子容器超出的部分，会按照对应的比例给子容器减去对应的值。
	- flex-basis 设置基准大小
- order 子容器的排列顺序 属性定义项目的排列顺序。数值越小，排列越靠前，默认为 0
- align-self 子容器的 align-self 属性允许单个项目有与其他项目不一样的对齐方式，可覆盖父容器 align-items 属性。默认值为 auto，表示继承父元素的 align-items属性，如果没有父元素，则等同于 stretch。
	- flex-start flex-end 
	- center
	- auto
	- baseline
	- stretch 

| 属性                                                         | 描述                                              |
| :----------------------------------------------------------- | :------------------------------------------------ |
| [flex-flow](https://www.runoob.com/cssref/css3-pr-flex-flow.html) | flex-direction 和 flex-wrap 的简写                |
| [order](https://www.runoob.com/cssref/css3-pr-order.html)    | 设置弹性盒子的子元素排列顺序。                    |
| [align-self](https://www.runoob.com/cssref/css3-pr-align-self.html) | 在弹性子元素上使用。覆盖容器的 align-items 属性。 |
| [flex](https://www.runoob.com/cssref/css3-pr-flex.html)      | 设置弹性盒子的子元素如何分配空间。                |

## Grid 网格布局

> - [ ] [最强大的 CSS 布局 —— Grid 布局](https://juejin.cn/post/6854573220306255880#heading-21)

-  IE 10 以下不支持

子元素div个数 要与 设置的 grid-template row *  grid-template-column 个数一致 

| grid container                                               | grid  item                                                   |      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| grid[template auto]:grid-tempate[grid-template-row grid-template-column grid-template-areas] grid-auto[grid-auto-column grid-auto-row grid-auto-flow 分析 row column /row dense 尽可能填充空格 column dense] | grid-area:grid-row-start / grid-column-start / grid-row-end / grid-column-end \|itemname;   2  /2 / span  2 / span 2 |      |
| grid-gap:grid-row-gap grid-column-grap  [单位px]  间距       | place-self:justify-self align-self  [ start \|end \|center \|stretch;]  子元素 |      |
| place-item:justify-item align-item [ start \|end \|center \|stretch   ]  子元素单元格 |                                                              |      |
| place-content:justify-content align-content [ start \|end \|center \|stretch \|space-around \|space-between \|space-evenly;] 项目整体 |                                                              |      |

repeat()、auto-fill 自动填充、fr、minmax()、auto、网格线的名称[]

- Flex 布局是轴线布局，只能指定"项目"针对轴线的位置，可以看作是**一维布局**(1-Dimension)。

- Grid 布局则是将容器划分成"行"和"列"，产生单元格，然后指定"项目所在"的单元格，可以看作是**二维布局**(2-Dimension)。Grid 布局远比 Flex 布局强大。可以一次控制两个方向 和 表格table布局差不多，是使用css控制的，不是html控制的，同时还可以依赖于媒体查询根据不同的上下文得新定义布局 和 table 不同的是，grid 布局不需要在 HTML 中使用特定的标签布局，所有的布局都是在 CSS 中完成的，你可以随意定义你的 grid 网格。

- 网格布局还可以让我们摆脱现在布局中存在的文档流限制，换句话说，你的结构不需要根据设计稿从上往上布置了。这也意味着您可以自由地更改页面元素位置。这最适合你在不同的断点位置实现你最需要的布局，而不再需要为响应你的设计而担心HTML结构的问题。

- 没有 HTML 结构的网格布局有助于使用流体、调整顺序等技术管理或更改布局。通过结合 CSS 的媒体查询属性，可以控制网格布局容器和他们的子元素，使用页面的布局根据不同的设备和可用空间调整元素的显示风格与定位，而不需要去改变文档结构的本质内容。

### 基本概念

- 容器(container)和项目(item)
	- 容器属性
	- 项目属性
- 行(row)和列(column)
	- 列（column） 决定的是 宽度 
	- 行（row）决定的是 高度
- 单元格(cell)

- 网格线(grid line)：
	- 水平网格线划分出行，垂直网格线划分出列
	- `n`行有`n + 1`根水平网格线，`m`列有`m + 1`根垂直网格线
	容器属性
- 网格区域（grid area）: 任意四条网格线组成的空间，所以他可能包含一个或多个单元格。相当于表格中的合并单元格之后的区域。
- 当元素设置了网格布局，column、float、clear、vertical-align属性无效

### 容器 container  

- 6个 grid-template  grid-gap 间距  grid-auto item content

- grid：grid-template [  column row areas ] grid-auto [ column row flow ]
	- grid-template
		- grid-template-column
		- grid-template-row
		- grid-template-areas
	- grid-auto
		- grid-auto-column
		- grid-auto-row
		- grid-auto-flow
- grid-gap ：gird-row-gap grid-column-gap 间距 
	- grid-row-gap
	- grid-column-gap
- place-content：justify-content align-content 
	- justify-content 
	- align-content 
	- place-content 
- place-item：justify-item align-item
	- justify-item   
	- align-item 
	- place-item

#### grid

```css
display: grid inline-grid
display:grid  块级元素
display:inline-grid; 行内元素
```

##### grid:grid-template auto

- grid-template \ grid-auto
- grid-template-rows、grid-template-columns、grid-template-areas、 grid-auto-rows、grid-auto-columns、grid-auto-flow这六个属性的合并简写形式。

#### grid-template 模板

grid-template属性是grid-template-columns、grid-template-rows和grid-template-areas这三个属性的合并简写形式。

##### grid-template-columns(列) 、grid-template-rows(行)

网格线的名称
grid-template-columns(宽度) / rows (高度) 决定 每个单元格的高度和宽度
重点： 设置的单元格的范围  而不是盒子的具体大小
<img src="C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200925170728159.png" alt="image-20200925170728159" style="zoom:50%;" />

```css
.container{
	display:grid;
    // 一个单元格 250px * 250px
    grid-template-columns: repeat(3,250px);
    grid-template-rows: repeat(3,250px);
}
// 间距 150px gap:column-gap row-gap;
// 
.box{
	width:100px;
	heigh:100px;
}
```

```css
display:grid/inline-grid;
display: grid;
grid-template-rows: 100px 100px 100px; // n行  
grid-template-columns:100px 100px 100px; // n列
// 可以使用百分比
grid-template-rows: 33.33% 33.33% 33.33%;
```

> repeat()、auto-fill 自动填充、fr、minmax()、auto、网格线的名称[]

- repeat()  重复

```css
grid-template-rows:repeat(3,100px);
grid-template-columns:repeat(2,100px 20px 80px); // 100px 20px 80px 100px 20px 80px
```

- auto-fill 单元格的大小是固定，容器的大小不确定。希望每一行（或每一列）``容纳尽可能多的单元格``，

```css
grid-template-colums:repeart(auto-fill,100px);
```

- fr 表示比例关系  1fr *2  = 2fr fr 单位是一个自适应单位，fr单位被用于在一系列长度值中分配剩余空间，如果多个已指定了多个部分，则剩下的空间根据各自的数字按比例分配。
	- 设置列，将宽度按照比例进行分

```css
grid-template-rows: 1fr 1fr 2fr;
grid-template-column: 1fr 1fr 2fr;
// 可以和绝对单位结合使用
grid-template-columns :150px 1fr 2fr;
```

- minmax() 长度范围 创建行或列的最小或最大尺寸，第一个参数定义网格轨道的最小值，第二个参数定义网格轨道的最大值。可以接受任何长度值，也接受 auto 值。auto 值允许网格轨道基于内容的尺寸拉伸或挤压。

```css
grid-template-columns:100px auto 100px;
```

- auto 由浏览器自已决定长度 可以设置 三栏布局

```css
grid-template-column:100px auto 100px;
```

- 网格线的名称:   使用方括号，指定每一根网格线的名字，网格布局允许同一根线有多个名字 `[c1 col1]` 3行 x 3列，因此有4根垂直网格线和4根水平网格线

```css
display：flex;
grid-template-columns:[c1] 100px [c2] 100px [c2] 100px [c3] auto [c4];
grid-template-rows:[r1] 100px [r2] 100px [r3] auto [r4] 
```

- 网页布局

```css
// 两栏布局
grid-template-columns:70% 30%;
// 传统的十二网格布局
grid-template-columns: repeart(12,1fr);
```

> 注意，设为网格布局以后，容器子元素（项目）的`float`、`display: inline-block`、`display: table-cell`、`vertical-align`和`column-*`等设置都将失效。

##### grid-template-areas

更好的对每一元素进行布局  指定区域（一个区域由单个或多个）定义网格区域的名称，然后需要放在对应网格区域的元素

grid-template-areas 属性用于定义区域，一个区域由一个或者多个单元格组成

一般这个属性跟网格元素的 grid-area 一起使用，我们在这里一起介绍。 

grid-area 属性指定项目放在哪一个区域

```css
<div class="wrapper">
  <div class="box header">Header</div>
  <div class="box sidebar">Sidebar</div>
  <div class="box content">Content</div>
</div>

.wrapper
grid-template-columns:repeat(3,100px);
grid-template-areas:
	". header header"
	"sidebar content content"
// 可以随便修改元素块的位置和宽度 和 是否出现

.sidebar
	grid-area:sidebar

.content
	grid-area:content

.header
	grid-area:header
```



#### grid-gap 间距

##### grid-row-gap，grid-column-gap

`最新 gap:<row-gap> <column-gap>;` 取消前缀

grid-gap:  间距 <grid-gap grid-row-gap(行间距) >、<grid-column-gap(列间距) >

```css
grid-gap:grid-row-gap grid-column-grap;
gap:<row-gap> <column-gap>;
```

> Shorthand that specifies the gutters between grid columns and grid rows in one declaration. Replaced by 'gap' property.
>
> (Firefox 52, Chrome 57, Safari 10, Opera 44)
>
> Syntax: <'grid-row-gap'> <'grid-column-gap'>?
>
> 根据最新标准，上面三个属性名的`grid-`前缀已经删除，`grid-column-gap`和`grid-row-gap`写成`column-gap`和`row-gap`，`grid-gap`写成`gap`。

#### grid-auto

##### grid-auto-flow

子元素放置的位置 方向

>  划分网格以后，容器的子元素会按照顺序，自动放置在每一个网格。默认的放置顺序是"先行后列"，即先填满第一行，再开始放入第二行，即下图数字的顺序

```css
grid-auto-flow:row(默认值 先行后列) column（先列后行） (row dense) (column dense);
```

##### grid-auto-columns、grid-auto-rows

解决如果gird-template-columns/rows 没有设置到的单元格

隐式和显式网格：显式网格包含了你在 grid-template-columns 和 grid-template-rows 属性中定义的行和列。如果你在网格定义之外又放了一些东西，或者因为内容的数量而需要的更多网格轨道的时候，网格将会在隐式网格中创建行和列

假如有多余的网格（也就是上面提到的隐式网格），那么它的行高和列宽可以根据 grid-auto-columns 属性和 grid-auto-rows 属性设置。它们的写法和grid-template-columns 和 grid-template-rows 完全相同。如果不指定这两个属性，浏览器完全根据单元格内容的大小，决定新增网格的列宽和行高

- grid-auto-colums
- grid-auto-rows

#### place-item 单元格子元素

justify-item、align-items、place-items

justify-items 属性设置单元格内容的水平位置（左中右），align-items 属性设置单元格的垂直位置（上中下）

单元格 水平和垂直 设置单元格内容的水平位置（左中右）

- justify-item:start | end | center | stretch  设置单元格内容的水平位置（左中右）
	- start：对齐单元格的起始边缘。
	- end：对齐单元格的结束边缘。
	- center：单元格内部居中。
	- stretch：拉伸，占满单元格的整个宽度（默认值）。
- align-item:start | end | center | stretch   设置单元格内容的垂直位置（上中下）
- `place-items: <align-items> <justify-items>`

#### place-content 整个容器

justify-content 、align-content、place-content

- justify-content 整个内容区域在容器里面的水平位置（左中右）
- align-content 整个内容区域的垂直位置（上中下）。
- place-content :

```
 justify-content: start | end | center | stretch | space-around | space-between | space-evenly;
  align-content: start | end | center | stretch | space-around | space-between | space-evenly;  
```

### 项目 item 

grid-area 和 place-self

项目属性

- grid-area：grid-row-start、grid-column-start、grid-row-end、grid-column-end
	- grid-column grid-column-start、grid-column-end、
	- grid-row grid-row-start、grid-row-end
- place-selft：justify-self aligin-self 
	- justify-self、align-self、place-self

#### grid-area

指元素的扩展区域  指定网格项目所在的四个边框，分别定位在哪根网格线，从而指定项目的位置

- 指定项目放在哪一个区域
- grid-column-start 属性：左边框所在的垂直网格线
- grid-column-end 属性：右边框所在的垂直网格线
- grid-row-start 属性：上边框所在的水平网格线
- grid-row-end 属性：下边框所在的水平网格线

```css
grid-area: grid-row-start / grid-column-start / grid-row-end / grid-column-end | itemname;
// 默认值 auto auto auto auto

 grid-area: 2 / 1 / span 2 / span 3;
// 从第2行第1列开始，并跨越2行3列： 


// 从 格子 2,1 位置 到 2 ，3 位置
扩展大小
从 对角线

垂直网格线是从 2 到 4，水平网格线是从 1 到 2。
```

| 属性值                                                       | 描述                                   |
| :----------------------------------------------------------- | :------------------------------------- |
| [grid-row-start](https://www.jc2182.com/css-grid-row-start-prop/1405.html) | 指定开始显示项目的行。                 |
| [grid-column-start](https://www.jc2182.com/css-grid-column-start-prop/1399.html) | 指定开始显示项目的列。                 |
| [grid-row-end](https://www.jc2182.com/css-grid-row-end-prop/1402.html) | 指定停止显示项目的行线或要跨越的行数。 |
| [grid-column-end](https://www.jc2182.com/css-grid-column-end-prop/1397.html) | 指定停止显示项目的列线，或跨越的列数。 |
| itemname                                                     | 指定网格项的名称                       |

grid-row 

- grid-row-start 和 grid-row-end 的简写。

grid-column 

- grid-column-start 和 grid-column-end 的简写。

```css
grid-row:2;
grid-column: 3 / 3
如果提供两个值，第一个值是 grid-row-start 或者 grid-column-start 的值，第二个值是 grid-row-end 或者 grid-column-end 的值，两者之间必须要用/隔开。
grid-area: 2 / 2 / 3 / 3;
```

#### place-self 子元素自已

- justify-self 单元格内容的水平位置（左中右）
- align-self 属性设置单元格内容的垂直位置（上中下），
- place-self place-self 是设置 align-self 和 justify-self 的简写形式

```css
 justify-self: start | end | center | stretch;
  align-self: start | end | center | stretch;
```



```
记住
父元素
/*
grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
grid-template-rows: repeat(5,1fr);
*/
Gred line 可以改名
grid-template-rows: [Y1] 100px [Y2] 100px [Y3] 100px [Y4] 100px [Y5] 100px;
grid-template-columns: [X1] [100px [X2] 100px [X3] 100px [X4] 100px [X5] 100px;
grid-template-columns: 100px 100px 100px 100px 100px;
grid-template-areas:
                "header header header header header"
                "nav main main main main"
                "nav main main main main"
                "nav main main main main"
                ". footer footer footer .";
               注意："header header header header header"
                "nav main main main nav"
                "nav main main main nav"
                "nav main main main main"
                ". footer footer footer .";
                的写法错误 nav不能专门
row-gap:10px;
column-gap:10px;                
子元素
grid-row: 1/4;
grid-column: 5/6; 
grif-column:2/span 3; span延伸 (2,5) 2开始延伸3格
grid-row :Y2/Y4
//Grid Areas 
grid-area: 1/1/4/4; //grid-area: grid-row,grid-column;  = grid-row: 1/4;  grid-column: 1/4; 
grid-area:header;
grid-area:nav;
方格是紧贴的
```
```html
<div id="grid-container">
    <div class="cell-1"></div>
    <div class="cell-2"></div>
    <div class="cell-3"></div>
    <div class="cell-4"></div>
</div>
```
网页排版方式：
Table、Float、Flexbox、Grid
Flexbox属于一维（1-Dimension）的排版方式，一个flexbox容器只能控制一个方向，即水平方向或垂直方向，如需要控制另一个方向则需要再添加一层Flexbox容器
Grid则是二维（2-Dimensions）的排版方式，Grid容器可以一次控制两个方向，这样就可以直接定义容器内元素的位置
**水平方向column,垂直方向row**
```
#grid-container {
    width: 500px;
    height: 500px;
    background-color: #bdbdbd;
    margin: 50px auto;
    display: grid;
    /* 
    5*5的正方形
    (1,1） ==> (6,6)
    */
    grid-template-rows: 100px 100px 100px 100px 100px;
    /* 
    grid-template-rows: [Y1] 100px [Y2] 100px [Y3] 100px [Y4] 100px [Y5] 100px;
    */
    grid-template-columns: 100px 100px 100px 100px 100px;
    /* 
    grid-template-columns: [X1] [100px [X2] 100px [X3] 100px [X4] 100px [X5] 100px;
   grid-template-areas:
                "header header header header header"
                "nav main main main main"
                "nav main main main main"
                "nav main main main main"
                ". footer footer footer .";
    “. footer footer footer .” //点号表示忽略
*/
}
.cell-1 {
    background-color: pink;
    /* grid-row: 1/4;
    grid-column: 1/4; 
    grif-column:2/span 3; span延伸
    grid-row :Y2/Y4
    */
    grid-area: 1/1/4/4;
    /* grid-area: grid-row,grid-column; */
    /* 
    1，1 ==1,4
    grid-area:header;
    */
    }
    .cell-2 {
    background-color: yellow;
    grid-row: 5/6;
    grid-column: 5/6;
    /* 
    5，5 ==6,6
    */
}
```
fr 单位与repeat()函数
fr 专门用于Grid 的·比例单位
1fr 占一份
repeat(第一个参数重复多少次，重复些什么) 不适用与 *grid-template-area*
```
grid-template-rows: 100px 100px 100px 100px 100px;
grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
grid-template-rows: repeat(5,1fr);
grid-template-rows: 3fr repeat(4,1ft);
```
flexbox 布局 一维布局方式
按照行或者列布局
```
display:flex; //子元素默认按照行排列
```
```
object-fit:cover;
pointer-events:none;
https://developer.mozilla.org/zh-CN/docs/Web/CSS/pointer-events
```
`object-fit:fill | contain | cover | none | scale-down`
> object-fit CSS 属性指定可替换元素的内容应该如何适应到其使用的高度和宽度确定的框
属性
contain
被替换的内容将被缩放，以在填充元素的内容框时保持其宽高比。 整个对象在填充盒子的同时保留其长宽比，因此如果宽高比与框的宽高比不匹配，该对象将被添加黑边
cover
被替换的内容在保持其宽高比的同时填充元素的整个内容框。如果对象的宽高比与内容框不相匹配，该对象将被剪裁以适应内容框。
fill
被替换的内容正好填充元素的内容框。整个对象将完全填充此框。如果对象的宽高比与内容框不相匹配，那么该对象将被拉伸以适应内容框。
none
被替换的内容将保持其原有的尺寸。
scale-down
被替换的内容正好填充元素的内容框。整个对象将完全填充此框。如果对象的宽高比与内容框不相匹配，那么该对象将被拉伸以适应内容框。
[CSS双列、三列、双飞翼、圣杯等15种布局 - 知乎](https://zhuanlan.zhihu.com/p/162119920)
[(22 封私信 / 73 条消息) 网页布局都有哪种？一般都用什么布局？ - 知乎](https://www.zhihu.com/question/21775016)
垂直布局的几种方法
Grid网页布局

```
记住
父元素
display: grid;
grid-template-rows: 100px 100px 100px 100px 100px;
/*
grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
grid-template-rows: repeat(5,1fr);
*/
Gred line 可以改名
grid-template-rows: [Y1] 100px [Y2] 100px [Y3] 100px [Y4] 100px [Y5] 100px;
grid-template-columns: [X1] [100px [X2] 100px [X3] 100px [X4] 100px [X5] 100px;
grid-template-columns: 100px 100px 100px 100px 100px;
grid-template-areas:
                "header header header header header"
                "nav main main main main"
                "nav main main main main"
                "nav main main main main"
                ". footer footer footer .";
               注意："header header header header header"
                "nav main main main nav"
                "nav main main main nav"
                "nav main main main main"
                ". footer footer footer .";
                的写法错误 nav不能专门
                

row-gap:10px;
column-gap:10px;                
子元素
grid-row: 1/4;
grid-column: 5/6; 
grif-column:2/span 3; span延伸 (2,5) 2开始延伸3格
grid-row :Y2/Y4
//Grid Areas 
grid-area: 1/1/4/4; //grid-area: grid-row,grid-column;  = grid-row: 1/4;  grid-column: 1/4; 
grid-area:header;
grid-area:nav;
方格是紧贴的

```

```html
<div id="grid-container">
    <div class="cell-1"></div>
    <div class="cell-2"></div>
    <div class="cell-3"></div>
    <div class="cell-4"></div>
</div>
```

网页排版方式：

Table、Float、Flexbox、Grid

Flexbox属于一维（1-Dimension）的排版方式，一个flexbox容器只能控制一个方向，即水平方向或垂直方向，如需要控制另一个方向则需要再添加一层Flexbox容器

Grid则是二维（2-Dimensions）的排版方式，Grid容器可以一次控制两个方向，这样就可以直接定义容器内元素的位置

**水平方向column,垂直方向row**

```
#grid-container {
    width: 500px;
    height: 500px;
    background-color: #bdbdbd;
    margin: 50px auto;
    display: grid;
    /* 
    5*5的正方形
    (1,1） ==> (6,6)
    */
    grid-template-rows: 100px 100px 100px 100px 100px;
    /* 
    grid-template-rows: [Y1] 100px [Y2] 100px [Y3] 100px [Y4] 100px [Y5] 100px;
    */
    grid-template-columns: 100px 100px 100px 100px 100px;
    /* 
    grid-template-columns: [X1] [100px [X2] 100px [X3] 100px [X4] 100px [X5] 100px;
   grid-template-areas:
                "header header header header header"
                "nav main main main main"
                "nav main main main main"
                "nav main main main main"
                ". footer footer footer .";
    “. footer footer footer .” //点号表示忽略
*/
}
.cell-1 {
    background-color: pink;
    /* grid-row: 1/4;
    grid-column: 1/4; 
    grif-column:2/span 3; span延伸
    grid-row :Y2/Y4
    */
    grid-area: 1/1/4/4;
    /* grid-area: grid-row,grid-column; */
    /* 
    1，1 ==1,4
    grid-area:header;
    */
    }
    .cell-2 {
    background-color: yellow;
    grid-row: 5/6;
    grid-column: 5/6;
    /* 
    5，5 ==6,6
    */
}
```

fr 单位与repeat()函数

fr 专门用于Grid 的·比例单位

1fr 占一份

repeat(第一个参数重复多少次，重复些什么) 不适用与 *grid-template-area*

```
grid-template-rows: 100px 100px 100px 100px 100px;
grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
grid-template-rows: repeat(5,1fr);
grid-template-rows: 3fr repeat(4,1ft);
```

flexbox 布局 一维布局方式

按照行或者列布局

```
display:flex; //子元素默认按照行排列
```

```
object-fit:cover;
pointer-events:none;
https://developer.mozilla.org/zh-CN/docs/Web/CSS/pointer-events
```

`object-fit:fill | contain | cover | none | scale-down`

> object-fit CSS 属性指定可替换元素的内容应该如何适应到其使用的高度和宽度确定的框

属性

contain

被替换的内容将被缩放，以在填充元素的内容框时保持其宽高比。 整个对象在填充盒子的同时保留其长宽比，因此如果宽高比与框的宽高比不匹配，该对象将被添加黑边

cover

被替换的内容在保持其宽高比的同时填充元素的整个内容框。如果对象的宽高比与内容框不相匹配，该对象将被剪裁以适应内容框。

fill

被替换的内容正好填充元素的内容框。整个对象将完全填充此框。如果对象的宽高比与内容框不相匹配，那么该对象将被拉伸以适应内容框。

none

被替换的内容将保持其原有的尺寸。

scale-down

被替换的内容正好填充元素的内容框。整个对象将完全填充此框。如果对象的宽高比与内容框不相匹配，那么该对象将被拉伸以适应内容框。

### 重点

#### item content self 三者pk

place-item

place-content 

place-self 



place-item 相当于 批量的 place-self



#### grid-template column rows 



grid-template-areas 与 grid-area



### 基本布局

#### 12 列网格布局



#### fr分响应式布局

```css
grid-template-columns: 1fr 1fr 1fr;
```

#### repeat + auto-fit——固定列宽，改变列数量

```
 grid-template-columns: repeat(auto-fit, 200px);
```

#### repeat+auto-fit+minmax 去掉右侧空白

上面看到的效果中，右侧通常会留下空白，

```
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
```

#### repeat+auto-fit+minmax-span-dense 解决空缺问题

每个网格元素的长度可能不相同，这也简单，通过 span 关键字进行设置网格项目的跨度，grid-column-start: span 3，表示这个网格项目跨度为 3。

```
grid-column-start: span 3;
```

grid-auto-flow: row dense 表示尽可能填充，而不留空白

```css
.wrapper, .wrapper-1 {
  margin: 50px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-gap: 10px 20px;
  grid-auto-rows: 50px;
}

.wrapper-1 {
  grid-auto-flow: row dense;
}
```



## 全屏布局

经典的全屏布局由顶部、底部和主体三部分组成，其特点为三部分左右满屏拉伸、顶部底部高度固定和主体高度自适应。

```html
.fullscreen-layout>header+main+footer
```

- position + left/right/top/bottom

```css
.fullscreen-layout {
    position: relative;
    width: 400px;
    height: 400px;
    header,
    footer,
    main {
        position: absolute;
        left: 0;
        right: 0;
    }
    header {
        top: 0;
        height: 50px;
        background-color: #f66;
    }
    footer {
        bottom: 0;
        height: 50px;
        background-color: #66f;
    }
    main {
        top: 50px;
        bottom: 50px;
        background-color: #3c9;
    }
}
```

- flex 、flex-direcition:column, flex:1 高度自适应

```css
.fullscreen-layout {
    display: flex;
    flex-direction: column;
    
    width: 400px;
    height: 400px;
    header {
        height: 50px;
        background-color: #f66;
    }
    footer {
        height: 50px;
        background-color: #66f;
    }
    main {
        flex: 1;
        background-color: #3c9;
    }
}
```

grid   grid-template-rows

[CodePen 示例](https://codepen.io/una/pen/bGVXPWB)

```css
display: grid;
    grid-template-rows: auto 1fr auto;
```

## 双列布局

经典的两列布局由左右两列组成，其特点为一列宽度固定、另一列宽度自适应和两列高度固定且相等。

### float + margin-left/right 

- float
-  margin-left: 

```css
.two-column-layout {
    width: 400px;
    height: 400px;
    .left {
        float: left;
        width: 100px;
        height: 100%;
        background-color: #f66;
    }
    .right {
        margin-left: 100px;
        height: 100%;
        background-color: #66f;
    }
}
```

### overflow + float 

- float 
- overflow

```cs
.two-column-layout {
    width: 400px;
    height: 400px;
    .left {
        float: left;
        width: 100px;
        height: 100%;
        background-color: #f66;
    }
    .right {
        overflow: hidden; // bfc
        height: 100%;
        background-color: #66f;
    }
}
```

### table table-cell

```xaa
.parent{
	display: table; width: 100%;
	table-layout: fixed;
}
.left,.right{
	display: table-cell;
}
.left{
	width: 100px;
	padding-right: 20px;
}
```

### flex、flex:1

```css
.two-column-layout {
    display: flex;
    width: 400px;
    height: 400px;
    .left {
        width: 100px;
    }
    .right {
        flex: 1;
    }
}
```

### grid grid-template-columns: minmax(150px, 25%) 1fr;

- 两栏式布局就是一个边栏，一个主栏。

https://codepen.io/una/pen/gOaNeWL

```
.container {
    display: grid;
    grid-template-columns: minmax(150px, 25%) 1fr;
}
```



## 三列布局

### 经典三列布局 左中定宽右自适应

左中列宽度固定和右列宽度自适应

经典的三列布局由左中右三列组成，其特点为连续两列宽度固定、剩余一列宽度自适应和三列高度固定且相等。

```html
<div class="three-column-layout">
    <div class="left"></div>
    <div class="center"></div>
    <div class="right"></div>
</div>
```

- overflow(right)+float(left center)

```css
.three-column-layout {
    width: 400px;
    height: 400px;
    .left {
        float: left;
        width: 50px;
        height: 100%;
        background-color: #f66;
    }
    .center {
        float: left;
        width: 100px;
        height: 100%;
        background-color: #66f;
    }
    .right {
        overflow: hidden;
        height: 100%;
        background-color: #3c9;
    }
}
```

- flex:1(right)

```css
.three-column-layout {
    display: flex;
    width: 400px;
    height: 400px;
    .left {
        width: 50px;
        background-color: #f66;
    }
    .center {
        width: 100px;
        background-color: #66f;
    }
    .right {
        flex: 1;
        background-color: #3c9;
    }
}
```

### 圣杯布局 两边顶宽，中间自适应

 Holy Grail Layout

![img](css&css3.assets/bg2020080717.jpg)

> [css经典布局——圣杯布局 - 掘金](https://juejin.im/post/6844903763329679368)
> Web 中典型的布局模式，网页布局有很多种方式，一般分为以下几个部分：**头部区域、菜单导航区域、内容区域、底部区域**。![img](https://i.loli.net/2020/08/19/W27w8tzLyGgQ6kH.jpg)
> 内容区域
> 内容区域一般有三种形式:

- **1 列**：一般用于移动端
- **2 列**：一般用于平板设备
- **3 列**：一般用于 PC 桌面设备![img](https://i.loli.net/2020/08/19/vAUyJtgFX8wn4LP.jpg)
- float + margin-left/right + padding-left/right
- 中间栏要在放在文档流前面以优先渲染

```css
<div class="grail-layout-x">
    <div class="left"></div>
    <div class="right"></div>
    <div class="center"></div>
</div>
.grail-layout-x {
    padding: 0 100px;
    width: 400px;
    height: 400px;
    .left {
        float: left;
        margin-left: -100px;
        
        width: 100px;
        height: 100%;
        background-color: #f66;
    }
    .right {
        float: right;
        margin-right: -100px;
        
        width: 100px;
        height: 100%;
        background-color: #66f;
    }
    .center {
        height: 100%;
        background-color: #3c9;
    }
}
```

```css
<div class="container">
    <div class="middle">测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试</div>
    <div class="left">left</div>
    <div class="right">right</div>
</div>   
.container{
            padding: 0 200px;
        }
        .middle{
            width: 100%;
            background: paleturquoise;
            height: 200px;
            float: left;
        }
        .left{
            background: palevioletred;
            width: 200px;
            height: 200px;
            float: left;
            font-size: 40px;
            color: #fff;
            margin-left:-100%;
        }
        .right{
            width: 200px;
            height: 200px;
            background: purple;
            font-size: 40px;
            float: left;
            color: #fff;
            margin-left:-200px;
        }
```

```css
center{
	box-sizing:border-box;
	padding:0 200px
}
```

grid 

（[CodePen 示例](https://codepen.io/una/pen/mdVbdBy)）

```css
<div class="container">
    <header/>
    <div/>
    <main/>
    <div/>
    <footer/>
</div

.container {
    display: grid;
    grid-template: auto 1fr auto / auto 1fr auto;
}
grid-template属性那一行，它是两个属性grid-template-rows（垂直方向）和grid-template-columns（水平方向）的简写形式。
grid-template: <grid-template-rows> / <grid-template-columns>
```

`grid-template-rows`和`grid-template-columns`都是`auto 1fr auto`，就表示页面在垂直方向和水平方向上，都分成三个部分。第一部分（页眉和左边栏）和第三部分（页脚和右边栏）都是本来的内容高度（或宽度），第二部分（内容区和主栏）占满剩余的高度（或宽度）。

pos

```
<div class="container">
    <div class="header">header</div>
    <div class="wrapper clearfix">
        <div class="main col">main</div>
        <div class="left col">left</div>
        <div class="right col">right</div>
    </div>
    <div class="footer">footer</div>
</div>
.container {width: 500px; margin: 50px auto;}
.wrapper {padding: 0 100px 0 100px;}
.col {position: relative; float: left;}
.header,.footer {height: 50px;}
.main {width: 100%;height: 200px;}
.left {width: 100px; height: 200px; margin-left: -100%;left: -100px;}
.right {width: 100px; height: 200px; margin-left: -100px; right: -100px;}
.clearfix::after {content: ""; display: block; clear: both; visibility: hidden; height: 0; overflow: hidden;}


```



### 双飞翼布局 两边顶宽，中间自适应

> 经典的圣杯布局和双飞翼布局都是由左中右三列组成，其特点为左右两列宽度固定、中间一列宽度自适应和三列高度固定且相等。其实也是上述两列布局和三列布局的变体，整体的实现原理与上述N列布局一致
>
> 圣杯布局和双飞翼布局在大体相同下也存在一点不同，区别在于双飞翼布局中间列需插入一个子节点。在常规实现方式里也是在这个中间列里做文章，如何使中间列内容不被左右列遮挡。
>
> 相同
> 中间列放首位且声明其宽高占满父节点
> 被挤出的左右列使用float和margin负值将其拉回与中间列处在同一水平线上
> 不同
> 圣杯布局：父节点声明padding为左右列留出空位，将左右列固定在空位上
> 双飞翼布局：中间列插入子节点并声明margin为左右列让出空位，将左右列固定在空位上

圣杯布局弊端：双飞翼布局是为了解决圣杯布局的弊端提出的，当浏览器宽度缩短到一定程度的时候，会使得中间子元素的宽度比左右子元素宽度小的时候，这时候布局就会出现问题。所以首先，这提示了我们在使用圣杯布局的时候一定要设置整个容器的最小宽度。

双飞翼布局，为了中间div内容不被遮挡，直接在中间div内部创建子div用于放置内容，在该子div里用margin-left和margin-right为左右两栏div留出位置。

双飞翼布局也是经典的三列布局之一，核心也是浮动。但是它比圣杯布局要复杂，因为它只是中间元素被包裹，而左右元素并没有对应的父元素。

- float + margin-left/right

```css
<div class="grail-layout-y">
    <div class="left"></div>
    <div class="right"></div>
    <div class="center">
        <div></div>
    </div>
</div>
.grail-layout-y {
    width: 400px;
    height: 400px;
    .left {
        float: left;
        width: 100px;
        height: 100%;
        background-color: #f66;
    }
    .right {
        float: right;
        width: 100px;
        height: 100%;
        background-color: #66f;
    }
    .center {
        margin: 0 100px;
        height: 100%;
        background-color: #3c9;
    }
}
```

```css
container{
	position:relative;
}
left{
	position:absolute;
	top:0;
	left:0;
}
right{
	position:absolute;
	top:0;
	right:0;
}
```

pos

```
<div class="container">
    <div class="header">header</div>
    <div class="wrapper clearfix">
        <div class="main col">
            <div class="main-wrap">main</div>
        </div>
        <div class="left col">left</div>
        <div class="right col">right</div>
    </div>
    <div class="footer">footer</div>
</div>
.col {float: left;}
.header {height: 50px;}
.main {width: 100%;}
.main-wrap {margin: 0 100px 0 100px;height: 200px;}
.left {width: 100px; height: 200px; margin-left: -100%;}
.right {width: 100px; height: 200px; margin-left: -100px;}
.footer {height: 50px;}
.clearfix::after {content: ""; display: block; clear: both; visibility: hidden; height: 0; overflow: hidden;}

```



### 圣杯 vs 双飞翼 vs 普通定位

[【布局】聊聊为什么淘宝要提出「双飞翼」布局 · Issue #11 · zwwill/blog](https://github.com/zwwill/blog/issues/11)

- 圣杯 container padding
- 双飞翼 center>div margin  

### flex实现圣杯布局/双飞翼布局

可忽略上述分析，左右两列宽度固定，中间列宽度自适应。

```css
<div class="grail-layout">
    <div class="left"></div>
    <div class="center"></div>
    <div class="right"></div>
</div>
.grail-layout {
    display: flex;
    width: 400px;
    height: 400px;
    .left {
        width: 100px;
        background-color: #f66;
    }
    .center {
        flex: 1;
        background-color: #3c9;
    }
    .right {
        width: 100px;
        background-color: #66f;
    }
}
```

## 多列布局

### 均分布局

经典的均分布局由多列组成，其特点为每列宽度相等和每列高度固定且相等。总体来说也是最简单的经典布局，由于每列宽度相等，所以很易找到合适的方式处理。

```css
<div class="average-layout">
    <div class="one"></div>
    <div class="two"></div>
    <div class="three"></div>
    <div class="four"></div>
</div>
```



- float + width
	- 每列宽度声明为相等的百分比，若有4列则声明width:25%。N列就用公式100 / n求出最终百分比宽度，记得保留2位小数，懒人还可用width:calc(100% / n)自动计算呢

```css
.average-layout {
    width: 400px;
    height: 400px;
    div {
        float: left;
        width: 25%;
        height: 100%;
    }
}
```

- flex
- 使用flex实现会更简洁。节点声明display:flex后，生成的FFC容器里所有子节点的高度都相等，因为容器的align-items默认为stretch，所有子节点将占满整个容器的高度。每列声明flex:1自适应宽度。

```css
.average-layout {
    display: flex;
    width: 400px;
    height: 400px;
    div {
        flex: 1;
    }
}
```

## 等高布局

float + overflow

```css
.parent{
	overflow: hidden;
}
.left,.right{
	padding-bottom: 9999px;
	margin-bottom: -9999px;
}
.left{
	float: left; width: 100px;
}
.right{
	overflow: hidden;
}
```

table

```css
.parent{
	display: table; 
	width: 100%;
}
.left{
	display:table-cell; 
	width: 100px;
	margin-right: 20px;
}
.right{
	display:table-cell; 
}
```

flex

```css
.parent{
	display:flex;
	width: 100%;
}
.left{
	width: 100px;
}
.right{
	flex:1;
}
```



## 两端对齐

## 基于Sticky Footer



## 并排等分，单排对齐靠左布局

![效果图](css&css3.assets/166c3c99fd4d5773)

```css
.main {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
}
.item {
    display: inline-block;
}
.empty{
    height: 0;
    visibility: hidden;
}
```



## 居中布局

- 元素居中

## 自适布局

自适布局指相对视窗任何尺寸都能占据特定百分比的占位布局。自适布局的容器都是根据视窗尺寸计算，即使父节点或祖先节点的尺寸发生变化也不会影响自适布局的容器尺寸。

搭建自适布局就离不开视窗比例单位。在CSS3里增加了与viewport相关的四个长度单位，随着时间推移，目前大部分浏览器对这四个长度单位都有较好的兼容性，这也是未来最建议在伸缩方案里使用的长度单位。

- 1vw表示1%视窗宽度
- 1vh表示1%视窗高度
- 1vmin表示1%视窗宽度和1%视窗高度里最小者
- 1vmax表示1%视窗宽度和1%视窗高度里最大者

[8则未必知道且超级实用的纯CSS布局排版技巧 | 网易4年实践](https://juejin.cn/post/6986873449721364510#heading-1)

## 吸附布局



## 横向布局





## 凸显布局





## 间距布局



## 空载布局





## 多格布局

## 并列式布局

并列式布局就是多个项目并列。

![img](css&css3.assets/bg2020080706.jpg)

如果宽度不够，放不下的项目就自动折行。![img](css&css3.assets/bg2020080708.jpg)

```css
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.item{
   flex: 0 1 150px;
   margin: 5px;
}
flex: 0 1 150px;的意思就是，项目的初始宽度是150px，且不可以扩大，但是当容器宽度不足150px时，项目可以缩小。
```



## 视口窗口

ViewPort

vw和vh
有没有一个单位不需要JS和CSS耦合在一起的单位？答案是有的，就是`vw／vh`。

- vw = view width
- vh = view height
- 这两个单位是CSS3引入的，以上称为**视口单位**允许我们更接近浏览器窗口定义大小。
视口单位(Viewport units)
- Q：什么是视口？A：Peter-Paul Koch（”PPK大神”）提出视口的解释是：在桌面端，视口指的是在桌面端，指的是浏览器的可视区域；而在移动端，它涉及3个视口：Layout Viewport（布局视口），Visual Viewport（视觉视口），Ideal Viewport（理想视口）。
- 视口单位中的“视口”，桌面端指的是浏览器的可视区域；移动端指的就是Viewport中的Layout Viewport。
- 比如：浏览器视口尺寸为370px,那么 1vw = 370px * 1% = 6.5px(浏览器会四舍五入向下取7)
#### vh/vw与%区别
> 单位	解释
> vw	1vw = 视口宽度的1%
> vh	1vh = 视口高度的1%
> vmin	选取vw和vh中最小的那个
> vmax	选取vw和vh中最大的那个
>
> vh/vw与%区别在于，
>
> 单位	依赖于
> %	元素的祖先元素
> vh/vw	视口的尺寸
九宫格响应布局
![image-20200925162508070](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200925162508070.png)
```css
section {
    display: grid;
    grid-template-columns: repeat(3, calc(100vw/3));
    grid-template-rows: repeat(3, calc(100vh/3));
}
```
## 多列布局

`column`

| 属性                                                         | 描述                                      |
| :----------------------------------------------------------- | :---------------------------------------- |
| [column-count](https://www.runoob.com/cssref/css3-pr-column-count.html) | 指定元素应该被分割的列数。                |
| [column-fill](https://www.runoob.com/cssref/css3-pr-column-fill.html) | 指定如何填充列                            |
| [column-gap](https://www.runoob.com/cssref/css3-pr-column-gap.html) | 指定列与列之间的间隙                      |
| [column-rule](https://www.runoob.com/cssref/css3-pr-column-rule.html) | 所有 column-rule-* 属性的简写             |
| [column-rule-color](https://www.runoob.com/cssref/css3-pr-column-rule-color.html) | 指定两列间边框的颜色                      |
| [column-rule-style](https://www.runoob.com/cssref/css3-pr-column-rule-style.html) | 指定两列间边框的样式                      |
| [column-rule-width](https://www.runoob.com/cssref/css3-pr-column-rule-width.html) | 指定两列间边框的厚度                      |
| [column-span](https://www.runoob.com/cssref/css3-pr-column-span.html) | 指定元素要跨越多少列                      |
| [column-width](https://www.runoob.com/cssref/css3-pr-column-width.html) | 指定列的宽度                              |
| [columns](https://www.runoob.com/cssref/css3-pr-columns.html) | column-width 与 column-count 的简写属性。 |

- 盒模型
	- box-sizing:border-box content-box 
		- margin border padding content 
		- margin 控制的不是元素的位置 而已 盒子 的大小 本身还是占据位置的 元素没有发生位移 
- 浮动
- 定位
	- position absolute vs relative
		- absolute 相对于 父元素的 relative	
			- body 默认有relative
		- relative 相对于  父元素 进行定位

```css
 position: absolute; 生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。
 position: relative; 相对定位
 position: fixed;    生成绝对定位的元素，相对于浏览器窗口进行定位。 固定定位
 position: static; 默认值
 position: sticky;
```

- 浮动

	- float:right left  没有指定宽度 就依靠内容撑开
	- clear：right left both  none 清除元素浮动的影响 作用是 让元素不受左边或者右面元素的影响
		- clear 属性规定``元素的哪一侧不允许其他浮动元素``
			- left  左侧不允许浮动元素
			- right 
			- both
			- none

- 布局

	- 三列布局

		- 三列布局 

			- 两边固定 中间自适应
			- 三列自适应
				- 定位 pos:left top  // padding  // position: right top
					- 要容器、提升层级
				- 浮动 float:right left
					- 优先加载问题

		- 解决问题：当中列要完整形式且优先加载  center 要写在最先

		- 圣杯布局 两边固定 中间自适应

			- float

			```css
			header 
			content
				middle
				left
				right
			footer
			content: padding:0px 20px; 
			
			middle   float:left width:100% 
			
			// 添加等高布局
			left middle right
				padding-bottom:10000px
				margin-bottom:-10000px
			content 
				overflow:hidden
			
			left margin-left:-100%; 
			float:left
			
			right  width:200px float:right margin-left:-200px
			```

			- position
				- 
			- margin 设置负值
				- 负值向反方向移动
			- 清除浮动 在父元素中设置 清除子元素中的  因为 浮动 会造成 BFC 高度塌陷的问题 可以在 父元素中清除浮动 保证父级元素有高度 或者可以生成 BFC块

			```css
			// 当子元素浮动时会
			父元素添加 class="clearfix"
			
			.clearfix{
				*zoom:1;
			}
			
			.clearfix:after{
				content:'';
				display:block;
				clear:both;
			}
			```

		- 双飞翼布局

			

			

			

			flex:1 flex-basis:0% flex-grow:1 flex-shrink:1

			

	- 等高布局  左右两列 与中间等高

		- float + overflow

	```
	.parent{
		overflow: hidden;
	}
	.left,.right{
		padding-bottom: 9999px;
		margin-bottom: -9999px;
	}
	.left{
		float: left; width: 100px;
	}
	.right{
		overflow: hidden;
	}
	```

	- 粘连布局 footer 布局

		- 有一块内容 `<main>`
		- 当`main`的高度足够长的时候，main后面的元素footer会跟 在main元素的后面
		- 当main元素足够短的时候 （小于屏幕的高度），我们期望footer元素 能够粘连在屏幕的底部

# Less

scss sass 

less

stylus 

基础

新建文件夹 mixin 

注释

```js
/* 这是暴露出去的注释 */ 用户看的
// 开发人员看的
```

变量

- 声明变量 @pink：pink;
- 使用普通属性值只来使用：直接使用@pink 
- 选择器和属性名 ：#@{selector的值}的形式
- 作为URL: @{url}
- 变量的延迟加载 遵循块级作用域 

```
@color:pink;
@b:border;
@selector:#wrap;
@themecolor:red; 
 
@b:1px solid red;

@{selector}{

}
background:@color; 
```

嵌套规则

- `&`的使用 平级 

混合 Mixin

- 混合就是``将一系列属性从一个规则集引入到另一个规则集的方式``  就是可以复用一段公共的代码 

混合的定义在less规则中有明确的指定 使用 `.`混合名的形式 来定义

普通混合 编译到原生css中

```less
.blackborder{ // .blackborder{}
	border:1px solid black;
}
.container{
    .inner{
        .blackborder;
    }
    .inner2{
        .blackborder;
    }
}
```

不带输出的混合（加括号）

```
.blackborder(){ // .blackborder{}
	border:1px solid black;
}
.container{
    .inner{
        .blackborder();
    }
    .inner2{
        .blackborder();
    }
}
```

带参数的混合

```less
.blackborder(@w,@s,@c){ // .blackborder{}
	border:@w @s @c;
}
.container{
    .inner{
        .blackborder(1px,solid,red);
    }
    .inner2{
        .blackborder(10px,dotted,blue);
    }
}
```

带多个参数并且有默认值的混合

```less
.blackborder(@w:10px,@s:solid,@c){ // .blackborder{}
	border:@w @s @c;
}
.container{
    .inner{
        .blackborder(1px,solid,red);
    }
    .inner2{
        .blackborder(10px,dotted,blue);
    }
}
```

兼容IE6的三角形

```js
width:0px;
height:0px;
border-width:40px;
border-style:solid;
border-color:transparent red transparent transparent;
overflow:hidden; // haslayout window IE6和IE7的私有属性  
```

![image-20210816200354061](https://i.loli.net/2021/08/17/drguKizaQ2VL4Go.png)

命名参数

```less
.blackborder(@w:10px,@s:solid,@c){ // .blackborder{}
	border:@w @s @c;
}
.container{
    .inner{
        .blackborder(1px,solid,red);
    }
    .inner2{
        .blackborder(@c:yello);
    }
}
```

匹配模式

```less
@import './triangle.less';
#wrap{
	.trangle(R,40px,yellow)
}
 
.triangle(@_){ // 公共部分
 	width:0px;
 	height:0px;
 	overflow:hidden;
 }

.triangle(L,@w,@c){
    border-width:@w;
    border-style:dashed solid dashed dashed;
    border-color:transparent @c transparent transparent;
}

.triangle(R,@w,@c){
    border-width:@w;
    border-style:dashed solid dashed dashed;
    border-color:transparent transparent transparent @c;
}

.triangle(T,@w,@c){
    border-width:@w;
    border-style:dashed solid dashed dashed;
    border-color: @c  transparent  transparenttransparent;
}

.triangle(B,@w,@c){
    border-width:@w;
    border-style:dashed solid dashed dashed;
    border-color:transparent  transparent  @c  transparent;
}
```

arguments变量

```js
.border(@width,@style,@color){
	border:@arguments; // 实参列表 
}

.box{
    .border(1px,solid,black)
}
```

计算

加减乘除

```js
width:(199 + 300px) // 只要一个带单位
```

继承

```css
.juzhong{ // 要
	
}

// == .inner,.juzhong{}
.inner:extend(.juzhong){ // inner下面的子元素添加juzhong
// &:extend(.juzhong) .inner 继承juzhong的代码 
 // &:extend(.juzhong all) juzhong的所有状态继承 
	$:nth-child(1){
		width:100px;
		height:100px;
		background:red;
	}
	$:nth-child(2){
		width:50px;
		height:50px;
	}
}
```

避免编译

```js
padding: ~"calc(100px + 100)"
```

浏览器 

```css
<sty  le type="text/less"></style>
<script src="less.min.js"></script>
```

less编译工具 

- koala 





《CSS权威指南 第三版》 和 《CSS权威指南 第四版》

> 480页  9h - 23h   ===> 14h  11h  1h  ==> 50张     

# [CSS权威指南 第四版](https://github.com/gdut-yy/CSS-The-Definitive-Guide-4th-zh/tree/master/docs)

HTML与CSS









字体：系统自带字体









## 值和单位

CSS 定义了三个全局关键字： inherit initial 和 unset 可以在任何属性上使用 

### inherit 继承父元素

> inherit  关键词使元素上该属性的值继承其父元素响应属性的值。换句话来说，在继承没有发生的情况下，它会强行进行属性继承。在很多情况下，你不需要特意指明继承，很多继承是自动进行的。但是，inherit关键词还是非常有用的。通过继承来做的话会使代码更加健壮

```html
继承父元素的样式
<div class="father">
	<p class="son"></p>
</div>

.father{
	border:1px solid red;
}

p{
	border:inherit;
}
```

### initial 恢复初始值(可以更改用户的CSS的默认值)  CSS 默认值

可以使用这个避免父元素的样式影响子元素

**initial** 关键词可以将属性的值恢复成初始值，某种程度上可以说它“重置”了该值。例如：fontweight属性的默认值为normal。因此，`font-weight: initial`这样声明跟`font-weight: normal`这样声明是一个效果。

> 如果所有的属性都有明确的初始值，你会觉得这个关键词的设计有点愚蠢，但事实并不是这样的。举个例子，字体颜色的初始值是由用户代理来决定的，而不是你设置的某种时髦字体。这意味着字体颜色的默认值是由浏览器的偏好设置决定的。虽然大部分用户的文本设置是黑色字体，也有一部分用户将字体设置成灰色甚至是亮红色。通过声明`color: initial;`,你可以告诉浏览器将元素内的字体颜色更改成用户设置的默认值。

### unset

**unset** 关键词是inherit和initial的通用替代。如果一个属性是继承的，unset的效果跟inherit关键词的效果相同，如果一个属性不是继承的，unset的效果则跟initial关键词的效果相同。

### all 特殊的属性 它只能接受全局关键字

**all** 关键词用于指代全部属性，除direction、unicode-bidi。因此，如果你在一个元素中这样声明`all: inherit`，意思是除了direction、unicode-bidi属性外，全部属性的值均继承自它们的父元素。如下：

```
section {color: white; background: black; font-weight: bold;}
#example {all: inherit;} // 强制从CSS中继承所有的属性 直接一步到位
<section>
<div id="example">This is a div.</div>
</section>
```

### 地址的两种表示方式

> /   ==  当前目录
>
> ./ == 下一级目录
>
> ../ ==  上一级目录

绝对路径  从盘符或者服务器的根目录开始

```html
url(protocol://server/pathname)
```

相对路径 从文件相对位置

> 在CSS中，``相对地址是相对于样式表自身的，而不是HTML文档``。例如，如果你的文档中引入了一个外部样式表，这个外部样式表中又以相对位置引入了另一个外部样式表，第二个样式表必须在第一个样式表的相对位置。即使以自身的目录找到要引入的目录位置

```html
url(pathname)
```

html 文件引入 css样式表

```html
<link rel="stylesheet" type:"text/css" href="http://heweilinag.github.io/he/wei/liang.css">
```

css 文件 引入 css样式表

```html
@import url("http://heweilinag.github.io/he/wei/liang.css")
```









image  

url



image-set

根据嵌入值中的一组条件选择一组图像。 例如，image-set（）可以指定将较大的图像用于桌面布局，而将较小的图像（像素大小和文件大小）用于移动设计。 它旨在至少近似于图片元素的srcset属性的行为。 截至2016年底，浏览器对图像集的支持仅限于Safari，Chrome和桌面Opera，并且无法与srcset的全部功能相提并论。

gradient 

单独或重复地引用线性或径向渐变图像。

url

一个外部资源的地址标识符；在这里，指的是图像的URL。



href





src



 Identifiers

部分属性可以接收一个标识符值，它是用户自己定义的某种标识符。最常见的例子是生成列表计数器。它们在值语法中表示为`<identifer>`。 标识符本身就是单词，并且区分大小写；因此，就CSS而言，myID和MyID完全不同且彼此无关。如果某个属性同时接受标识符和一个或多个关键字，则作者应注意不要定义与有效关键字相同的标识符。









值 



像素单位

|      |      |
| ---- | ---- |
| %    |      |
| px   |      |
| rem  |      |
| em   |      |
|      |      |
|      |      |





颜色单位

|      |      |      |
| ---- | ---- | ---- |
| RGB  |      |      |
| HEX  |      |      |
|      |      |      |





## 布局

盒子

形态

padding



borders



outlines



margins







IE 盒子

```

```





w3C盒子

```

```







表格







浮动





定位





flex 布局



网格



CSS 常见问题

有时设置margin:0 auto;不起作用？

+maigin: 0 auto; 指元素的上下边距为0，左右边距根据于父元素（body）宽度自适应，即左右水平居中。如果该设置不起作用大致下面两种原因。

+（1）没有为p设置宽度，如果p么有宽度，就无法参考父元素的宽度来进行自身的auto。

+（2）p具有包裹性，即脱离标准流，就好比父对象所在的标准流比喻成地表，那包裹性元素就已经上天了。没有了可供参考的父元素宽度进行auto。

+块级元素中margin、border、padding以及content宽度之和构成父元素width。

使用auto属性后，父元素宽度发生变化，该元素的宽度也会随之变化。

下图中 auto 的值就是margin、border、padding以及content宽度之和



但是当该元素被设为浮动时，该元素的width就变成了内容的宽度了，由内容撑开，也就是所谓的有了包裹性。

overflow | position:absolute | float:left/right都可以产生包裹性，替换元素也同样具有包裹性。

*|position:relavtive|相对定位 占原来的位置，不能实现模式的转化，即不具有包裹性。









#### calc()是什么？

简单来说就是CSS3中新增的一个函数，calculate（计算）的缩写。用于动态计算宽/高，你可以使用calc()给元素的各个属性设置值【margin、border、padding、font-size】等，

#### calc()语法

calc的语法就是简单的四则运算，

1. 使用“+”、“-”、“*” 和 “/”四则运算；
2. 可以使用百分比、px、em、rem等单位；
3. 可以混合使用各种单位进行计算；
4. 表达式中有“+”和“-”时，其前后必须要有空格，如"width: calc(12%+5em)"这种没有空格的写法是错误的；
5. 表达式中有“*”和“/”时，其前后可以没有空格，但建议留有空格。

#### calc()的用途




min-width || max-width ()

min-witdth:500px ===> width:500px 以上

width:500px ===> 刚好500px

max-witdth:500px ===< width:0px ~ 500px 之间



max-width(不大于) — width —- min-width(不小于)  



CSS实现宽高等比例自适应矩形

```
        .son3 {
            width:100%;
            height: calc(100vw/2);
            background-color: greenyellow;
        }
        
           .son3 {
            width: calc(100vw -(2*10)px);
            /* width: 100vw; */
            /* padding: 0px 10px; */
            margin: 0px 100px;
            height: 100vh;
            background-color: teal;
        }
```



[(29条消息)CSS中的块级元素、行内元素和行内块元素_swebin的专栏-CSDN博客_行内块元素](https://blog.csdn.net/swebin/article/details/90405950)

内联元素（行内元素）内联元素(inline element)

* a - 锚点
* abbr - 缩写
* acronym - 首字
* b - 粗体(不推荐)
* bdo - bidi override
* big - 大字体
* br - 换行
* cite - 引用
* code - 计算机代码(在引用源码的时候需要)
* dfn - 定义字段
* em - 强调
* font - 字体设定(不推荐)
* i - 斜体
* img - 图片
* input - 输入框
* kbd - 定义键盘文本
* label - 表格标签
* q - 短引用
* s - 中划线(不推荐)
* samp - 定义范例计算机代码
* select - 项目选择
* small - 小字体文本
* span - 常用内联容器，定义文本内区块
* strike - 中划线
* strong - 粗体强调
* sub - 下标
* sup - 上标
* textarea - 多行文本输入框
* tt - 电传文本
* u - 下划线
* var - 定义变量

块元素(block element)

* address - 地址
* blockquote - 块引用
* center - 举中对齐块
* dir - 目录列表
* div - 常用块级容易，也是css layout的主要标签
* dl - 定义列表
* fieldset - form控制组
* form - 交互表单
* h1 - 大标题
* h2 - 副标题
* h3 - 3级标题
* h4 - 4级标题
* h5 - 5级标题
* h6 - 6级标题
* hr - 水平分隔线
* isindex - input prompt
* menu - 菜单列表
* noframes - frames可选内容，（对于不支持frame的浏览器显示此区块内容
* noscript - ）可选脚本内容（对于不支持script的浏览器显示此内容）
* ol - 排序表单
* p - 段落
* pre - 格式化文本
* table - 表格
* ul - 非排序列表

可变元素
可变元素为根据上下文语境决定该元素为块元素或者内联元素。

* applet - java applet
* button - 按钮
* del - 删除文本
* iframe - inline frame
* ins - 插入的文本
* map - 图片区块(map)
* object - object对象
* script - 客户端脚本



区别主要是三个方面:一是排列方式，二是宽高边距设置，三是默认宽度。

块级元素会独占一行，而内联元素和内联块元素则会在一行内显示。
块级元素和内联块元素可以设置 width、height 属性，而内联元素设置无效。
块级元素的 width 默认为 100%，而内联元素则是根据其自身的内容或子元素来决定其宽度。
而行内块级元素又同时拥有块级元素和行内元素的特点。

# 《CSS揭秘》 

> 共235 页 5h 完成 1h === 50 页

## 第一章 引言

### 浏览器前缀

| 浏览器前缀 | 浏览器        |
| ---------- | ------------- |
| -moz-      | Firefox       |
| -ms-       | IE            |
| -o-        | Opera         |
| -webkit-   | Safari/Chrome |

```
-moz-border-radius:10px;
-ms-border-radius:10px;
-webkit-border-radius:10px;
-o-border-radius:10px;
border-radius:10px;
-ms-border-radius // -o-border-radius 没有在任何浏览器出现过  
```

<!-- more -->

### CSS编码技巧

#### 尽量减少代码重复

使用父级元素固定单位，修改父级元素的固定单位，子元素的单位相应的发生改变，不用修改子元素 

```
绝对单位 和 相对单位
1. 绝对单位 px
font-size: 20px;
line-height:30px;

2. 倍数
//行高是字号的1.5 倍。因此，把代码改成下面这样会更易维护：
font-size:20px;
line-height:1.5; // 使用倍数  20 * 1.5 = 30px

font-size:125%; /* 假设父级的字号是16px */
line-height 1.5;

3.相对单位 em
0.3em == .3em
```

#### 合理使用简写

```css
background: url(tr.png) top right,
url(br.png) bottom right,
url(bl.png) bottom left;
background-size: 2em 2em;
background-repeat: no-repeat;
```





## 第二章 背景与边框

RGBA/HSLA 颜色

### 半透明边框

---

半透明边框效果：盒子的边框可以透明看到 背景

```css
border:10px solid hsla(0,0%,100%,.5);
background:white;
background-clip:padding-box;
```

### 多重边框



### 灵活的背景定位



### 边框内圆角



### 条纹背景





### 复杂的背景图案



### 伪随机背景



### 连续的图像边框







## 第三章 形状

#### 自适应的椭圆

##### 圆

```
background: pink;
width: 200px;
height: 200px;
border-radius: 100px;  
// 如果指定任何大于100px 的半径，仍然可以得到一个圆形。
```

> 当任意两个相邻圆角的半径之和超过border box 的尺寸时，用户代理必须按比例减小各个边框半径所使用的值，直到它们不会相互重叠为止。

##### 椭圆 （ellipse）

单独指定水平和垂直半径，只要用一个斜杠（/）分隔这两个值即可。这个特性允许我们在拐角处创建椭圆圆角。

像素固定值（长度值）

```
border-radius: 100px/ 75px;
第一个值是水平半径
第二个值是垂直半径
```

百分比值

> 使用百分比值会得到 响应式的椭圆

```
border-radius:50%/50%;
前后的两个值现在是一致的（即使它们最终可能会被计算为不同的值）
border-radius: 50%;
```

##### 半椭圆

```
border-radius
-- border-top-left-radius
-- border-top-right-radius
-- border-bottom-left-radius
-- border-bottom-right-radius
从左上角开始以顺时针顺序应用到元素的各个拐角
```



#### 平行四边形

> skew 倾斜
>
> rotate 旋转

```
transform: skew(-45deg); //通过skew() 的变形属性来对这个矩形进行斜向拉伸
```

问题文字倾斜

解决方法

嵌套元素方案

```
<a href="#yolo" class="button">
<div>Click me</div>
</a>
.button { transform: skewX(-45deg); }
.button > div { transform: skewX(45deg); }
```

伪元素方案

```
.button {
position: relative;
/* 其他的文字颜色、内边距等样式…… */
}
.button::before {
content: ''; /* 用伪元素来生成一个矩形 */
position: absolute;
z-index:-1;
top: 0; right: 0; bottom: 0; left: 0;
background: blue;
transform:skew(45deg);
}
```



#### 菱形图片

#### 基于变形的方案 (缺点 ：不够健壮 不够简洁 只使用于处理一张正方形的图片，处理不了非正方形的图片)

```html
<div class="picture">
	<img src=".jpg" alt="..." />
</div>
.picture{
	width: 400px;
	transform:rotate(45deg);
	overflow:hidden;
}
.picture > img{
	max-width:100%;  //主要问题在于max-width: 100% 这条声明。100% 会被解析为容器（.picture）的边长。
	transform:rotate(-45deg) scale(1.42);
}

```



#### 裁切路径的方案 `clip-path`

裁切路径允许我们把元素裁剪为我们想要的任何形状。

```html
img {
    clip-path: polygon(50% 0, 100% 50%, 50% 100%, 0 50%);
	// polygon()（多边形）函数来指定一个菱形 n. 多边形；多角形物体
    transition: 1s clip-path;
}
    img:hover {
    clip-path: polygon(0 0, 100% 0,
    100% 100%, 0 100%);
}
```



#### 切角效果 





#### 梯形标签页 





#### 简单的饼图

transform 的解决方案





<section style="display:flex;justify-content: space-around;">
        <svg width="200px" height="200px" style="background:orange;border-radius:50%;transform:rotate(-90deg);">
            <circle r="100" cx="100" cy="100" fill="orange" stroke="pink" stroke-width="200" stroke-dasharray="130 600"></circle>
    </svg>
</section> 


```css
重点： 圆的虚线边框`stroke-width`必须是 圆半径 r 的两倍
svg 语法 与 CSS 语法不一样的
<svg width="100px" height="100px"> // 设置绘画容器的大小 建立直角坐标系   svg 设置容器的大小
	<circle r="30" cx="50" cy="50"> // r 半径 (cx,cy) 设置圆心的坐标位置 设置形状 circle 圆形 cx/cy 坐标点 r 半径
</svg>

svg{
	transform:rotate(-90deg); // 旋转到从正半轴开始
	border-radius:50%;  //设置一个新的圆形填充缺失的部分
	background-color:teal; // 设置与原本的圆 fill 颜色一致的颜色
}

circle {
    fill: teal;  // fill 颜色
    stroke: pink; // 边框颜色
    stroke-width: 30; // 边框宽度
    stroke-dasharray:130 189(超出整个扇形图的周长); // stroke-dasharray 虚线的线段长度  间隙长度;
    圆形的周长C = 2πr，因此在这里 C=2π × 30 ≈ 189。
    虚线的线段长度 是扇形图 占用的比例  把虚线间隙的长度设置为等于或大于整个圆周的长度时
	//虚线边框 还有很多不那么为人所知的属性可以微调描边的效果，其中之一就是stroke-dasharray，它是为虚线描边而准备
注意点: 绘画扇形图的步骤 是 画圆内 ==> 画圆外

```

添加动画效果

```css
circle {
    fill: orange;
    stroke: purple;
    stroke-width: 250;
    stroke-dasharray: 10 900;
    animation: fillup 35s linear infinite;
}

@keyframes fillup {
    to {
       
        
    }
}
```

自动适应容器的大小

```
<svg>

</svg>
```



## 第四章 视觉效果

> box-shadow: 2px 3px 4px rgba(0,0,0,.5);	// 水平距离  垂直距离  模糊半径  阴影颜色
>
> 水平 和 垂直 距离是移动距离 模糊半径是指定在原图形的模糊距离
>
> box-shadow 的本质就是一个新的盒子 从  原本的元素中分开出来
>
> 默认方向是：右下角 



### 单侧投影

---

#### 单侧投影

<div style="width:200px;height:200px;box-shadow:0px 10px 10px red;background:pink;margin:auto"></div>

问题 

```css
box-shadow: 0px -10px 4px red; 
// 这种效果没有办法做出单侧阴影的效果,它会使左右两侧产生阴影
```

解决方法

最终的解决方案来自box-shadow 鲜为人知的第四个长度参数。它排在
模糊半径参数之后，称作扩张半径。这个参数会根据你指定的值去扩大或
（当指定负值时）缩小投影的尺寸。举例来说，一个-5px 的扩张半径会把投
影的宽度和高度各减少10px（即每边各5px）。

```

```



#### 邻近投影





#### 双侧投影

把投影设置在元素的两条对边（比如左侧和右侧）时

```

```





### 不规则投影

---





### 染色效果

---



### 毛玻璃效果

---

> 半透明颜色最初的使用场景之一就是作为背景。将其叠放在照片类或其他花哨的背层1①之上，可以减少对比度，确保文本的可读性。这种效果确实很有视觉冲击力，但仍然可能导致文字很难阅读，特别是当不透明度较低或背层图案太过花哨时

解决的思路

使用伪类元素::before 再重新使用一次 背景图片 + `filter:blur(20px)`再使用z-index 把这一层图片层叠到背景透明色块的下一层 （毛玻璃效果背景图片一共使用了两次）

重点隐藏掉

```css
body {  // 背景图片层  剩余不模糊的部分
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    background: url("./壁纸.jpg") center center fixed;

}
main {  // 字体文字层  filter: blur(20px);用在这一层会模糊掉字体
    width: 70%;
    margin: 100px auto;
    padding: 30px;
    font-size: 20px;
    line-height: 1.5;
    color: white;
    background: hsla(0, 0%, 100%, 0.3); 重点 第一个 没有百分号 第二个有
    border-radius: 8px;
    position: relative;
    overflow: hidden; // 把filter:blur(20px) 中模糊出来的部分隐藏 保持 ::before 层没有其他部分
}
main::before // 设置了一个新的一层HTML 的内容 content 里面的是html 内容
main::before { // 模糊背景图片层 将这一层放在 字体文字层的下一层 达成folter:blur(20px)  模糊的区域
    content: '';
    position: absolute; // 将两层的位置置于层叠
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    background: url("./壁纸.jpg") center center fixed;
    filter: blur(20px);
    z-index: -1;
    margin: -30px;
}
<main>
    <blockquote>
    " T I used to  me."
        <footer>
            <cite>
            "this is a blue"
            </cite>
        </footer>
    </blockquote>
</main>
//可以不用body中的清晰背景图片层 直接使用 毛玻璃效果（两层内容）
```

模糊效果在
中心区域看起来非常完美，但在接近边缘处会逐渐消退。这是因为模糊效果
会削减实色像素所能覆盖的范围，削减的幅度正是模糊半径的长度

为了补偿这种情况，我们需要让伪元素相对其宿主元素的尺寸再向
外扩大至少20px（即它的模糊半径）。可以通过-20px 的外边距来达到目
的，由于不同浏览器的模糊算法可能存在差异，用一个更大的绝对值（比
如-30px）会更保险一些。如图4-22 所示，这个方法可以修复边缘模糊消
伪元素模糊的方法基本上成功了，
但模糊效果在边缘处会逐渐消退，
削弱了毛玻璃的视觉效果
添加一个red 背景有助于解释
事情的真相
18　毛玻璃效果103
退的问题，但现在的情况是有一圈模糊效果超出了容器，这让它看起来不像
毛玻璃，而更像是玻璃脏了。

```
overflow: hidden;

::before
margin:-30px
```

### 折角效果

---





## 第五章 字体排印

### 连字符断行

---



### 插入换行

---





### 文本行的斑马条纹

---

### 调整tab 的宽度

---

### 连字 

---

### 华丽的& 符号 

---

### 自定义下划线 

---

### 现实中的文字效果 

---

### 环形文字

---



## 第六章 用户体验

### 选用合适的鼠标光标

---



### 扩大可点击区域

---



### 自定义复选框

---





### 通过阴影来弱化背景

---





### 通过模糊来弱化背景

---





### 滚动提示

---





### 交互式的图片对比控件

---





## 第七章 结构与布局

### 自适应内部元素

---





### 精确控制表格列宽

---





### 根据兄弟元素的数量来设置样式

---





### 满幅的背景，定宽的内容

---





### 垂直居中

---

水平居中

如果它是一个行内元素，就对它的父元素应用``text-align: center`；如果它是一个块级元素，就对它自身应用`margin: auto`。

#### 绝对定位

方法一：

局限性：它要求元素的宽高是固定的。在通常情况下，对那些需要居中的元素来说，其尺寸往往是由其内容来决定的。如果
能找到一个属性的百分比值以元素自身的宽高作为解析基准，那我们的难题就迎刃而解了！遗憾的是，对于绝大多数CSS 属性（包括margin）来说，百分比都是以其父元素的尺寸为基准进行解析的。

```css
section{
	 width: 100%;
     height: 500px;
     background-color: pink;
     position: relative;
}

.box{
	width: 18em;
    height: 14em;
    background-color: orange;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -7em; //	14em/2
    margin-left: -9em; //	18em/2
}
```

```css
.box{
	width:18em;
	height:6em;
	position:absolute;
	top:calc(50% - 3em);
	left:calc(50% - 9em);
}
```

方法二：

不用局限于宽度和高度

```css
.box{
	position:absolute;
	top:50%;
	left:50%;
	transform:translate(-50%,-50%);
}
```



#### 视口单位

> vw 是与视口宽度相关的。与常人的直觉不符的是，1vw 实际上表示
> 视口宽度的1%，而不是100%。
> 与 vw类似，1vh表示视口高度的 1%。
>
> 当视口宽度小于高度时，1vmin等于 1vw，否则等于 1vh。
> 当视口宽度大于高度时，1vmax等于 1vw，否则等于 1vh。

他是相对于视口（整个窗口） 居中的不是父元素居中的

```
main { // 设置父元素
    width: 18em;
    padding: 1em 1.5em;
    margin: 50vh auto 0; 
    transform: translateY(-50%);
}
```

#### FlexBox

```css
body{ //父元素
	display:flex;
	min-height:100vh;
	margin:0;
}

main{ // 子元素
	margin:auto;
}
```

```
body{ //父元素
	width:18em;
	height:10em;
	display:flex;
	align-item:center;
	justify-content:center;
}
```



### 紧贴底部的页脚

---

```html
<header>
<h1>Site name</h1>
</header>
<main>
<p>Bacon Ipsum dolor sit amet...
<!-- 从baconipsum.com那里复制一些示意文字过来 --></p>
</main>
<footer>
<p>© 2015 No rights reserved.</p>
<p>Made with ♥ by an anonymous pastafarian.</p>
</footer>
```

固定高度





FlexBox的解决方法



```css
body{
	display: flex;
	flex-flow:column;
	min-height:100vh;
}
main{
	flex:1;  //flex: flex-grow flex-shrink flex-basis;
}
```



## 第八章过渡和动画

### 缓动效果

---



### 逐帧动画

---



### 闪烁效果

---





### 打字动画

---





### 状态平滑的动画

---





### 沿环形路径平移的动画







