---
title: babel&eslint
categories:
- 前端
tags:
- babel
abbrlink: 19930
---
# Babel

## 教程

- [ ] [Babel 是什么？ · Babel 中文网](https://www.babeljs.cn/docs/)

## 概念

- Babel 是一个广泛的转码器，可以将ES6代码转换为ES5代码，从而在现有的环境执行 
- Javascript 编译器，将ECMAScript 2015+版本的代码转换为向后兼容的JavaScript语法
- ES6的某些语法在浏览器环境甚至在Node.js环境中无法运行
- Babel 是一个编译器（输入源码 => 输出编译后的代码）。就像其他编译器一样，编译过程分为三个阶段：解析、转换和打印输出。

## 配置

Node安装方式
- core `@babel/core` Babel 的核心功能包含在 [@babel/core](https://www.babeljs.cn/docs/babel-core) 模块中
- cli `@babel/cli` 命令行
- preset `@babel/preset-env`

```
npm init -y  
```
全局安装：**不安装在全局**

> 如果安装在全局，那意味着项目要运行，全局环境必须有bable，也就是说项目产生了对环境的依赖。另一方面，这样做也无法支持不同项目使用不同版本的babel。
```bash
npm install -g @babel/core @babel/cli @babel/preset-env
babel --version
```
本地安装
```bash
npm install --save-dev @babel/core @babel/cli @babel/preset-env
```
浏览器环境

- Babel 也可以用于浏览器环境，使用[@babel/standalone](https://babeljs.io/docs/en/next/babel-standalone.html)模块提供的浏览器版本，将其插入网页，添加Babel.js CDN 再添加`text/babel`

```
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
<script type="text/babel">
// Your ES6 code
</script>
```

`presets`字段设定转码规则，官方提供以下的规则集

```bash
// 最新转码规则
npm i --save-dev @babel/preset-env
// react 转码规则
npm i --save-dev @babel/preset-react
// 安装后将转码规则添加到.babelrc文件中
{
	"presets":[
		"@babel/env",
		"@babel/preset-react"
	]
}
```

`cli`命令行转码

```bash
$ npm i --save-dev @babel/cli
```

使用

```js
babel example.js
// 一个文件
babel example.js -o compiled.js
// 整个目录
babel src-d lib 
// -s 参数生成source map文件
babel src -d lib -s
```

`babel-node` ES6 REPL环境

- 提供一个支持 ES6 的 REPL 环境。它支持 Node 的 REPL 环境的所有功能，而且可以直接运行 ES6 代码。

```bash
npm install --save-dev @babel/node
// 可以直接运行ES6脚本
babel-node es6.js
```

`@babel/register`  对`require`引入的文件进行转码

- `@babel/register`模块改写`require`命令，为它加上一个钩子。此后，每当使用`require`加载`.js`、`.jsx`、`.es`和`.es6`后缀名的文件，就会先用 Babel 进行转码。
- `@babel/register`只会对`require`命令加载的文件转码，而不会对当前文件转码。另外，由于它是实时转码，所以只适合在开发环境使用。

```js
npm i --save-dev @babel/register
// index.js 
require('@babel/register')
require('./es.js')
```

配置文件

- `.babelrc`   设置转码规则和插件 需要 `v7.8.0` 或更高版本）
- `babel.config.json `和 ``.babelrc.json``
- `babel.config.js`
- `package.json` 中的配置信息作为 `babel` 键（key）的值添加到 `package.json` 文件中
- 用 JavaScript 编写 `babel.config.json` 和 `.babelrc.json`文件

```json
// .babelrc
{
	"presets":[],
    "plugins":[]
}
```

```js
const presets = [];
const plugins = [];
module.exports = { presets,plugins };
```

```js
// 安装转码器
// npm install --save-dev babel-preset-2015
{
    "presets":["es2015"], // presets字段设置的就是转码规则
    "plugins":[] // plugins是设置的babel的插件
}
```
```json
// `babel.config.json `需要 `v7.8.0` 或更高版本）
{
	"presets":[
		"@babel/env",
		{
			"targets":{
				"edge":"17",
				"firefox":"60",
				"chrome":"67",
                "safari":"11.1"
			},
            "useBuiltIns":"usage",
            "corejs":"3.6.5"
		}
	]
}
const presets = [];
const plugins = [];
module.exports = { presets,plugins };
```
```js
const presets = [];
const plugins = [];
if(process.env["ENV"] == "prood"){
	plugins.push(...);
}
module.exports = {presets,plugins}
```
```js
// 旧版本babel `babel.config.js`
const presets = [
    [
        "@babel/env",
        {
             targets: {
                edge: "17",
                firefox: "60",
                chrome: "67",
                safari: "11.1",
              },
             useBuiltIns:"usage", // 加载上面所提到的最后一个优化措施，也就是只包含你所需要的 polyfill
             corejs:"3.6.4"
        },
    ],
];
module.exports = { presets };
```
```json
// `package.json` 中的babel
{
  "name": "my-package",
  "version": "1.0.0",
  "babel": {
    "presets": [ ... ],
    "plugins": [ ... ],
  }
}
```

自定义脚本
```json
{
  "devDependencies": {
    "babel-cli": "^6.26.0",
    "babel-preset-es2015": "^6.24.1"
  },
  "scripts":{
      "build":"babel demo.js --out-file bunder.js"
      //     "build":"babel src -d dist"
  }
}
// npm run build
```
三个功能库
>  `@babel/cli` 从终端运行 Babel，利用 `@babel/polyfill` 来模拟所有新的 JavaScript 功能，而 `env` preset 只对我们所使用的并且目标浏览器中缺失的功能进行代码转换和加载 polyfill。
core 核心库 `@babel/core`
`@babel/core` 核心代码

```bash
npm install --save-dev @babel/core
```
`@babel/cli` cli 命令行工具 

```bash
npm instll --save-dev @babel/core @babel/cli
./node_modules/.bin/babel src --out-dir lib
// 代码转换功能,把每一个文件输出到lib目录下
babel --plugins @babel/plugin-transform-arrow-functions script.js
```
preset `@babel/preset-env`

一组预先设定的插件

插件和预设 presets 和 plugins

```js
// .babelrc
{
	"presets":[],
    "plugins":[]
}
```

- 代码转换功能以插件的形式出现，插件是小型的 JavaScript 程序，用于指导 Babel 如何对代码进行转换。你甚至可以编写自己的插件将你所需要的任何代码转换功能应用到你的代码上。
```bash
npm install --save-dev @babel/plugin-transform-arrow-functions
./node_modules/.bin/babel src --out-dir lib --plugins=@babel/plugin-transform-arrow-functions
const fn = () => 1;
var fn = function fn(){
	reutrn 1;
}
```
- 就像插件一样，你也可以根据自己所需要的插件组合创建一个自己的 preset 并将其分享出去。J对于当前的用例而言，我们可以使用一个名称为 `env` 的 preset。名为 `env` 的 preset 只会为目标浏览器中没有的功能加载转换插件
```bash
npm install --save-dev @babel/preset-env
./node_modules/.bin/babel src --out-dir lib --presets=@babel/env
```
Polyfill 填充物

- Babel 默认只转换新的JavaScript句法（Syntax）,而不转换新的API 。比如`Iterator`、`Generator`、`Set`、`Map`、`Proxy`、`Reflect`、`Symbol`、`Promise`等全局对象，以及一些定义在全局对象上的方法（比如`Object.assign`）都不会转码。

```bash
npm install --sava @babel/polyfill
```

- 从 Babel 7.4.0 版本开始，这个软件包已经不建议使用了，建议直接包含 `core-js/stable` （用于模拟 ECMAScript 的功能）和 `regenerator-runtime/runtime` （需要使用转译后的生成器函数）：

```js
npm install --save-dev core-js regenerator-runtime
import "core-js/stable";
import "regenerator-runtime/runtime";
// 或者
require('core-js');
require('regenerator-runtime/runtime);
```
- Babel 默认不转码的 API 非常多，详细清单可以查看`babel-plugin-transform-runtime`模块的[definitions.js](https://github.com/babel/babel/blob/master/packages/babel-plugin-transform-runtime/src/runtime-corejs3-definitions.js)文件

# ESLint

代码检查工具

禁用ESLint
·`package.json`
```josn
  "eslintConfig": {
    "root": true,
    "env": {
      "node": true,
      "useeslint":false  // 禁用Eslint
    },
    "extends": [
      "plugin:vue/essential",
      "eslint:recommended",
      "@vue/prettier"
    ],
    "parserOptions": {
      "parser": "babel-eslint"
    },
    "rules": {
      "no-console": "off"
    }
  },
```
[ESLint - Pluggable JavaScript linter - ESLint中文](http://eslint.cn/)
- 可组装的JavaScript和JSX检查工具
- 一个插件化的javascript代码检测工具
- ESLint 使用 [Espree](https://github.com/eslint/espree) 解析 JavaScript。
- ESLint 使用 AST 去分析代码中的模式
- ESLint 是完全插件化的。每一个规则都是一个插件并且你可以在运行时添加更多的规则。
## 配置
```
package.json
"script":{
	"eslint":"eslint ./src/*.js"
}
yarn eslint
```
```bash
yarn add -D eslint
npm install eslint --save-dev
./node_modules/.bin/eslint --init
./node_modules/.bin/eslint yourfile.js
npm install eslint --global
// 设置配置文件
npx eslint --init
npx eslint main.js //单文件文件
npx eslint ./src/*.js
```
配置文件`eslintrc` 、`.eslintrc.json`
```json
{
	“parserOptions”:{
        "ecmaVersion":6,
        "sourceType":"module",
        "ecmaFeatures":{
            "jsx":true
        }
    }
    "rules":{
        "semi":["error","always"],
        "quotes":["error","double"]
        // semi 错误级别 quotes   // 规则名称 
        // off 关闭规则 warn 规则视为警告 error错误
    }
}
```
## 规则
## 集成
# Prettier

[Prettier首页、文档和下载 - 前端代码格式化工具 - OSCHINA - 中文开源技术交流社区](https://www.oschina.net/p/prettier?hmsr=aladdin1e1)

JSX

- JSX是JavaScript XML,是React提供的Syntax Sugar, 能让我们可以在JS中写html标记语言。
JSX 是一种JavaScript的语法扩展，运用于React架构，其格式比较像模板语言，但事实上完全是在JavaScript内部实现的。元素是构成React应用的最小单位，JSX就是用来声明React当中的元素，React使用JSX来描述用户界面

