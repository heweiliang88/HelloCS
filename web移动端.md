---
title: 移动端开发指南
categories:
- 前端
tags:
- 移动端开发
abbrlink: 36646
---
# 移动端开发

- 前端开发： html、css、Js、React、Vue

- 移动端开发：Android 、iOS、ReactNative、Flutter

- 后端开发： Java 、C++ 、PHP、Go、Python、数据采集、音频开发


# H5 学习

> - [x] [Hybrid设计-慕课网](https://www.imooc.com/learn/850)
> - [ ] [移动端web开发rem适配方案视频教程-慕课网](https://www.imooc.com/learn/942)
> - [ ] [移动前端开发和 Web 前端开发的区别是什么？](https://juejin.cn/post/6844904183892541453)
> - [ ] [给客户端同学的一份前端学习指南](https://juejin.cn/post/6844903709382541320)
> - [ ] [中高级前端必须注意的40条移动端H5坑位指南 | 网易三年实践](https://juejin.cn/post/6921886428158754829)
> - [ ] [前端基础知识概述 -- 移动端开发的屏幕、图像、字体与布局的兼容适配](https://juejin.cn/post/6844903935568789517)
> - [ ] [前端移动端适配总结 - SegmentFault 思否](https://segmentfault.com/a/1190000011586301)
> - [ ] [移动端前端适配方案对比 | Hancoson'blog](http://www.vsoui.com/2017/03/15/mobile-FE-Adaptive/)
> - [ ] [前端响应式布局原理与方案（详细版）](https://juejin.cn/post/6844903814332432397)
> - [ ] [前端响应式布局原理与方案（详细版）](https://juejin.cn/post/6844903814332432397)
> - [ ] [HTML5 移动端自适应方案与踩坑](https://juejin.cn/post/6844903795613237261)
> - [ ] [浅谈前端和移动端的事件机制](https://juejin.cn/post/6844903506311118856)
> - [ ] [移动前端开发和 Web 前端开发的区别是什么？](https://juejin.cn/post/6844904183892541453)

移动端设备

- Android 系统版本和屏幕分辨率
- iOS 顽固标准和未知特性

APP技术的种类

- App 本身就有个webview容器，在容器里可以运行 Web 前端相关代码，由此 H5 和原生 App 结合又衍生出来了 Hybrid App 技术。

| Web app    | hybrid App(webview) 混合App | Native app(原生 App) | React Native | Weex |
| ---------- | --------------------------- | -------------------- | ------------ | ---- |
| html       | html                        |                      |              |      |
| css        | css                         |                      |              |      |
| javascript | javascript                  |                      |              |      |

|          | Native      | Html5             | Hybrid    |
| -------- | ----------- | ----------------- | --------- |
| App特性  |             |                   |           |
| 图形渲染 | 本地API渲染 | HTML、Canvas、CSS | 混合      |
| 性能     | 快          | 慢                | 慢        |
| 原生界面 | 原生        | 模仿              | 模仿      |
| 发布     | App store   | Web               | App store |

Hybrid App

- Hybrid  混合开发
	- 解决开发效率的问题

H5主要内容

- H5布局技术
- H5相关框架

H5 技术是一系列移动端 web 前端技术的集合 用于移动端web网页

布局方式

移动端 web 、 PC web  和 H5 App

PC 适配到 移动端H5 

设备

兼容性适配 和 屏幕适配

meta属性

```css
<meta name="screen-orientation" content="portrait"> //Android 禁止屏幕旋转
<meta name="full-screen" content="yes">             //全屏显示
<meta name="browsermode" content="application">     //UC应用模式，使用了application这种应用模式后，页面讲默认全屏，禁止长按菜单，禁止收拾，标准排版，以及强制图片显示。
<meta name="x5-orientation" content="portrait">     //QQ强制竖屏
<meta name="x5-fullscreen" content="true">          //QQ强制全屏
<meta name="x5-page-mode" content="app">            //QQ应用模式
```

在 iOS Safari （其他浏览器和 Android 均不会）上会对那些看起来像是电话号码的数字处理为电话链接

- 7 位数字，形如：1234567
	带括号及加号的数字，形如：(+86)123456789
	双连接线的数字，形如：00-00-00111
	11 位数字，形如：13800138000

```
<meta name="format-detection" content="telephone=no" /> //关闭识别
<meta name="format-detection" content="telephone=no" /> //开启识别
 
```

邮箱识别（Android）

```
<meta content="email=no" name="format-detection" /> // 安卓上会对符合邮箱格式的字符串进行识别，我们可以通过如下的 meta 来管别邮箱的自动识别：
<a mailto:dooyoe@gmail.com">dooyoe@gmail.com</a> // 同样地，我们也可以通过标签属性来开启长按邮箱地址弹出邮件发送的功能：
```

# 移动端兼容适配

## 业务

- 各屏幕适配（分辨率差异）
- Retina屏(视网膜)下的细节处理（主要是1px的问题）

### Retina屏 1px问题

- 有些手机上的1px明显跟另外的一些手机的1px粗细不一样（1px在屏幕上就应该显示一个像素点，但是在Retina屏下则不仅仅是一个像素点）
- 出现原因：Retina(视网膜) dpr（设备像素比） * px  vs  普通屏幕
	- iphone6为例，其dpr(device pixel ratio)设备像素比为2，css中一个1x1的点，其实在iphone6上是2x2的点,并且1px的边框在devicePixelRatio = 2的Retina屏下会显示成2px
	- 在iPhone6 Plus下甚至会显示成3px

解决方案

- [postcss-write-svg](https://github.com/jonathantneal/postcss-write-svg)插件

### 移动端字体放大的问题

- 很多webview提供了调整页面字体大小的功能，例如手机QQ、微信、部分Android内置浏览器等。大部分浏览器调整字体只会导致字体显示大小发生改变，其他元素的大小不受影响。但对于结构稍微复杂一点的页面，字体大小的变动就足以导致页面布局乱掉，导致文本不居中、文字折行、布局混乱等问题。

[移动端字体放大问题的研究](https://juejin.cn/post/6844903507061932040)

ios

[总结移动端H5开发常用技巧（干货满满哦！）](https://juejin.cn/post/6844904066301050893)

android

0.5px 细线

## 流程

1. 在head 设置width=device-width的viewport‘

2. 在css中使用px

3. 在适当的场景使用flex布局，或者配合vw进行自适应

4. 在跨设备类型的时候（pc <-> 手机 <-> 平板）使用媒体查询

5. 在跨设备类型如果交互差异太大的情况，考虑分开项目开发

## 概念

需要在适配的地方进行适配处理，而不是全局的，所有元素都进行适配处理

- 字体的大小
- 元素的大小和位置
- 图片的大小和位置

- 完成的项目

	- 尽量不要改动代码 
	- post-px-to-viewport  px==>viewport 的一个包 

- 刚开始的项目（规范、准则）

	- 使用响应式的库 

	- 媒体查询适配不兼容
	- 布局不要使用其他布局，使用flex布局
	- 不要把固定宽度写死，使用 rem、百分比、vw 

- 适配的方法 

	- 媒体查询
	- flex布局
	- rem + viewport 
	- vw + vh

- 响应式设计  Responsive Web Design  

	- ​                 

- 响应式 vs 自适应

	- 响应式设计  Responsive Web Design(RWD)  
	- 自适应 Adaptive Web Design(AWD)
		- 目的：适配各种不同的移动设备，致力于提升用户体验所产生的的技术
		- RWD 是 AWD 的子集

## 设备

- 手机的不同设备
- 电脑的不同设备
- 电脑上的分辨率  
- 手机上的尺寸

像素 px

分辨率

- 设备物理分辨率（设备像素 ）物理像素  720p => 1080 => 2k=>4k 变大 
	- 出现问题 同一张图片 分辨率越大 图像不就要被缩小一倍

- 逻辑分辨率（设备独立像素） 逻辑像素
	- 首次提出了Retina Display(视网膜屏幕)的概念，在iPhone4使用的视网膜屏幕中，把2x2个像素当1个像素使用，这样让屏幕看起来更精致，但是元素的大小却不会改变。从此以后高分辨率的设备，多了一个逻辑像素。这些设备逻辑像素的差别虽然不会跨度很大，但是仍然有点差别，于是便诞生了移动端页面需要适配这个问题，既然逻辑像素由物理像素得来，那他们就会有一个像素比值

设备像素比 dpr 

设备像素比device pixel ratio简称dpr，即物理像素和设备独立像素的比值。为什么要知道设备像素比呢？因为这个像素比会产生一个非常经典的问题，1像素边框的问题。

[面试官：你了解过移动端适配吗？](https://juejin.cn/post/6844903631993454600)

| 设备 | 屏幕尺寸 | 分辨率 pt | 分辨率 px | PPI(DPI) |      |
| ---- | -------- | --------- | --------- | -------- | ---- |
|      |          |           |           |          |      |
|      |          |           |           |          |      |
|      |          |           |           |          |      |

|              | 手机 iphone 6                                                | 电脑             |
| ------------ | ------------------------------------------------------------ | ---------------- |
| 分辨率       | 屏幕分辨率是指纵横向上的像素点数，单位是px。屏幕分辨率确定计算机屏幕上显示多少信息的设置，以水平和垂直像素来衡量。就相同大小的屏幕而言，当屏幕分辨率低时（例如 640 x 480），在屏幕上显示的像素少，单个像素尺寸比较大。屏幕分辨率高时（例如 1600 x 1200），在屏幕上显示的像素多，单个像素尺寸比较小，1334pt x 750pt (屏幕上垂直(横向)有1334个物理像素，水平(纵向)有750个物理像素) | 1920*1080  2k 4k |
| 屏幕尺寸     | 4.7in  英寸是长度单位，不是面积单位。4.7英寸指的是屏幕对角线的长度， 1英寸等于2.54cm。 |                  |
| 像素         | 像素（Pel，pixel;pictureelement），为组成一幅图像的全部亮度和色度的最小图像单元、它指显示屏的画面上表示出来的最小单位(注意每个像素的大小是不固定的，他是根据设备的分辨率决定的，知识点，后面要考) |                  |
| 屏幕像素密度 |                                                              |                  |
| 设备独立密度 |                                                              |                  |
| 物理像素     |                                                              |                  |

## 单位

| 单位                | 描述                                    |
| ------------------- | --------------------------------------- |
| rem                 | root em 根em  相对大小 相对HTML的根元素 |
| em                  | 相对单位                                |
| px                  | 像素                                    |
| vw、vh 、vmin、vmax | 视图窗口                                |
| %                   | 百分比                                  |
| rpx                 | 微信小程序的单位 root px                |

## viewport 

视口(viewport)代表当前可见的计算机图形区域。在Web浏览器术语中，通常与浏览器窗口相同，但不包括浏览器的UI， 菜单栏等——即指你正在浏览的文档的那一部分

```
<meta name="viewport" content="width=device-width; initial-scale=1; maximum-scale=1; minimum-scale=1; user-scalable=no;">
```

## 媒体查询

- 媒体查询 media queries：查询设备的宽度来执行不同的 `css` 代码，最终达到界面的配置。

```css
@media screen and(max-width:600px){  
    // 当屏幕尺寸小于600px时，应用下面的CSS样式
    // 主要通过查询不同的宽度来执行不同的css,最终达到界面的配置
    // seaction{    
    } 
}
```

- 解决方案
	- 对不同的设备编写不同的css代码
	- 支持响应式的库 Bootstrap(栅格系统) 、Foundation、UI库
- 优点
	- 可以做到设备像素比的判断，方法简单、成本较低
	- 调整屏幕宽度的时候，不需要刷新页面即可响应
	- 图片便于修改，只需要修改css文件
- 缺点
	- 代码量比较大，维护不方便
	- 为了兼顾大屏幕或高清设备，会造成其他设备资源浪费，特别是加载图片资源
	- 为了兼顾移动端和PC端各自响应式的展示效果，难免会损失各自特有的交互方式

## flex弹性布局

```html
// viewport 固定
<meta name="viewport" content="width=device-width,initial-scale=1,maximu-scale=1,user-scalable=no">
```

- 高度定死，宽度自适应，元素都采用`px`做单位

随着屏幕宽度变化，页面也会跟着变化，效果就和PC页面的流体布局差不多，在哪个宽度需要调整的时候使用响应式布局调调就行

- iphone6/7/8 下： 底部tab栏，position:fixed定位；display:flex;盒子布局；flex-direction:row;justify-content:space-between;
- iPad下： 在中间分类栏：以position:absolute;display:flex;flex-direction:column;弹性盒子

### flex + vw 的布局方式

### flex + 百分比的布局方式

### flex + rem 的布局方式

```css
// 依次将页面上的px转换为rem，这样我们就得到了全是rem为尺寸单位的页面
html{
	font-size:15px;
}
p{
	font-size:2rem; // 30px
    // 这个只能指定在一个设备上自适应，没有办法在多个设备下设置，通过以下方法
}
```

- flexible_css.js flexible.js : 通过flexible.js实现了rem自适应，有了flexible.js，我们就不必再为移动端各种设备兼容烦恼

```html
// 实现用js来自动根据屏幕宽度设置 html元素的font-size的值
<script src="http://g.tbcdn.cn/mtb/lib-flexible/0.3.4/??flexible_css.js,flexible.js"></script>
```

## rem和viewport缩放

根据屏幕宽度设定 `rem` 值，需要适配的元素都使用 `rem` 为单位，不需要适配的元素还是使用 `px` 为单位。`1em=16px`

```html
<meta name="viewport" content="width=device-width,initial-scale=1,maximu-scale=1,user-scalable=no">
// device-width = 设备的物理分辨率
```

- 这样整个网页在设备内显示时的页面宽度就会等于设备逻辑像素大小，也就是device-width。
- device-width的计算公式为：设备的物理分辨率/(devicePixelRatio * scale)， 在scale为1的情况下，device-width = 设备的物理分辨率/devicePixelRatio 。
	- 设备的物理分辨率

## rem方式

rem : root em 根元素的相对单位

```css
:root{
	font-size:16px; // 默认值
}
p{
  	font-size:1em // 16px
}
```

## vw + vh

vw、vh、vmin、vmax ：可视视图的宽度

- vw 是一个尺寸单位，等于1%屏幕的宽度
	- ipone6手机 100vw = 750px  => 1vw = 7.5px
	- 1vw = 650 *  1% = 6.5px(如果浏览器不支持0.5px，那么实际渲染结果可能是7px)
- vw : 1vw 等于视口宽度的1%
- vh : 1vh 等于视口高度的1%
- vmin : 选取 vw 和 vh 中最小的那个
- vmax : 选取 vw 和 vh 中最大的那个

## vw + rem

```css
// meta标签设置
<meta name="viewport" content="width=device-width, initial-scale=2.0, maximum-scale=2.0, minimum-scale=2.0, user-scalable=no">
```

```css
// 设置body、html的font-size
html{
	font-size: 13.3333333333333vw // 设计图100px，浏览器根据缩放为 50px
}

p{
    // width: 设计图100px，实际浏览器根据缩放为 50px; 
    width:1rem; // 100px
}

span{
    height:.12rem;
}

// 1px = 100 / 750 =  0.133333333333333vw
// 100px =  0.133333333333333vw * 100 = 13.3333333333333vw 
// 100px = 1rem (设计图100px，浏览器根据缩放为 50px)
```

## 响应式布局



## 工具

post-px-to-viewport （px 转 vw）

- 不必要的计算时间去把标注图中的px转换为vw
- 安装postcss-px-to-viewport插件后进行简单配置就可以在页面直接使用px单位，项目编译后自动转换为对应的vw或vh属性

```bash
npm install postcss-px-to-viewport --save-dev
```

```json
// package.json
```

兼容性测试网站

[Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/)

# 小程序屏幕适配

- 小程序单位 rpx （responsive pixel） 可以根据屏幕宽度进行自适应
	- 以iphnoe6 为基准（750）
	- px => rpx  750 / 屏幕宽度 = rpx   
		- iphone 6  1px像素下 750 /  350 = 2rpx
	- rpx  => px  屏幕宽度 / 750 = px
		- 1rpx下 350/750 = 0.5px
	- 屏幕宽度  px 每个手机的屏幕宽度都不一样
	- 物理像素  rpx
	- 750rpx = 350px 1rpx = 0.5px = 1物理像素

| 设备     | rpx换算px (屏幕宽度/750) | px换算rpx (750/屏幕宽度) |
| -------- | ------------------------ | ------------------------ |
| iPhone5  | 1rpx = 0.42px            | 1px = 2.34rpx            |
| Phone6   | 1rpx = 0.5px             | 1px = 2rpx               |
| iPhone6p | 1rpx = 0.552px           | 1px = 1.81rpx            |

# 移动端性能优化

[移动端浏览器前端优化策略](https://juejin.cn/post/6844903889825693709)

# H5移动端库

## 移动端UI框架

[Mint UI](http://mint-ui.github.io/) 

- npm i mint-ui -S

[Vant](https://youzan.github.io/vant/) 

-  npm i vant -S

[Cube UI](https://didi.github.io/cube-ui/) 

- npm i cube-ui -S

[Muse UI](https://muse-ui.org/) 

- npm i muse-ui -S

[NutUI]( http://nutui.jd.com/)

- npm i @nutui/nutui -S

报错

```
Syntax Error: TypeError: this.getOptions is not a function
// 是less-loader安装的版本太高，卸载重新安装7.0版本即可
// 卸载
npm uninstall --save less-loader
// 安装
npm install -D less-loader@7.x
```





