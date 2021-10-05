---
title: webpack
categories:
  - webpack
tags:
  - 前端
  - webpack
abbrlink: 15317
---

# webpack

项目构建工具

Grunt、Gulp、Webpack

> [Grunt: JavaScript 世界的构建工具 | Grunt 中文网](https://www.gruntjs.net/)
>
> [gulp.js - 基于流(stream)的自动化构建工具 | gulp.js 中文网](https://www.gulpjs.com.cn/)
>
> [webpack 中文文档 | webpack 中文网](https://www.webpackjs.com/)
>
> [前端工程化](https://juejin.im/entry/5b5724d05188251aa01647fd)
>
> [webpack使用教程](https://juejin.im/post/5a5f3513f265da3e5133239a)
>
> [Webpack基本使用](https://juejin.im/post/5d2fd19be51d4576bc1a0eb0)
>
> [NPM你真的会吗？](https://juejin.im/post/5d031b2ae51d454d544abf43)
>
> [前端工程化：你所需要的npm知识储备都在这了 ](https://juejin.im/post/5d08d3d3f265da1b7e103a4d)
>
> [前端工程化——构建工具选型：grunt、gulp、webpack - 前端 ](https://juejin.im/entry/5b5724d05188251aa01647fd)
>
> [JSON文件内容加注释的几种方法](https://blog.csdn.net/ShiMengRan107/article/details/101761922)

## 教程

- 书籍： 
	- [x] [深入浅出 Webpack ](https://webpack.wuhaolin.cn/)
- 教程：
	- 官方教程：[webpack 中文文档](https://webpack.docschina.org/guides/getting-started/)
	- 第三方教程：
		- - [ ] [ Webpack 教程 ](https://www.jiangruitao.com/webpack/)
		- - [x] [（翻译）阮一峰老师的webpack使用教程](https://juejin.cn/post/6844903551806750734)
- 视频：[尚硅谷最新版Webpack5实战教程(从入门到精通)_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1e7411j7T5?from=search&seid=15175345929707821504)
- 好文：
	- [2020年了,再不会webpack敲得代码就不香了(近万字实战)](https://juejin.cn/post/6844904031240863758)
	- [webpack详解](https://juejin.cn/post/6844903573675835400)
	- [带你深度解锁Webpack系列(基础篇)](https://juejin.cn/post/6844904079219490830)
	- [webpack4-用之初体验，一起敲它十一遍](https://juejin.cn/post/6844903599080734728)
	- [一步步从零开始用 webpack 搭建一个大型项目](https://juejin.cn/post/6844904007903772679)
	- - [ ] [webpack：从入门到真实项目配置](https://juejin.cn/post/6844903495959576583)
	- - [x] [妈妈再也不用担心我不会webpack了](https://juejin.cn/post/6844903510530588685)
- 项目
	- [webpack实战（一）：真实项目中一个完整的webpack配置](https://juejin.cn/post/6844903599923806222)
	- [webpack实战 - SegmentFault 思否](https://segmentfault.com/a/1190000015020658)
- 面试：
	- [「吐血整理」再来一打Webpack面试题](https://juejin.cn/post/6844904094281236487)
	- [关于webpack的面试题总结 - 知乎](https://zhuanlan.zhihu.com/p/44438844)
	- [前端面试题 -- webpack - SegmentFault 思否](https://segmentfault.com/a/1190000018704305)
	- [Webpack面试题-技术圈](https://jishuin.proginn.com/p/763bfbd58517)
	- [js-base/Webpack面试题.md at master · lesliecat/js-base](https://github.com/lesliecat/js-base/blob/master/front-end-interview/Webpack%E9%9D%A2%E8%AF%95%E9%A2%98.md)

## 插件

#### webpack

> 使用babel transpiling (ES6)创建一个最小的webpack配置文件。

- Launch the command pallete and look for `Webpack Create`. This will:
- 使用方法 `ctrl + shift + P` 输入 Webpack Create

#### webpack snippets

- `webpack.config.js文件代码提示`

```js
wpstart   // Build an empty webpack configuration content.
wprequire // Require webpack lib.
wprex     // Require Extract Plugin.
wprule    // Add a new loader
wpochunk  // Generate webpack.optimize.CommonsChunkPlugin code.
wpougf    // Generate webpack.optimize.UglifyJsPlugin code.
wpodef    // Generate webpack.DefinePlugin code.
wpoex     // Generate ExtractTextPlugin code.
```

## 基础

![webpack教程 姜瑞涛的官方网站](https://i.loli.net/2021/08/09/Tv2bPYGuwW9ZzmO.jpg)

### 概念

- [webpack](https://www.webpackjs.com/)是**前端的一个项目构建工具**、它是基于Node.js开发出来的一个前端工具 。
- webpack是一个模块打包工具(module bundler)，因为平常多用来对前端工程打包，所以也是一个前端构建工具。其最主要的功能就是模块打包。模块打包，通俗地说就是：找出模块之间的依赖关系，按照一定的规则把这些模块组织合并为一个JavaScript文件。
- webpack认为一切都是模块，JS文件、CSS文件、jpg/png图片等等都是模块。Webpack会把所有的这些模块都合并为一个JS文件，这是它最本质的工作。当然，我们可能并不想要它把这些合并成一个JS文件，这个时候我们可以通过一些规则或工具来改变它

webpack 组成 ： 

- entry 入口 
- output 出口 
- loader 预处理器 
- plugin 插件
- webpack.config.js 和 package.json 文件 
- 开发环境配置 与 生产环境配置

webpack版本

- 3.x
- 4.x
- 5.x

webpack命令

- webpack 供开发构建
- webpack -p 供生产构建一次
- webpack --watch – 连续的增量构建
- webpack -d – 包括源地图
- webpack --colors – 让内部更好看

项目名不能与现有包名一致 webpack node vue react

- webpack 与 webpack-cli
	- webpack  核心包
	- webpack-cli 命令行工具包

webpack安装 webpack 依赖于 webpack-cli 

```bash
// -S 发布环境 生产环境 dependencies
// -D 本地环境 开发环境 devDependencies
// -G 全局环境
npm i webpack-cli -g // 全局安装
npm install webpack@3.10.0 -g
npm i webpack -g // 全局安装
// npm i webpack-cli -D  // 本地安装
cnpm i webpack -D // 安装到开发环境依赖中 --save-dev
```

> webpack  和 webpack-cli 的区别 webpack-cli 是webpack 的命令行工具
>
> 使用Webpack 4.x的命令行需要安装单独的命令行工具

在项目中根目录中运行命令安装到项目开发依赖中

```bash
npm i webpack --save-dev // 开发环境依赖
npm i webpack -D
```

初始化项目(使用npm管理项目中的依赖包)

```bash
npm init -y
npm init
```

安装jQuery

```bash
npm i jquery -S  //--save 生产依赖
```

> 误区：安装的是jquery 包 而不是 jQuery包 这两个包不是同一个版本

webpack运行

```bash
webpack .\src\main.js -o .\dest\bundle.js
webpack 要打包的文件路径 -o 打包好的输出文件的路径
原来webpack的打包cli命令已改为：
webpack <entry> [<entry>] -o <output>
webpack .\src\main.js -o .\dist\bundle.js
```

webpack的作用

1. webpack能够处理JS文件的相互依赖关系（可以把文件导入到 main.js 中）
2. webpack能够处理JS的兼容问题，把高级的、浏览器不能识别的语法转为低级的、浏览器能正常识别的语法

导入jquery

```bash
main.js 文件
import $ from 'jquery' 小写单引号  
```

ES6导入语法

```js
import ** from ** //是ES6中导入模块的方式  
import { name } from './b.js';
console.log(name);
export var name = 'Jack';
```

Common.js导入语法

```js
const * = require('*')
```

网页中会引用那些常用的静态资源

| 静态资源       |                           文件后缀                           |
| -------------- | :----------------------------------------------------------: |
| JS             |        .js、.jsx、.coffee、.ts(TypeScript 类 C# 语言)        |
| CSS            | css、less、sass 、(.css、.less、.sass（旧版本）、.scss（新版本） |
| Images         |                .jpg、.png 、.gif、.bmp、.svg                 |
| 字体文件(font) |          .svg 、.ttf 、 .otf、eot、 .woff、 .woff2           |
| 模板文件       | .ejs、.jade、.vue[这是在webpack中定义组件的方式，推荐这么用] |

网页引用静态资源多了以后有什么问题

- 网页加载速度慢，因为我们要发起很多的二次请求
- 要处理错综复杂的依赖关系

解决问题

1. 合并、压缩、精灵图 雪碧图（CSS Sprites(精灵)）、图片的Base64编码（适用于小图片）
2. 可以使用之前学过的requireJS、也可以使用webpack解决各个包之间的复杂依赖关系

图片的相关优化问题： 减少http请求，减少图片占用的空间

> [【前端攻略】：玩转图片Base64编码 - ChokCoco - 博客园](https://www.cnblogs.com/coco1s/p/4375774.html)
>
> 图片的 base64 编码就是可以将一副图片数据编码成一串字符串，使用该字符串代替图像地址。 节省一个 http 请求
>
> **如果图片足够小且因为用处的特殊性无法被制作成雪碧图（CssSprites），在整个网站的复用性很高且基本不会被更新**。
>
> **使用base64直接把图片编码成字符串写入CSS文件：**
>
> 只有 50 字节的2*2的的背景图。将其转化成 base64 编码，只有 100 多个字符，相比一个 http 请求
>
> **使用 Base64 不代表性能优化**
>
> 是的，使用 Base64 的好处是能够减少一个图片的 HTTP 请求，然而，与之同时付出的代价则是 CSS 文件体积的增大。
>
> CSS 文件体积的增大意味着什么呢？意味着 CRP 的阻塞。
>
> CRP（Critical Rendering Path，关键渲染路径）：当浏览器从服务器接收到一个HTML页面的请求时，到屏幕上渲染出来要经过很多个步骤。浏览器完成这一系列的运行，或者说渲染出来我们常常称之为“**关键渲染路径**”。
>
> 通俗而言，就是图片不会导致关键渲染路径的阻塞，而转化为 Base64 的图片大大增加了 CSS 文件的体积，CSS 文件的体积直接影响渲染，导致用户会长时间注视空白屏幕。HTML 和 CSS 会阻塞渲染，而图片不会。
>
> 页面解析 CSS 生成的 CSSOM 时间增加
>
> [(...) 浅谈 CSS Sprites 雪碧图应用 - 浅谈前端 - SegmentFault 思否](https://segmentfault.com/a/1190000007686042)
>
> **使用CssSprites合并为一张大图：**
>
> [CSS Sprite(精灵图)雪碧图用法视频教程-慕课网](http://www.imooc.com/learn/93)

解决上述的2种解决方案

1. 使用Gulp，是基于task任务的（小巧灵活）
2. 使用Webpack，是基于整个项目进行构建的
	- webpack官网
	- 官网的图片介绍webpack打包的过程
	- 借助于webpack这个前端自动化构建工具，可以完美实现资源的合并、打包、压缩、混淆等诸多功能

webpack目录

> src 源代码
>
> ​	css
>
> ​	js
>
> ​	images
>
> ​	index.html
>
> ​	main.js 项目JS入口文件
>
> dist  完成项目，发布完整项目的文件夹

### webapack最基本的配置文件的使用

---

#### `webpack.config.js`

Webpack具有四个核心的概念，想要入门Webpack就得先好好了解这四个核心概念。它们分别是`Entry（入口）`、`Output（输出）`、`loader`和`Plugins（插件）`。接下来详细介绍这四个核心概念。

`webpack.config.js `这个配置文件，起始就是一个JS文件，通过Node中的模块操作，向外暴露了一个配置对象

`path.join()` 方法使用特定于平台的分隔符作为定界符将所有给定的 `path` 片段连接在一起，然后规范化生成的路径

path.resolve(__dirname, '')表示的其实就是当前文件夹根目录的绝对路径。

```js
const path = require('path')
// 在配置文件中，需要手动指定入口和出口 exports出口
console.log(path)
module.exports = {
    //	入口，表示，要使用webpack打包那个文件
    //  单入口
    entry: path.join(__dirname, './src/main.js'),
    output: { // 输出文件相关的配置
        path: path.join(__dirname, './dist'),//指定打包好的文件，输出到哪个目录中去
        filename: 'bundle.js' //输出的文件的名称
    },
    mode: none  // production(默认) development 
}

//  多入口
    entry: {
        bundle1:'./main1.js',
        bundle2:'./main2.js'
    }

	output:{
        filename:'[name].js'
    }
```

#### webpack运行命令行

```bash
webpack
```

> 新建webpack.config.js文件
> 控制台输出webpack命令执行的时候，webpack做了以下几步：
>
> 1. 首先，webpack 发现，我们并没有通过命令的形式，给他指定入口和出口
> 2. webpack就会去项目的根目录中，查找一个叫做webpack.config.js的配置文件
> 3. 当找到配置文件后，webpack会执行这个配置文件，当解析执行完配置文件后，就得到了配置文件中，导出的配置对象
> 4. 当webpack拿到配置对象后，就拿到了配置对象中，指定的入口和出口，然后进行打包构建

#### `package.json`

**在这个文件中找到“scripts”节点加入：**

 **"dev": "webpack --mode development", // 开发环境**

**"build": "webpack --mode production" // 生产环境**

```json
{
  "name": "Webpack",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" $$ exit 1",
    "dev": "webpack --mode development", // 开发环境
      // "dev": "webpack-dev-server --devtool eval --progress --colors",
    "build": "webpack --mode production" // 生产环境
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "jquery": "^3.4.1"
  }
}
npm run dev
npm run build
```

### plugin插件

---

- webpack-dev-server
- html-webpack-plugin 能够创建index.html

plugin 插件；相关插件

#### webpack-dev-server插件 `自动运行`项目

>  "webpack": "^3.10.0",
>  "webpack-dev-server": "^2.9.7"

安装

```bash
//前提要在webpack安装好全局安装的webpack 和 webpack
npm install webpack-cli -D // webpack4.x以上才要命令行工具 一定要安装
npm install webpack@3.10.0 -D  // 开发依赖
npm install webpack-dev-server@2.9.7 -D
```

webpack-dev-server工具，来进行**自动打包编译的功能** 

```
npm i webpack-dev-server -D
//把这个工具安装到项目的本地开发依赖,本地项目安装，不是全局安装

package.json
"scripts": {
    "test": "echo \"Error: no test specified\" $$ exit 1",
    "dev": "webpack-dev-server", // "dev": "webpack --mode development", // 开发环境
    "build": "webpack --mode production"
},
npm run dev

"build": "webpack --config webpack.dev.config.js",
```

> webpack-dev-server这个工具，如果想要正常运行，要求，在本地项目中，必须安装webpack
>
> webpack-dev-server打包生成的bundle.js文件，并没有存放到实际的物理磁盘中，而是存放在内存中，项目根目录找不到打包好的bundle.js文件
>
> webpack-dev-server 把我们打包生成的文件，以一种虚拟的形式，托管到了项目的根目录中，虽然看不到它，但是，可以认为和dist src node_modules 目录平级，有一个看不到的文件，是bundle.js

```js
<script src="/bundle.js"></script>
```

###### webpack-dev-server的常用命令

```bash
"dev":"webpack-dev-server --open --port 3000 --contentBase src --hot"
webpack-dev-server --open --port 3000 --contentBase src 
--hot 减少不必要的更新
```

index的路径要更改为

```
<script src="./bundle"></script>
```

###### webpack-dev-server的配置命令

webpack.config.js

```js
dev:'webpack-dev-server'

const webpack = require('webpack')

webpack-dev-server --open --port 3000 --contentBase src --hot
devServer:{ // 配置dev-server命令参数的第二次形式，相对来说，这种方式麻烦一些
    open:true, //自动打开浏览器
    port:3000,// 设置启动时候的运行端口
    contentBase: 'src'//指定托管的根目录 src 要带 ‘’ 号
    hot:true // 启用热更新 
}
plugins:[ //数组
    new webpack.HotModuleReplacementPlugin();
    //new 一个热更新的模块对象 这是启动更新
]

npm run dev
```

#### webpack-dev-server报错1

https://www.cnblogs.com/Smiled/p/9790649.html

```
npm WARN webpack-dev-server@3.10.3 requires a peer of webpack@^4.0.0 || ^5.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN webpack-dev-middleware@3.7.2 requires a peer of webpack@^4.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN Webpack@1.0.0 No description
npm WARN Webpack@1.0.0 No repository field.
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.12 (node_modules\fsevents):  
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.12: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
```

```
删除     
在全局下删除    
npm  uninstall  webpack  -g
```

```
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! webmo@1.0.0 dev: `webpack-dev-server --open --port 3000 --contentBase src --hot` 
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the webmo@1.0.0 dev script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\Administrator\AppData\Roaming\npm-cache\_logs\2020-05-22T07_10_16_880Z-debug.log
```

在Vue安装webpack时，遇见了上面的提示，可以安装一个较低的版本：

```bash
npm install webpack@3.0.0 -g
```

#### webpack-dev-server报错2

```
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! Webpack@1.0.0 dev: `webpack-dev-server`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the Webpack@1.0.0 dev script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.
npm ERR! A complete log of this run can be found in:
npm ERR!     D:\Program Files\NodeJs\dev\Node\Cache\_logs\2020-03-30T15_39_10_723Z-debug.log
```

webpack-dev-server的版本太高的锅，3.以上的还是不行。所以降到2.11.3一下左右即可

package.json

```json
{
  "name": "webpack",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "build": "webpack --mode production",
    "dev": "webpack-dev-server",
    "start": "webpack-dev-server --config webpack.dev.config.js --color --progress"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "webpack": "^3.10.0",
    "webpack-dev-server": "^2.9.7"
  },
  "dependencies": {
  }
}
```

删除包 node_modules 和 package-lock.json

```bash
npm i // 重新安装
```

#### html-webpack-plugin插件 在内存中生成主页/ 自动追加页面到主页

> 将index.html页面也放到内存中去
>
> 将物理磁盘中的index.html 页面放到内存中去
>
> 导入在内存中生成html页面的插件

###### html-webpack-plugin插件的两个基本操作

导入在内存中生成 HTML页面的插件

1. 自动在内存中根据指定页面生成一个内存的页面
2. 自动，把打包好的bundle.js追加到页面中去,不用自动引入

安装插件

```bash
 npm i html-webpack-plugin -D
```

webpack.config.js 文件的配置

```js
// 只要是插件，都要放到plugins 节点中去
const webpack = require('webpack')
const htmlWebpackPlugin = require('html-webpack-plugin')
// 导入在内存中生成html页面的插件
devServer:{
    
},
 //webpack.HothtmlWebpackPlugin
plugins:[
     new webpack.HotModuleReplacementPlugin(),
//创建一个在内存中，生成HTML页面的插件
   new htmlWebpackPlugin({
   	template:path.join(_dirname,'./src/index.html'),
   	//指定模板页面，会根据指定的页面路径，去生成内存中的页面
   	filename:'index123.html' //指定生成的页面的名称 
   })
]
//当使用html-wabpack-plugin之后，不在需要手动处理bundle.js的引用路径，这个插件，已经帮我们创建了一个合适的script，并且，引用了正确的路径
```

[webpack-dev-server 出现错误 webpack-dev-server Cannot GET /](https://blog.csdn.net/qq_31847185/article/details/81066537)

index 文件是在src源文件中的

方案一、直接将index.html文件放入dist中

> 我看的webpack3.x视频中，老师直接将index.html文件放入dist中，同样能够生成首页。

方案二，使用HtmlWebpackPlugin插件生成首页

> 因为出错，所以百度的时候找到了第二种解决方案，即用HtmlWebpackPlugin插件生成首页，去官网瞅了一眼，貌似官网也是用的这个插件，所以就了解了一下。

### loader加载器

loader 是预处理器，让webpack处理非js文件，将所有的文件转换为webpack能够处理的有效模块

loader的两个目标

- 识别出应该被loader转化的文件， 使用test属性
- 转换这些文件，使他们添加到依赖图中，最终添加到bundle中，使用use属性

CSS、less、scss

- npm i style-loader css-loader -D   `css`
- npm i less-loader less -D`less`
- npm i sass-loader node-sass -D`scss`

image，字体

- npm i url-loader file-loader -D

### loader配置和使用  引入 JS（webpack 默认部分）、CSS(less,scss) 、图片  、字体

---

修改文件webpack.config.js

```js
npm i style-loader css-loader less-loader node-sass sass-loader -D // 开发依赖
cnpm i url-loader file-loader -D
module:{
	rules:[
		{test:/\.css&/,use:['style-loader','css-loader']},
		{test:/\.less&/,use:['style-loader','css-loader','less-loader']},
        {test:/\.scss$/,use:['style-loader','css-loader','sass-loader']},
        {test:/\.(ttf|eot|svg|woff|woff2)$/,use:'url-loader'},
        {test:/\.(jpg|png|gif|bmp|jpeg)$/,use:'url-loader?limit=7631$name=[name].[ext]'}
	]
}
```



#### 一、CSS(less、scss)

----

#### css 、less、scss、字体

导入main.js 入口文件

```
import './css/index.css'
```

```js
import './css/index.css'

npm i style-loader css-loader -D
//模块的匹配规则
module:{ //配置所有第三方loader模块的
	rules;[ //处理CSS文件的loader
		{test:/\.css$/,use:['style-loader','css-loader']}
	]	
}
npm i less-loader less -D
//处理less文件的loader
	{test:/\.less$/,use:['style-loader','css-loader','less-loader']}
	
npm i sass-loader node-sass -D
//处理sass文件的loader
	{test:/\.less$/,use:['style-loader','css-loader','less-loader','sass-loader']}
```

#### loader配置处理css样式表的第三方loader

使用import语法，导入CSS样式表

```js
import './css/index.css
```

`注意：webpack、默认只能打包处理JS类型的文件，无法处理其他的非JS类型的文件`

如果要处理非JS类型的文件，我们需要手动安装一些第三方loader加载器

1. 如果想要打包处理css文件

```bash
npm i style-loader css-loader -D
```

2. webpack.config.js配置文件

新增module配置节点，有一个rules属性，这个rules属性是个数组，这个数组存放，第三方文件的匹配和处理规则

```js
module:{ //这个节点.配置第三方模块加载器
	rules:[ //所有第三方模块的匹配规则
		{test:/\.css$/,use:['style-loader','css-loader']}
		//配置处理 .css文件的第三方loader规则
		// 调用规则从右到左  
	]
}
```

> webpack 处理第三方文件类型得过程
>
> 1. 不是JS文件，然后去配置配置文件中查找有没有 第三方的loader规则
> 2. 如果找到对应的规则，就会把处理的结果，直接交给webpack会调用loader处理，这种文件类型
> 3. 在调用loader的时候，是从后往前调用的
> 4. 最后一个loader调用完毕，会把处理结果，直接交给webpack进行打包合并，最终输出到bundle.js中去

报错

```
ERROR in ./src/main.js
Module not found: Error: Can't resolve './css/index' in 'd:\GitRepository\VsWorkSpace\WebFrame\Webpack\src'
 @ ./src/main.js 2:0-21
 @ multi ./node_modules/_webpack-dev-server@2.11.5@webpack-dev-server/client?http://127.0.0.1:8081 ./src/main.js
```

#### loader配置处理less文件的loader

```js
cnpm i less -D 
cnpm i less-loader _D

module:{ //这个节点.配置第三方模块加载器
	rules:[ //所有第三方模块的匹配规则
		{test:/\.css$/,use:['style-loader','css-loader']}
		//配置处理 .css文件的第三方loader规则
		// 调用规则从右到左
        //配置处理less文件的第三方loader规则 
       	{test:/\.less$/,use:['style-loader','css-loader','less-loader']}
	]
}
```

#### loader配置处理scss文件的loader

```js
cnpm i node-sass -D
cnpm i sass-loader -D

module:{ //这个节点.配置第三方模块加载器
	rules:[ //所有第三方模块的匹配规则
		{test:/\.css$/,use:['style-loader','css-loader']}
		//配置处理 .css文件的第三方loader规则
		// 调用规则从右到左
        //配置处理less文件的第三方loader规则 
       	{test:/\.less$/,use:['style-loader','css-loader','less-loader']}
       	 //配置处理less文件的第三方loader规则 
       	{test:/\.sass$/,use:['style-loader','css-loader','sass-loader']}
       	 //配置处理sass文件的第三方loader规则 
	]
}
```



#### 二、字体

----

#### webpack中使用url-loader处理字体

 Bootstrap安装

```js
index.html
  <link rel="stylesheet" src="/node_modules/bootstrap/dist/css/bootstrap.css">

main.js
npm i boostrap@3 -S  // 要安装bootstrap 3
cnpm i url-loader -D
{test:/\.(ttf|eot|svg|woff|woff2)$/,use:'url-loader'} //处理字体文件的loader
```

```js
  
//如果要通过路径的形式，去引入node_modules中相关的文件，可以直接省略 路径前面的node_modules 这一层目录，直接写包的名称，然后后面跟上具体的文 件路径
// 不写node_modules这一层目录，默认 就会去node_modules中查找
module:{ //这个节点.配置第三方模块加载器
	rules:[ //所有第三方模块的匹配规则
		{test:/\.css$/,use:['style-loader','css-loader']}
		//配置处理 .css文件的第三方loader规则
		// 调用规则从右到左
        //配置处理less文件的第三方loader规则 
       	{test:/\.less$/,use:['style-loader','css-loader','less-loader']}
       	 //配置处理scss文件的第三方loader规则 
       	{test:/\.scss$/,use:['style-loader','css-loader','sass-loader']}
       	 //配置处理lass文件的第三方loader规则 
		{test:/\.(ttf|eot|svg|woff|woff2)$/,use:'url-loader'},
		//处理字体文件的loader
	]
}
```

```
bootstrap 有两个版本 3、4 
引入css要安装 css-loader 和 style-loader 这两个依赖 
如果不指定安装那么，bootstrap 默认的版本就是bootstrap4
npm i 包 -g // 默认的版本是最新的 
```



#### 三、图片

---

默认情况下，webpack无法处理CSS文件中的url地址，不管是图片还是字体库，只要是URL地址，都处理不了

```js
cnpm i url-loader file-loader -D

{test:/\.(jpg|png|gif|bmp|jpeg)$/,use:'url-loader?limit=7631&name=[name].[ext]'}
{test:/\.(jpg|png|gif|bmp|jpeg)$/,use:'url-loader?limit=7631&name=[hash:8]-[name].[ext]'} 
//添加hash值 解决不同目录的不同图片名字相同 出现冲突的问题
// ?传参 7631图片大小的字
//name=[hash:8]-[name].[ext] 添加8位hash值解决重命名
// name=[name].[ext] 保留原本的名称 .[ext] 保留文件的后缀名
// limit 给定的值，是图片的大小，单位是byte ,如果我们引用的图片大于，或等于更定的limit值，则不会被转为base64格式的字符串，如果图片小于给定的limit值，则会被转为base64的字符串
//图片的名称是哈希值
//处理图片路径的loader
```



#### 四、JS文件（ES6\ES7及以上的高级语法）、 webpack中的babel的配置

---

`Babel,可以帮助我们将高级的语法转为低级的语法`

在webpack中，可以运行如下两套命令，安装两套包，去安装Babel相关的loader功能

```bash
//第一套包 babel转换工具
npm i babel-core babel-loader babel-plugin-transform-runtime -D
babel-core/loader plugin-transform-runtime 
//第二套包 语法插件
npm i babel-preset-env babel-preset-stage-0 -D
babel-preset- env/stage-0
```

```js
webpack配置文件，在module节点下的rules数组中，添加一个新的匹配规则：
{ test:/\.js$/,use:'babel-loader',exclude:/node_modules/ }
 
//exclude
exclude:/node_modules/ 
注意：在配置balbe的loader规则的时候，必须把node_modules目录，通过exclude选项排除掉
不排除node_modules,则Babel会把node_modules中所有的第三方JS文件，都打包编译，这样，会非常消耗CPU,同时，打包速度非常慢；
Babel把所有node_modeues中的JS装换完毕了，项目也无法运行

项目根目录中，新建一个.babelrc 的Babel配置文件，这个配置文件，属于JSON格式，在写.babelrc配置的时候 ,必须符合JSON语法规范；不能注释，字符串必须用双引号

// presets  语法
.babelrc文件
{
	"presets":["env","stage-0"], //语法
	"plugins":["transform-runtime"] //插件
}
```

```js
class关键字，是ES6中提供的新语法，是用来实现ES6中面向对象编程的方式
class Person{
//使用static关键字，可以定义静态属性
// 静态属性，就是直接通过类名，直接访问的属性
//实例属性：只能通过类的实例，来访问的属性，叫做实例属性
	static info = {name:'zs',age:20}
}
//Java C# 实现面向对象的方式完全一样了，class是从后端语言中借鉴过来的。来实现面向对象
var p1 = new Person()
conslole.log(Person.info})
在webpack中，默认只能处理一部分ES6的新语法，一些更高级的ES6语法或者ES7语法，webpack是处理不了的;这时候就需要借助于第三方的loader,来帮助webpack 处理这些高级的语法，当第三方loader把高级语法转为低级语法之后，会把结果交给webpack去打包到bundle.js中
//通过babel,可以帮助我们将高级的语法转为低级的语法
//
function Animal(name)
{
	this.name = name
}
Animal.info = 123
var al = new Aninal('小花')
//静态属性
console.log(Animal.info);
//实例属性
console.log(al.name)
```

### uglify 压缩JS代码

webpack有很多管道系统来扩展他的功能，uglify是用来压缩js代码的

```
var uglifyJsPlugin = webpack.optimize.UglifyJsPlugin;

plugins:[
	new uglifyJsPlugin({
		compress:{
			warnings:false
		}
	})
	
	new webpack.optimize.UglifyJsPlugin({
            compress: {
                warnings: false
            }
     })
]
```

### open-browser-webpack-plugin  自动打开浏览器标签页

能在webpack加载的时候打开一个浏览器标签页

```js
var OpenBrowserPlugin = require('open-browser-webpack-plugin');

plugins:[
    new OpenBrowserPlugin({
      url: 'http://localhost:8080'
    })
]
```

### webpack + Vue结合

---

#### 在普通页面中使用render函数渲染组件

```html
<div id="app">
    <p>this is a p</p>
</div>
<script>
    var login = {
        template: '<h1>this is a h1</h1>'
    }
    var vm = new Vue({
        el: '#app',
        data: {},
        methods: {},
        //注意：这里
        render(createElements) {
            return createElements(login)
        },
        render:function(createElements) {
           return createElements(login)
        },
        //compontents:{
        //  login
        //}
    });
</script>
```

> render 与 compontents 的区别
>
> render：return 的结果，会替换页面中el指定的那个容器的内容，compontents 则不会清空

#### render的几种写法

```js
render(createElements) {
	return createElements(login)
},
render:function(createElements) {
	return createElements(login)
},
// 简写方法    
render: c => c(login)
```

#### 如何在webpack中构建项目中，使用Vue进行开发

##### 在普通网页中如何使用vue

> 1. 使用script标签，引入vue的包
> 2. 在index页面中，创建一个id为appdiv容器
> 3. 通过newVue得到一个vm的实例

##### 在webpack中如何使用vue

>注意：在webpack 中，使用import Vue from'vue'导入的Vue构造函数，功能不完整，只提供了runtime-only的方式，并没有提供像网页中那样的使用方式，
>回顾包的查找规则:
>
>1. 找项目根目录中有没有node modules 的文件夹
>2. 在node modules中根据包名，找对应的vue 文件夹
>3. 在vue文件夹中，找一个叫做package.json的包配文件
>4. 在package.json 文件中，查找一个main 属性[main属性指定了这个包在被加载时候的入口文件]

方法一 、直接在引入vue中vue,js

```js
main.js 入口文件
import Vue from '../node_modules/vue/dist/vue.js'
```

方法二  在webpack.config.js中添加resolve属性：

```js
//vue会默认导入vue.runtime.common.js文件
import Vue from 'vue'
resolve:{
    alias:{ //修改Vue被导入时候的包的路径
        "vue$":"vue/dist/vue.js" 
    }
}
```

方法三、修改 node_modules中 vue 的 package.json下的 包配置文件

```js
//ctrl+f 查找main的属性
dist/vue.runtime.common.js => dist/vue.js
```

方法四、直接使用vue.runtime.common.js文件（ runtime-only的方式） 需要安装第三方loader

这种方法能直接解析``vue后缀的文件`进行

```js
npm i vue -S
npm i vue-loader vue-template-compiler -D
npm i style-loader css-loader -D
import Vue from 'vue'
单独的把组件的内容新建成.vue文件
```

main.js

```js
// var login = {
//   template: '<h1>这是login组件，是使用网页中形式创建出来的组件</h1>'
// }
// 1. 导入 login 组件
import login from './login.vue'
// 默认，webpack 无法打包 .vue 文件，需要安装 相关的loader： 
//  cnpm i vue-loader vue-template-compiler -D
//  在配置文件中，新增loader哦配置项 { test:/\.vue$/, use: 'vue-loader' }
var vm = new Vue({
  el: '#app',
  data: {
    msg: '123'  
  },
  // components: {
  //   login
  // }
  /* render: function (createElements) { // 在 webpack 中，如果想要通过 vue， 把一个组件放到页面中去展示，vm 实例中的 render 函数可以实现
    return createElements(login)
  } */
  render: c => c(login)
})
import m222, { title as title123, content } from './test.js'
console.log(m222)
console.log(title123 + ' --- ' + content)
```

##### 在webpack中配置.vue 组件页面的解析

webpack无法打包.vue 文件需要安装 vue相关的1oader

1. 运行`cnpm i vue -S`将vue安装为运行依赖；

2. 运行`cnpm i vue-loader vue-template-compiler -D`将解析转换vue的包安装为开发依赖；

3. 运行`cnpm i style-loader css-loader -D`将解析转换CSS的包安装为开发依赖，因为.vue文件中会写CSS样式；

4. 在`webpack.config.js`中，添加如下`module`规则：

```js
module: {
    rules: [
     { test: /\.css$/, use: ['style-loader', 'css-loader'] },
     { test: /\.vue$/, use: 'vue-loader' }
    ]
}
```

5. 创建`App.js`组件页面：

```

```

6. 创建`main.js`入口文件：

```js
// 导入 Vue 组件
import Vue from 'vue'
// 导入 App组件
import App from './components/App.vue'
// 创建一个 Vue 实例，使用 render 函数，渲染指定的组件
var vm = new Vue({
    el: '#app',
    render: c => c(App)
});
```

##### vue组件由三个部分构成 `template script style`

```vue
login.vue 
<template>
  <div>
    <h1>这是登录组件，使用 .vue 文件定义出来的 --- {{msg}}</h1>
  </div>
</template>  
<script>
export default {
  data() {
    // 注意：组件中的 data 必须是 function
    return {
      msg: "123"
    };
  },
  methods: {
    show() {
      console.log("调用了 login.vue 中的 show 方法");
    }
  }
};
</script>
<style>
</style>
 
main.js
import login from './login.vue'
```

####  export default 和 export的使用方式

> 这是Node 中向外暴露成员的形式：
> module.exports =()
> 在ES6中，也通过规范的形式，规定了ES6中如何导入和导出模块
>
> ES6中导入模块，使用import 模块名称from植块示识符	’import”表示路径’
> 在ES6中，使用export default和export 向外暴露成员：
>
> 在Node中使用
> var名称= require（‘模块标识符’）
> module.exports 和 exports 来暴露成员

```js
test.js 
//第一种
export default{
	name:'zs',
	age:20
}
//第二种
var info = {
    name:'zs',
    age：20
}
export default info
// export default 向外暴露的成员可以使用任意的变量来接收
// 在一个模块中，export default 只允许向外暴露1次
//在一个模块中，可以同时使用export defaplt和export 向外暴露成员  
export var title = '小星星'
// 使用export 向外暴露的成员，只能使用{}的形式来接收，这种形式，叫做[按需导出]
注意，export 可以向外暴露多个成员，同时，如果某些成员，我们在import 的时候，不需要，则可不在{}中定义
注意：使用export 导出的成员，必须严格按照导出时候的名称，来使用（}按需接收：注意：使用export 导出的成员，如果就想换个名称来接收，可以使用as来起别名；
 
main.js 导入
import m,{ title as title123 } from './test.js'
console.log(m)
console.log(title)
```

#### 总结梳理：webpack中如何使用vue：

> 1.安装vue的包：cnpm i vue -S
> 2.由于在webpack中，推荐使用.vue 这个组件模板文件定义组件，所以，需要安装能解析这种文件的loader 
>
> cnpm i vue-1oader vue-template-complier -D
> 3.在main.js 中，导入vue模块
> `import Vue from 'vue'`
> 4.定义一个.vue 结尾的组件，其中，组件有二部分组成：template script style
> 5.使用``import login from '../login.vue'``导入这个组件
> 6、创建Vm的实例var Vm = new Vue（{el：'#app'，render：C => c（ogin）}）
> 7.在页面中创建一个id为app 的div元素，作为我们vm实例要控制的区域；

webpack.config.js

```js
// 由于 webpack 是基于Node进行构建的，所有，webpack的配置文件中，任何合法的Node代码都是支持的
var path = require('path')
// 在内存中，根据指定的模板页面，生成一份内存中的首页，同时自动把打包好的bundle注入到页面底部
// 如果要配置插件，需要在导出的对象中，挂载一个 plugins 节点
var htmlWebpackPlugin = require('html-webpack-plugin')
// 当以命令行形式运行 webpack 或 webpack-dev-server 的时候，工具会发现，我们并没有提供 要打包 的文件的 入口 和 出口文件，此时，他会检查项目根目录中的配置文件，并读取这个文件，就拿到了导出的这个 配置对象，然后根据这个对象，进行打包构建
module.exports = {
  entry: path.join(__dirname, './src/main.js'), // 入口文件
  output: { // 指定输出选项
    path: path.join(__dirname, './dist'), // 输出路径
    filename: 'bundle.js' // 指定输出文件的名称
  },
  plugins: [ // 所有webpack  插件的配置节点
    new htmlWebpackPlugin({
      template: path.join(__dirname, './src/index.html'), // 指定模板文件路径
      filename: 'index.html' // 设置生成的内存页面的名称
    })
  ],
  module: { // 配置所有第三方loader 模块的
    rules: [ // 第三方模块的匹配规则
      { test: /\.css$/, use: ['style-loader', 'css-loader'] }, // 处理 CSS 文件的 loader
      { test: /\.less$/, use: ['style-loader', 'css-loader', 'less-loader'] }, // 处理 less 文件的 loader
      { test: /\.scss$/, use: ['style-loader', 'css-loader', 'sass-loader'] }, // 处理 scss 文件的 loader
      { test: /\.(jpg|png|gif|bmp|jpeg)$/, use: 'url-loader?limit=7631&name=[hash:8]-[name].[ext]' }, // 处理 图片路径的 loader
      // limit 给定的值，是图片的大小，单位是 byte， 如果我们引用的 图片，大于或等于给定的 limit值，则不会被转为base64格式的字符串， 如果 图片小于给定的 limit 值，则会被转为 base64的字符串
      { test: /\.(ttf|eot|svg|woff|woff2)$/, use: 'url-loader' }, // 处理 字体文件的 loader 
      { test: /\.js$/, use: 'babel-loader', exclude: /node_modules/ }, // 配置 Babel 来转换高级的ES语法
      { test: /\.vue$/, use: 'vue-loader' } // 处理 .vue 文件的 loader
    ]
  },
  resolve: {
    alias: { // 修改 Vue 被导入时候的包的路径
      // "vue$": "vue/dist/vue.js"
    }
  }
}
```

#### vue路由

##### 结合webpack使用vue-router

```js
main.js
import Vue from 'vue'
import app from './App.vue'
import Vue from 'vue'
import VueRouter from 'vue-router'
import account from './main/Account.vue'
import goodslist from './main/GoodsList.vue'
//如果在一个模块化工程中使用它，必须要通过Vvue.use（）明确地安装路由功能：
Vue.use(VueRouter)
 
// 创建路由对象
var router = new VueRouter({
    routes:[
        { path:'/account',component:account},
        { path:'/goodslist',component:goodslist}
    ]
})
 
var vm = new Vue({
	el:'#app',
	render:c => c(app),
    router  
})

App.vue
<template>
  <div>
    <h1>这是登录组件，使用 .vue 文件定义出来的 --- {{msg}}</h1>
	
	<router-link to="/account">Account</router-link>
	<router-link to="/goodslist">Goodslist</router-link>
	<router-view></router-view>
  </div>
</template>  
<script>
export default {
  data() {
    // 注意：组件中的 data 必须是 function
    return {
      msg: "123"
    };
  },
  methods: {
    show() {
      console.log("调用了 login.vue 中的 show 方法");
    }
  }
};
 pp这个组件，是通过VM实例的render 函数，渲染出来的，render 函数如果要渲染组件，渲染出来的组件，只能放到e1：#app'所指定的元素中；I
// Account和GoodsList组件，是通过路由匹配监听到的，所以，这两个组件，只能展示到属于路由的<outer-view></router-view>中去
</script>
<style>
</style>
```

```
安装 vue-router
npm i vue-router -S
```

##### webpack实现children子路由

```
// 创建路由对象
import login form './submon/login.vue'
import register form './submon/register'
var router = new VueRouter({
    routes:[
        { path:'/account',component:account,
        	children:[
        		{path:'login',component:login},
        		{path:'register',component:register}
        	]
        },
        { path:'/goodslist',component:goodslist}
    ]
})
```

##### 组件中style标签lang(设置scss或less)属性和scoped(局部作用域的样式  )属性

```vue
.vue 文件

<style> 全局的样式

</style>

<style scoped> 样式应用于当前作用域

</style>

/*普通的style 标签只支持普通的样式，如果想要启用scss 或1ess，需要为sty1e 元素，设置lang属性*/
只要咱们的style标签，是在vue组件中定义的，那么，推荐都为style开启scoped属性

<style lang="scss">

</style>
```

scoped 属性选择器的实现原理

```
样式的scoped 是通过css的属性选择器实现
添加div data-v-53d445f4或者其他属性
```

##### 抽离路由模块

新建router.js 文件

把所有的路由代码复制到router.js 文件

```
// 导入 自定义路由模块
main.js 文件导入
import router from './router.js'
```

## 高级



## 配置

### 安装

- webpack-cli webpack4.x 版本以上要安装webpack-cli 脚手架

```bash
npm init -y
npm i webpack webpack-cli -g // 全局安装
npm i webpack webpack-cli -D // 本地安装
npm i webpack webpack-cli -D  // 安装脚手架工具 安装webpack
```

#### 运行一 命令行  输入完整路径运行 手动

```bash
webpack .\src\main.js -o .\dist\bundle.js  // 运行的第一种方法
```

#### 运行二：配置webpack.config.js 运行 手动

```js
// webpack-dev-server
npm i webpack-dev-server -D

//webpack是基于Node进行构建的，所有，webpack的配置文件中，任何合法的Node代码都是支持的
var path = require('path')
// ES6写法
import $ from jqurey;
module.exports = {
	entry.path.join(_dirname,'./src/main.js'), //输出路径
	output:{
		path:path.join(_dirname,'./dist'),
		filename:'bundle.js' //指定输出文件的名称
	}
}

webpack
```

#### 运行三：配置package.json script 运行 自动运行

```bash
npm i webpack-dev-server -D

script:
"dev": "webpack-dev-server --open --port 3000 --contentBase src --hot"
// --open
// --port 3000
// --contentBase 内容
// --hot
npm run dev
```

webpack-dev-server 中的script

```js
<script src="./bist/bundle.js"/>
<script src="./bundle.js" />
// webpack-dev-server应该导入的是加载到内存中的bundle文件，而不是实际磁盘中的bundle.js 文件    
```

#### 运行四：配置webpack.config.js 运行 自动运行

webpack-dev-server  它是webpack提供的服务器

```js
devServer:{ // 配置dev-server命令参数的第二次形式，相对来说，这种方式麻烦一些
    open:true, //自动打开浏览器
    port:3000,// 设置启动时候的运行端口
    contentBase: 'src'//指定托管的根目录 src 要带 ‘’ 号
    hot:true // 启用热更新 
}
plugins:[ //数组
    new webpack.HotModuleReplacementPlugin();
    //new 一个热更新的模块对象 这是启动更新
]
```

### plugin

#### html-webpack-plugin 配置index主页

不可能每次都去手动复制一个index.html到打包好的dist文件中, 它可以自动添加html文件到dist文件中，同时它会自动添加js文件并带有hash值

```js
npm i html-webpack-plugin -D
// 配置插件，需要在导出的对象中，plugins挂载节点
var htmlWebpackPlugin = require('html-webpack-plugin')

plugins:[
//创建一个在内存中，生成HTML页面的插件
   new htmlWebpackPlugin({
   	template:path.join(_dirname,'./src/index.html',
   	//指定模板页面，会根据指定的页面路径，去生成内存中的页面
   	filename:'index.html' //指定生成的页面的名称
   })
]

npm run dev
```

### loader  

- 导入其他文件 CSS、字体、图片、JS、TS

```js
const path = require('path')
const htmlWebpackPlugin = require('html-webpack-plugin')
import $ from 'jquery' 
import './css/index.css'
import 'boostrap/dist/css/bootstrap.css'
module.exports = {
    entry: path.join(__dirname, './src/main.js'),
    output: {
        path: path.join(__dirname, './dist/'),
        filename: 'bundle.js'
    },
    module: {
        rules: [
            { test: /\.css$/, use: ['style-loader', 'css-loader'] },
            {test:/\.less$/,use:['style-loader','css-loader','less-loader']},
            { test: /\.sass$/, use: ['style-loader', 'css-loader', 'less-loaer', 'sass-loader'] },
            { test: /\.(ttf|eot|svg|woff|woff2)$/, use: 'url-loader' },
            {test:/\.(jpg|png|gif|bmp|jpeg)$/,use:'url-loader?limit=7631$name=[name].[ext]'}
              { test:/\.js$/,use:'babel-loader',exclude:/node_modules/ }
            
        ]
    },
    plugins: [
        new htmlWebpackPlugin({
            template: path.join(__dirname, './src/index.html'),
            filename:'index.html'
        })
    ]

}
```

postcss + autoprefixer 解决兼容问题 目前css兼容性的解决方案，会自动帮我们加入前缀

```js
{ test:/\.css$/,use;:['style-loader','css-loader','less-loader','postcss-loader'] }
```

postcss解决兼容性问题主要靠的其实是它的插件autoprefixer

```js
module.exports = {
    plugins:[
        require('autoprefixer')
    ]
}
```

### 配置文件

#### webpack.config.js 配置文件

- 自动将开发环境使用的webpack的配置文件和生产环境的配置文件分开，将压缩代码，添加hash控制版本等操作放在项目上线时运行，这样避免了在开发阶段打包时间过长的问题。
- webpack.config.js
- webpack.production.config.js

```
package.json 
script
"build":"NODE_ENV=production webpack --config ./webpack.production.config.js --progress"
NODE_ENV=production 就是将运行环境设置成生产环境
webpack --config 就是运行webpack的配置文件
./webpack.production.config.js 是要运行的指定位置的文件，这个路径是相对根目录来说的
--progress 是编译过程显示进程百分比的
```

[webpack.config.js文件配置](https://webpack.docschina.org/configuration/)

```js
const path = require('path')

module.exports = {
    entry: path.join(__dirname, './src/main.js'),
    
    output: {
        path:path.join(__dirname, './dist/'),
        filename:'bundle.js'
    }
}
```

#### `package.json文件详解`

[重新认识 package.json ](https://juejin.im/post/5ebcd8b1e51d454dc20dd8a0)

[npm的package.json中文文档 ](https://github.com/ericdum/mujiang.info/issues/6/)

npm命令安装包并将信息保持到项目的package.json文件

重点: `npm install <package>` 只是下载到本地node_module模块，而不加载到 package.json 文件中

```bash
npm install <package...> --save # 写入 dependencies 属性
npm install <package...> --save-dev # 写入 devDependencies 属性
```

> `devDependencies` (开发环境使用) 与 dependencies(生产环境使用) 的区别
>
> devDependencies：devDependencies 节点下的模块是我们在开发时需要用的，比如项目中使用的 gulp ，压缩css、js的模块。这些模块在我们的项目部署后是不需要的，所以我们可以使用 -save-dev 的形式安装。 指定了项目开发所需要的模块（开发环境使用）
>
> `dependencies`: 字段指定了项目运行所依赖的模块（生产环境使用）
>
> `engines `有时候，新拉一个项目的时候，由于和其他开发使用的 `node` 版本不同，导致会出现很多奇奇怪怪的问题（如某些依赖安装报错、依赖安装完项目跑步起来等）`package.json` 的 `engines` 字段来指定项目 node 版本

- 项目名称、项目构建版本、许可证的定义；
- 依赖定义（包括 `dependencies` 字段，`devDependencies` 字段）；
- 使用`scripts`字段指定运行脚本命令的 `npm` 命令行缩写。

```json
{
  "name": "my-test", # 项目名称
  "version": "1.0.0", # 项目版本（格式：大版本.次要版本.小版本）
  "description": "", # 项目描述
  "main": "index.js", # 定义入口文件 默认index.js
  "scripts": { # 指定运行脚本命令的 npm 命令行缩写 简化终端命令（scripts）
    "test": "echo \"Error: no test specified\" $$ exit 1"
     // "dev":"webpack-dev-server --open --port 3000 --hot" # npm run dev
    //   "start": "node index.js" #npm run start
  },
  "keywords": [], # 关键词
  "author": "", # 作者
  "license": "ISC", # 许可证
  "devDependencies": {
    // 开发环境依赖   npm install 包名 -D
   },
  "dependencies": {
     // 生产环境依赖   npm install 包名 -S
   },
    "optionalDependencies": {
        "gulp": "^3.9.1"
        //（可选阶段的依赖）  npm install 包名 -O
    }
   "engines": {
       "node": ">= 8.16.0" #指定项目 node 版本（engines）
	   "npm": ">= 6.9.0" #指定适用的 npm 版本
   },
    "bin": {
      "my-app-cli": "./bin/cli.js"
    }
}
```

定义项目入口（main）

- `main` 字段是 `package.json` 中的另一种元数据功能，它可以用来指定加载的入口文件。假如你的项目是一个 `npm` 包，当用户安装你的包后，`require('my-module')` 返回的是 `main` 字段中所列出文件的 `module.exports` 属性。
- 当不指定`main` 字段时，默认值是模块根目录下面的`index.js` 文件。

自定义命令（bin）

`bin` 字段用来指定各个内部命令对应的可执行文件的位置。当`package.json` 提供了 `bin` 字段后，即相当于做了一个命令名和本地文件名的映射。

当用户安装带有 `bin` 字段的包时，

- 如果是全局安装，`npm` 将会使用符号链接把这些文件链接到`/use/local/node_modules/.bin/`；
- 如果是本地安装，会链接到`./node_modules/.bin/`。

举个 🌰，如果要使用 `my-app-cli` 作为命令时，可以配置以下 `bin` 字段：

```bash
"bin": {
  "my-app-cli": "./bin/cli.js"
}
```

上面代码指定，`my-app-cli` 命令对应的可执行文件为 `bin` 子目录下的 `cli.js`，因此在安装了 `my-app-cli` 包的项目中，就可以很方便地利用 `npm`执行脚本：

```
"scripts": {
  start: 'node node_modules/.bin/my-app-cli'
}
```

- 咦，怎么看起来和 vue create create-react-app之类的命令不太像？原因：
	- 当需要 `node` 环境时就需要加上 `node` 前缀
	- 如果加上 `node` 前缀，就需要指定 `my-app-cli` 的路径 -> `node_modules/.bin`，否则 `node my-app-cli`会去查找当前路径下的 `my-app-cli.js`，这样肯定是不对。
- 若要实现像 `vue create`/`create-react-app`之类的命令一样简便的方式，则可以在上文提到的 `bin` 子目录下可执行文件`cli.js` 中的第一行写入以下命令：

```bash
#!/use/bin/env node
```

- 这行命令的作用是告诉系统用 `node` 解析，这样命令就可以简写成 `my-app-cli` 了。

## 环境

- css 文件 
	- css less  scss
	- postcss 和 autoprefixer
- js 文件 babel 

### 生产环境

- 压缩js 代码  UglifyJsPlugin
- 拆分文件 就是将原本的依赖文件 vue react 等 第三方依赖 不放到一起打包 

```js
externals:{
	"vue":"Vue",
	"vuex":"vuex"
}

index.html 
// 可以引入对应的CDN资源

// 也可以将node_module中的依赖导出
new CopyWebpackPlugin([// from是要copy的文件，to是生成出来的文件
            { from: "node_modules/react/umd/react.xxx.js", to: "js/react.min.js" },
            { from: "node_modules/react-dom/umd/react-dom.xxx.js", to: "js/react-dom.min.js" }
            { from: "public/favicon.ico", to: "favicon.ico" }
])
// 然后修改index的引入
```

- 拆分css(压缩css到CDN)  将css文件单独拆分出来，这样的好处就是打包的css文件我们可以放到cdn上，然后缓存到浏览器客户端中。这样就尽可能的减小文件的体积，以及不必要的资源重新加载，浪费带宽。
	- 对css进行打包到 cdn 

```js
module.export = {
	module:{
		rules:[
			  {
			  	test: /\.css$/,
                user: ExtractTextPlugin.extract('style-loader',
                'css-loader!postcss-loader') // 这里我目前使用less还没有成功
              }
		]
	},
	postcss: function() {
      return [autoprefixer, cssnext, precss, cssnano]
    },
	plugins:[
		new ExtractTextPlugin('./css/[name].min.css') // 生成到css文件夹下
	]
}
```

- 图片处理 url-loader  'url?limit=8192&name=images/[hash:8].[name].[ext]'
- 浏览器缓存资源
	- 我们的后台会给资源设置Cache-Control: max-age=秒替代，来对资源进行缓存时间的设置，这使得我们在刷新页面之后会去缓存中加载资源，但是存在一个问题，就是，一旦我们更新版本之后，客户没有去清除缓存，同时缓存还没有过期的情况下，就无法加载到最新的资源。这时我们就需要hash值来进行版本控制

```
output: {
        path: __dirname + "/dist",
        filename: "[name][hash].js"
    }
<script type="text/javascript" src="main3d1cb903f77dad5737e9.js"></script> 
```



### 开发环境



## 脚手架



## 面试题

什么是webpack

- 前端项目构建工具 模块打包工具

webpack解决什么问题

- 浏览器不能识别scss less es6 转换为浏览器可以识别的语法
- 减少http的请求次数
- 压缩文件、图片
- 将手动操作转自动操作

webpack四大核心概念

- 入口(entry)、出口(output)、加载器(loader)、插件(plugins)
	- 加载器：加载除了js文件其他文件的功能
	- 插件：处理加载器完成不了的功能，使用插件
