---
title: Bootstrap3学习
categories:
  - 前端
  - Bootstrap
tags:
  - Bootstrap3
abbrlink: 531
---
# Bootstrap3 `基础、样式、组件、插件`
Bootstrap 是最受欢迎的 HTML、CSS 和 JS 框架（前端组件库），用于开发响应式布局、移动设备优先的 WEB 项目。
[50个Bootstrap扩展插件 - 芮源 - 博客园](https://www.cnblogs.com/ruiyuan/p/11242190.html)
## <font color="red">零、VSCode插件</font>
### Bootstrap 3 snippets 使用方法
[Bootstrap 3 sinippets插件安装](https://github.com/JasonMortonNZ/bs3-sublime-plugin/)
[Bootstrap 3 snippets使用文档](https://github.com/JasonMortonNZ/bs3-sublime-plugin/blob/master/README.md)
### Bootstrap 4, Font awesome 4, Font Awesome 5 Free & Pro snippets使用方法
[bootstrap4-snippets/vscode at master · 1tontech/bootstrap4-snippets](https://github.com/1tontech/bootstrap4-snippets/tree/master/vscode)
## <font color="red">一、基础</font>
### 概念
- Bootstrap 是最受欢迎的 HTML、CSS 和 JS 框架，用于开发响应式布局、移动设备优先的 WEB 项目。
- 是基于HTML、CSS、JavaScript的一个简洁、灵活的开源框架
- 快速、简单、灵活的栅格系统、小而强大、响应式布局
- 跨平台、简单、直观、强悍的前端开发框架，让web开发更迅速、简单
- 使用场景：响应式界面、移动端页面、后台页面、带交互效果的页面
- bootstrap插件是基于jquery要在引入bootstrap.min之前引入jquery文件
### 快速输入
#### CDN + Local + Template
| Component                                  | Snippet code      |
| ------------------------------------------ | ----------------- |
| HTML5 Template Layout                      | bs3-template:html |
| Link to local bootstrap All files(CSS、JS) | bs3-local         |
| CDN link (both CSS & JS)                   | bs3-cdn           |
| CDN link (CSS only)                        | bs3-cdn:css       |
| CDN link (JS only)                         | bs3-cdn:js        |
### 安装
#### 移动设备优先
```html
<meta name="viewport" content="width="device-width,user-scalable=no,initial-scale=1.0 />//initial-scale=1 缩放比 = 1 不缩放
```
#### npm安装
```js
npm install bootstrap@3
npm install bootstrap@4
```
#### 本地文件
```html
<meta name="viewport" content="width="device-width,user-scalable=no,initial-scale=1.0 />//initial-scale=1
<link href="bootstrap.css" rwl="stylesheet">
<body>
    <script src="jquery.js"></script>
	<script src="bootstrap.js"></script>
</body>
//用于生产环境的 Bootstrap boostrap.min.js 文件
//用于开发环境的 Bootstrap bootstrap.js 文件
```
#### [CDN](https://www.bootcdn.cn/twitter-bootstrap/)
```html
<!-- 最新版本的 Bootstrap 核心 CSS 文件 -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@3.3.7/dist/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
<!-- 可选的 Bootstrap 主题文件（一般不用引入） -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@3.3.7/dist/css/bootstrap-theme.min.css" integrity="sha384-rHyoN1iRsVXV4nD0JutlnGaslCJuC7uwjduW9SVrLvRYooPp2bWYgmgJQIXwl/Sp" crossorigin="anonymous">
<!-- 最新的 Bootstrap 核心 JavaScript 文件 jquery.min.js+bootstrap.min.js 位置 body里面而不是head -->
<script src="https://cdn.jsdelivr.net/npm/jquery@1.12.4/dist/jquery.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@3.3.7/dist/js/bootstrap.min.js"></script>
```
> CDN与本地文件引入的区别:
>
> CDN没有代码提示，本地引入会有代码提示、CDN(内容分发网络)、CDN引入需要网络
### 目录结构
#### 预编译版 dist
```html
bootstrap/
├── css/
│   ├── bootstrap.css
│   ├── bootstrap.css.map
│   ├── bootstrap.min.css
│   ├── bootstrap.min.css.map
│   ├── bootstrap-theme.css
│   ├── bootstrap-theme.css.map
│   ├── bootstrap-theme.min.css
│   └── bootstrap-theme.min.css.map
├── js/
│   ├── bootstrap.js
│   └── bootstrap.min.js
└── fonts/
    ├── glyphicons-halflings-regular.eot
    ├── glyphicons-halflings-regular.svg
    ├── glyphicons-halflings-regular.ttf
    ├── glyphicons-halflings-regular.woff
    └── glyphicons-halflings-regular.woff2
//fonts 字体文件 eot/svg/ttf/woff/woff2
```
#### 源码
```html
bootstrap/
├── less/
├── js/
├── fonts/
├── dist/
│   ├── css/
│   ├── js/
│   └── fonts/
└── docs/
    └── examples/ //docs/examples/ 实例
```
## <font color="red">二、样式</font>
### 概览
#### HTML5文档类型（Doctype）
#### 移动设备优先
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
#### 响应式图像
```html
<img src="..." class="img-responsive" alt="响应式图像">
```
#### 全局显示、排列和链接
##### 基本的全局显示
```css
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 14px;
  line-height: 1.428571429;
  color: #333333;
  background-color: #ffffff;
}
```
##### 排版与链接样式(a)
使用 @font-family-base、 @font-size-base 和 @line-height-base 属性作为排版样式。
```css
a:hover,
a:focus {
  color: #2a6496;
  text-decoration: underline;
}
a:focus {
  outline: thin dotted #333;
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
```
链接没有下划线,hover出现下划线
##### 布局容器
.container类 用于**固定宽度**并支持响应式布局的容器 
```html
<div class="container"></div>
```
.container-fluid类 用于**100%宽度**,占据全部视口(Viewport)的容器
```html
<div class="container-fluid"></div>
```
### 栅栏系统（网络系统）
---
#### Grid
**Note:** The bs3-col snippet can be used both on its own or with the addition of a colon followed by the number of columns required: **E.g.**
- bs3-col
- bs3-col:6
- bs3-col:12
| Component | Snippet code  | Options |
| --------- | ------------- | ------- |
| Column    | bs3-col       | :1-12   |
| Row       | bs3-row       |         |
| Container | bs3-container |         |
一套响应式、移动设备优先的流式网格系统，随着屏幕或视口（viewport）尺寸的增加，系统会自动分为最多``12列``。
`多余的列（column）将另起一行排列`
#### 媒体查询
```html
@media (min-width: @screen-md-min) { ... }
@media (min-width: @screen-sm-min) and (max-width: @screen-sm-max) { ... }
```
#### 网格选项`768px、992px、1200px`
| 超小设备手机（<768px） | 小型设备平板电脑（≥768px） | 中型设备台式电脑（≥992px） | 大型设备台式电脑（≥1200px） |
| ---------------------- | -------------------------- | -------------------------- | --------------------------- |
| .col-xs-               | .col-sm-                   | .col-md-                   | .col-lg-                    |
| xs < 768px             | 768px<= sm < 992px         | 992px <= md <= 1200px      | 1200px=<lg                  |
```html
<div class="row">
	<div class="col-lg-x col-md-x cd-sm-x cd-xs-x"></div>
    <div class="col-lg-x col-md-x cd-sm-x cd-xs-x"></div>
    <div class="col-lg-x col-md-x cd-sm-x cd-xs-x"></div>
</div>
[class*="col-"]{} //通配选择器
```
#### 列偏移
col-md-offset-* 偏移量	列向右侧偏移
#### 列重置
​	在某些阈值时，某些列可能会出现比别的列高的情况。为了克服这一问题，建议联合使用 .clearfix 和 响应式工具类。
​	.clearfix
```html
<div class="clearfix visible-xs-block"></div>
```
#### 嵌套列
- ​	在一个列里面又嵌套一个列
- ​	被嵌套的行（row）所包含的列（column）的个数不能超过12（其实，没有要求你必须占满12列）
#### 列排序
- 交换位置 .col-md-push-* (后面) .col-md-pull-*(前面) 位移
### 排版
---
#### 标题
HTML 中的所有标题标签，`` 到 `` 均可使用。另外，还提供了 `.h1` 到 `.h6` 类，为的是给内联（inline）属性的文本赋予标题的样式。
```html
h1~h6 ||  .h1~.h6
```
#### 副标题
```html
<h1>h1标题<small>副标题</small></h1>
```
#### 页面主体
全局 font-size 14px line-height 1.428 p元素（段落）还被设置了等于1/2行高（即10px）的底部外边框（margin）。
#### 内联文本元素
|                            标签                             |          作用          |
| :---------------------------------------------------------: | :--------------------: |
|                            mark                             |      Marked text       |
|                             del                             |      被删除的文本      |
|                              s                              |        无用文本        |
|                             ins                             |        插入文本        |
|                          strong、b                          |          着重          |
|                              u                              |     带下划线的文本     |
|                            i、em                            |          斜体          |
|                            small                            |        小号文本        |
|       p.text-lowercase/text-uppercase/text-capitalize       | 小写、大写、首字母小写 |
| p.text-left/text-center/text-right/text-justify/text-nowrap |        文本对齐        |
```html
//HTML标签
<mark></mark> 添加一个背景颜色的效果,默认的效果
<del></del> 删除线
<s></s> 无用文本 与删除线效果一致
<u></u> 下划线
<ins></ins> 插入文本 效果以下划线一致
小号文本 即是缩小 font-size <small></small>
着重 <strong></strong>
斜体 <em></em>
//对齐
p.text-left
p.text-center
p.text-right
p.justify
p.text-nowrap
// 改变大小写
p.text-lowecase  小写
p.text-uppercase	大写
p.text-capitalize	首字母大写
```
#### 中心内容
通过.lead类可以让段落突出显示
```html
<p class="lead"></p>
```
#### 缩略语
##### 基本缩略语
```html
<abbr title="attribute">attr</abbr> //效果下划线虚线，鼠标移到虚线出现问号
```
##### 首字母缩略语
```html
<abbr title="HyperText Markup Language" class="initialism">HTML</abbr>
//为缩略语添加 .initialism 类，可以让 font-size 变得稍微小些。
```
#### 地址
```html
<address>
让联系信息以最接近日常使用的格式呈现。在每行结尾添加呈现<br>可以保留需要的样式。
</address>
```
#### 引用
```html
默认样式的引用
<blockquote>
效果：前面有小标识
直接引用
<blockquote>
<p></p>
</blockquote>
多种引用样式
添加<footer> 用于标明引用来源。来源的名称可以包裹进<cite> 标签中。
<blockquote>
<p></p>
<footer><cite title="source Title"></site><footer>
</blockquote>
 //右对齐   
<blockquote class="blockquote-reverse">
 </blockquoteb>
```
#### 列表
1. ##### 有序列表
```html
<ol>
<li></li>
</ol>
```
2. ##### 无序列表
```html
<ul>
<li></li>
</ul>
```
3. ##### 无样式列表(list-unstyled)
移除了默认的list-style样式和左侧外边距的一组元素（只针对直接子元素）
```html
<ul class="list-unstyled">
<li></li>
</ul>
```
4. ##### 内联列表(list-inline)
设置display:inline-block;并添加少量的内补（padding）,``将所有元素放置于同一行 水平排列``
```html
<ul class="list-inline">
<li></li>
</ul>
```
5. ##### 描述
带有描述的短语列表
水平排列的描述 .``dl-horizontal`
```html
.dl-horizontal 可以让<dl> 内短语及其描述排在第一行，开始是像<dl>的默认样式堆叠在一起，随着导航条逐渐展开而排列在一行
<dl class="dl-horizontal">
  <dt>...</dt>
  <dd>...</dd>
</dl>
```
### 代码
---
#### 内联代码 `<code>`
```html
<code>内联代码</code>
```
#### 代码块`<pre>`
```html
多行代码使用块<pre> 
&lt;     
$gt;
```
#### 用户输入`<kbd>`
```html
<kdb>标签标记用户通过键盘输入的内容</kdb>
```
#### 变量`<var>`
```html
<var>标签标记变量</var>
```
#### 程序输出`<samp>`
```html
<samp>标记程序输出的内容</samp>
```
### 表格
---
#### Tables
| Component       | Snippet code                    |
| --------------- | ------------------------------- |
| Table           | bs3-table 表格                  |
| Bordered Table  | bs3-table:bordered 带边框的表格 |
| Condensed Table | bs3-table:condensed 紧缩表格    |
| Hover Table     | bs3-table:hover 鼠标悬停        |
| Striped Table   | bs3-table:striped 条纹表格      |
#### 基本实例
`.table`
```
<table> 标签添加.table类 可以为其赋予基本的样式--少量的内补（padding）和水平方向得分割线。
<div class="container">
	<table class="table">
		<thread>
			<tr>
				<th>表格标题</th>
				<th>表格标题</th>
				<th>表格标题</th>
			</tr>
		</thread>
		<tbody>
			<tr>
				<td>表格内容</td>
				<td>表格内容</td>
				<td>表格内容</td>
			</tr>
			<tr>
				<td>表格内容</td>
				<td>表格内容</td>
				<td>表格内容</td>
			</tr>
		</tbody>
	</table>
</div>
```
#### 条纹状表格
`.table .table-striped`
通过.table-stripe 类可以给<tbody>之内的每一行增加斑马条纹样式,每隔一行，出现颜色隔行
```
<table class="table table-stripe">
</table>
```
#### 带边框的表格
`.table .table-bordered`
添加.table-bordered 类为表格和其中的每一个单元格增加边框
```
<table class="table table-bordered">
</table>
```
#### 鼠标悬停
`.table .table:hover`
```
<table class="table table-hover">
</table>
```
#### 紧缩表格
`.table table-condensed`
通过添加 `.table-condensed` 类可以让表格更加紧凑，单元格中的内补（padding）均会减半。
```
<table class="table table-condensed">
  ...
</table>
```
#### 状态类
通过这些类可以为行或单元格设置颜色
| Class      | 描述                                           |
| :--------- | :--------------------------------------------- |
| `.active`  | 鼠标**悬停**在行或单元格上时所设置的颜色  绿色 |
| `.success` | 标识**成功**或积极的动作 蓝色                  |
| `.info`    | 标识普通的**提示信息**或动作                   |
| `.warning` | 标识**警告**或需要用户注意  黄色               |
| `.danger`  | 标识**危险**或潜在的带来负面影响的动作红色     |
```html
<!-- On rows -->
<tr class="active">...</tr>
<tr class="success">...</tr>
<tr class="warning">...</tr>
<tr class="danger">...</tr>
<tr class="info">...</tr>
<!-- On cells (`td` or `th`) -->
<tr>
  <td class="active">...</td>
  <td class="success">...</td>
  <td class="warning">...</td>
  <td class="danger">...</td>
  <td class="info">...</td>
</tr>
```
#### 响应式表格
```html
<div class="table-responsive">
  <table class="table">
    ...
  </table>
</div>
```
### 表单
---
#### 表单的分类
> 表单域``<form>`` 
>
> 提示信息`<label>`
>
> 表单控件（表单元素）`input 表的输入标签/select 菜单列表标签/textarea 文本域标签`
#### Forms
| Component       | Snippet code                 |
| --------------- | ---------------------------- |
| Form            | bs3-form 表单                |
| Inline Form     | bs3-form:inline 内联表单     |
| Horizontal Form | bs3-form:horizontal 水平表单 |
#### Input Fields (Form fields)
**Note:** you can add " :h " to the end of any input field snippet to make it compatible with Bootstrap 3 horizontal forms. **E.g.**
- bs3-input:text:h
- bs3-input:hidden:h
| Component       | Snippet code       | Options |
| --------------- | ------------------ | ------- |
| Label           | bs3-input:label    |         |
| Text Input      | bs3-input:text     | :h      |
| Email Input     | bs3-input:email    | :h      |
| Password Input  | bs3-input:password | :h      |
| Hidden Input    | bs3-input:hidden   | :h      |
| Url Input       | bs3-input:url      | :h      |
| Color Input     | bs3-input:color    | :h      |
| Number Input    | bs3-input:number   | :h      |
| Range Input     | bs3-input:range    | :h      |
| Date Input      | bs3-input:date     | :h      |
| Week Input      | bs3-input:week     | :h      |
| Month Input     | bs3-input:month    | :h      |
| Time Input      | bs3-input:time     | :h      |
| Tel Input       | bs3-input:tel      | :h      |
| Search Input    | bs3-input:search   | :h      |
| Reset Input     | bs3-input:reset    | :h      |
| Submit Input    | bs3-input:submit   | :h      |
| Checkbox Input  | bs3-input:checkbox | :h      |
| Radio Box Input | bs3-input:radio    | :h      |
| Select Box      | bs3-select         | :h      |
| Textarea        | bs3-textarea       | :h      |
#### Labels
| Component     | Snippet code      |
| ------------- | ----------------- |
| Label         | bs3-label         |
| Danger Label  | bs3-label:danger  |
| Info Label    | bs3-label:info    |
| Success Label | bs3-label:success |
| Warning Label | bs3-label:warning |
#### 基本实例
> input、textarea、select .form-control
>
> 所有设置了 `.form-control` 类的 input、textarea、select 元素都将被默认设置宽度属性为 width: 100%;。
>
> ```html
> <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
> ```
>
> label .form-group
>
> `label` 元素和前面提到的控件包裹在 `.form-group` 中可以获得最好的排列。
>
> ```html
>  <div class="form-group">
>     <label for="exampleInputEmail1">Email address</label>
>     <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
>   </div>
> ```
```html
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-group">
    <label for="exampleInputFile">File input</label>
    <input type="file" id="exampleInputFile">
    <p class="help-block">Example block-level help text here.</p>
  </div>
  <div class="checkbox">
    <label>
      <input type="checkbox"> Check me out
    </label>
  </div>
  <button type="submit" class="btn btn-default">Submit</button>
</form>
```
#### 内联表单`排列在一行`
- 可能需要手动设置宽度
- 一定要添加 `label` 标签
·`form-inline 类可使其内容左对齐并且表现为 inline-block 级别的控件,让块级并列的input 内联`
#### 水平排列的表单`排列在多行`
通过为表单添加 ``.form-horizontal 类``，并联合使用 Bootstrap 预置的栅格类，可以将 label 标签和控件组水平并排布局。这样做将改变 .form-group 的行为，使其表现为栅格系统中的行（row），因此就无需再额外添加 .row 了。
```html
<form class="form-horizontal">
  <div class="form-group">
    <label for="inputEmail3" class="col-sm-2 control-label">Email</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="inputEmail3" placeholder="Email">
    </div>
  </div>
  <div class="form-group">
    <label for="inputPassword3" class="col-sm-2 control-label">Password</label>
    <div class="col-sm-10">
      <input type="password" class="form-control" id="inputPassword3" placeholder="Password">
    </div>
  </div>
  <div class="form-group">
    <div class="col-sm-offset-2 col-sm-10">
      <div class="checkbox">
        <label>
          <input type="checkbox"> Remember me
        </label>
      </div>
    </div>
  </div>
  <div class="form-group">
    <div class="col-sm-offset-2 col-sm-10">
      <button type="submit" class="btn btn-default">Sign in</button>
    </div>
  </div>
</form>
```
#### 被支持的控件
##### 输入框 input
包括大部分表单控件、文本输入域控件，还支持所有 HTML5 类型的输入控件： `text、password、datetime、datetime-local、date、month、time、week、number、email、url、search、tel 和 color`。
```html
<input type="text" class="form-control" placeholder="Text input">
```
##### 文本域 textarea
```html
<textarea class="form-control" rows="3"></textarea>
```
##### 多选和单选框 input:ckeckbox/input
`默认（块级）和内联两种.checkbox/.radio-inline`
```html
多选:checkbox
单选:radio
```
###### 默认外观(单选按钮与文字堆叠在一起)
```html
<div class="checkbox">
  <label>
    <input type="checkbox" value="">
    Option one is this and that&mdash;be sure to include why it's great
  </label>
</div>
<div class="checkbox disabled">
  <label>
    <input type="checkbox" value="" disabled>
    Option two is disabled
  </label>
</div>
<div class="radio">
  <label>
    <input type="radio" name="optionsRadios" id="optionsRadios1" value="option1" checked>
    Option one is this and that&mdash;be sure to include why it's great
  </label>
</div>
<div class="radio">
  <label>
    <input type="radio" name="optionsRadios" id="optionsRadios2" value="option2">
    Option two can be something else and selecting it will deselect option one
  </label>
</div>
<div class="radio disabled">
  <label>
    <input type="radio" name="optionsRadios" id="optionsRadios3" value="option3" disabled>
    Option three is disabled
  </label>
</div>
```
###### 内联单选和多选框
`.checkbox/.radio-inline`
```html
label通过将 .checkbox-inline 或 .radio-inline 类应用到一系列的多选框（checkbox）或单选框（radio）控件上，可以使这些控件排列在一行。
两个元素内联对齐
<label class="checkbox-inline">
  <input type="checkbox" id="inlineCheckbox1" value="option1"> 1
</label>
<label class="checkbox-inline">
  <input type="checkbox" id="inlineCheckbox2" value="option2"> 2
</label>
<label class="checkbox-inline">
  <input type="checkbox" id="inlineCheckbox3" value="option3"> 3
</label>
<label class="radio-inline">
  <input type="radio" name="inlineRadioOptions" id="inlineRadio1" value="option1"> 1
</label>
<label class="radio-inline">
  <input type="radio" name="inlineRadioOptions" id="inlineRadio2" value="option2"> 2
</label>
<label class="radio-inline">
  <input type="radio" name="inlineRadioOptions" id="inlineRadio3" value="option3"> 3
</label>
```
##### 下拉列表（select）
```html
标记了 multiple 属性的 <select> 控件来说，默认显示多选项。
<select multiple class="form-control">
  <option>1</option>
  <option>2</option>
  <option>3</option>
  <option>4</option>
  <option>5</option>
</select>
```
#### 静态控件
如果需要在表单中将一行纯文本和 label 元素放置于同一行，为 <p> 元素添加 .form-control-static 类即可， `	form-control-static`
```html
<form class="form-horizontal">
  <div class="form-group">
    <label class="col-sm-2 control-label">Email</label>
    <div class="col-sm-10">
      <p class="form-control-static">email@example.com</p>
    </div>
  </div>
  <div class="form-group">
    <label for="inputPassword" class="col-sm-2 control-label">Password</label>
    <div class="col-sm-10">
      <input type="password" class="form-control" id="inputPassword" placeholder="Password">
    </div>
  </div>
</form>
```
#### 焦点状态
默认，将某些表单控件的默认 outline 样式移除，然后对 :focus 状态赋予 box-shadow 属性。
#### 禁用状态
`disabled`
```html
<input class="form-control" id="disabledInput" type="text" placeholder="Disabled input here..." disabled>
```
#### 只读状态
为输入框设置 `readonly `属性可以禁止用户修改输入框中的内容。处于只读状态的输入框颜色更浅（就像被禁用的输入框一样），但是仍然保留标准的鼠标状态。
```html
<input class="form-control" type="text" placeholder="Readonly input here…" readonly>
```
#### Help text
帮助文本
`.help-block`
将帮助文本与表单控件相关联
```html
<label class="sr-only" for="inputHelpBlock">Input with help text</label>
<input type="text" id="inputHelpBlock" class="form-control" aria-describedby="helpBlock">
...
<span id="helpBlock" class="help-block">A block of help text that breaks onto a new line and may extend beyond one line.</span>
```
#### 校验状态
​		Bootstrap 对表单控件的校验状态，如 error、warning 和 success 状态，都定义了样式。使用时，添加 .has-warning、.has-error 或 .has-success 类到这些控件的父元素即可。任何包含在此元素之内的 .control-label、.form-control 和 .help-block 元素都将接受这些校验状态的样式。
​		.has-warning、.has-error、。has-success
​		.control-label、.form-control 和 .help-block 
​	添加额外的图标
​		你还可以针对校验状态为输入框添加额外的图标。只需设置相应的 .has-feedback 类并添加正确的图标即可
​		反馈图标（feedback icon）只能使用在文本输入框 <input class="form-control"> 元素上。
#### 控件尺寸 `宽度||高度`
`通过 .input-lg 类似的类可以为控件设置高度，通过 .col-lg-* 类似的类可以为控件设置宽度。`
##### 高度尺寸 input select
```html
.input-lg / .input-sm
<input class="form-control input-lg" type="text" placeholder=".input-lg">
<input class="form-control" type="text" placeholder="Default input">
<input class="form-control input-sm" type="text" placeholder=".input-sm">
<select class="form-control input-lg">...</select>
<select class="form-control">...</select>
<select class="form-control input-sm">...</select>
```
##### 水平排列的表单组的尺寸
通过添加 .form-group-lg 或 .form-group-sm 类，为 .form-horizontal 包裹的 label 元素和表单控件快速设置尺寸。
​form .form-horizontal包裹的 label 元素和表单控件快速设置尺寸。
​form-group-lg || form-group-sm
```html
<form class="form-horizontal">
  <div class="form-group form-group-lg">
    <label class="col-sm-2 control-label" for="formGroupInputLarge">Large label</label>
    <div class="col-sm-10">
      <input class="form-control" type="text" id="formGroupInputLarge" placeholder="Large input">
    </div>
  </div>
  <div class="form-group form-group-sm">
    <label class="col-sm-2 control-label" for="formGroupInputSmall">Small label</label>
    <div class="col-sm-10">
      <input class="form-control" type="text" id="formGroupInputSmall" placeholder="Small input">
    </div>
  </div>
</form>
```
##### 调整列（column）尺寸
用栅格系统中的列（column）包裹输入框或其任何父元素，都可很容易的为其设置宽度。
```html
<div class="row">
  <div class="col-xs-2">
    <input type="text" class="form-control" placeholder=".col-xs-2">
  </div>
  <div class="col-xs-3">
    <input type="text" class="form-control" placeholder=".col-xs-3">
  </div>
  <div class="col-xs-4">
    <input type="text" class="form-control" placeholder=".col-xs-4">
  </div>
</div>
```
### 按钮
----
#### 按钮
> 为 a、button、input元素添加按钮类（button class）即可使用 Bootstrap 提供的样式。
```html
<a class="btn btn-default" href="#" role="button">Link</a>
<button class="btn btn-default" type="submit">Button</button>
<input class="btn btn-default" type="button" value="Input">
<input class="btn btn-default" type="submit" value="Submit">
```
#### 预定义样式
- 默认样式 Default  浅灰色 	btn-default
- 首选项 Primary 深蓝色        btn-primary
- 成功 Success 绿色                btn-success
- 一般信息 Info 浅蓝色           btn-info
- 警告 Warning 黄色               btn-warning
- 危险 Danger 红色                 btn-danger
- 链接 Link                               btn-link
```html
<!-- Standard button -->
<button type="button" class="btn btn-default">（默认样式）Default</button>
<!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
<button type="button" class="btn btn-primary">（首选项）Primary</button>
<!-- Indicates a successful or positive action -->
<button type="button" class="btn btn-success">（成功）Success</button>
<!-- Contextual button for informational alert messages -->
<button type="button" class="btn btn-info">（一般信息）Info</button>
<!-- Indicates caution should be taken with this action -->
<button type="button" class="btn btn-warning">（警告）Warning</button>
<!-- Indicates a dangerous or potentially negative action -->
<button type="button" class="btn btn-danger">（危险）Danger</button>
<!-- Deemphasize a button by making it look like a link while maintaining button behavior -->
<button type="button" class="btn btn-link">（链接）Link</button>
```
#### 尺寸
需要让按钮具有不同尺寸吗？使用 `.btn-lg`、`.btn-sm` 或 `.btn-xs` 就可以获得不同尺寸的按钮。
#### 激活状态 .active
button元素
	由于 :active 是伪状态，因此无需额外添加，但是在需要让其表现出同样外观的时候可以添加 .active 类。
链接<a>元素
	可以为基于 <a> 元素创建的按钮添加 .active 类
#### 禁用状态 
通过为按钮的背景设置 opacity 属性就可以呈现出无法点击的效果。
button元素
	disabled="disabled"
链接a元素
	.disabled
### 图片
---
#### Images
| Component              | Snippet code          |
| ---------------------- | --------------------- |
| Thumbnail              | bs3-thumbnail         |
| Thumbnail with content | bs3-thumbnail:content |
#### 响应式图片
`.img-responsive `响应式图片
其实质是为图片设置了 max-width: 100%;、 height: auto; 和 display: block; 属性，从而让图片在其父元素中更好的缩放。
如果需要让使用了 .img-responsive 类的图片水平居中，请使用 .center-block 类，不要用 .text-center。 请参考助手类章节 了解更多关于 .center-block 的用法。
`.center-block ` 图片水平居中
#### 图片形状
| 图片名称      | 图片形状       |
| ------------- | -------------- |
| img-rounded   | 带圆角的正方形 |
| img-circle    | 圆             |
| img-thumbnail | 带边框         |
### 辅助类
---
#### 情境文本颜色
| class类名      | 功能作用 |
| -------------- | -------- |
| p.text-muted   |          |
| p.text-primary |          |
| p.text-success |          |
| p.text-info    |          |
| p.text-warning |          |
| p.text-danger  |          |
#### 情境背景色
| class类名    | 功能作用 |
| ------------ | -------- |
| p.bg-primary |          |
| p.bg-success |          |
| p.bg-info    |          |
| p.bg-warning |          |
| p.bg-danger  |          |
#### 关闭按钮
通过使用一个象征关闭的图标，可以让模态框和警告框消失。
```html
<button type="button" class="close" aria-label="Close"><span aria-hidden="true">&times;</span></button>
```
#### 三角符号
​	通过使用三角符号可以指示某个元素具有下拉菜单的功能。注意，向上弹出式菜单中的三角符号是反方向的。
```html
<span class="caret"></span>
```
#### 快速浮动
通过添加一个类，可以将任意元素向左或向右浮动。
```html
<div class="pull-left">...</div>
<div class="pull-right">...</div>
```
不能用于导航条组件中
排列导航条中的组件时可以使用这些工具类：`.navbar-left` 或 `.navbar-right` 。
#### 让内容块居中	
`.center-block`
```html
<div class="center-block"></div>
```
#### 清除浮动
#### Clearfix
| Component | Snippet code |
| --------- | ------------ |
| Clearfix  | bs3-clearfix |
`.clearfix`
```
.clearfix类可以很容易清除浮动（float）
```
#### 显示或隐藏内容
``.hidden 、 .sr-only 或 .show``
`.show` 和 `.hidden` 类可以强制任意元素显示或隐藏(**对于屏幕阅读器也能起效**)。这些类通过 `!important` 来避免 CSS 样式优先级问题，就像 [quick floats](https://v3.bootcss.com/css/#helper-classes-floats) 一样的做法。注意，这些类只对块级元素起作用，另外，还可以作为 mixin 使用。
`.hide` 类仍然可用，但是它不能对屏幕阅读器起作用，并且从 v3.0.1 版本开始就**不建议使用**了。请使用 `.hidden` 或 `.sr-only` 。
另外，`.invisible` 类可以被用来仅仅影响元素的可见性，也就是说，元素的 `display` 属性不被改变，并且这个元素仍然能够影响文档流的排布。
```
<div class="show">...</div>
<div class="hidden">...</div>
```
#### 屏幕阅读器和键盘导航
`.sr-only` 类可以对隐藏内容。`.sr-only` 和 `.sr-only-focusable` 联合使用的话可以在元素有焦点的时候再次显示出来（例如，使用键盘导航的用户）。
```html
<a class="sr-only sr-only-focusable" href="#content">Skip to main content</a>
```
#### 图片替换
使用 .text-hide 类或对应的 mixin 可以用来将元素的文本内容替换为一张背景图。
```html
<h1 class="text-hide">Custom heading</h1> //文本内容隐藏
```
### 响应式工具
---
#### 可用的类
##### 屏幕尺寸
| 屏幕                 | 尺寸         |
| -------------------- | ------------ |
| 超小屏幕    （手机） | 0~768px      |
| 小屏幕  （平板）     | 768px~992px  |
| 中等屏幕（桌面）     | 992px~1200px |
| 大屏幕 （桌面）      | 1200px以上   |
##### 针对不同屏幕尺寸隐藏或显示页面内容。
.col-屏幕标识符-*
```html
.visible-屏幕标识符-*
visible 显示当前屏幕的
.hidden-屏幕标识符
hidden 隐藏当前屏幕的
```
v3.2.0版本起
```html
.visible-*-block  //display:block
.visible-*-inline 	//display:inline
.visible-*-inline-block //display:inline-block
```
​		
## <font color="red">三、组件</font>
### 字体图标
---
#### Icons
| Component           | Snippet code       |
| ------------------- | ------------------ |
| Glyphicon           | bs3-icon:glyphicon |
| Icon (Font Awesome) | bs3-icon           |
[Customize 字形图标（Glyphicons） 字体图标定制](https://www.runoob.com/try/demo_source/bootstrap-glyph-customization.htm)
#### CDN使用
```html
.glyphicons 图标名称（.glyphicons）
<i class="glyphicon glyphicon-search" aria-hidden="true"></i>
<span class="glyphicon glyphicon-open-file" aria-hidden="true"></span>
图标装饰用做设置使用 aria-hidden="true"属性
使用图标是为了表达某些含义（不仅仅是为了装饰用） 设置aria-lablel="图标表示的含义"
```
#### 本地网络使用
本地文件字体font目录
- glyphicons-halflings-regular.eot
- glyphicons-halflings-regular.svg
- glyphicons-halflings-regular.ttf
- glyphicons-halflings-regular.woff
无需用@font-face的方式引入，无需引入、只要用CDN的方法使用，但是需要本地用字体文件在font文件夹下
#### 图标大小
```html
<button type="button" class="btn btn-primary btn-lg" style="font-size: 60px">
  <span class="glyphicon glyphicon-user"></span> User
</button>
```
### 表单
---
#### 基本实例
​	
#### 内联表单
#### 输入框组
#### 下拉菜单
下拉菜单
	.dropdown
		速度打
			b4-dropdown-default
	.dropup
		b4-dropdown-up
	对齐
	标题
	分割线
	禁用的菜单项
#### 按钮组
#### Input-groups
| Component                       | Snippet code               |
| ------------------------------- | -------------------------- |
| Input group                     | bs3-input-group            |
| Input group(addon & text-field) | bs3-input-group:addon:text |
| Input group (addon)             | bs3-input-group-addon      |
| Input group (button)            | bs3-input-group-btn        |
| Input group (text-field & btn)  | bs3-input-group:text:btn   |
#### 按钮式下拉菜单
按钮式下拉菜单
	单按钮下拉菜单
		只要改变一些基本的标记，就能把按钮变成下拉菜单的开关。
	分裂式按钮下拉菜单
		btn btn-danger
		btn btn-primary
		btn btn-sucess
		btn btn-info
		btn btn-warning
	尺寸
		btn-lg
		btn-sm
		btn-xs
	向上弹出式菜单
		给父元素添加 .dropup 类就能使触发的下拉菜单朝上方打开。
		btn-group dropup
####  Buttons
**Note:** all button snippets below can have any of the following options append to the end of the snippet *.
- :danger
- :default
- :disabled
- :info
- :primary
- :success
- :warning
**An example:**
- bs3-button:success
- bs3-large-button:disabled
- bs3-block-button:warning
| Component    | Snippet code     | Options |
| ------------ | ---------------- | ------- |
| Button       | bs3-button       | *       |
| Block Button | bs3-block-button | *       |
| Mini Button  | bs3-xs-button    | *       |
| Small Button | bs3-sm-button    | *       |
| Large Button | bs3-lg-button    | *       |
### 导航`导航 <nav>+ 导航条<navbar> 面包屑导航<breadcrumbs>`
----
#### Navigation 导航条
| Component             | Snippet code            |
| --------------------- | ----------------------- |
| Navbar (basic navbar) | bs3-navbar              |
| Navbar Brand Element  | bs3-navbar:brand        |
| Navbar Button         | bs3-navbar:button       |
| Navbar Form           | bs3-navbar:form         |
| Navbar Link           | bs3-navbar:link         |
| Navbar Text           | bs3-navbar:text         |
| Navbar Fixed-Botton   | bs3-navbar:fixed-bottom |
| Navbar Fixed-Top      | bs3-navbar:fixed-top    |
| Navbar Inverse        | bs3-navbar:inverse      |
| Navbar Responsive     | bs3-navbar:responsive   |
| Navbar Static-Top     | bs3-navbar:static-top   |
#### Breadcrumbs 面包屑导航
| Component   | Snippet code    |
| ----------- | --------------- |
| Breadcrumbs | bs3-breadcrumbs |
#### 导航元素 nav
导航 `nav-tabs`
胶囊式 `nav-pills`
###### 标签页
```html
<ul class="nav nav-tabs"></ul>
```
##### 胶囊式的导航菜单
###### 基本的胶囊式导航菜单 `nav-pills`
```html
.nav-pills类
<ul class="nav nav-pills">
  <li class="active"><a href="#">Home</a></li>
  <li><a href="#">SVN</a></li>
  <li><a href="#">iOS</a></li>
</ul>
```
###### 垂直的胶囊式导航菜单 	`nav-stacked`
```html
nav .nav-stacked  
<ul class="nav nav-pills nav-stacked">
  <li class="active"><a href="#">Home</a></li>
  <li><a href="#">SVN</a></li>
  <li><a href="#">iOS</a></li>
</ul>
胶囊是标签页也是可以垂直方向堆叠排列的。只需添加 .nav-stacked 类。
```
###### 两端对齐的导航	`nav-justified`
```html
.nav-justified
<ul class="nav nav-tabs nav-justified">
  <li class="active"><a href="#">Home</a></li>
  <li><a href="#">SVN</a></li>
  <li><a href="#">iOS</a></li>
</ul>
```
###### 禁用的链接 `class="disabled"`
```html
对任何导航组件（标签页、胶囊式标签页），都可以添加 .disabled 类，从而实现链接为灰色且没有鼠标悬停效果。
.disabled 
<li role="presentation" class="disabled"><a href="#">Disabled link</a></li>
```
###### 下拉菜单
导航菜单与下拉菜单使用相似的语法。默认情况下，列表项的锚与一些数据属性协同合作来触发带有 **.dropdown-menu** class 的无序列表。
###### 带有下拉菜单的标签
向标签添加下拉菜单的步骤如下：
- 以一个带有 class **.nav** 的无序列表开始。
- 添加 class **.nav-tabs**。
- 添加带有 **.dropdown-menu** class 的无序列表。
```html
带下拉菜单的标签页
dropdown-menu
<ul class="dropdown-menu"></ul>
<p>带有下拉菜单的标签</p>
  <ul class="nav nav-tabs">
    <li class="active"><a href="#">Home</a></li>
    <li><a href="#">SVN</a></li>
    <li><a href="#">iOS</a></li>
    <li><a href="#">VB.Net</a></li>
    <li class="dropdown">
      <a class="dropdown-toggle" data-toggle="dropdown" href="#">
        Java <span class="caret"></span>
      </a>
      <ul class="dropdown-menu">
        <li><a href="#">Swing</a></li>
        <li><a href="#">jMeter</a></li>
        <li><a href="#">EJB</a></li>
        <li class="divider"></li>
        <li><a href="#">分离的链接</a></li>
      </ul>
    </li>
    <li><a href="#">PHP</a></li>
  </ul>
```
###### 带下拉菜单的胶囊式标签页
把 **.nav-tabs** class 改为 **.nav-pills**
```html
<p>带有下拉菜单的胶囊</p>
  <ul class="nav nav-pills">
    <li class="active"><a href="#">Home</a></li>
    <li><a href="#">SVN</a></li>
    <li><a href="#">iOS</a></li>
    <li><a href="#">VB.Net</a></li>
    <li class="dropdown">
      <a class="dropdown-toggle" data-toggle="dropdown" href="#">
        Java <span class="caret"></span>
      </a>
      <ul class="dropdown-menu">
        <li><a href="#">Swing</a></li>
        <li><a href="#">jMeter</a></li>
        <li><a href="#">EJB</a></li>
        <li class="divider"></li>
        <li><a href="#">分离的链接</a></li>
      </ul>
    </li>
    <li><a href="#">PHP</a></li>
  </ul>
```
#### 导航条 bs3-navbar
导航条是在您的应用或网站中作为导航页头的响应式基础组件。它们在移动设备上可以折叠（并且可开可关），且在视（viewport）宽度增加时逐渐变为水平展开模式。
##### 默认样式的导航条
```html
navbar navbar-default	
<nav class="navbar navbar-default" role="navigation">
    <div class="container-fluid">
    <div class="navbar-header">
        <a class="navbar-brand" href="#">菜鸟教程</a>
    </div>
    <div>
        <ul class="nav navbar-nav">
            <li class="active"><a href="#">iOS</a></li>
            <li><a href="#">SVN</a></li>
            <li class="dropdown">
                <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                    Java
                    <b class="caret"></b>
                </a>
                <ul class="dropdown-menu">
                    <li><a href="#">jmeter</a></li>
                    <li><a href="#">EJB</a></li>
                    <li><a href="#">Jasper Report</a></li>
                    <li class="divider"></li>
                    <li><a href="#">分离的链接</a></li>
                    <li class="divider"></li>
                    <li><a href="#">另一个分离的链接</a></li>
                </ul>
            </li>
        </ul>
    </div>
    </div>
</nav>
```
##### 组件对齐方式
 class **.navbar-left** 或 **.navbar-right** 向左或向右对齐导航栏中的 *导航链接、表单、按钮或文本* 这些组件。这两个 class 都会在指定的方向上添加 CSS 浮动。下面的实例演示了这点：
##### 品牌图标
```html
<a class="navbar-brand" href="#">
		<img alt="Brand" src="...">
</a>
```
##### 表单 navbar:form
将表单放置于 .navbar-form 之内可以呈现很好的垂直对齐，并在较窄的视口（viewport）中呈现折叠状态。 使用对齐选项可以规定其在导航条上出现的位置。
##### 按钮 
.navbar-btn
```html
<nav class="navbar navbar-default" role="navigation">
    <div class="container-fluid">
    <div class="navbar-header">
        <a class="navbar-brand" href="#">菜鸟教程</a>
    </div>
    <div>
        <form class="navbar-form navbar-left" role="search">
            <div class="form-group">
                <input type="text" class="form-control" placeholder="Search">
            </div>
            <button type="submit" class="btn btn-default">提交按钮</button>
        </form>
        <button type="button" class="btn btn-default navbar-btn">
            导航栏按钮
        </button>
    </div>
    </div>
</nav>
```
##### 文本 	
.navbar-text
```html
<p class="navbar-text">Signed in as Mark Otto</p>
<nav class="navbar navbar-default" role="navigation">
    <div class="container-fluid">
    <div class="navbar-header">
        <a class="navbar-brand" href="#">菜鸟教程</a>
    </div>
    <div>
        <p class="navbar-text">Runoob 用户登录</p>
    </div>
    </div>
</nav>
```
##### 非导航的链接
或许你希望在标准的导航组件之外添加标准链接，那么，使用 .navbar-link 类可以让链接有正确的默认颜色和反色设置。
##### 组件排列
```html
<nav class="navbar navbar-default navbar-fixed/static-bottom/top navbar-inverse" role="navigation"></nav>
```
###### 固定在顶部
​		.navbar-fixed-top
###### 固定在底部
​		.navbar-fixed-bottom
###### 静止在顶部
​		.navbar-static-top
###### 反色的导航条
​		通过添加 .navbar-inverse 类可以改变导航条的外观	
#### 路径导航	breadcrumb面包屑
表示当前页面在导航层次结构内的位置。
```html
<ol class="breadcrumb">
  <li><a href="#">Home</a></li>
  <li><a href="#">Library</a></li>
  <li class="active">Data</li>
</ol>
```
在一个带有层次的导航结构中标明当前页面的位置	
#### 标签 label
```html
<h3>Example heading <span class="label label-default">New</span></h3>
用下面的任何一个类即可改变标签的外观
//	label default /primary /success /iinfo /warning/danger
<span class="label label-warning">Warning</span>
<span class="label label-danger">Danger</span>
<span class="label label-default">Default</span>		
```
### 分页 pagination
----
#### Pagination
| Component        | Snippet code      |
| ---------------- | ----------------- |
| Pager            | bs3-pager         |
| Aligned Pager    | bs3-pager:aligned |
| Pagination       | bs3-pagination    |
| Pagination:small | bs3-pagination:sm |
| Pagination:large | bs3-pagination:lg |
#### 分页
```html
<nav aria-label="Page navigation">
    <ul class="pagination"></ull>
</nav>
```
```html
			nav aria-label="Page navigation"
			速打
				pagination
	禁用和激活状态
		.disabled
		.active
```
#### 尺寸
> .pagination-lg
> .paginaiton
> .pagination-sm
#### 翻页
默认实例
		.pager
对齐链接
		你还可以把链接向两端对齐：
		.previous
			向左
		.next
			向右
可选的禁用状态
		.disabled 类也可用于翻页中的链接。
### 标签 label、徽章 badge
----
#### Badges
| Component       | Snippet code |
| --------------- | ------------ |
| Badge (Default) | bs3-badge    |
#### 徽章 badge
给链接、导航等元素嵌套`` <span class="badge"> `元素，可以很醒目的展示新的或未读的信息条目。
### 巨幕jumbotorn、页头page-header、缩略图 thumbnail
#### Jumbotron
| Trigger                  | Description       |
| ------------------------ | ----------------- |
| b4-**jumbotron-default** | Jumbotron default |
| b4-**jumbotron-fluid**   | Jumbotron fluid   |
#### 巨幕 jumbotron
> jumbotron-fuild 和 jumbotron
这是一个轻量、灵活的组件，它能延伸至整个浏览器视口来展示网站上的关键内容。
如果需要让巨幕组件的宽度与浏览器宽度一致并且没有圆角，请把此组件放在所有 .container 元素的外面，并在组件内部添加一个 .container 元素。
#### 页头 page-header
页头组件能够为 h1 标签增加适当的空间，并且与页面的其他部分形成一定的分隔。它支持 h1 标签内内嵌 small 元素的默认效果，还支持大部分其他组件（需要增加一些额外的样式）。
#### 缩略图 	thumbnail
通过缩略图组件扩展 Bootstrap 的 栅格系统，可以很容易地展示栅格样式的图像、视频、文本等内容。
如果你想实现一个类似 Pinterest 的页面效果（不同高度和/宽度的缩略图顺序排列）的话，你需要使用一个第三方插件，比如 Masonry、Isotope 或 Salvattore。
默认样式的实例
自定义内容
添加一点点额外的标签，就可以把任何类型的 HTML 内容，例如标题、段落或按钮，加入缩略图组件内。
### 进度条 progress
---
通过这些简单、灵活的进度条，为当前工作流程或动作提供实时反馈。
#### 基本实例
​		.progress
```
 <span class="sr-only">60% Complete</span>
```
#### 带有提示标签的进度条
		<div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%;">
	60%
  </div>
​		将设置了 .sr-only 类的 <span> 标签从进度条组件中移除 类，从而让当前进度显示出来。
​		60%
#### 根据情境变化效果
​		progress-bar progress-bar-success
​		progress-bar progress-bar-info
​		progress-bar progress-bar-warning
​		progress-bar progress-bar-danger
#### 条纹效果
​		 progress-bar-striped
#### 动画效果
​		 .progress-bar-striped 添加 .active 类，使其呈现出由右向左运动的动画效果。IE9 及更低版本的浏览器不支持。
​		rogress-bar progress-bar-striped active
​		.active
#### 堆叠效果
​		把多个进度条放入同一个 .progress 中，使它们呈现堆叠的效果。
### 媒体对象
---
#### Media Objects
| Component    | Snippet code     |
| ------------ | ---------------- |
| Media Object | bs3-media-object |
媒体对象
	这是一个抽象的样式，用以构建不同类型的组件，这些组件都具有在文本内容的左或右侧对齐的图片（就像博客评论或 Twitter 消息等）
	默认样式
		默认样式的媒体对象组件允许在一个内容块的左边或右边展示一个多媒体内容（图像、视频、音频）。
		.media
		对齐
			图片或其他媒体类型可以顶部、中部或底部对齐。默认是顶部对齐。
			.media-middle
	媒体对象列表
		media-list
### 面版
---
#### Panels
| Component            | Snippet code                                    |
| -------------------- | ----------------------------------------------- |
| Panel                | bs3-panel                                       |
| Panel (contextual)   | bs3-panel:{warning,success,info,danger,primary} |
| Panel (with heading) | bs3-panel:heading                               |
| Panel (with footer)  | bs3-panel:footer                                |
默认的 .panel 组件所做的只是设置基本的边框（border）和内补（padding）来包含内容。
		.panpel .panpel-default
#### 带标题的面板
```html
.panel-heading 
```
#### 带脚注的面板
```html
.panel-footer
```
#### 情景效果
```
.panel panel-prinmary
panel:prinmary
.panel panel-sucess
.panel panel-info
.panel panel-warning
.panel panel-danger
```
#### 带表格的面板
​			panel:table
#### 带列表组的面板
​		list-group
​			速打
​				panel:table +list-group
### Wells
Well 是一种会引起内容凹陷显示或插图效果的容器 ，把 Well 用在元素上，就能有嵌入（inset）的简单效果。
```html
<div class="well">...</div>
<div class="well well-lg/sm">...</div>
```
尺寸大小
**well-lg** 或 **well-sm** 来改变 Well 的尺寸大小
## <font color="red">四、插件 </font>
`自带12种jQuery插件三个框+过渡效果+折叠+滚动监听+下拉菜单+标签页+提示工具+按钮+附加导航+轮播`
### 插件概述
- Bootstrap 自带 12 种 jQuery 插件，扩展了功能，可以给站点添加更多的互动。
- 使用时要先引入jQuery和bootstrap的js文件
#### data属性
- 你可以仅仅通过`` data 属性 API 就能使用所有的 Bootstrap 插件，无需写一行 JavaScript 代码。这是 Bootstrap 中的一等 API，也应该是你的首选方式。``
- 话又说回来，在某些情况下可能需要将此功能关闭。因此，我们还提供了``关闭 data 属性 API `的方法，即解除以
  为命名空间并绑定在文档上的事件。就像下面这样：
  ```js
  $(document).off('.data-api')
  //只是关闭bootstrap的data属性的AP，让其每没有JS插件没有功能
  ```
- 如需``关闭一个特定的插件``，只需要在 data-api 命名空间前加上该插件的名称作为命名空间即可，如下所示：
  ```js
  $(document).off('.alert.data-api')
  ```
#### 编程方式的API
我们为所有 Bootstrap 插件提供了纯 JavaScript 方式的 API。所有公开的 API 都是支持单独或链式调用方式，并且返回其所操作的元素集合（注：	`和jQuery的调用形式一致`）。例如：
```
$(".btn.danger").button("toggle").addClass("fat")
```
#### 避免命名空间冲突
发生命名空间冲突，可以通过调用插件的 **.noConflict** 方法恢复其原始值。
```js
// 返回 $.fn.button 之前所赋的值
var bootstrapButton = $.fn.button.noConflict() 
// 为 $().bootstrapBtn 赋予 Bootstrap 功能                           
$.fn.bootstrapBtn = bootstrapButton     
```
#### 自定义事件`动词不定式(事件开始时被触发) + 过去分词形式（动作执行完毕之后被触发）`
Bootstrap 为大多数插件的独特行为提供了自定义事件。一般来说，这些事件有两种形式：
**动词不定式**:这会在``事件开始时被触发``。例如 `ex: show`。动词不定式事件提供了 preventDefault 功能。这使得在事件开始前可以停止操作的执行。
```js
$('#myModal').on('show.bs.modal', function (e) {
// 阻止模态框的显示
  if (!data) return e.preventDefault() 
})
```
**过去分词形式**：这会在``动作执行完毕之后被触发``。例如 *``ex: shown`*。
### 一、过渡效果
####  使用案例
- 具有幻灯片或淡入效果的模态对话框。具体实例参见 [Bootstrap 模态框（Modal）插件](https://www.runoob.com/bootstrap/bootstrap-modal-plugin.html)。
- 具有淡出效果的标签页。具体实例参见 [Bootstrap 标签页（Tab）插件](https://www.runoob.com/bootstrap/bootstrap-tab-plugin.html)。
- 具有淡出效果的警告框。 具体实例参见 [Bootstrap 警告框（Alert）插件](https://www.runoob.com/bootstrap/bootstrap-alert-plugin.html)。
- 具有幻灯片效果的轮播板。具体实例参见 [Bootstrap 轮播（Carousel）插件](https://www.runoob.com/bootstrap/bootstrap-carousel-plugin.html)。
### 二、滚动监听
滚动监听（Scrollspy）插件，即自动更新导航插件，会根据滚动条的位置自动更新对应的导航目标。其基本的实现是随着您的滚动，基于滚动条的位置向导航栏添加 **.active** class。
#### 用法
您可以向顶部导航添加滚动监听行为：
- 通过 data 属性：向您想要监听的元素（通常是 body）添加data-spy="scroll"。然后添加带有 Bootstrap.nav组件的父元素的 ID 或 class 的属性data-target。为了它能正常工作，您必须确保页面主体中有匹配您所要监听链接的 ID 的元素存在。
  ```
  <body data-spy="scroll" data-target=".navbar-example">
  ...
  <div class="navbar-example">
      <ul class="nav nav-tabs">
          ...
      </ul>
  </div>
  ...
  </body>
  ```
- 通过 JavaScript：您可以通过 JavaScript 调用滚动监听，选取要监听的元素，然后调用.scrollspy()函数：
  ```
  $('body').scrollspy({ target: '.navbar-example' })
  ```
#### 快速生成
#### 选项
通过 data 属性或 JavaScript 来传递。下表列出了这些选项：
| 选项名称 | 类型/默认值         | Data 属性名称 | 描述                                   |
| :------- | :------------------ | :------------ | :------------------------------------- |
| offset   | number *默认值：10* | data-offset   | 当计算滚动位置时，距离顶部的偏移像素。 |
#### 方法
**.scrollspy('refresh')**：当通过 JavaScript 调用 scrollspy 方法时，您需要调用 **.refresh** 方法来更新 DOM。这在 DOM 的任意元素发生变更（即，您添加或移除了某些元素）时非常有用。下面是使用该方法的语法。
```
$('[data-spy="scroll"]').each(function () {
  var $spy = $(this).scrollspy('refresh')
})
```
#### 事件
下表列出了滚动监听中要用到事件。这些事件可在函数中当钩子使用。
| 事件                  | 描述                                         | 实例                                                         |
| :-------------------- | :------------------------------------------- | :----------------------------------------------------------- |
| activate.bs.scrollspy | 每当一个新项目被滚动监听激活时，触发该事件。 | `$('#myScrollspy').on('activate.bs.scrollspy', function () {  // 执行一些动作... })` |
### 三、标签页
#### Tabs
| Component | Snippet code |
| --------- | ------------ |
| Tabs pane | bs3-tabs     |
#### 用法
**通过 data 属性**：您需要添加 **data-toggle="tab"** 或 **data-toggle="pill"** 到锚文本链接中。
添加 **nav** 和 **nav-tabs** 类到 **ul** 中，将会应用 Bootstrap [标签样式](https://www.runoob.com/bootstrap/bootstrap-navigation-elements.html)，添加 **nav** 和 **nav-pills** 类到 **ul** 中，将会应用 Bootstrap [胶囊式样式](https://www.runoob.com/bootstrap/bootstrap-navigation-elements.html)
```html
<ul class="nav nav-tabs">
    <li><a href="#identifier" data-toggle="tab">Home</a></li>
    ...
</ul>
```
**通过 JavaScript**：您可以使用 Javascript 来启用标签页，如下所示：
```js
$('#myTab a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
```
#### 淡入淡出效果
如果需要为标签页设置淡入淡出效果，请添加 **.fade** 到每个 **.tab-pane** 后面。第一个标签页必须添加 **.in** 类，以便淡入显示初始内容
#### 方法
**.$().tab**：该方法可以激活标签页元素和内容容器。标签页需要用一个 **data-target** 或者一个指向 DOM 中容器节点的 **href**。
```
<ul class="nav nav-tabs" id="myTab">
    <li class="active"><a href="#identifier" data-toggle="tab">Home</a></li>
    .....
</ul>
<div class="tab-content">
    <div class="tab-pane active" id="home">...</div>
    .....
</div>
<script>
    $(function () {
        $('#myTab a:last').tab('show')
    })
</script>
```
#### 事件
下表列出了标签页（Tab）插件中要用到的事件。这些事件可在函数中当钩子使用。
| 事件         | 描述                                                         | 实例                                                         |
| :----------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| show.bs.tab  | 该事件在标签页显示时触发，但是必须在新标签页被显示之前。分别使用 **event.target** 和 **event.relatedTarget** 来定位到激活的标签页和前一个激活的标签页。 | `$('a[data-toggle="tab"]').on('show.bs.tab', function (e) {  e.target // 激活的标签页  e.relatedTarget // 前一个激活的标签页 })` |
| shown.bs.tab | 该事件在标签页显示时触发，但是必须在某个标签页已经显示之后。分别使用 **event.target** 和 **event.relatedTarget** 来定位到激活的标签页和前一个激活的标签页。 | `$('a[data-toggle="tab"]').on('shown.bs.tab', function (e) {  e.target // 激活的标签页  e.relatedTarget // 前一个激活的标签页 })` |
### 四、提示工具（Tooltip）`链接或者按钮的提示`
---
`当您想要描述一个链接的时候，提示工具（Tooltip）就显得非常有用。`提示工具（Tooltip）插件做了很多改进，例如不需要依赖图像，而是改用 CSS 实现动画效果，用 data 属性存储标题信息。
#### 快速用法
> ```html
> <a href="#" data-toggle="tooltip" title="Example tooltip">请悬停在我的上面</a>
> ```
>
> button 速打
>
> b4-tooltip-default // tooltip
>
> data-toggle="tooltip"
>
> data-placement 方向
>
> //它不是纯 CSS 插件。如需使用该插件，您必须使用 jquery 激活它
>
> $(function () { $("[data-toggle='tooltip']").tooltip(); });
```html
<h4>提示工具（Tooltip）插件 - 锚</h4>
这是一个 <a href="#" class="tooltip-test" data-toggle="tooltip"
        title="默认的 Tooltip">
    默认的 Tooltip
</a>.
这是一个 <a href="#" class="tooltip-test" data-toggle="tooltip"
        data-placement="left" title="左侧的 Tooltip">
    左侧的 Tooltip
    //data-placement = top bottom left right
</a>.
<h4>提示工具（Tooltip）插件 - 按钮</h4>
<button type="button" class="btn btn-default" data-toggle="tooltip"
        title="默认的 Tooltip">
    默认的 Tooltip
</button>
<button type="button" class="btn btn-default" data-toggle="tooltip"
        data-placement="left" title="左侧的 Tooltip">
    左侧的 Tooltip
</button>
	 //data-placement = top bottom left right
<script>
    $(function () { $("[data-toggle='tooltip']").tooltip(); });
</script>
```
#### 用法
提示工具（Tooltip）插件根据需求生成内容和标记，默认情况下是把提示工具（tooltip）放在它们的触发元素后面。您可以有以下两种方式添加提示工具（tooltip）：
- 通过 data 属性：如需添加一个提示工具（tooltip），只需向一个锚标签添加==data-toggle="tooltip"==即可。锚的 title 即为提示工具（tooltip）的文本。默认情况下，插件把提示工具（tooltip）设置在顶部。
  ```html
  <a href="#" data-toggle="tooltip" title="Example tooltip">请悬停在我的上面</a>
  ```
- ==通过 JavaScript：通过 JavaScript 触发提示工具（tooltip）==：
  ```js
  $('#identifier').tooltip(options)
  ```
#### 选项`data-`
有一些选项是通过 Bootstrap 数据 API（Bootstrap Data API）添加或通过 JavaScript 调用的。下表列出了这些选项：
| 选项名称  | 类型/默认值                     | Data 属性名称  | 描述                                                         |
| :-------- | :------------------------------ | :------------- | :----------------------------------------------------------- |
| animation | boolean *默认值：true*          | data-animation | 提示工具使用 CSS 渐变滤镜效果。                              |
| html      | boolean *默认值：false*         | data-html      | 向提示工具插入 HTML。如果为 false，jQuery 的 text 方法将被用于向 dom 插入内容。如果您担心 XSS 攻击，请使用 text。 |
| placement | string\|function *默认值：top*  | data-placement | `规定如何定位提示工具`（即 top\|bottom\|left\|right\|auto）。 当指定为 *auto* 时，会动态调整提示工具。例如，如果 placement 是 "auto left"，提示工具将会尽可能显示在左边，在情况不允许的情况下它才会显示在右边。 |
| selector  | string *默认值：false*          | data-selector  | 如果提供了一个选择器，提示工具对象将被委派到指定的目标。     |
| title     | string \| function *默认值：''* | data-title     | 如果未指定 *title* 属性，则 title 选项是默认的 title 值。    |
| trigger   | string *默认值：'hover focus'*  | data-trigger   | 定义如何触发提示工具： **click\| hover \| focus \| manual**。您可以传递多个触发器，每个触发器之间用空格分隔。 |
| delay     | number \| object *默认值：0*    | data-delay     | 延迟显示和隐藏提示工具的毫秒数 - 对 manual 手动触发类型不适用。如果提供的是一个数字，那么延迟将会应用于显示和隐藏。如果提供的是对象，结构如下所示：`delay: { show: 500, hide: 100 }` |
| container | string \| false *默认值：false* | data-container | 向指定元素追加提示工具。 实例： container: 'body'            |
#### 方法 `$('#identifier').tooltip(options)`
下面是一些提示工具（Tooltip）插件中有用的方法：
| 方法                             | 描述                          | 实例                               |
| :------------------------------- | :---------------------------- | :--------------------------------- |
| **Options:** .tooltip(options)   | 向元素集合附加提示工具句柄。  | `$().tooltip(options)`             |
| **Toggle:** .tooltip('toggle')   | 切换显示/隐藏元素的提示工具。 | `$('#element').tooltip('toggle')`  |
| **Show:** .tooltip('show')       | 显示元素的提示工具。          | `$('#element').tooltip('show')`    |
| **Hide:** .tooltip('hide')       | 隐藏元素的提示工具。          | `$('#element').tooltip('hide')`    |
| **Destroy:** .tooltip('destroy') | 隐藏并销毁元素的提示工具。    | `$('#element').tooltip('destroy')` |
#### 事件 `show/n//hide/n.bs.tooltip `
下表列出了提示工具（Tooltip）插件中要用到的事件。这些事件可在函数中当钩子使用。
| 事件              | 描述                                                         | 实例                                                         |
| :---------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| show.bs.tooltip   | 当调用 show 实例方法时``立即触发``该事件。                   | `$('#myTooltip').on('show.bs.tooltip', function () {  // 执行一些动作... })` |
| shown.bs.tooltip  | `当提示工具对用户可见时触发该事件`（将等待 CSS 过渡效果完成）。 | `$('#myTooltip').on('shown.bs.tooltip', function () {  // 执行一些动作... })` |
| hide.bs.tooltip   | 当调用 hide 实例方法时立即触发该事件。                       | `$('#myTooltip').on('hide.bs.tooltip', function () {  // 执行一些动作... })` |
| hidden.bs.tooltip | 当提示工具对用户隐藏时触发该事件（将等待 CSS 过渡效果完成）。 | `$('#myTooltip').on('hidden.bs.tooltip', function () {  // 执行一些动作... })` |
### 五、六、七、三个框
#### 	五、模态框(modal)
##### 快速生成
> bs3-modal
```html
<!-- 按钮触发模态框 -->
<a class="btn btn-primary" data-toggle="modal" href='#modal-id'>Trigger modal</a>
<!-- 模态框（Modal） -->
<div class="modal fade" id="modal-id">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <button type="button" class="close" data-dismiss="modal" aria-hidden="true">&times;</button>
                <h4 class="modal-title">Modal title</h4>
            </div>
            <div class="modal-body">
                在这里添加一些文本
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
                <button type="button" class="btn btn-primary">Save changes</button>
            </div>
        </div>
    </div>
</div>
```
模态框（Modal）是覆盖在父窗体上的子窗体。通常，目的是显示来自一个单独的源的内容，可以在不离开父窗体的情况下有一些互动。子窗体可提供信息、交互等。
##### 用法
**代码讲解：**
- 使用模态窗口，您需要有某种触发器。您可以使用按钮或链接。这里我们使用的是按钮。
- 如果您仔细查看上面的代码，您会发现在 <button> 标签中，**data-target="#myModal"** 是您想要在页面上加载的模态框的目标。您可以在页面上创建多个模态框，然后为每个模态框创建不同的触发器。现在，很明显，您不能在同一时间加载多个模块，但您可以在页面上创建多个在不同时间进行加载。
- 在模态框中需要注意两点：
  1. 第一是 **.modal**，用来把 <div> 的内容识别为模态框。
  2. 第二是 **.fade** class。当模态框被切换时，它会引起内容淡入淡出。
- **aria-labelledby="myModalLabel"**，该属性引用模态框的标题。
- 属性 **aria-hidden="true"** 用于保持模态窗口不可见，直到触发器被触发为止（比如点击在相关的按钮上）。
- <div class="modal-header">，modal-header 是为模态窗口的头部定义样式的类。
- **class="close"**，close 是一个 CSS class，用于为模态窗口的关闭按钮设置样式。
- **data-dismiss="modal"**，是一个自定义的 HTML5 data 属性。在这里它被用于关闭模态窗口。
- **class="modal-body"**，是 Bootstrap CSS 的一个 CSS class，用于为模态窗口的主体设置样式。
- **class="modal-footer"**，是 Bootstrap CSS 的一个 CSS class，用于为模态窗口的底部设置样式。
- **data-toggle="modal"**，HTML5 自定义的 data 属性 data-toggle 用于打开模态窗口。
##### 选项
有一些选项可以用来定制模态窗口（Modal Window）的外观和感观，它们是通过 data 属性或 JavaScript 来传递的。下表列出了这些选项：
| 选项名称 | 类型/默认值                               | Data 属性名称 | 描述                                                         |
| :------- | :---------------------------------------- | :------------ | :----------------------------------------------------------- |
| backdrop | boolean 或 string 'static' *默认值：true* | data-backdrop | 指定一个静态的背景，当用户点击模态框外部时不会关闭模态框。   |
| keyboard | boolean *默认值：true*                    | data-keyboard | 当按下 escape 键时关闭模态框，设置为 false 时则按键无效。    |
| show     | boolean *默认值：true*                    | data-show     | 当初始化时显示模态框。                                       |
| remote   | path *默认值：false*                      | data-remote   | 使用 jQuery *.load* 方法，为模态框的主体注入内容。如果添加了一个带有有效 URL 的 href，则会加载其中的内容。如下面的实例所示：`[请点击我](remote.html)` |
##### 方法
下面是一些可与 modal() 一起使用的有用的方法。
| 方法                         | 描述                                           | 实例                                          |
| :--------------------------- | :--------------------------------------------- | :-------------------------------------------- |
| **Options:** .modal(options) | 把内容作为模态框激活。接受一个可选的选项对象。 | `$('#identifier').modal({ keyboard: false })` |
| **Toggle:** .modal('toggle') | 手动切换模态框。                               | `$('#identifier').modal('toggle')`            |
| **Show:** .modal('show')     | 手动打开模态框。                               | `$('#identifier').modal('show')`              |
| **Hide:** .modal('hide')     | 手动隐藏模态框。                               | `$('#identifier').modal('hide')`              |
##### 事件
下表列出了模态框中要用到事件。这些事件可在函数中当钩子使用。
| 事件            | 描述                                                  | 实例                                                         |
| :-------------- | :---------------------------------------------------- | :----------------------------------------------------------- |
| show.bs.modal   | 在调用 show 方法后触发。                              | `$('#identifier').on('show.bs.modal', function () {  // 执行一些动作... })` |
| shown.bs.modal  | 当模态框对用户可见时触发（将等待 CSS 过渡效果完成）。 | `$('#identifier').on('shown.bs.modal', function () {  // 执行一些动作... })` |
| hide.bs.modal   | 当调用 hide 实例方法时触发。                          | `$('#identifier').on('hide.bs.modal', function () {  // 执行一些动作... })` |
| hidden.bs.modal | 当模态框完全对用户隐藏时触发。                        | `$('#identifier').on('hidden.bs.modal', function () {  // 执行一些动作... })` |
#### 	六、弹出框(Popover)
弹出框（Popover）与工具提示（Tooltip）类似，提供了一个扩展的视图。如需激活弹出框，用户只需把鼠标悬停在元素上即可。弹出框的内容完全可使用 Bootstrap 数据 API（Bootstrap Data API）来填充。该方法依赖于工具提示（tooltip）。
##### 快速生成
> popover `data-toggle="popover" data-placement="left"`
>
> ```html
>  <button type="button" class="btn btn-secondary" data-toggle="popover" title="Popup title" data-content="Popup content">Trigger</button>
> ```
>
> data-toggle="popver"
>
> data-container 内容
>
> ```js
>   $(function () {
>             $("[data-toggle='popover']").popover()
>         })
> ```
```html
<div class="container" style="padding: 100px 50px 10px;" >
    <button type="button" class="btn btn-default" title="Popover title"
            data-container="body" data-toggle="popover" data-placement="left"
            data-content="左侧的 Popover 中的一些内容">
        左侧的 Popover
    </button>
</div>
<script>
$(function (){
    $("[data-toggle='popover']").popover();
});
</script>
</div>
```
##### 用法
弹出框（Popover）插件根据需求生成内容和标记，默认情况下是把弹出框（popover）放在它们的触发元素后面。您可以有以下两种方式添加弹出框（popover）：
- 通过 data 属性：如需添加一个弹出框（popover），只需向一个锚/按钮标签添加data-toggle="popover"
  即可。锚的 title 即为弹出框（popover）的文本。默认情况下，插件把弹出框（popover）设置在顶部。
  ```html
  <a href="#" data-toggle="popover" title="Example popover">
      请悬停在我的上面
  </a>
  ```
- 通过 JavaScript：通过 JavaScript 启用弹出框（popover）：
  ```
  $('#identifier').popover(options)
  ```
  弹出框（Popover）插件不像之前所讨论的下拉菜单及其他插件那样，它不是纯 CSS 插件。如需使用该插件，您必须使用 jquery 激活它（读取 javascript）。使用下面的脚本来启用页面中的所有的弹出框（popover）：
```js
$(function () { $("[data-toggle='popover']").popover(); });
```
##### 选项
有一些选项是通过 Bootstrap 数据 API（Bootstrap Data API）添加或通过 JavaScript 调用的。下表列出了这些选项：
| 选项名称  | 类型/默认值                     | Data 属性名称  | 描述                                                         |
| :-------- | :------------------------------ | :------------- | :----------------------------------------------------------- |
| animation | boolean *默认值：true*          | data-animation | 向弹出框应用 CSS 褪色过渡效果。                              |
| html      | boolean *默认值：false*         | data-html      | 向弹出框插入 HTML。如果为 false，jQuery 的 text 方法将被用于向 dom 插入内容。如果您担心 XSS 攻击，请使用 text。 |
| placement | string\|function *默认值：top*  | data-placement | 规定如何定位弹出框（即 top\|bottom\|left\|right\|auto）。 当指定为 *auto* 时，会动态调整弹出框。例如，如果 placement 是 "auto left"，弹出框将会尽可能显示在左边，在情况不允许的情况下它才会显示在右边。 |
| selector  | string *默认值：false*          | data-selector  | 如果提供了一个选择器，弹出框对象将被委派到指定的目标。       |
| title     | string \| function *默认值：''* | data-title     | 如果未指定 *title* 属性，则 title 选项是默认的 title 值。    |
| trigger   | string *默认值：'hover focus'*  | data-trigger   | 定义如何触发弹出框： **click\| hover \| focus \| manual**。您可以传递多个触发器，每个触发器之间用空格分隔。 |
| delay     | number \| object *默认值：0*    | data-delay     | 延迟显示和隐藏弹出框的毫秒数 - 对 manual 手动触发类型不适用。如果提供的是一个数字，那么延迟将会应用于显示和隐藏。如果提供的是对象，结构如下所示：`delay: { show: 500, hide: 100 }` |
| container | string \| false *默认值：false* | data-container | 向指定元素追加弹出框。 实例： container: 'body'              |
##### 方法
下面是一些弹出框（Popover）插件中有用的方法：
| 方法                             | 描述                        | 实例                               |
| :------------------------------- | :-------------------------- | :--------------------------------- |
| **Options:** .popover(options)   | 向元素集合附加弹出框句柄。  | `$().popover(options)`             |
| **Toggle:** .popover('toggle')   | 切换显示/隐藏元素的弹出框。 | `$('#element').popover('toggle')`  |
| **Show:** .popover('show')       | 显示元素的弹出框。          | `$('#element').popover('show')`    |
| **Hide:** .popover('hide')       | 隐藏元素的弹出框。          | `$('#element').popover('hide')`    |
| **Destroy:** .popover('destroy') | 隐藏并销毁元素的弹出框。    | `$('#element').popover('destroy')` |
##### 事件
下表列出了弹出框（Popover）插件中要用到的事件。这些事件可在函数中当钩子使用。
| 事件              | 描述                                                         | 实例                                                         |
| :---------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| show.bs.popover   | 当调用 show 实例方法时立即触发该事件。                       | `$('#mypopover').on('show.bs.popover', function () {  // 执行一些动作... })` |
| shown.bs.popover  | 当弹出框对用户可见时触发该事件（将等待 CSS 过渡效果完成）。  | `$('#mypopover').on('shown.bs.popover', function () {  // 执行一些动作... })` |
| hide.bs.popover   | 当调用 hide 实例方法时立即触发该事件。                       | `$('#mypopover').on('hide.bs.popover', function () {  // 执行一些动作... })` |
| hidden.bs.popover | 当工具提示对用户隐藏时触发该事件（将等待 CSS 过渡效果完成）。 | `$('#mypopover').on('hidden.bs.popover', function () {  // 执行一些动作... })` |
#### 七、警告框(Alert)
##### Alerts
| Component           | Snippet code      |
| ------------------- | ----------------- |
| Alert Box (Default) | bs3-alert         |
| Danger Alert Box    | bs3-alert:danger  |
| Info Alert Box      | bs3-alert:info    |
| Success Alert Box   | bs3-alert:success |
| Warning Alert Box   | bs3-alert:warning |
警告框
	实例
		.alert alert-success
	可关闭的警告框
		.alert-dismissible类和一个关闭按钮
		<button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
		 <button> 元素添加 data-dismiss="alert"
	警告框中的链接
		.alert-link
		用 .alert-link 工具类，可以为链接设置与当前警告框相符的颜色
		.alert-sucess
		.alert-info
		.alert-warning
		.alert-danger
		  <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span
警告框（Alert）消息大多是用来向终端用户显示诸如警告或确认消息的信息。使用警告框（Alert）插件，您可以向所有的警告框消息添加可取消（dismiss）功能。
##### 快速生成
> bs3-alert  
>
> 设置按钮为btn-sucess
##### 用法
您可以有以下两种方式启用警告框的可取消（dismissal）功能：
- 通过 data 属性：通过数据 API（Data API）添加可取消功能，只需要向关闭按钮添加data-dismiss="alert"，就会自动为警告框添加关闭功能。
  ```
  <a class="close" data-dismiss="alert" href="#" aria-hidden="true">
      &times;
  </a>
  ```
- 通过 JavaScript：通过 JavaScript 添加可取消功能：
  ```
  $(".alert").alert()
  ```
##### 方法
下面是一些警告框（Alert）插件中有用的方法：
| 方法                         | 描述                                 | 实例                               |
| :--------------------------- | :----------------------------------- | :--------------------------------- |
| .alert()                     | 该方法让所有的警告框都带有关闭功能。 | `$('#identifier').alert();`        |
| **关闭方法** .alert('close') | 关闭所有的警告框。                   | `$('#identifier').alert('close');` |
##### 事件
下表列出了警告框（Alert）插件中要用到的事件。这些事件可在函数中当钩子使用。
| 事件            | 描述                                                    | 实例                                                         |
| :-------------- | :------------------------------------------------------ | :----------------------------------------------------------- |
| close.bs.alert  | 当调用 *close* 实例方法时立即触发该事件。               | `$('#myalert').bind('close.bs.alert', function () {  // 执行一些动作... })` |
| closed.bs.alert | 当警告框被关闭时触发该事件（将等待 CSS 过渡效果完成）。 | `$('#myalert').bind('closed.bs.alert', function () {   // 执行一些动作... })` |
### 八、九、表单
#### 八、下拉菜单
##### 快速生成
##### 用法
您可以切换下拉菜单（Dropdown）插件的隐藏内容：
使用下拉菜单（Dropdown）插件，您可以向任何组件（比如导航栏、标签页、胶囊式导航菜单、按钮等）添加下拉菜单。
- 通过 data 属性：向链接或按钮添加``data-toggle="dropdown"``来切换下拉菜单，如下所示：
  ```html
  <div class="dropdown">
    <a data-toggle="dropdown" href="#">下拉菜单（Dropdown）触发器</a>
    <ul class="dropdown-menu" role="menu" aria-labelledby="dLabel">
      ...
    </ul>
  </div>
  ```
  如果您需要保持链接完整（在浏览器不启用 JavaScript 时有用），请使用 **data-target** 属性代替 **href="#"**：
  ```html
  <div class="dropdown">
    <a id="dLabel" role="button" data-toggle="dropdown" data-target="#" href="/page.html">
      下拉菜单（Dropdown） <span class="caret"></span>
    </a>
    <ul class="dropdown-menu" role="menu" aria-labelledby="dLabel">
      ...
    </ul>
  </div>
  ```
- 通过 JavaScript：通过 JavaScript 调用下拉菜单切换，请使用下面的方法：
  ```js
  $('.dropdown-toggle').dropdown()
  ```
##### 方法
下拉菜单切换有一个简单的方法用来显示或隐藏下拉菜单。
```js
$().dropdown('toggle')
```
#### 九、 按钮
快速生成
>bs3-button
##### 加载状态
向 button 元素添加 **data-loading-text="Loading..."** 
##### 单个切换
向 button 元素添加 **data-toggle="button"** 作为其属性即可
##### 复选框(checkbox)
向 **btn-group** 添加 data 属性 **data-toggle="buttons"** 来添加复选框组的切换。
##### 单选按钮(radio)
向 **btn-group** 添加 data 属性 **data-toggle="buttons"** 来添加单选按钮组的切换
```html
<button id="fat-btn" class="btn btn-primary" data-loading-text="Loading..." 
    type="button"> 加载状态
</button>
<script>
    $(function() {
        $(".btn").click(function(){
            $(this).button('loading').delay(1000).queue(function() {
            // $(this).button('reset');
            // $(this).dequeue(); 
            });
        });
    });  
</script>
<button type="button" class="btn btn-primary" 
    data-toggle="button"> 单个切换
</button>
<div class="btn-group" data-toggle="buttons">
    <label class="btn btn-primary">
        <input type="checkbox"> 选项 1
    </label>
    <label class="btn btn-primary">
        <input type="checkbox"> 选项 2
    </label>
    <label class="btn btn-primary">
        <input type="checkbox"> 选项 3
    </label>
</div>
<div class="btn-group" data-toggle="buttons">
    <label class="btn btn-primary">
        <input type="radio" name="options" id="option1"> 选项 1
    </label>
    <label class="btn btn-primary">
        <input type="radio" name="options" id="option2"> 选项 2
    </label>
    <label class="btn btn-primary">
        <input type="radio" name="options" id="option3"> 选项 3
    </label>
</div>
```
##### 用法
您可以 **通过 JavaScript** 启用按钮（Button）插件，如下所示：
```js
$('.btn').button()
```
##### 方法
下面是一些按钮（Button）插件中有用的方法：
| 方法               | 描述                                                         | 实例                    |
| :----------------- | :----------------------------------------------------------- | :---------------------- |
| button('toggle')   | 切换按压状态。赋予按钮被激活的外观。您可以使用 **data-toggle** 属性启用按钮的自动切换。 | `$().button('toggle')`  |
| .button('loading') | 当加载时，按钮是禁用的，且文本变为 button 元素的 **data-loading-text** 属性的值。 | `$().button('loading')` |
| .button('reset')   | 重置按钮状态，文本内容恢复为最初的内容。当您想要把按钮返回为原始的状态时，该方法非常有用。 | `$().button('reset')`   |
| .button(string)    | 该方法中的字符串是指由用户声明的任何字符串。使用该方法，重置按钮状态，并添加新的内容。 | `$().button(string)`    |
```html
<h2>点击每个按钮查看方法效果</h2>
<h4>演示 .button('toggle') 方法</h4>
<div id="myButtons1" class="bs-example">
    <button type="button" class="btn btn-primary">原始</button>
</div>
<h4>演示 .button('loading') 方法</h4>
<div id="myButtons2" class="bs-example">
    <button type="button" class="btn btn-primary" 
        data-loading-text="Loading...">原始
    </button>
</div>
<h4>演示 .button('reset') 方法</h4>
<div id="myButtons3" class="bs-example">
    <button type="button" class="btn btn-primary" 
        data-loading-text="Loading...">原始
    </button>
</div>
<h4>演示 .button(string) 方法</h4>
<button type="button" class="btn btn-primary" id="myButton4" 
    data-complete-text="Loading finished">请点击我
</button>
<script>
$(function () {
        $("#myButtons1 .btn").click(function(){
            $(this).button('toggle');
        });
    });
    $(function() { 
        $("#myButtons2 .btn").click(function(){
            $(this).button('loading').delay(1000).queue(function() {
            });        
        });
    });   
    $(function() { 
        $("#myButtons3 .btn").click(function(){
            $(this).button('loading').delay(1000).queue(function() {
                $(this).button('reset');
            });        
        });
    });  
   $(function() { 
        $("#myButton4").click(function(){
            $(this).button('loading').delay(1000).queue(function() {
                $(this).button('complete');
            });        
        });
    });
</script>
```
### 十、Collapse 折叠
#### 快速生成
```html
<div class="panel-group" id="accordion">
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">
                <a data-toggle="collapse" data-parent="#accordion" 
                href="#collapseOne">
                点击我进行展开，再次点击我进行折叠。第 1 部分
                </a>
            </h4>
        </div>
        <div id="collapseOne" class="panel-collapse collapse in">
            <div class="panel-body">
                Nihil anim keffiyeh helvetica, craft beer labore wes anderson 
                cred nesciunt sapiente ea proident. Ad vegan excepteur butcher 
                vice lomo.
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">
                <a data-toggle="collapse" data-parent="#accordion" 
                href="#collapseTwo">
                点击我进行展开，再次点击我进行折叠。第 2 部分
            </a>
            </h4>
        </div>
        <div id="collapseTwo" class="panel-collapse collapse">
        <div class="panel-body">
            Nihil anim keffiyeh helvetica, craft beer labore wes anderson 
            cred nesciunt sapiente ea proident. Ad vegan excepteur butcher 
            vice lomo.
        </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">
                <a data-toggle="collapse" data-parent="#accordion" 
                href="#collapseThree">
                点击我进行展开，再次点击我进行折叠。第 3 部分
                </a>
            </h4>
        </div>
        <div id="collapseThree" class="panel-collapse collapse">
            <div class="panel-body">
                Nihil anim keffiyeh helvetica, craft beer labore wes anderson 
                cred nesciunt sapiente ea proident. Ad vegan excepteur butcher 
                vice lomo.
            </div>
        </div>
    </div>
</div>
```
#### 选项
#### 方法
#### 事件
### 十 一、Carousel  轮播
#### Carousel
| Component | Snippet code |
| --------- | ------------ |
| Carousel  | bs3-carousel |
```html
<div id="myCarousel" class="carousel slide">
    <!-- 轮播（Carousel）指标 -->
    <ol class="carousel-indicators">
        <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
        <li data-target="#myCarousel" data-slide-to="1"></li>
        <li data-target="#myCarousel" data-slide-to="2"></li>
    </ol>   
    <!-- 轮播（Carousel）项目 -->
    <div class="carousel-inner">
        <div class="item active">
            <img src="/wp-content/uploads/2014/07/slide1.png" alt="First slide">
        </div>
        <div class="item">
            <img src="/wp-content/uploads/2014/07/slide2.png" alt="Second slide">
        </div>
        <div class="item">
            <img src="/wp-content/uploads/2014/07/slide3.png" alt="Third slide">
        </div>
    </div>
    <!-- 轮播（Carousel）导航 -->
    <a class="carousel-control left" href="#myCarousel" 
       data-slide="prev"> <span _ngcontent-c3="" aria-hidden="true" class="glyphicon glyphicon-chevron-right"></span></a>
    <a class="carousel-control right" href="#myCarousel" 
       data-slide="next">&rsaquo;</a>
</div>
=========================================================================================================
<div id="carousel-id" class="carousel slide" data-ride="carousel">
      <!-- 轮播（Carousel）指标 -->
    <ol class="carousel-indicators">
        <li data-target="#carousel-id" data-slide-to="0" class=""></li>
        <li data-target="#carousel-id" data-slide-to="1" class=""></li>
        <li data-target="#carousel-id" data-slide-to="2" class="active"></li>
    </ol>
      <!-- 轮播（Carousel）项目 -->
    <div class="carousel-inner">
        <div class="item">
            <img data-src="holder.js/900x500/auto/#777:#7a7a7a/text:First slide" alt="First slide"
                src="image/1.jpg">
            <div class="container">
                <div class="carousel-caption">
                    <h1>Example headline.</h1>
                    <p>Note: If you're viewing this page via a <code>file://</code> URL, the "next" and
                        "previous"
                        Glyphicon buttons on the left and right might not load/display properly due toweb
                        browser
                        security rules.</p>
                    <p><a class="btn btn-lg btn-primary" href="#" role="button">Sign up today</a></p>
                </div>
            </div>
        </div>
        <div class="item">
            <img data-src="holder.js/900x500/auto/#666:#6a6a6a/text:Second slide" alt="Second slide"
                src="image/2.jpg">
            <div class="container">
                <div class="carousel-caption">
                    <h1>Another example headline.</h1>
                    <p>Cras justo odio, dapibus ac facilisis in, egestas eget quam. Donec id elit non mi
                        porta
                        gravida at eget metus. Nullam id dolor id nibh ultricies vehicula ut id elit.</p>
                    <p><a class="btn btn-lg btn-primary" href="#" role="button">Learn more</a></p>
                </div>
            </div>
        </div>
        <div class="item active">
            <img data-src="holder.js/900x500/auto/#555:#5a5a5a/text:Third slide" alt="Third slide"
                src="image/3.jpg">
            <div class="container">
                <div class="carousel-caption">
                    <h1>One more for good measure.</h1>
                    <p>Cras justo odio, dapibus ac facilisis in, egestas eget quam. Donec id elit non mi
                        porta
                        gravida at eget metus. Nullam id dolor id nibh ultricies vehicula ut id elit.</p>
                    <p><a class="btn btn-lg btn-primary" href="#" role="button">Browse gallery</a></p>
                </div>
            </div>
        </div>
    </div>
     <!-- 轮播（Carousel）导航 -->
    <a class="left carousel-control" href="#carousel-id" data-slide="prev"><span
            class="glyphicon glyphicon-chevron-left"></span></a>
    <a class="right carousel-control" href="#carousel-id" data-slide="next"><span
            class="glyphicon glyphicon-chevron-right"></span></a>
</div>
```
#### 用法
- 通过 data 属性：使用 data 属性可以很容易控制轮播（Carousel）的位置。
  - 属性 **data-slide** 接受关键字 *prev* 或 *next*，用来改变幻灯片相对于当前位置的位置。
  - 使用 **data-slide-to** 来向轮播传递一个原始滑动索引，**data-slide-to="2"** 将把滑块移动到一个特定的索引，索引从 0 开始计数。
  - **data-ride="carousel"** 属性用于标记轮播在页面加载时就开始动画播放。
- 通过 JavaScript：轮播（Carousel）可通过 JavaScript 手动调用，如下所示：
  ```html
  $('.carousel').carousel()
  ```
#### 选项
有一些选项是通过 data 属性或 JavaScript 来传递的。下表列出了这些选项： `interval pause wrap`
| 选项名称 | 类型/默认值              | Data 属性名称 | 描述                                                         |
| :------- | :----------------------- | :------------ | :----------------------------------------------------------- |
| interval | number *默认值：5000*    | data-interval | 自动循环每个项目之间延迟的时间量。如果为 false，轮播将不会自动循环。 |
| pause    | string *默认值："hover"* | data-pause    | 鼠标进入时暂停轮播循环，鼠标离开时恢复轮播循环。             |
| wrap     | boolean *默认值：true*   | data-wrap     | 轮播是否连续循环。                                           |
#### 方法
下面是一些轮播（Carousel）插件中有用的方法： `carousel(options/cycle/pause(停止)/number/prev/next)`
| 方法               | 描述                                                  | 实例                                              |
| :----------------- | :---------------------------------------------------- | :------------------------------------------------ |
| .carousel(options) | 初始化轮播为可选的 options 对象，并开始循环项目。     | `$('#identifier').carousel({   interval: 2000 })` |
| .carousel('cycle') | 从左到右循环轮播项目。                                | `$('#identifier').carousel('cycle')`              |
| .carousel('pause') | 停止轮播循环项目。                                    | `$('#identifier').carousel('pause')`              |
| .carousel(number)  | 循环轮播到某个特定的帧（从 0 开始计数，与数组类似）。 | `$('#identifier').carousel(number)`               |
| .carousel('prev')  | 循环轮播到上一个项目。                                | `$('#identifier').carousel('prev')`               |
| .carousel('next')  | 循环轮播到下一个项目。                                | `$('#identifier').carousel('next')`               |
```html
<script>
$(function(){
        // 初始化轮播
        $(".start-slide").click(function(){
            $("#myCarousel").carousel('cycle');
        });
        // 停止轮播
        $(".pause-slide").click(function(){
            $("#myCarousel").carousel('pause');
        });
        // 循环轮播到上一个项目
        $(".prev-slide").click(function(){
            $("#myCarousel").carousel('prev');
        });
        // 循环轮播到下一个项目
        $(".next-slide").click(function(){
            $("#myCarousel").carousel('next');
        });
        // 循环轮播到某个特定的帧 
        $(".slide-one").click(function(){
            $("#myCarousel").carousel(0);
        });
        $(".slide-two").click(function(){
            $("#myCarousel").carousel(1);
        });
        $(".slide-three").click(function(){
            $("#myCarousel").carousel(2);
        });
    });
</script>
```
#### 事件
下表列出了轮播（Carousel）插件中要用到的事件。这些事件可在函数中当钩子使用。`slide\slid.bs.carousel`
| 事件              | 描述                                    | 实例                                                         |
| :---------------- | :-------------------------------------- | :----------------------------------------------------------- |
| slide.bs.carousel | 当调用 slide 实例方法时立即触发该事件。 | `$('#identifier').on('slide.bs.carousel', function () {   // 执行一些动作... })` |
| slid.bs.carousel  | 当轮播完成幻灯片过渡效果时触发该事件。  | `$('#identifier').on('slid.bs.carousel', function () {   // 执行一些动作... })` |
```js
$(function(){
	$("#myCarousel").on("slide.bs.carousel",function(){
		console.log("当调用slide实例方法时立即触发该事件。")
	})
});
```
### 十二、Affix 附加导航`侧边栏导航`
附加导航（Affix）插件允许指定 <div> 固定在页面的某个位置。一个常见的例子是社交图标。它们将在某个位置开始，但当页面点击某个标记，该 <div> 会锁定在某个位置，不会随着页面其他部分一起滚动。
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Bootstrap 附加导航（Affix）插件</title>
<link rel="stylesheet" href="http://cdn.static.runoob.com/libs/bootstrap/3.3.7/css/bootstrap.min.css">
<script src="http://cdn.static.runoob.com/libs/jquery/2.1.1/jquery.min.js"></script>
<script src="http://cdn.static.runoob.com/libs/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<style>
/* Custom Styles */
    ul.nav-tabs{
        width: 140px;
        margin-top: 20px;
        border-radius: 4px;
        border: 1px solid #ddd;
        box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
    }
    ul.nav-tabs li{
        margin: 0;
        border-top: 1px solid #ddd;
    }
    ul.nav-tabs li:first-child{
        border-top: none;
    }
    ul.nav-tabs li a{
        margin: 0;
        padding: 8px 16px;
        border-radius: 0;
    }
    ul.nav-tabs li.active a, ul.nav-tabs li.active a:hover{
        color: #fff;
        background: #0088cc;
        border: 1px solid #0088cc;
    }
    ul.nav-tabs li:first-child a{
        border-radius: 4px 4px 0 0;
    }
    ul.nav-tabs li:last-child a{
        border-radius: 0 0 4px 4px;
    }
    ul.nav-tabs.affix{
        top: 30px; /* Set the top position of pinned element */
    }
</style>
</head>
<body data-spy="scroll" data-target="#myScrollspy">
<div class="container">
   <div class="jumbotron">
        <h1>Bootstrap Affix</h1>
    </div>
    <div class="row">
        <div class="col-xs-3" id="myScrollspy">
            <ul class="nav nav-tabs nav-stacked" data-spy="affix" data-offset-top="125">
                <li class="active"><a href="#section-1">第一部分</a></li>
                <li><a href="#section-2">第二部分</a></li>
                <li><a href="#section-3">第三部分</a></li>
                <li><a href="#section-4">第四部分</a></li>
                <li><a href="#section-5">第五部分</a></li>
            </ul>
        </div>
        <div class="col-xs-9">
            <h2 id="section-1">第一部分</h2>
            <p>Lo</p>
            <hr>
            <h2 id="section-2">第二部分</h2>
            <p>Nullam </p>
            <p>Ves augue.</p>
            <hr>
            <h2 id="section-3">第三部分</h2>
            <p>Integ b</p>
            <p>P</p>
            <p>Qui+ potenti.</p>
            <hr>
            <h2 id="section-4">第四部分</h2>
            <p>Suspbero.</p>
            <p>Vestibulum quis quam ut magna consequat faucibus. Pellentesque eget nisi a mi suscipit tincidunt. Ut drerit tellus.</p>
            <p>Phs facilisis id.</p>
            <p>Ut utultricies pellentesque. Fusce eu suscipit massa.</p>
            <hr>
            <h2 id="section-5">第五部分</h2>
            <p>Nam ege.</p>
            <p>Subero.</p>
            <p>Morbi sedm leo.</p>
            <p>Sed vitae logiat sit amet.</p>
        </div>
    </div>
</div>
</body>
</html>
```



# Bootstrap4 `基础、样式、组件、插件`

## 零、 bootstrap3与bootstrap4的区别

- Bootstrap4 是 Bootstrap3 的最新版本，与 Bootstrap3 相比拥有了更多的具体的类以及把一些有关的部分变成了相关的组件。同时 Bootstrap.min.css 的体积减少了40%以上。
- Bootstrap4 `放弃了对 IE8 以及 iOS 6 的支持，现在仅仅支持 IE9 以上 以及 iOS 7 以上版本的浏览器`。如果对于其中需要用到以前的浏览器，那么请使用bootstrap3。

## 一、基础

### 安装使用

#### CDN

```js
<!-- 新 Bootstrap4 核心 CSS 文件 -->
<link rel="stylesheet" href="https://cdn.staticfile.org/twitter-bootstrap/4.3.1/css/bootstrap.min.css">
<!-- jQuery文件。务必在bootstrap.min.js 之前引入 -->
<script src="https://cdn.staticfile.org/jquery/3.2.1/jquery.min.js"></script>
<!-- bootstrap.bundle.min.js 用于弹窗、提示、下拉菜单，包含了 popper.min.js -->
<script src="https://cdn.staticfile.org/popper.js/1.15.0/umd/popper.min.js"></script>
<!-- 最新的 Bootstrap4 核心 JavaScript 文件 -->
<script src="https://cdn.staticfile.org/twitter-bootstrap/4.3.1/js/bootstrap.min.js"></script>
```

#### 本地

[Download · Bootstrap](https://getbootstrap.com/docs/4.4/getting-started/download/)

#### 快速生成模板

> b4-$

#### 移动设备优先

```html
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
//width=device-width 表示宽度是设备屏幕的宽度。
//initial-scale=1 表示初始的缩放比例。
//shrink-to-fit=no 自动适应手机屏幕的宽度。
```

#### 容器类

- ``.container` 类用于固定宽度并支持响应式布局的容器。 (固定宽度) 
- ``.container-fluid `类用于 100% 宽度，占据全部视口（viewport）的容器。(全屏宽度) 

### 网格系统

Bootstrap 提供了一套响应式、移动设备优先的流式网格系统，随着屏幕或视口（viewport）尺寸的增加，系统会自动分为最多 12 列
Bootstrap 3 和 Bootstrap 4 最大的区别在于 Bootstrap 4 现在使用 flexbox（弹性盒子） 而不是浮动。 Flexbox 的一大优势是，没有指定宽度的网格列将自动设置为**等宽与等高列** 。
`sm[576] - md(smd)[768] -lg[992] - xl(lgxl)[1200x]`

| 类名     | 设备                                        |
| -------- | ------------------------------------------- |
| .col-    | 针对所有设备                                |
| .col-sm- | 平板 - 屏幕宽度等于或大于 576px             |
| .col-md- | 桌面显示器 - 屏幕宽``度等于或大于 768px)    |
| .col-lg- | 大桌面显示器 - 屏幕宽度等于或大于 992px)    |
| .col-xl- | 超大桌面显示器 - 屏幕宽度等于或大于 1200px) |

<table class="reference">
  <thead>
    <tr>
      <th></th>
      <th class="text-center">
        超小设备<br>
        <small>&lt;576px</small>
      </th>
      <th class="text-center">
        平板<br>
        <small>≥576px</small>
      </th>
      <th class="text-center">
        桌面显示器<br>
        <small>≥768px</small>
      </th>
      <th class="text-center">
        大桌面显示器<br>
        <small>≥992px</small>
      </th>
      <th class="text-center">
        超大桌面显示器<br>
        <small>≥1200px</small>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th class="text-nowrap" scope="row">容器最大宽度</th>
      <td>None (auto)</td>
      <td>540px</td>
      <td>720px</td>
      <td>960px</td>
      <td>1140px</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">类前缀</th>
      <td><code>.col-</code></td>
      <td><code>.col-sm-</code></td>
      <td><code>.col-md-</code></td>
      <td><code>.col-lg-</code></td>
      <td><code>.col-xl-</code></td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">列数量和</th>
      <td colspan="5">12</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">间隙宽度</th>
      <td colspan="5">30px
（一个列的每边分别 15px）</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">可嵌套</th>
      <td colspan="5">Yes</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">列排序</th>
      <td colspan="5">Yes</td>
    </tr>
  </tbody>
</table>

创建相等宽度的列，Bootstrap 自动布局

```html
<div class="row">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
</div>
```

```html
// 每行分12列 sm md lg xl
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-3 col-md-6 col-lg-4 col-xl-2">
      <p></p>
    </div>
    <div class="col-sm-9 col-md-6 col-lg-8 col-xl-10">
      <p></p>
    </div>
  </div>
</div>
```

#### 偏移列

偏移列通过 `offset-*- `类来设置。第一个星号( * )可以是 **sm、md、lg、xl**，表示屏幕设备类型，第二个星号( * )可以是 **1** 到 **11** 的数字。`offset-md-4`

```html
<div class="row">
  <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
  <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
</div>
```

## 二、样式

### 文字排版 font

默认值

- **font-size** 为 16px, **line-height** 为 1.5
- **font-family** 为 "Helvetica Neue", Helvetica, Arial, sans-serif
- `<p> `元素 margin-top: 0 、 margin-bottom: 1rem (16px)
- h1 到 h6
	- h1 2.5 rem = 40px
	- h2 2rem = 32px
	- h3 1.75rem = 28px
	- h4 1.5rem = 24px
	- h5 1.5rem = 24px
	- h6 1rem = 16px、
	- `.display-=*` 6.5rem  5.5rem 4.5rem 3.5rem

| 类名                                                         | 作用                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `<h1> - <h6>`                                                | HTML 标题（h1 到 h6）的样式                                  |
| 标题类<br />.display-1, .display-2, .display-3, .display-4   | 四个 Display 类来控制标题的样式                              |
| `<small>`                                                    | 副标题，创建字号更小的颜色更浅的文本:                        |
| `<mark>`                                                     | 高亮、黄色背景及有一定的内边距                               |
| `<abbr>`                                                     | 缩略图、元素的样式为显示在文本底部的一条虚线边框             |
| ` <blockquote>上添加 .blockquote 类`                         | 引用                                                         |
| `<code>、<kbd>、<pre>`                                       | 代码、键盘输入、代码块                                       |
|                                                              |                                                              |
| `.font-weight-bold、.font-weight-normal、.font-weight-light.font-italic` | 加粗文本、普通文本、更细的文本、斜体文本                     |
|                                                              |                                                              |
| .text-left、.text-center、.text-right、.text-justify         | text-justify设定文本对齐,段落中超出屏幕部分文字自动换行      |
|                                                              |                                                              |
| .text-lowercase、.text-uppercase、.text-capitalize           | 小写、大写、首字母大写                                       |
|                                                              |                                                              |
| .initialism                                                  | 显示在`` <abbr> `元素中的文本以小号字体展示，且可以将小写字母转换为大写字母 |
| .list-unstyled                                               | 移除默认的列表样式，列表项中左对齐 ( <ul> 和 <ol> 中)。 这个类仅适用于直接子列表项 (如果需要移除嵌套的列表项，你需要在嵌套的列表中使用该样式) |
| .list-inline、.list-inline-item                              | 将所有列表项放置同一行                                       |
| .pre-scrollable                                              | 使 `<pre>` 元素可滚动，代码块区域最大高度为340px,一旦超出这个高度,就会在Y轴出现滚动条 |
| .lead                                                        | 让段落更突出                                                 |
| .text-nowrap                                                 | 段落中超出屏幕部分不换行                                     |

```html
<h1 class="display-1">Display 1</h1>
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

```html
<ul class="list-inline">
    <li class="list-inline-item">Coffee</li>
    <li class="list-inline-item">Tea</li>
    <li class="list-inline-item">Milk</li>
</ul>
```

### 颜色 color

#### 文本颜色类

| 类名              | 作用                             |
| ----------------- | -------------------------------- |
| `.text-muted`     | 柔和的文本                       |
| `.text-white`     | 深灰色文字                       |
|                   |                                  |
| `.text-primary`   | 重要的文本                       |
| `.text-success`   | 执行成功的文本                   |
| `.text-info`      | 代表一些提示信息的文本           |
| `.text-warning`   | 警告文本                         |
| `.text-danger`    | 危险操作文本                     |
| `.text-secondary` | 副标题                           |
| `.text-dark`      | 浅灰色文本（白色背景上看不清楚） |
| `.text-light`     | 白色文本（白色背景上看不清楚）。 |

#### 背景颜色类

| 类名            | 作用     |
| --------------- | -------- |
| `.bg-primary`   | 重要     |
| `.bg-success`   | 执行成功 |
| `.bg-info`      | 信息提示 |
| `.bg-warning`   | 警告背景 |
| `.bg-danger`    | 危险背景 |
| `.bg-secondary` | 副标题   |
| `.bg-dark`      | 深灰背景 |
| `.bg-light`     | 浅灰背景 |

背景颜色不会设置文本的颜色，你需要与 ``.text-``类一起使用。

### 表格 tanle

| 类名                           | 作用                       |
| ------------------------------ | -------------------------- |
| `.table`                       | 基础表格                   |
| `.table-striped`               | 条纹表格                   |
| `.table-border`                | 带边框表格                 |
| `.table-hover`                 | 鼠标悬停状态表格           |
| `.table-dark`                  | 黑色背景表格               |
| `.table-dark`和`table-striped` | 黑色条纹表格               |
| `.table-dark`和`.table-hover`  | 鼠标悬停效果的黑色背景表格 |
| `.thead-dark`和`.thead-light`  | 表头颜色                   |
| `.table-sm`                    | 较小的表格                 |

表格颜色类
指定意义的颜色类：通过指定意义的颜色类可以为表格的行或者单元格设置颜色
可以指定``表格中的所有元素``

- primary、sucess、danger、info、warning
- active、secondary、light、dark

| 类名                 | 描述                             |
| :------------------- | :------------------------------- |
| **.table-primary**   | 蓝色: 指定这是一个重要的操作     |
| **.table-success**   | 绿色: 指定这是一个允许执行的操作 |
| **.table-danger**    | 红色: 指定这是可以危险的操作     |
| **.table-info**      | 浅蓝色: 表示内容已变更           |
| **.table-warning**   | 橘色: 表示需要注意的操作         |
|                      |                                  |
| **.table-active**    | 灰色: 用于鼠标悬停效果           |
| **.table-secondary** | 灰色: 表示内容不怎么重要         |
| **.table-light**     | 浅灰色，可以是表格行的背景       |
| **.table-dark**      | 深灰色，可以是表格行的背景       |

```html
<table class="table table-striped table-bordered table-hover table-dark table-responsive-md">
</table>
```

响应式表格
创建响应式表格：在屏幕宽度小于 992px 时会创建水平滚动条，如果可视区域宽度大于 992px 则显示不同效果（没有滚动条）:
小于设置值、创建水平滚动条（大于设置值，无效）

| 类名                     | 屏幕宽度 |
| :----------------------- | :------- |
| **.table-responsive-sm** | < 576px  |
| **.table-responsive-md** | < 768px  |
| **.table-responsive-lg** | < 992px  |
| **.table-responsive-xl** | < 1200px |

指定屏幕宽度下显示滚动条：``重点使用在table的父级元素上``

```html
<div class="table-responsive-sm">  <table class="table">    ...  </table></div> 
```

表头颜色

```html
<table class="table ">    <thread class="thread-dark">        <tr>            <th></th>        </tr>    </thread></table>
```

### 图像形状 img

| 类名              | 屏幕作用                    |
| ----------------- | --------------------------- |
| `.img-fluid`      | 响应式图片                  |
| `.rounded`        | `圆角图片`                  |
| `.rounded-circle` | `椭圆图片`                  |
| `.img-thumbnail`  | `椭圆图片`(图片有边框)      |
| 图片对齐方式      | `.float-right、.float-left` |

## 三、组件

### 表单 `form`

#### 按钮 `btn`

按钮类可用于`a` 、`button` 、`input`

| 类名                                                         | 作用                             |
| ------------------------------------------------------------ | -------------------------------- |
| `.btn`                                                       |                                  |
| `.btn-primary`、`.btn-secondary`、`.btn-info`、`.btn-warning`、`.btn-danger`、`.btn-dark`、`.btn-light`、`.btn-link` |                                  |
| `btn-outline-primary/info...8个情境色`                       | 按钮设置边框，只有边框和文字颜色 |
| `.btn-lg 大.btn 中.btn-sm 小`                                | 不同大小的按钮                   |
| `.btn-block`                                                 | 块级按钮                         |
| `.active 和 .disabled`                                       | 激活和禁用的按钮                 |

#### 按钮组 `btn-gruop`

| 类名                           | 方法           |
| ------------------------------ | -------------- |
| `.btn-group`                   | 按钮组         |
| `.btn-group-lg（大）|sm（小）` | 设置按钮组大小 |
| `.btn-group-vertical`          | 垂直按钮组     |

```html
<div class="btn-group btn-group-lg btn-group-vertical"> <button type="button" class="btn btn-primary">Apple</button>  <button type="button" class="btn btn-primary">Samsung</button>  <button type="button" class="btn btn-primary">Sony</butto	</div>
```

内嵌按钮组及下拉菜单

```html
<div class="btn-group">  <button type="button" class="btn btn-primary">Apple</button>  <button type="button" class="btn btn-primary">Samsung</button>  <div class="btn-group">    <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">       Sony    </button>    <div class="dropdown-menu">      <a class="dropdown-item" href="#">Tablet</a>      <a class="dropdown-item" href="#">Smartphone</a>    </div>  </div></div>
```

拆分按钮下拉菜单

```html
<div class="btn-group">  <button type="button" class="btn btn-primary">Sony</button>  <button type="button" class="btn btn-primary dropdown-toggle dropdown-toggle-split" data-toggle="dropdown">    <span class="caret"></span>  </button>  <div class="dropdown-menu">    <a class="dropdown-item" href="#">Tablet</a>    <a class="dropdown-item" href="#">Smartphone</a>  </div></div>
```

垂直按钮组及下拉菜单

```html
<div class="btn-group-vertical">  <button type="button" class="btn btn-primary">Apple</button>  <button type="button" class="btn btn-primary">Samsung</button>  <div class="btn-group">    <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">       Sony    </button>    <div class="dropdown-menu">      <a class="dropdown-item" href="#">Tablet</a>      <a class="dropdown-item" href="#">Smartphone</a>    </div>  </div></div>
```

#### 输入框组

#### 表单控件

#### 下拉菜单

| 类名                     | 作用               |
| ------------------------ | ------------------ |
| `.dropdown-divider`      | 水平分割线         |
| `.dropdown-header`       | 标题               |
| `.active`                | 下拉菜单中的可用项 |
| `.disabled`              | 下拉菜单的禁用项   |
| `.dropdown-item`         | 下拉菜单项         |
| `.dropdown-menu`         |                    |
| `.dropdown-menu-right`   | 下拉菜单的定位     |
| 下拉菜单弹出方向设置     |                    |
| 指定向右弹出的下拉菜单   | `dropright`        |
| 指定向上弹出的上拉菜单   | `dropup`           |
| 指定向左边弹出的下拉菜单 | `dropleft`         |

[popper.js ](https://www.shejidaren.com/popper-js.html)
Popper.js 是一个扩展性较好的 tooltips 提示类 JS 插件，不需要依赖 jQuery 库，大小仅为 3.5KB 左右，使用与配置相当简单

```html
  <script src="https://cdn.staticfile.org/popper.js/1.15.0/umd/popper.min.js"></script>
```

> bootstrap 4 下来菜单依赖于 `popper.min.js`

- `.dropdown`
- `.dropdown-toggle ` 和 `data-toggle="dropdown"`
- `.dropdown-menu > .dropdown-item`
	下拉菜单是可切换的，是以列表格式显示链接的上下文菜单

```html
// dropdown > button +  .dropdown-menu > .dropdown-item<div class="dropdown dropright"> //dropup    <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">        Dropdown button    </button>    <div class="dropdown-menu dropdown-menu-right">        <h5 class="dropdown-header">Dropdown header</h5>        <a class="dropdown-item active" href="#">Link 1</a>        <a class="dropdown-item disabled" href="#">Link 2</a>        <div class="dropdown-divider"></div>        <a class="dropdown-item" href="#">Link 3</a>        <h5 class="dropdown-header">Dropdown header</h5>        <a class="dropdown-item" href="#">Another link</a>    </div></div>
```

按钮设置下拉菜单

```html
<div class="btn-group">  <button type="button" class="btn btn-primary">Sony</button>  <button type="button" class="btn btn-primary dropdown-toggle dropdown-toggle-split" data-toggle="dropdown">    <span class="caret"></span>  </button>  <div class="dropdown-menu">    <a class="dropdown-item" href="#">Tablet</a>    <a class="dropdown-item" href="#">Smartphone</a>  </div></div>
```

#### 列表组 `list-group`

| 类名                         | 方法             |
| ---------------------------- | ---------------- |
| `.list-group`                | 列表组           |
| `.list-group-item`           | 列表项           |
| `.active`                    | 激活状态的列表项 |
| `.disabled`                  | 禁用的列表项     |
| `.list-group-item-action`    | 链接列表项       |
| `.list-group-item-8个颜色类` | 多种颜色列表项   |

```html
<ul class="list-group">    <li class="list-group-item active"></li>        <li class="list-group-item disabled"></li>    <li class="list-group-item list-group-item-action"></li>    <li class="list-group-item list-group-item-success"></li></ul>
```

#### 自定义表单

### 导航 `nav navbar`

#### Nav

| Trigger                            | Description                 |
| ---------------------------------- | --------------------------- |
| b4-**nav-a**                       | Nav a                       |
| b4-**nav-complete**                | Nav complete                |
| b4-**nav-tabs-pills-a-variation**  | Nav tabs pills a variation  |
| b4-**nav-tabs-pills-dropdown**     | Nav tabs pills dropdown     |
| b4-**nav-tabs-pills-ul-variation** | Nav tabs pills ul variation |
| b4-**nav-ul**                      | Nav ul                      |

#### Navbar

| Trigger                        | Description             |
| ------------------------------ | ----------------------- |
| b4-**navbar-background-color** | Navbar background color |
| b4-**navbar-background**       | Navbar background       |
| b4-**navbar-default**          | Navbar default          |
| b4-**navbar-minimal-a**        | Navbar minimal a        |
| b4-**navbar-minimal-ul**       | Navbar minimal ul       |
| b4-**navbar-non-responsive**   | Navbar non responsive   |
| b4-**navbar-placement**        | Navbar placement        |

#### 导航

- 基本导航  `b4-nav-ul`
	`<ul class="nav"> <li class="nav-item"> <a class="nav">`
- 导航对齐方式
	**.justify-content-center** 类设置导航居中显示， **.justify-content-end** 类设置导航右对齐。
- 垂直导航
	**.flex-column** 类用于创建垂直导航：
- 选项卡
	使用 **.nav-tabs** 类可以将导航转化为选项卡。然后对于选中的选项使用 .active 类来标记。
- 胶囊导航
	**.nav-pills** 类可以将导航项设置成胶囊形状。
- 导航等宽
	**.nav-justified** 类可以设置导航项齐行等宽显示
- 胶囊下拉菜单
- 选项卡下拉菜单
- 动态选项卡
	如果你要设置选项卡是动态可切换的，可以在每个链接上添加 **data-toggle="tab"** 属性。 然后在每个选项对应的内容的上添加 **.tab-pane** 类。
	如果你希望有淡入效果可以在 **.tab-pane** 后添加 **.fade**类:
- 胶囊状动态选项卡
	胶囊状动态选项卡只需要将以上实例的代码中 data-toggle 属性设置为 **data-toggle="pill"**:

#### 导航栏

##### 垂直导航栏

通过删除 **.navbar-expand-xl|lg|md|sm** 类来创建垂直导航栏:

##### 不同颜色导航栏

可以使用以下类来创建不同颜色导航栏：**.bg-primary**, **.bg-success**, **.bg-info**, **.bg-warning**, **.bg-danger**, **.bg-secondary**, **.bg-dark** 和 **.bg-light**)。

##### 品牌/Logo

**.navbar-brand** 类用于高亮显示品牌/Logo:

##### 导航栏使用下拉菜单

##### 导航栏的表单与按钮

导航栏的表单 **** 元素使用 **class="form-inline"** 类来排版输入框与按钮：

##### 导航栏文本

使用 **.navbar-text** 类来设置导航栏上非链接文本，可以保证水平对齐，颜色与内边距一样。

##### 固定导航栏

导航栏可以固定在头部或者底部。
我们使用 **.fixed-top** 类来实现导航栏的固定：

##### 折叠导航栏

通常，小屏幕上我们都会折叠导航栏，通过点击来显示导航选项。
要创建折叠导航栏，可以在按钮上添加 **class="navbar-toggler", data-toggle="collapse" 与 data-target="#\*thetarget\*"** 类。然后在设置了 **class="collapse navbar-collapse"** 类的 div 上包裹导航内容（链接）, div 元素上的 id 匹配按钮 **data-target** 的上指定的 id:

#### 面包屑导航 Breadcrumb

面包屑导航是一种基于网站层次信息的显示方式。以博客为例，面包屑导航可以显示发布日期、类别或标签。它们表示当前页面在导航层次结构内的位置，是在用户界面中的一种导航辅助。
Bootstrap 中的面包屑导航是一个简单的带有 **.breadcrumb** class 的无序列表。分隔符会通过 CSS（bootstrap.min.css）中的 ::before 和 content 来添加，下面所示的 class 自动被添加：

```html
<ol class="breadcrumb">  <li class="breadcrumb-item active">Home</li></ol><ol class="breadcrumb">  <li class="breadcrumb-item"><a href="#">Home</a></li>  <li class="breadcrumb-item active">Library</li></ol><ol class="breadcrumb">  <li class="breadcrumb-item"><a href="#">Home</a></li>  <li class="breadcrumb-item"><a href="#">Library</a></li>  <li class="breadcrumb-item active">Data</li></ol><nav class="breadcrumb">  <a class="breadcrumb-item" href="#">Home</a>  <a class="breadcrumb-item" href="#">Library</a>  <a class="breadcrumb-item" href="#">Data</a>  <span class="breadcrumb-item active">Bootstrap</span></nav>
```

### 徽章`badge`

徽章（Badges）主要用于突出显示新的或未读的项。

| 类名                                                         | 作用               |
| ------------------------------------------------------------ | ------------------ |
| `.badge`                                                     |                    |
| `.badge-primary、.badge-secondary、.badge-success、.btn-danger、.btn-warning、.btn-info、.btn-light、.btn-dark` | 各种颜色类型的徽章 |
| `.badge-pill`                                                | 药丸形状徽章       |

徽章插入到元素内

```html
<button type="button" class="btn btn-primary">  Messages <span class="badge badge-light">4</span></button>
```

### 进度条 `progress`

进度条可以显示用户任务的完成过程
使用 `progress`> `progress-bar`（进度条标签）

| 类名                     | 作用                                    |
| ------------------------ | --------------------------------------- |
| `bg-颜色类`              | 不同颜色的进度条                        |
| `height`                 | 默认：16px，进度条高度作用于 `progress` |
| `progress-bar`           | 进度条标签                              |
| `.progress-bar-striped`  | 条纹的进度条                            |
| `.progress-bar-animated` | 动画进度条                              |

混合色彩进度条

```html
<div class="progress" style="height:50px">   <div class="progress-bar bg-danger progress-bar-animated progress-bar-striped" style="width: 30%;">       Your Name   </div>  <div class="progress-bar bg-warning" style="width:10%">    Warning  </div>  <div class="progress-bar bg-danger" style="width:20%">    Danger  </div></div>
```

### 分页 pagination

内容过多，一般进行分页处理

| 类名                                | 作用               |
| ----------------------------------- | ------------------ |
| `.pagination`                       | 分页               |
| `.page-item`                        | 分页项             |
| `.page-link`                        | 分页链接           |
| `.active`                           | 当前页码状态       |
| `.disabled`                         | 不可点击的分页链接 |
| `.pagination-lg > pagination > sm`  | 分页显示大小       |
| `.breadcrumb` 和 `.breadcrumb-item` | 面包屑导航         |

```html
<ul class="pagination pagination-lg">  <li class="page-item"><a class="page-link" href="#">Previous</a></li>  <li class="page-item active"><a class="page-link" href="#">1</a></li>  <li class="page-item disabled"><a class="page-link" href="#">2</a></li>  <li class="page-item"><a class="page-link" href="#">3</a></li>  <li class="page-item"><a class="page-link" href="#">Next</a></li></ul>
```

### 折叠 `collapse`

| 类名           | 作用                               |
| -------------- | ---------------------------------- |
| `.collapse`    | 折叠                               |
| `.show`        | 默认显示                           |
| `.data-parent` | 确保所有的折叠元素在指定的父元素下 |

实现内容的显示与隐藏

- `data-toggle="collapse"`、`data-target="#id"`
- `id="demo" class="collapse"`

```html
<button data-toggle="collapse" data-target="#demo">按钮</button><div id="demo" class="collapse">    折叠内容</div>   
```

手风琴

```html
   <div id="accordion">        <div class="card">            <div class="card-header">                <a class="card-link" data-toggle="collapse" href="#collapseOne">                    选项一                </a>            </div>            <div id="collapseOne" class="collapse show" data-parent="#accordion">                <div class="card-body">                   Message1                </div>            </div>        </div>        <div class="card">            <div class="card-header">                <a class="collapsed card-link" data-toggle="collapse" href="#collapseTwo">                    选项二                </a>            </div>            <div id="collapseTwo" class="collapse" data-parent="#accordion">                <div class="card-body">                  Message2                </div>            </div>        </div>    </div>
```

### Jumbotron	(超大屏幕)

Jumbotron（超大屏幕）会创建一个大的灰色背景框，里面可以设置一些特殊的内容和信息。

```html
<div class="jumbotron">       <h1>Title</h1>    <p>Text</p></div>
```

全屏幕的Jumbotron 
创建一个没有圆角的全屏幕，可以在 ``.jumbotron-fluid `类里头的 div添加 **.container** 或 **.container-fluid** 类

```html
<div class="jumbotron jumbotron-fluid">    <div class="container">    	<h1>Title</h1>    	<p>Text</p>							    </div></div>    
```

### 卡片 card

Bootstrap4 的卡片类似 Bootstrap 3 中的面板、图片缩略图、well。

| 类名                                    | 作用                     |
| --------------------------------------- | ------------------------ |
| `.card`                                 |                          |
| `.card-header .card-body  .card-footer` | 头部和底部               |
| `.bg-8种颜色类`                         | 多种颜色卡片             |
| `.card-title、.card-text、.card-link`   | 标题、文本和链接         |
| `.card-img-top`、`.card-img-bottom`     | 图片卡片在文字上方、下方 |
| `.card-img-overlay`                     | 图片要设置为背景         |

```html
<div class="card bg-info text-light">        <div class="card-header">            <h4 class="card-title">Card title</h4>            <p class="card-text">Some example text. Some example text.</p>            <a href="#" class="card-link">Card link</a>        </div>        <div class="card-body">内容        </div>        <div class="card-footer">底部</div>    </div>
```

图片卡片的图片的位置

```html
<div class="card" style="width:400px">  <img class="card-img-top" src="img_avatar1.png" alt="Card image">    // card-img-bottom/top  <div class="card-body">    <h4 class="card-title">John Doe</h4>    <p class="card-text">Some example text.</p>    <a href="#" class="btn btn-primary">See Profile</a>  </div>      <img class="card-img-bottom" src="img_avatar1.png" alt="Card image">    // card-img-bottom/top</div>
```

### 信息提示框 `alert`

| 类名                 | 作用           |
| -------------------- | -------------- |
| `.alert`             | 提示框         |
| `.alert-success`     | 成功           |
| `.alert-info`        | 信息           |
| `.alert-warning`     | 警告           |
| `.alert-danger`      | 危险           |
| `.alert-primary`     | 首选           |
| `.alert-secondary`   | 次要的         |
| `.alert-light`       | 浅灰色         |
| `.alert-dark`        | 深灰色         |
|                      |                |
| `.alert-link`        | 提示框添加链接 |
| `.alert-dismissible` | 关闭提示框     |
| `.fade`和`.show`     | 提示框动画     |

提示框链接：`.alert-link`

```php+HTML
<div class="alert alert-success">  <strong>成功!</strong> 你应该认真阅读 <a href="#" class="alert-link">这条信息</a>。</div>
```

关闭提示框 `.alert-dismissible`

- `.alert-dismissible`
- 关闭按钮的链接添加`class="close"` 和 `data-dismiss="alert"`

```html
<div class="alert alert-success alert-dismissible">  <button type="button" class="close" data-dismiss="alert">&times;</button>  <strong>成功!</strong> 指定操作成功提示信息。</div>
```

提示框动画 `.fade 和 .show`

```html
  <div class="alert alert-light alert-dismissible fade show">    <button type="button" class="close" data-dismiss="alert">&times;</button>    <strong>浅灰色!</strong>浅灰色提示框。  </div>
```

### 多媒体对象

## 四、插件

#### 滚动监听			

#### 小工具			

#### 四个框

##### 信息提示框

##### 模态框

##### 提示框

##### 弹出框

#### 轮播

| 类                            | 描述                                                         |
| :---------------------------- | :----------------------------------------------------------- |
| `.carousel`                   | 创建一个轮播                                                 |
| `.carousel-indicators`        | 为轮播添加一个指示符，就是轮播图底下的一个个小点，轮播的过程可以显示目前是第几张图。 |
| `.carousel-inner`             | 添加要切换的图片                                             |
| `.carousel-item`              | 指定每个图片的内容                                           |
| `.carousel-control-prev`      | 添加左侧的按钮，点击会返回上一张。                           |
| `.carousel-control-next`      | 添加右侧按钮，点击会切换到下一张。                           |
| `.carousel-control-prev-icon` | 与 .carousel-control-prev 一起使用，设置左侧的按钮           |
| `.carousel-control-next-icon` | 与 .carousel-control-next 一起使用，设置右侧的按钮           |
| `.slide`                      | 切换图片的过渡和动画效果，如果你不需要这样的效果，可以删除这个类。 |

# bootstrap速打技巧

[Bootstrap 3 snippets使用文档](https://github.com/JasonMortonNZ/bs3-sublime-plugin/blob/master/README.md)

### Bootstrap 4, Font awesome 4, Font Awesome 5 Free & Pro snippets使用方法

[Bootstrap 4, Font awesome 4, Font Awesome 5 Free & Pro snippets使用方法](https://github.com/1tontech/bootstrap4-snippets/tree/master/vscode)

## bootstrap3

### CDN

| Component                | Snippet code |
| ------------------------ | ------------ |
| CDN link (both CSS & JS) | bs3-cdn      |
| CDN link (CSS only)      | bs3-cdn:css  |
| CDN link (JS only)       | bs3-cdn:js   |

### Local

| Component                     | Snippet code |
| ----------------------------- | ------------ |
| Link to local bootstrap files | bs3-local    |

### Templates

| Component             | Snippet code       |
| --------------------- | ------------------ |
| HTML5 Template Layout | bs3-template:html5 |

### Forms

| Component       | Snippet code        |
| --------------- | ------------------- |
| Form            | bs3-form            |
| Inline Form     | bs3-form:inline     |
| Horizontal Form | bs3-form:horizontal |

### Tables

| Component       | Snippet code        |
| --------------- | ------------------- |
| Table           | bs3-table           |
| Bordered Table  | bs3-table:bordered  |
| Condensed Table | bs3-table:condensed |
| Hover Table     | bs3-table:hover     |
| Striped Table   | bs3-table:striped   |

### Input Fields (Form fields)

**Note:** you can add " :h " to the end of any input field snippet to make it compatible with Bootstrap 3 horizontal forms. **E.g.**

- bs3-input:text:h
- bs3-input:hidden:h

| Component       | Snippet code       | Options |
| --------------- | ------------------ | ------- |
| Label           | bs3-input:label    |         |
| Text Input      | bs3-input:text     | :h      |
| Email Input     | bs3-input:email    | :h      |
| Password Input  | bs3-input:password | :h      |
| Hidden Input    | bs3-input:hidden   | :h      |
| Url Input       | bs3-input:url      | :h      |
| Color Input     | bs3-input:color    | :h      |
| Number Input    | bs3-input:number   | :h      |
| Range Input     | bs3-input:range    | :h      |
| Date Input      | bs3-input:date     | :h      |
| Week Input      | bs3-input:week     | :h      |
| Month Input     | bs3-input:month    | :h      |
| Time Input      | bs3-input:time     | :h      |
| Tel Input       | bs3-input:tel      | :h      |
| Search Input    | bs3-input:search   | :h      |
| Reset Input     | bs3-input:reset    | :h      |
| Submit Input    | bs3-input:submit   | :h      |
| Checkbox Input  | bs3-input:checkbox | :h      |
| Radio Box Input | bs3-input:radio    | :h      |
| Select Box      | bs3-select         | :h      |
| Textarea        | bs3-textarea       | :h      |

### Alerts

| Component           | Snippet code      |
| ------------------- | ----------------- |
| Alert Box (Default) | bs3-alert         |
| Danger Alert Box    | bs3-alert:danger  |
| Info Alert Box      | bs3-alert:info    |
| Success Alert Box   | bs3-alert:success |
| Warning Alert Box   | bs3-alert:warning |

### Badges

| Component       | Snippet code |
| --------------- | ------------ |
| Badge (Default) | bs3-badge    |

### Breadcrumbs

| Component   | Snippet code    |
| ----------- | --------------- |
| Breadcrumbs | bs3-breadcrumbs |

### Carousel

| Component | Snippet code |
| --------- | ------------ |
| Carousel  | bs3-carousel |

### Buttons

**Note:** all button snippets below can have any of the following options append to the end of the snippet *.

- :danger
- :default
- :disabled
- :info
- :primary
- :success
- :warning
	**An example:**
- bs3-button:success
- bs3-large-button:disabled
- bs3-block-button:warning

| Component    | Snippet code     | Options |
| ------------ | ---------------- | ------- |
| Button       | bs3-button       | *       |
| Block Button | bs3-block-button | *       |
| Mini Button  | bs3-xs-button    | *       |
| Small Button | bs3-sm-button    | *       |
| Large Button | bs3-lg-button    | *       |

### Grid

**Note:** The bs3-col snippet can be used both on its own or with the addition of a colon followed by the number of columns required: **E.g.**

- bs3-col
- bs3-col:6
- bs3-col:12

| Component | Snippet code  | Options |
| --------- | ------------- | ------- |
| Column    | bs3-col       | :1-12   |
| Row       | bs3-row       |         |
| Container | bs3-container |         |

### Icons

| Component           | Snippet code       |
| ------------------- | ------------------ |
| Glyphicon           | bs3-icon:glyphicon |
| Icon (Font Awesome) | bs3-icon           |

### Images

| Component              | Snippet code          |
| ---------------------- | --------------------- |
| Thumbnail              | bs3-thumbnail         |
| Thumbnail with content | bs3-thumbnail:content |

### Labels

| Component     | Snippet code      |
| ------------- | ----------------- |
| Label         | bs3-label         |
| Danger Label  | bs3-label:danger  |
| Info Label    | bs3-label:info    |
| Success Label | bs3-label:success |
| Warning Label | bs3-label:warning |

### Pagination

| Component        | Snippet code      |
| ---------------- | ----------------- |
| Pager            | bs3-pager         |
| Aligned Pager    | bs3-pager:aligned |
| Pagination       | bs3-pagination    |
| Pagination:small | bs3-pagination:sm |
| Pagination:large | bs3-pagination:lg |

### Navigation

| Component             | Snippet code            |
| --------------------- | ----------------------- |
| Navbar (basic navbar) | bs3-navbar              |
| Navbar Brand Element  | bs3-navbar:brand        |
| Navbar Button         | bs3-navbar:button       |
| Navbar Form           | bs3-navbar:form         |
| Navbar Link           | bs3-navbar:link         |
| Navbar Text           | bs3-navbar:text         |
| Navbar Fixed-Botton   | bs3-navbar:fixed-bottom |
| Navbar Fixed-Top      | bs3-navbar:fixed-top    |
| Navbar Inverse        | bs3-navbar:inverse      |
| Navbar Responsive     | bs3-navbar:responsive   |
| Navbar Static-Top     | bs3-navbar:static-top   |

### Jumbotron

| Component                | Snippet code  |
| ------------------------ | ------------- |
| Jumbotron (ex Hero Unit) | bs3-jumbotron |

### Panels

| Component            | Snippet code                                    |
| -------------------- | ----------------------------------------------- |
| Panel                | bs3-panel                                       |
| Panel (contextual)   | bs3-panel:{warning,success,info,danger,primary} |
| Panel (with heading) | bs3-panel:heading                               |
| Panel (with footer)  | bs3-panel:footer                                |

### List-groups

| Component                 | Snippet code           |
| ------------------------- | ---------------------- |
| List group                | bs3-list-group         |
| List group (with badges)  | bs3-list-group:badges  |
| List group (linked list)  | bs3-list-group:linked  |
| List group (with content) | bs3-list-group:content |

### Media Objects

| Component    | Snippet code     |
| ------------ | ---------------- |
| Media Object | bs3-media-object |

### Clearfix

| Component | Snippet code |
| --------- | ------------ |
| Clearfix  | bs3-clearfix |

### Wells

| Component    | Snippet code |
| ------------ | ------------ |
| Well         | bs3-well     |
| Well (small) | bs3-well:sm  |
| Well (large) | bs3-well:lg  |

### Tabs

| Component | Snippet code |
| --------- | ------------ |
| Tabs pane | bs3-tabs     |

### Input-groups

| Component                       | Snippet code               |
| ------------------------------- | -------------------------- |
| Input group                     | bs3-input-group            |
| Input group(addon & text-field) | bs3-input-group:addon:text |
| Input group (addon)             | bs3-input-group-addon      |
| Input group (button)            | bs3-input-group-btn        |
| Input group (text-field & btn)  | bs3-input-group:text:btn   |

## Bootstrap 4 snippets

#### Bootstrap master template

| Trigger  | Description               |
| -------- | ------------------------- |
| b4-**$** | Bootstrap master template |

#### Alert

| Trigger                         | Description              |
| ------------------------------- | ------------------------ |
| b4-**alert-additional-content** | Alert additional content |
| b4-**alert-closable**           | Alert closable           |
| b4-**alert-default**            | Alert default            |
| b4-**alert-dismissible**        | Alert dismissible        |
| b4-**alert-link**               | Alert link               |

#### Badge

| Trigger              | Description   |
| -------------------- | ------------- |
| b4-**badge-button**  | Badge button  |
| b4-**badge-default** | Badge default |
| b4-**badge-heading** | Badge heading |
| b4-**badge-link**    | Badge link    |
| b4-**badge-pill**    | Badge pill    |

#### Bgroup

| Trigger                         | Description              |
| ------------------------------- | ------------------------ |
| b4-**bgroup-default**           | Bgroup default           |
| b4-**bgroup-dropdown-vertical** | Bgroup dropdown vertical |
| b4-**bgroup-dropdown**          | Bgroup dropdown          |
| b4-**bgroup-size**              | Bgroup size              |
| b4-**bgroup-toolbar**           | Bgroup toolbar           |

#### Breadcrumb

| Trigger                   | Description        |
| ------------------------- | ------------------ |
| b4-**breadcrumb-default** | Breadcrumb default |
| b4-**breadcrumb-list**    | Breadcrumb list    |

#### Button

| Trigger                  | Description       |
| ------------------------ | ----------------- |
| b4-**button-a**          | Button a          |
| b4-**button-block**      | Button block      |
| b4-**button-checkbox**   | Button checkbox   |
| b4-**button-default**    | Button default    |
| b4-**button-disabled-a** | Button disabled a |
| b4-**button-input**      | Button input      |
| b4-**button-outline**    | Button outline    |
| b4-**button-radio**      | Button radio      |
| b4-**button-sizes**      | Button sizes      |
| b4-**button-toggle**     | Button toggle     |

#### Card

| Trigger                       | Description            |
| ----------------------------- | ---------------------- |
| b4-**card-align**             | Card align             |
| b4-**card-background-custom** | Card background custom |
| b4-**card-background**        | Card background        |
| b4-**card-blockquote**        | Card blockquote        |
| b4-**card-border**            | Card border            |
| b4-**card-columns**           | Card columns           |
| b4-**card-decks**             | Card decks             |
| b4-**card-default**           | Card default           |
| b4-**card-grid**              | Card grid              |
| b4-**card-groups**            | Card groups            |
| b4-**card-head-foot**         | Card head foot         |
| b4-**card-links**             | Card links             |
| b4-**card-list**              | Card list              |
| b4-**card-overlay**           | Card overlay           |
| b4-**card-pill-head**         | Card pill head         |
| b4-**card-subtitle**          | Card subtitle          |
| b4-**card-tab-head**          | Card tab head          |

#### Carousel

| Trigger                 | Description      |
| ----------------------- | ---------------- |
| b4-**carousel-caption** | Carousel caption |
| b4-**carousel-default** | Carousel default |

#### Collapse

| Trigger                   | Description        |
| ------------------------- | ------------------ |
| b4-**collapse-accordion** | Collapse accordion |
| b4-**collapse-button**    | Collapse button    |
| b4-**collapse-default**   | Collapse default   |

#### Dropdown

| Trigger                   | Description        |
| ------------------------- | ------------------ |
| b4-**dropdown-alignment** | Dropdown alignment |
| b4-**dropdown-anchor**    | Dropdown anchor    |
| b4-**dropdown-button**    | Dropdown button    |
| b4-**dropdown-colored**   | Dropdown colored   |
| b4-**dropdown-default**   | Dropdown default   |
| b4-**dropdown-sized**     | Dropdown sized     |
| b4-**dropdown-split**     | Dropdown split     |
| b4-**dropdown-up-split**  | Dropdown up split  |
| b4-**dropdown-up**        | Dropdown up        |

#### Form

| Trigger                          | Description               |
| -------------------------------- | ------------------------- |
| b4-**form-checkbox-custom**      | Form checkbox custom      |
| b4-**form-checkbox-inline**      | Form checkbox inline      |
| b4-**form-checkbox-nolabel**     | Form checkbox nolabel     |
| b4-**form-checkbox**             | Form checkbox             |
| b4-**form-email**                | Form email                |
| b4-**form-file-custom**          | Form file custom          |
| b4-**form-file**                 | Form file                 |
| b4-**form-grid**                 | Form grid                 |
| b4-**form-group-text**           | Form group text           |
| b4-**form-group**                | Form group                |
| b4-**form-help-text-inline**     | Form help text inline     |
| b4-**form-help-text**            | Form help text            |
| b4-**form-hidden**               | Form hidden               |
| b4-**form-inline**               | Form inline               |
| b4-**form-input-sizing**         | Form input sizing         |
| b4-**form-input-text**           | Form input text           |
| b4-**form-input**                | Form input                |
| b4-**form-multi-select-custom**  | Form multi select custom  |
| b4-**form-multi-select**         | Form multi select         |
| b4-**form-multil-select-sizing** | Form multil select sizing |
| b4-**form-password**             | Form password             |
| b4-**form-radio-custom**         | Form radio custom         |
| b4-**form-radio-inline**         | Form radio inline         |
| b4-**form-radio-nolabel**        | Form radio nolabel        |
| b4-**form-radio**                | Form radio                |
| b4-**form-reset**                | Form reset                |
| b4-**form-select-custom**        | Form select custom        |
| b4-**form-select-sizing**        | Form select sizing        |
| b4-**form-select**               | Form select               |
| b4-**form-submit**               | Form submit               |
| b4-**form-textarea**             | Form textarea             |
| b4-**form-validation**           | Form validation           |

#### Igroup

| Trigger                          | Description               |
| -------------------------------- | ------------------------- |
| b4-**igroup-button**             | Igroup button             |
| b4-**igroup-checkbox-radio**     | Igroup checkbox radio     |
| b4-**igroup-dropdown-segmented** | Igroup dropdown segmented |
| b4-**igroup-dropdown**           | Igroup dropdown           |
| b4-**igroup-size**               | Igroup size               |
| b4-**igroup-text-both**          | Igroup text both          |
| b4-**igroup-text-prefix**        | Igroup text prefix        |
| b4-**igroup-text-sufix**         | Igroup text sufix         |

#### Jumbotron

| Trigger                  | Description       |
| ------------------------ | ----------------- |
| b4-**jumbotron-default** | Jumbotron default |
| b4-**jumbotron-fluid**   | Jumbotron fluid   |

#### List

| Trigger             | Description  |
| ------------------- | ------------ |
| b4-**list-a**       | List a       |
| b4-**list-badge**   | List badge   |
| b4-**list-button**  | List button  |
| b4-**list-colors**  | List colors  |
| b4-**list-custom**  | List custom  |
| b4-**list-default** | List default |

#### Modal

| Trigger                | Description     |
| ---------------------- | --------------- |
| b4-**modal-customize** | Modal customize |
| b4-**modal-default**   | Modal default   |
| b4-**modal-grid**      | Modal grid      |
| b4-**modal-sizes**     | Modal sizes     |

#### Nav

| Trigger                            | Description                 |
| ---------------------------------- | --------------------------- |
| b4-**nav-a**                       | Nav a                       |
| b4-**nav-complete**                | Nav complete                |
| b4-**nav-tabs-pills-a-variation**  | Nav tabs pills a variation  |
| b4-**nav-tabs-pills-dropdown**     | Nav tabs pills dropdown     |
| b4-**nav-tabs-pills-ul-variation** | Nav tabs pills ul variation |
| b4-**nav-ul**                      | Nav ul                      |

#### Navbar

| Trigger                        | Description             |
| ------------------------------ | ----------------------- |
| b4-**navbar-background-color** | Navbar background color |
| b4-**navbar-background**       | Navbar background       |
| b4-**navbar-default**          | Navbar default          |
| b4-**navbar-minimal-a**        | Navbar minimal a        |
| b4-**navbar-minimal-ul**       | Navbar minimal ul       |
| b4-**navbar-non-responsive**   | Navbar non responsive   |
| b4-**navbar-placement**        | Navbar placement        |

#### Pagination

| Trigger                     | Description          |
| --------------------------- | -------------------- |
| b4-**pagination-alignment** | Pagination alignment |
| b4-**pagination-default**   | Pagination default   |
| b4-**pagination-sized**     | Pagination sized     |

#### Popover

| Trigger                    | Description         |
| -------------------------- | ------------------- |
| b4-**popover-default**     | Popover default     |
| b4-**popover-direction**   | Popover direction   |
| b4-**popover-dismissable** | Popover dismissable |

#### Progress

| Trigger                 | Description      |
| ----------------------- | ---------------- |
| b4-**progress-colored** | Progress colored |
| b4-**progress-default** | Progress default |
| b4-**progress-ie9**     | Progress ie9     |
| b4-**progress-striped** | Progress striped |

#### Scrollspy

| Trigger                  | Description       |
| ------------------------ | ----------------- |
| b4-**scrollspy-default** | Scrollspy default |

#### Tooltip

| Trigger                | Description     |
| ---------------------- | --------------- |
| b4-**tooltip-default** | Tooltip default |

#### Figure

| Trigger               | Description    |
| --------------------- | -------------- |
| b4-**figure-default** | Figure default |

#### Image

| Trigger              | Description   |
| -------------------- | ------------- |
| b4-**image-default** | Image default |

#### Table

| Trigger              | Description   |
| -------------------- | ------------- |
| b4-**table-default** | Table default |
| b4-**table-special** | Table special |

#### Typography

| Trigger                              | Description                   |
| ------------------------------------ | ----------------------------- |
| b4-**typography-blockquote-reverse** | Typography blockquote reverse |
| b4-**typography-blockquote**         | Typography blockquote         |
| b4-**typography-description-list**   | Typography description list   |
| b4-**typography-display-heading**    | Typography display heading    |
| b4-**typography-lead**               | Typography lead               |
| b4-**typography-list-inline**        | Typography list inline        |
| b4-**typography-list-unstyled**      | Typography list unstyled      |
| b4-**typography-muted-text**         | Typography muted text         |

#### Grid

| Trigger                     | Description          |
| --------------------------- | -------------------- |
| b4-**grid-col**             | Grid col             |
| b4-**grid-container-fluid** | Grid container fluid |
| b4-**grid-container**       | Grid container       |
| b4-**grid-default**         | Grid default         |
| b4-**grid-row**             | Grid row             |

#### Media

| Trigger              | Description   |
| -------------------- | ------------- |
| b4-**media-bottom**  | Media bottom  |
| b4-**media-default** | Media default |
| b4-**media-list**    | Media list    |
| b4-**media-middle**  | Media middle  |
| b4-**media-nesting** | Media nesting |
| b4-**media-right**   | Media right   |
| b4-**media-top**     | Media top     |

#### Responsive

| Trigger                      | Description           |
| ---------------------------- | --------------------- |
| b4-**responsive-hide-down**  | Responsive hide down  |
| b4-**responsive-hide-up**    | Responsive hide up    |
| b4-**responsive-print-show** | Responsive print show |

​		
​		
