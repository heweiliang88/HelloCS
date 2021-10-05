---
title: Font Awesome 
categories:
- 前端
tags:
- FontAwesome
abbrlink: 18936
---
 Font Awesometitle: icon
categories:
- 前端
- CSS
tags:
- csser
abbrlink: 12014



# 阿里巴巴字体

[Iconfont-webfont平台](https://www.iconfont.cn/webfont?spm=a313x.7781069.1998910419.12&puhui=1#!/webfont/index)
@font-family属性
引入
使用

> CDN
>
> CDN  要输入对应的文字才能生出相应的CDN ,所以CDN不是通用的是根据字体的内容而改变的 
>
> 可以在平台上直接获取到cdn地址替换。由于cdn地址以//开头，因此使用cdn地址时，请确保demo页在某个服务里面。直接本地以file形式打开是无法访问//开头的cdn的，如确有必要请加上http。

```css
@font-face {
    font-family: 'webfont';
    font-display: swap;
    src: url('//at.alicdn.com/t/webfont_dnya9gb2zfu.eot');
    /* IE9*/
    src: url('//at.alicdn.com/t/webfont_dnya9gb2zfu.eot?#iefix') format('embedded-opentype'),
        /* IE6-IE8 */
        url('//at.alicdn.com/t/webfont_dnya9gb2zfu.woff2') format('woff2'),
        url('//at.alicdn.com/t/webfont_dnya9gb2zfu.woff') format('woff'),
        /* chrome、firefox */
        url('//at.alicdn.com/t/webfont_dnya9gb2zfu.ttf') format('truetype'),
        /* chrome、firefox、opera、Safari, Android, iOS 4.2+*/
        url('//at.alicdn.com/t/webfont_dnya9gb2zfu.svg#AlibabaPuHuiTiL') format('svg');
    /* iOS 4.1- */
}
// 字体 大小  样式
.web-font {
    font-family: "webfont" !important;
    font-size: 16px;
    font-style: normal;
    -webkit-font-smoothing: antialiased;
    -webkit-text-stroke-width: 0.2px;
    -moz-osx-font-smoothing: grayscale;
}
```

本地下载离线

# Font Awesome 图标

## 总结
```css
<link rel="stylesheet" href="https://cdn.staticfile.org/font-awesome/4.7.0/css/font-awesome.css">
```
> 1. fa fa-名称
> 2. fa-lg、fa-5x ~ 2x 图标大小
> 3. fa-ul、fa-li 列表图标
> 4. fa-spin、fa-pulse 动态图标
> 5. fa-rotate-度数、fa-flip-度数 旋转 翻转
> 6. fa-fw 固定宽度
> 7. fa-stack (父类) 堆叠 fa-stack-1、2 层叠顺序 
> 8. fa-inverse 颜色取反
> 9. fa-border 边框 fa-pull-left/right 左浮动或者右浮动
> 10. aria-hidden="true"  属性可以用来控制一系列可访问API中的非交互内容的显示或隐藏。
## 官网
[Font Awesome，一套绝佳的图标字体库和CSS框架](https://fontawesome.dashgame.com/)
## 使用
[Font Awesome，一套绝佳的图标字体库和CSS框架](https://fontawesome.dashgame.com/)
## 图标搜索
[Font Awesome图标搜索-ThinkCMF](https://www.thinkcmf.com/font/search/index.html)
## 安装
国内推荐 CDN：
```css
<link rel="stylesheet" href="https://cdn.staticfile.org/font-awesome/4.7.0/css/font-awesome.css">
```
```css
<link href="//netdna.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
```
> aria-hidden="true"
>
> aria-hidden属性可以用来控制一系列可访问API中的非交互内容的显示或隐藏。
>
> 把 `aria-hidden="true"` 加到元素上会把该元素和它的所有子元素从可访问性树上移除。这样做可以通过隐藏下列内容来提升使用辅助技术的用户体验：
>
> - 纯装饰性的内容，如图标、图片
> - 重复的内容，如重复的文本
> - 屏幕外或被折叠的内容，如菜单
>
> false:（默认）元素会暴露给可访问性API。
>
> true:元素不会暴露给可访问性API。
>
> undefined:（默认）客户端决定元素是否暴露给可访问性API。
>
> [使用aria-hidden属性 - 无障碍 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/Accessibility/ARIA/ARIA_Techniques/%E4%BD%BF%E7%94%A8aria-hidden%E5%B1%9E%E6%80%A7)
## 基本使用 `fa fa-图标名称`
```html
<i class="fa fa-camera-retro"></i> fa-camera-retro
```
## 大图标 `fa-lg(33%递增)`、`fa-2x`、`fa-3x`、`fa-4x`、`fa-5x`
使用`fa-lg(33%递增)`、`fa-2x`、`fa-3x`、`fa-4x`、`fa-5x` 类来放大图标
```html
<i class="fa fa-flag fa-lg"></i>
<i class="fa fa-flag fa-2x"></i>
<i class="fa fa-flag fa-3x"></i>
<i class="fa fa-flag fa-4x"></i>
<i class="fa fa-flag fa-5x"></i>
```
## 列表图标 `fa-ul` + `fa-li`
使用 `fa-ul` 和 `fa-li` 便可以简单的将无序列表的默认符号替换掉。
```html
<ul class="fa-ul">
  <li><i class="fa-li fa fa-check-square"></i>List icons</li>
  <li><i class="fa-li fa fa-check-square"></i>can be used</li>
  <li><i class="fa-li fa fa-spinner fa-spin"></i>as bullets</li>
  <li><i class="fa-li fa fa-square"></i>in lists</li>
</ul>
```
## 固定宽度图标 `fa-fw`
> 图标的宽度不一样
使用 `fa-fw` 可以`将图标设置为一个固定宽度`。主要用于不同宽度图标无法对齐的情况。 尤其在列表或导航时起到重要作用。
```html
<div class="list-group">
  <a class="list-group-item" href="#"><i class="fa fa-home fa-fw"></i>&nbsp; Home</a>
  <a class="list-group-item" href="#"><i class="fa fa-book fa-fw"></i>&nbsp; Library</a>
  <a class="list-group-item" href="#"><i class="fa fa-pencil fa-fw"></i>&nbsp; Applications</a>
  <a class="list-group-item" href="#"><i class="fa fa-cog fa-fw"></i>&nbsp; Settings</a>
</div>
```
## 边界和被拉的图标 `fa-border`，`fa-pull-right` 、 `fa-pull-left`
> fa-border 添加边框
>
> fa-pull-right // fa-pull-left(默认值) 浮动到左边还是右边
`fa-border`，`fa-pull-right` 或 `fa-pull-left` 类用于拉式引用或文章图标。
```html
<i class="fa fa-quote-left fa-3x fa-border"></i>
<i class="fa fa-quote-left fa-3x fa-pull-left fa-border"></i>
<i class="fa fa-quote-left fa-3x fa-pull-right fa-border"></i>
```
## （动态旋转）动态图标 `fa-spin`、`fa-pulse`
> spin 旋转,使旋转
>
> pulse 跳动、脉跳
>
> 
>
> spinner 自旋体
>
> refresh 刷新
>
> fa-cog 齿轮
使用 `fa-spin` 类来使任意图标旋转，现在您还可以使用 `fa-pulse` 来使其进行8方位旋转。
尤其适合 `fa-spinner`、`fa-refresh` 和 `fa-cog` 。
```html
<i class="fa fa-spinner fa-spin"></i>
<i class="fa fa-circle-o-notch fa-spin"></i>
<i class="fa fa-refresh fa-spin"></i>
<i class="fa fa-cog fa-spin"></i>
<i class="fa fa-spinner fa-pulse"></i>
```
## （静态旋转）旋转和翻转的图标 `fa-rotate-` 、`fa-flip-*`
使用 `fa-rotate-*` 和 `fa-flip-*` 类可以对图标进行任意旋转和翻转。
> fa-rotate- 度数
>
> fa-flip-horizontal  水平 vertical 竖直
```html
<i class="fa fa-shield"></i> normal<br>
<i class="fa fa-shield fa-rotate-90"></i> fa-rotate-90<br>
<i class="fa fa-shield fa-rotate-180"></i> fa-rotate-180<br>
<i class="fa fa-shield fa-rotate-270"></i> fa-rotate-270<br>
<i class="fa fa-shield fa-flip-horizontal"></i> fa-flip-horizontal<br>
<i class="fa fa-shield fa-flip-vertical"></i> icon-flip-vertical
```
## 堆叠的图标（多个图标层叠在一起） ` fa-stack`、`fa-inverse `
> 
要堆叠多个图标，请使用父级上的` fa-stack` 类，`fa-stack-1x` 类用于常规大小的图标，`fa-stack-2x `用于较大的图标。
`fa-inverse `类可以用作替代图标颜色。您还可以向父级添加更大的图标类，以进一步控制尺寸。
```html
<span class="fa-stack fa-lg">
  <i class="fa fa-circle-thin fa-stack-2x"></i>
  <i class="fa fa-twitter fa-stack-1x"></i>
</span>
fa-twitter on fa-circle-thin<br>
<span class="fa-stack fa-lg">
  <i class="fa fa-circle fa-stack-2x"></i>
  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
</span>
fa-twitter (inverse) on fa-circle<br>
<span class="fa-stack fa-lg">
  <i class="fa fa-camera fa-stack-1x"></i>
  <i class="fa fa-ban fa-stack-2x text-danger" style="color:red;"></i>
</span>
fa-ban on fa-camera
```
