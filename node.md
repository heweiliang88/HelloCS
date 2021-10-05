---
title: node
categories:
- 前端
  - node
tags:
  - 前端
  - node
abbrlink: 7878

---

# node

> [Node.js入门](https://www.jqhtml.com/42590.html)
>
> [Node.js 中文网](http://nodejs.cn/)
>
> [API 文档 | Node.js 中文网](http://nodejs.cn/api/)
>
> 实战
>
> [Node - 从0基础到实战企业官网](https://juejin.cn/post/6844903745755545614#heading-5)
>
> [NodeJS全栈开发一个功能完善的Express项目（附完整源码）](https://juejin.cn/post/6844904198551666701#heading-34)

## 命令行

- `.` 表示当前目录
- `..` 表示上级目录
- dir 列出所有文件 cd 进入目录 md 创建文件夹 rd 删除文件夹
- 环境变量 （window系统中的变量） 命令行找文件 ==> 当前目录下寻找文件程序 ==> 环境变量path的路径下寻找 
	- 将经常需要访问的程序和文件的路径添加到path中，就可以在任意位置访问这些文件和抽象

## 插件

- node debug 
- search node_moules
- node snipptes

### Node Debug

> This extension is bundled with Visual Studio Code and together with **Node Debug (legacy)** forms the [Node.js](https://nodejs.org/) debugging experience.
>
> **Node Debug** is the debugger for Node.js versions >= 8.0.
>
> See a general overview of debugging in VS Code [here](https://code.visualstudio.com/docs/editor/debugging).
>
> Documentation for Node.js specific debugging can be found [here](https://code.visualstudio.com/docs/nodejs/nodejs-debugging).
>
> Please submit bugs and feature requests to the [VS Code repository](https://github.com/microsoft/vscode/issues).
>
> License
>
> Copyright (c) Microsoft Corporation. All rights reserved.
>
> Licensed under the [MIT](https://github.com/Microsoft/vscode-node-debug2/blob/master/LICENSE.txt) License.

### Search node_modules

> Simple plugin for VS Code that allows you to quickly navigate the file inside your project's `node_modules` directory.
>
> Chances are you have the `node_modules` folder excluded from the built-in search in VS Code, which means if you want to open and/or edit a file inside `node_modules`, you can have to find it manually, which can be annoying when your `node_modules` folder is large.
>
> Features
>
> - Quickly navigate and open files in `node_modules` by traversing the folder tree.
>
>  Settings
>
> - `search-node-modules.useLastFolder`: Default to folder of last opened file when searching (defaults to `false`).
> - `search-node-modules.path`: Relative path to node_modules folder (defaults to `node_modules`).
>
> Extension Packs
>
> - [Node.js Extension Pack](https://marketplace.visualstudio.com/items?itemName=waderyan.nodejs-extension-pack)
>
> Links
>
> - Visual Studio Marketplace: https://marketplace.visualstudio.com/items?itemName=jasonnutter.search-node-modules
> - Repo: https://github.com/jasonnutter/vscode-search-node-modules
> - Known Issues: https://github.com/jasonnutter/vscode-search-node-modules/issues
> - Change Log: https://github.com/jasonnutter/vscode-search-node-modules/blob/master/CHANGELOG.md

### Node Exec

### Node Snippets

> Features
>
> A collection of NodeJS snippets
>
> The following commands are available:
>
> - `node-express`, creates an express server
> - `node-express-get`, creates GET route
> - `node-express-get-params`, creates a GET route and shows how to access parameters
> - `node-express-post`, creates a POST route
> - `node-express-post-params`, creates a POST route and shows how to access the body
> - `node-express-post-params-alt`, creates a POST route, shows how to access the body, works for express 4.16 and above
> - `node-express-middleware-logger`, creates an example middleware
> - `node-express-middleware-error`, creates an error handling middleware
> - `node-http-server`, creates a simple HTTP server
> - `node-file-read-sync`, reads a file synchronously
> - `node-file-read-async`, reads a file asynchronously, with a callback
> - `node-event-emitter`, creates an event emitter, emit events and shows to subscribe to said event
> - `node-promise-create`, creates a Promise
> - `node-promise-shorthand`, creates a Promises using the static methods `resolve()` and `reject()`
> - `node-promise-all`, resolves a list of Promises using the `Promise.all([])` method
> - `node-async-await`, using async/await
> - `node-express-schema-validation`, adding schema validation for express, read more about the usage of schema validation with `Joi` at https://github.com/hapijs/joi

## 安装

### node.js 安装

- 第一种直接安装
- [第二种nvm node版本管理工具（推荐）](https://github.com/coreybutler/nvm-windows/releases)
- [windows下安装nvm及nrm | fatboa](https://cloudintheking.github.io/2018/07/12/windows%E4%B8%8B%E5%AE%89%E8%A3%85nvm%E5%8F%8Anrm/)

#### settings.txt文件的配置

```txt
root: D:\SoftWare\NodeJs\nvm // nvm node版本控制的软件的位置
path: D:\SoftWare\NodeJs\nodejs //当前使用的node的位置
arch: 64 
proxy: none
node_mirror: http://npm.taobao.org/mirrors/node/
npm_mirror: https://npm.taobao.org/mirrors/npm/
```

#### 环境变量的配置

配置nvm和Node.js环境变量

+ NVM_HOME:D:\SoftWare\NodeJs\nvm （node版本控制软件nvm 的位置）
+ NVM_SYMLINK: D:\SoftWare\NodeJs\nodejs  （node.js的位置 符号链接）

> 环境变量的作用path 路径 可以在终端使用全局的作用命令

nodemon

[nodemon使用简介 - 掘金](https://juejin.im/post/5b5005f7f265da0f66401fe7)

### 安装错误

> 解决方法一：
>
> nvm不能安装在programs files，因为空格问题
> exit status 1: ‘C:\Program’ �����ڲ����ⲿ���Ҳ���ǿ����еĳ���
> ���������ļ���
>
> 可以通过在nvm根目录将program files替换为 progra~1，如下：
> root: C:\progra~1\nvm
> path: C:\progra~1\nodejs
>
> 解决方法二：
>
> 更换没有空格的安装目录

### nvm常用的命令

- nvm list 查看当前安装的Node.js所有版本
- nvm install 版本号 安装指定版本的Node.js nvm install latest 最新版本  nvm install node@13.5.0
- nvm uninstall 版本号 卸载指定版本的Node.js
- nvm use 版本号 选择指定版本的Node.js nvm use node12.16.3

[nodejs/node: Node.js JavaScript runtime](https://github.com/nodejs/node)

#### node 版本

[以往的版本 | Node.js](https://nodejs.org/zh-cn/download/releases/)

[(...) 版本命名及限定规则详解 - 个人文章 - SegmentFault 思否](https://segmentfault.com/a/1190000011368506) 

> 语义化版本命名规则
>
> [name].x.y.z-[state]
>
> x (主版本号(major))，y(次版本号(minor))，z(修订号(patch))非负整数
>
> - `0.y.z` 表示开发阶段，一切可能随时改变，非稳定版。
> - `1.0.0` 界定此版本为初始稳定版，后面的一切更新都基于此版本进行修改。
> - `a(α或a	alpha 版),b（β或b	beta 版）,rc（rc	Release Candidate）β或b	beta 版` 分别表示 内测,公测,发行状态

### node.js 安装

- 第一种直接安装
- 第二种nvm node版本管理工具

#### settings.txt文件的配置

```txt
root: D:\SoftWare\NodeJs\nvm // nvm node版本控制的软件的位置
path: D:\SoftWare\NodeJs\nodejs //当前使用的node的位置
arch: 64 
proxy: none
node_mirror: http://npm.taobao.org/mirrors/node/
npm_mirror: https://npm.taobao.org/mirrors/npm/
```

#### 环境变量的配置

配置nvm和Node.js环境变量

+ NVM_HOME:D:\SoftWare\NodeJs\nvm 
+ NVM_SYMLINK: D:\SoftWare\NodeJs\nodejs 

> nvm不能安装在programs files，因为空格问题，非常不爽
> exit status 1: ‘C:\Program’ �����ڲ����ⲿ���Ҳ���ǿ����еĳ���
> ���������ļ���
>
> 可以通过在nvm根目录将program files替换为 progra~1，如下：
> root: C:\progra~1\nvm
> path: C:\progra~1\nodejs

### nvm常用的命令

- nvm list 查看当前安装的Node.js所有版本
- nvm install 版本号 安装指定版本的Node.js nvm install latest 最新版本
- nvm uninstall 版本号 卸载指定版本的Node.js
- nvm use 版本号 选择指定版本的Node.js

cnpm、nrm、yarn、node

#### node.js版本命名规则

浏览器的内核包括两部分核心：

1. DOM渲染引擎
2. JS解析引擎

node.js使JavaScript不只是运行在浏览器

js运行在浏览器中的内核中的js引擎内部

基于Node.js 和第三方工具electron可以开发桌面应用程序

REPL read-eval-print-loop 读取代码-执行-打印结果

在REPL 环境中，

`_`表示最后一次执行的结果

.exit 退出REPL 环境

## 基础

### Node.js的诞生

- 2008年
- Ryan Dahl的目标：创建一个易扩展、适用于现代Web应用通信的服务器平台
- Node.js 是一个能够在服务器端运行JavaScript的开放源代码、跨平台JavaScript运行环境
- Node处理请求时是单线程，后台拥有一个I/O形线程池 

### 进程与线程

- 进程
- 线程
	- 单线程
	- 多线程

### Web开发概述

- Node.js服务器模型与 php服务器模型的区别

![](https://i.loli.net/2020/05/01/XChWwNZLqicjGER.png)

### 主要应用领域

- RESTFul API
- 实时通信：如消息推送等
- 高并发
- I/O阻塞

### 生态圈

- 以NPM为中心

项目

- MySQL 连接

- jwt-token认证

- md5 加密

- 中间件路由模块

- 异常错误处理

- 跨域配置

- 自动重启


###  知名度较高的Node.js开源项目

express、PM2、iade、socket.io、mongoose、mocha

###### IO.js

- Joyent的目标：兼容性、性能
- 社区：New features
- IO.js：A friendly fork of Node.js with an open governance model
- 现状：IO.js的发展速度，成为了有史以来成长最快的开源项目
- 关系：全面兼容，二者依然有可能合并

### Node.js与JavaScript的关系

#### Node.js的特点

Node.js可以用来做什么？

- 具有复杂逻辑的动态网站 
- WebSocket服务器 
- 命令行工具 
- 带有图形界面的本地应用程序 
- Web服务API REST
- 实时多人运行
- 后端的Web服务、例如跨域、服务器端的请求
- 基于Web的应用
- 多客户端的通信，如即时通信
- 渲染页面处理高并发请求

| 浏览器  | 内核    |
| ------- | ------- |
| IE      | Trident |
| FireFox | Gecko   |
| Chrome  | WebKit  |
| Safari  | WebKit  |
| Opera   | Presto  |
| Edge    | Chakra  |

>Node.js 是一种建立在Google Chrome’s v8 engine上的 non-blocking (非阻塞）, event-driven （基于事件的） I/O平台. 
>Node.js平台使用的开发语言是JavaScript，平台提供了操作系统低层的API，方便做服务器端编程，具体包括文件操作、进程操作、通信操作等系统模块
>
>- 事件驱动
>- 非阻塞
>- 异步I/O模型

## 内置

Node 是对ES标准的一个实现，Node也是一个JS引擎

Node可以使用所有内建对象

- String Number Boolean Math Date RegExp Functin Object Array
- 不能使用 BOM和DOM
- 可以使用console 和 setTimeout() 和 setInterval()

### assert断言

### buffer 缓冲区

> Buffer对象是Node`处理二进制数据`的一个接口。它是Node原生提供的全局对象，可以直接使用，不需要require(‘buffer’)。

- 实例化 构造方法
	+ Buffer.from(array)
	+ Buffer.from(string)
	+ Buffer.alloc(size)
- 功能方法 静态方法
	+ Buffer.isEncoding() 判断是否支持该编码
	+ Buffer.isBuffer() 判断是否为Buffer
	+ Buffer.byteLength() 返回指定编码的字节长度，默认utf8
	+ Buffer.concat() 将一组Buffer对象合并为一个Buffer对象
- 实例方法
	+ write() 向buffer对象中写入内容
	+ slice() 截取新的buffer对象
	+ toString() 把buf对象转成字符串
	+ toJson() 把buf对象转成json形式的字符串

```js
Global.Buffer


//实例化buf对象
let buf = new Buffer(5) // 不推荐使用
let buf = Buffer.alloc(5)
conole.log(buf);

// 字符=》16 进制
let buf = Buffer.form('hello');
let buf = Buffer.form('hello'，’utf-8‘);// 默认编码 utf-8
console.log(buf)
let buf = Buffer.form([0x62,0x75]);// 16进制
console.log(buf)
//静态方法
console.log(Buffer.isEncoding('utf-8'))
console.log(Buffer.isEncoding('base64'))

let buf = Buffer.from('hello');
console.log(Buffer.isBuffer(buf));
console.log(Buffer.isBuffer({}));

let buf = Buffer.from('hello');//默认 utf-8 三个字节 == 一个汉字
console.log(Buffer.byteLength('aasdf'));// 字节长度，不是字符长度

let buf1 = Buffer.alloc(3);
let buf2 = Buffer.alloc(5);
let buf3 = Buffer.concat([buf1,buf2]);
console.log(Buffer.byteLength(buf3)) // 8
console.log(buf3.toString())


+ write() 向buffer对象中写入内容

+ toString() 把buf对象转成字符串
+ toJson() 把buf对象转成json形式的字符串

---------------
实例方法
buf.write(string[, offset[, length]][, encoding])

write() 向Buffer中写入内容
let buf = Buffer.alloc(5);
buf,write('hello')
console.log(buf)

buf,write('hello',2，2) //第二个开始写 第三个参数 写入长度多少个字体
console.log(buf)


+ slice() 截取新的buffer对象 buf.slice([start[, end]])
let buf = Buffer.from('hello');
let buf1 = buf.slice(2,4);// 第一个参数 start 2 - 4 end
console.log(buf === buf1)
console.log(buf1.toString())


toJson() // 把buf对象转为 不需要显式调用，当JSON .stringify方法调用的时候toJSON方法
buf.toJSON()
Returns a JSON representation of buf. JSON.stringify() implicitly calls this function when stringifying a Buffer instance.

const buf = Buffer.from([0x1, 0x2, 0x3, 0x4, 0x5]);
const json = JSON.stringify(buf);

console.log(json);
// Prints: {"type":"Buffer","data":[1,2,3,4,5]}
const copy = JSON.parse(json, (key, value) => {
  return value && value.type === 'Buffer' ?
    Buffer.from(value) :
    value;
});
console.log(copy);
// Prints: <Buffer 01 02 03 04 05>
```

Buffer本质上是一个字节数组

1. 构造函数
2. 静态方法
3. 实例方法

- JSON
- AJAX 
- 正则表达式
- 同步和异步

核心模块API  Buffer // path // fs

### child_process 子进程



### cluster 集群



### console 控制台



### crypto 加密



### debugger调试器





### dns 域名服务器



### domain 域



### error 错误





### path 路径

- 路径基本操作API

path

```js
const path = require('path')
path
// 路径
获取路径的最后一部分
path.basename(path[, ext])
// linux的
path.basename('/foo/bar/baz/asdf/quux.html');
// Returns: 'quux.html'

path.basename('/foo/bar/baz/asdf/quux.html', '.html');
// Returns: 'quux'
获取路径
console.log(__dirname);
console.log(path.dirname('/foo/bar/baz/asdf/quux.html'))
获取扩展名称
path.extname(path)
path.extname('index.html');
// Returns: '.html'

path.extname('index.coffee.md');
// Returns: '.md'

path.extname('index.');
// Returns: '.'

path.extname('index');
// Returns: ''

path.extname('.index');
// Returns: ''

path.extname('.index.md');
// Returns: '.md

path.isAbsolute(path)



路径格式化处理
path.format(pathObject) obj -> string

let path1 = path.format({
  dir: 'C:\\path\\dir',
  base: 'file.txt'
});
console.log(path1)
// Returns: 'C:\\path\\dir\\file.txt'

path.parse(path) string -> obj

let obj = path.parse('C:\\path\\dir\\file.txt');
// Returns:
// { root: 'C:\\',
//   dir: 'C:\\path\\dir',
//   base: 'file.txt',
//   ext: '.txt',
//   name: 'file' }
console.log(obj.base);

path.isAbsolute(path)
path.isAbsolute('//server');    // true
path.isAbsolute('\\\\server');  // true
path.isAbsolute('C:/foo/..');   // true
path.isAbsolute('C:\\foo\\..'); // true
path.isAbsolute('bar\\baz');    // false
path.isAbsolute('bar/baz');     // false
path.isAbsolute('.');           // false

path.join([...paths]) 拼接路径 ../表示上层路径 .表示当前路径，在连接路径的时候会格式化

path.join('/foo', 'bar', 'baz/asdf', 'quux', '..');
// Returns: '/foo/bar/baz/asdf'

path.join('foo', {}, 'bar');
// Throws 'TypeError: Path must be a string. Received {}'


path.normalize(path)

path.normalize('/foo/bar//baz/asdf/quux/..');
// Returns: '/foo/bar/baz/asdf'
path.normalize('C:\\temp\\\\foo\\bar\\..\\');
// Returns: 'C:\\temp\\foo\\'
path.win32.normalize('C:////temp\\\\/\\/\\/foo/bar');
// Returns: 'C:\\temp\\foo\\bar'

path.relative(from, to)
path.relative('/data/orandea/test/aaa', '/data/orandea/impl/bbb');
// Returns: '../../impl/bbb'

path.relative('C:\\orandea\\test\\aaa', 'C:\\orandea\\impl\\bbb');
// Returns: '..\\..\\impl\\bbb'


path.resolve([...paths])

path.resolve('/foo/bar', './baz');
// Returns: '/foo/bar/baz'

path.resolve('/foo/bar', '/tmp/file/');
// Returns: '/tmp/file'

path.resolve('wwwroot', 'static_files/png/', '../gif/image.gif');
// If the current working directory is /home/myself/node,
// this returns '/home/myself/node/wwwroot/static_files/gif/image.gif'


两个特殊属性
cosole.log(path.delimiter);// 表示路径分隔符（window是 \ Linux 是 /）
console.log(path.sep);
// 环境变量分隔符（Windows中使用；linux中使用；）
```

异步I/O input output输入输出 

1. 文件操作 文件读写操作
2. 网络操作 网络的请求响应处理

 异步处理

在浏览器中也存在异步操作

1. 定时任务

2. 事件处理

3. Ajax回调处理


js 的运行时是单线程

引入事件队列机制

Node.js中的事件模型与浏览器中的事件模型类似

单线程 + 事件队列

Node.js中异步执行的任务

1. 文件I/O
2. 网络I/O

基于回调函数的

### fs 文件系统

- 文件信息获取
- 读文件操作
- 写文件操作

```js
fs.writeFile(file, data[, options], callback)

fs.writeFileSync(file, data[, options])

const fs = require('fs');
const path = require('path')

const data = new Uint8Array(Buffer.from('Hello Node.js'));
fs.writeFile('message.txt', data, (err) => {
  if (err) throw err;
  console.log('The file has been saved!');
});

// 异步
let strpath = path.join(__dirname,'data.txt');
fs.writeFile(strpath,'helloasdfasdf',’utf8‘,(err)=>{
    if(!err){
	    console.log('写入成功')
    }
});

let buf = Buffer.from('hi');
fs.writeFile(strpath,buf,'utf8',(err)=>{
   if(!err){
       console.log('文件写入成功');
   } 
});


fs.writeFileSync(strpath, 'asdfasdfsadfasdf','utf8');
// utf-8默认可以不写

```

- 目录操作一（处理内容量比较少的文件） 全部加载到内存

创建

fs.mkdir(path[,mode],callback)

fs.mkdirSync(path[,mode])

```
const path = require('path')
const fs = require('fs')
fs.mkdir(path.join(_dirname,'abc'),(err)=>{
	console.log(err);
})；
fs.mkdirSync(path.join(_dirname,'abc'));
```

删除目录

```js
fs.rmdir(path,callback)
fs.rmdirSync(path)
fs.rmdir(path.join(__dirname,'asdf'),(err)=>{
    console.log(err);
})
//同步 
fs.rmdirSync(path.join(__dirname,'asdf'));
```



读取目录

```js
fs.readdir(__dirname,(err,files)=>{
	files.forEach((item,inde)=>{
	 fs.stat(path.join(__dirname,item),(err,stat)=>{
	 	// 判断是不是目录还是文件
         if(stat.isFile()){
	 		console.log(item,'文件')
	 	}else if (stat.isDirectory()){
	 		console.log(item,'目录')
	 	})
	 });
	});
});

let files = fs.readdirSync(__dirname);
files.forEach((item,inde)=>{
    fs.stat(path.join(__dirname,item),(err,stat)=>{
        // 判断是不是目录还是文件
        if(stat.isFile()){
            console.log(item,'文件')
        }else if (stat.isDirectory()){
            console.log(item,'目录')
        })
    });
});

```



目录操作2 内容量多 大文件操作 (流式操作)

```js
fs.createReadStream(path[,options])fs.createWriteStream(path[,options]) const path = require('path');const fs = require('fs');let spath = path.join(__dirname,'../03-source','file.zip');let dpath = path.join('文件\\路\\径','文件名称 file.zip')let readStream = fs.cteateReadStream(spath);let writeStream = fs.createWriteStream(dpath);// 基于事件的处理方式 data 数据读取一部分 end 完成方法一let num = 1;readStream.on('data',(chunk)=>{    num++;    writeStream.write(chunk);});readStream.on('end',()=>{    console.log('文件处理完成'+num)})// pipe的作用直接把输入流和输出流 方法二readStream.pipe(writeStream);方法三fs.cteateReadStream(spath).pipe(fs.createWriteStream(dpath))
```





异步 和 同步

```html
异步fs.stat(path,callback);console.log('1')文件操作cons fs = require('fs');fs.stat('./data.ext',(err,stat)=>{	// 一般回调函数的第一个参数是错误对象，如果err为null,表示没有错误，否则表示报错了	if(errr) return;	//console.log(err);	if(stat.isFile()){		console.log('文件');	}else if(stat.isDirectory){		console,log('目录');	}	console.log(stat);console.log('2')}); //加入到事件队列console.log('3')1 -> 3  -> 2stat方法属性atime 文件访问时间ctime 文件的状态信息反生变化的时间(比如文件的权限)mtime 文件数据发生改变的时间birthtime 文件创建的时间同步操作console.log('1')fs.statSync(path)let ret = fs.statSync('./data.txt');console.log(ret);console.log('2')1 , 2
```

文件操作案例

初始化目录结构

```js
const path = require('path')const fs = require('fs')//目录位置let root = 'C:\\User\\www';let fileContent = `<!DOCTYPE html><html lang="en"><head>    <meta charset="UTF-8">    <meta name="viewport" content="width=device-width, initial-scale=1.0">    <title>Document</title></head><body>    </body></html>`初始化数据let initDate = {    	projectName :'mydemo',    	data:[{            name:'img',            type:'dir'        },        {            name:'css',            type:'dir'        },              {            name:'js',            type:'dir'        },         {            name:'index.html',            type:'file'        },        ]}创建目录跟路径fs.mkdir(path.join(root,initData.projectName),(err)=>{    if(err) return;    // 创建子目录和文件    initData.data.forEach((item)=>{        if(item.type  == 'dir'){            //创建子目录		  	fs.mkdirSync(path.join(root,initData.projectName,item.name)        }else if(item.type == 'file'){             //创建模板文件      		fs.writeFileSync(path.join(root,initData.projectName,item.name),fileContent); 		 } 	})})
```



文件信息获取

读文件操作

```js
const fs = require('fs');const path = require('path'); //path//fs.readFile(file[,options],callback)let strpath = path.join(_dirname,'data.txt')fs.readFile(strpath,(err,data)=>{	if(err) return;	console.log(data.toString()); //Buffer});//第二种方法 // 如果有第二个参数并且是编码，那么回调函数函数获取到的数据就是字符串//如果没有第二个参数，那么得到的就是Buffer实例对象// 异步 回调函数fs.readFile(strpath,‘utf8’，(err,data)=>{	if(err) return;	console.log(data; //Buffer});// 同步操作 返回值let ret = fs.readFileSync(strpath,'utf8');console.log(ret);
```

### http 超文本传输协议

服务器端模块化

不存在浏览器的window对象 ==> 

全局成员概述 Global Objects

 _filename 包含文件名的全路径

_dirname	文件的路径（不包含文件名称）

```js
const http = require('http')http.createServer((req, res) => {    // // 设置 HTTP 头部，状态码是 200，文件类型是 html，字符集是 utf8    res.writeHead(200, {        "Content-Type": "text/html;charset=UTF-8"    })    res.write('<h1 style="text-align:center">Hello HTTP</h1>')    res.end()}).listen(4000);
```

定时函数

​	var timer = etTimeout(function(){

},1000);

clearTimeout(timer);

```js
var timer = etTimeout(function(){	consloe.log('sadfasddf')},1000);setTimeout(function(){	clearTimeout(timer);},2000)global.console.log('asdfasdfasdf')
```

### process 进程

process.argv 是一个数组，默认情况下，前两项数据分别是 Node.js 环境的路径 当前执行的js文件的全路径，

从第三个参数起，接收命令行的参数

```
node 文件,js 123 234234 234
```

```
console.log(process.arch)
```

exports  // modules  require 模块化 

模块化开发

传统非模块化开发缺点

1. 命名冲突
2. 文件依赖

前端标准的模块化规范 异步

1. AMD -= requiresjs
2. CMS - seajs

服务器端标准的模块化规范 同步

1. CommonJS - Node.js

模块化相关的规则

1. 如何定义模块：一个js文件就是一个模块，模块内部的成员都是相互独立
2. 模块成员的导入和导出

文件加载

导出模块成员

```js
var sum = function(a,b){ return }//导出模块成员exports.sum = sum;//导出模块成员的第二种方式module.exports = sum;// 第三种方法 很少用var flag = 100;global.flag = flag
```

已经加载的模块会缓存，多次加载的文件会自会加载一次

引入模块

```
./ 当前路径下var module = require('./03.js');var module = require('./03'); 后缀可以省略 模块文件的后缀3种情况 .js .json 
```

- 服务器端模块化规范CommonJS与实现Node.js
- 模块导出与引入
- 模块导出机制分析
- 模块加载规则
	+ 模块查找 不加扩展名的时候会按照如下后缀顺序进行查找 .js .json .node（C语言编译）
	+ 
- 模块分类
	+ 自定义模块
	+ 系统核心模块
		* fs 文件操作
		* http 网络操作
		* path 路径操作
		* querystring 查询参数解析
		* url url解析

写文件操作

### url 网址

```js
var http = require('http')var url = require('url')http.createServe(function(req,res){    }).listen(4000)
```



### os操作系统

OS 常用功能

- [`os.EOL`](http://nodejs.cn/api/os.html#os_os_eol)
- [`os.arch()`](http://nodejs.cn/api/os.html#os_os_arch)
- [`os.constants`](http://nodejs.cn/api/os.html#os_os_constants)
- [`os.cpus()`](http://nodejs.cn/api/os.html#os_os_cpus)
- [`os.endianness()`](http://nodejs.cn/api/os.html#os_os_endianness)
- [`os.freemem()`](http://nodejs.cn/api/os.html#os_os_freemem)
- [`os.getPriority([pid\])`](http://nodejs.cn/api/os.html#os_os_getpriority_pid)
- [`os.homedir()`](http://nodejs.cn/api/os.html#os_os_homedir)
- [`os.hostname()`](http://nodejs.cn/api/os.html#os_os_hostname)
- [`os.loadavg()`](http://nodejs.cn/api/os.html#os_os_loadavg)
- [`os.networkInterfaces()`](http://nodejs.cn/api/os.html#os_os_networkinterfaces)
- [`os.platform()`](http://nodejs.cn/api/os.html#os_os_platform)
- [`os.release()`](http://nodejs.cn/api/os.html#os_os_release)
- `os.setPriority([pid, \]priority)`(http://nodejs.cn/api/os.html#os_os_setpriority_pid_priority)
- [`os.tmpdir()`](http://nodejs.cn/api/os.html#os_os_tmpdir)
- [`os.totalmem()`](http://nodejs.cn/api/os.html#os_os_totalmem)
- [`os.type()`](http://nodejs.cn/api/os.html#os_os_type)
- [`os.uptime()`](http://nodejs.cn/api/os.html#os_os_uptime)
- [`os.userInfo([options\])`](http://nodejs.cn/api/os.html#os_os_userinfo_options)
- [`os.version()`](



### util 实用工具



### v8 引擎



### report  诊断报告



## 模块

> 多个模块可以形成包，不过要满足特定的规则才能形成规范的
>
> 包

### 简介

- 模块化
	- 什么是模块、模块化
	- 为什么要模块化
	- 模块化的好处
	- 页面加载引入script
	- 模块化可以有多种形式、但至少应该提供能够代码分割为多个源文件的机制、
	- 一个JS文件就是一个模块    每一个js文件代码都是独立运行在一个函数中、而不是在全局作用域 global ，所以一个模块中的变量和函数在其他模块中无法访问 避免污染全局作用域空间
		- 全局创建的变量会作为gobal的属性保存
		- 全局创建的函数会作为gobal的方法保存
	- argument 参数 global.a arguments.callee  单个js文件函数作用越 局部变量 

```js
console.log(arguments.callee)// 实际上模块中的代码都是包装在一个函数中执行的，并且函数执行时，同时传递进了5个实参exports 该对象用来将变量或函数暴露到外部require 函数 移入外部的模块module // 当前模块本身// exports 就是modules的属性// 既可以使用exports导出,也可以使用module.exports导出__filename// 当前模块的完整路径__dirname // 所在文件夹的完整路径console.log(module.exports == exports)
```

- module.exports与exports 

```js
exports 只能使用.的方式来向外暴露内容变量exports.xxx = xxxmodules.exports 可以通过.形式也可以直接赋值module.exports.xxx = xxxmodule.exports = {}module.exports = { // 一个对象 	name:'code' 	age:'20'    sayName:function(){        console.log('hello world')    }}	exports.name = 'name'exports.age = '20'exports.sayName = funciton(){    console.log('hello world')}// exports 与 module.exportsvar obj = {}obj.a = {} // module.exportsvar a = obj.a // exports  a 和 obj.a 同时执行obj={}a.name = 'test' // obj.a 也会修改a = new Object() // a 不在指向 obj={}console.log(obj.a.name)console.log(a.name)
```

- 模块化规范

### CommonJS模块



### ECMAScript模块



- COMMONJS规范 

	- 解决JavaScript 没有标准的缺陷 

	- CommonJS对模块的定义简单

		- 模块引用

		- 模块定义

		- 模块标识 通过模块标识来找到指定的模块

			- 核心模块
				- node 引擎提供的模块
			- 文件模块
				- 用户创建的模块 
				- 文件模块的标识就是文件的路径 绝对路径 相对路径
					- 相对路径

			```js
			// 引入模块 requireconst fs = require('fs')console.log(fs)// 向外暴露属性或方法 导出 export  let num = 1000exports.numexports.num = 1999exports.cls = function(){    console.log('cls')}
			```

	- ES5标准的缺陷

		- 没有模块系统
		- 标准库较少
		- 没有标准接口
		- 缺乏管理系统 

	- exports和module.exports

- AMD规范

- CMD规范

- ES6规范

	- 基本使用
	- 默认暴露

### NPM （node.js package manager(工具)）

- CommonJS包规范是理论 NPM 是其中一种实践
- NPM完成第三方模块的发布 安装和依赖 。
- CommonJS的包规范允许我们将一组相关的模块组合到一起，形成一组完整的工具
- CommonJS的包规范由包结构和包描述文件两个部分组成
- 包结构 实际就是一个压缩文件 符合规范的目录
	- 用于组织包中的各种文件
	- package.json 描述文件
	- bin 可执行二进制文件
	- lib js代码 依赖
	- doc 文档 README.md
	- test 单元测试
- 包描述文件
	- 描述包的相关信息，以供外部读取分析

node.js / node_modules/npm

[npm | build amazing things](https://www.npmjs.com/) 

> 全球最大的模块生态系统，里面所有的模块都是开源免费的；也是Node.js的包管理工具。

- [官方网站](https://www.npmjs.com/ )

`npm(安装node.js包管理工具) nvm (安装node版本)nrm（切换不同node包管理工具的源） cnpm（淘宝的npm源）yarn与npm的功能差不多 ``

### npm包安装方式

- 本地安装  一般用于开发某个具体的功能

本地项目下

npm init

npm init -y

package.json文件

```
{  "name": "node.package",  "version": "1.0.0",  "description": "",  "main": "index.js",  "scripts": {    "test": "echo \"Error: no test specified\" && exit 1"    // "test":"node index.js"  },  "author": "",  "license": "ISC"}
```

```
node .npm run test
```

安装第三方包 art-template

- 全局安装 -g 安装目录为node.js环境目录下的 / node_modules/npm
- 全局安装的包用于命令行工具

### 解决npm安装包被墙的问题

- --registry

	+ npm config set registry=https//registry.npm.taobao.org 

- cnpm

	+ 淘宝NPM镜像,与官方NPM的同步频率目前为10分钟一次 

	+ 官网: http://npm.taobao.org/ 

	+ npm install -g cnpm –registry=https//registry.npm.taobao.org 

	+ 使用cnpm安装包: cnpm install 包名

- nrm

	+ 作用：修改镜像源 

	+ 项目地址：https://www.npmjs.com/package/nrm 

	+ 安装：npm install -g nrm


### npm常用命令

- 安装包 默认安装最新的版本

- npm install  -g 包名称  (全局安装)

- npm install  包名称 （本地安装)

	npm install -g es-checker

	es-checker

	//检测当前node环境支不支持es6 

	安装包的时候可以指定版本 

	npm install -g 包名称@版本号


​	npm install -g i5ting_toc

//把markdown 文件装换有一个markdown目录树的页面

使用

i5ting_toc -f  文件名.md -o

- 更新包
- npm update -g es-checker
- 卸载包
- npm uninstall -g es-checker

packgage.json 文件中添加两个键

dependencies// devDependencies 管理依赖

--save 向生产环境添加依赖 dependencies 

生产环境（项目部署上线之后的服务器环境）

```
dependencies 
```

--save-dev 向开发环境添加依赖

开发环境（平时开发使用的环境）DevDependencies 开发环境使用

```
devDependencies
```

```
npm install 安装所有环境下的包 npm install --production// 只会安装dependencies中的包不会安装devDependencies中的包
```

### yarn基本使用 facebook开发的

- 类比npm基本使用

npm的缺点 ： 

有些包没有办法更新

npm性能不太好

安装

npm install -g yarn

初始化

npm init

yarn init

安装包

npm install xxx –save

yarn add xxx

移除包

npm uninstall xxx

yarn remove xxx

更新包

npm update xxx

yarn upgrade xxx

安装开发依赖的包

npm install xxx   --save-dev

yarn add xxx --dev

全局安装

npm install -g xxx

yarn global add xxx

设置包的镜像地址

npm config set registry url

yarn config set registry url

安装所有依赖

npm install 

yarn install

执行包

npm run 

yarn run

### 自定义包

### 包的规范

- package.json必须在包的顶层目录下
- 二进制文件应该在bin目录下
- JavaScript代码应该在lib目录下
- 文档应该在doc目录下
- 单元测试应该在test目录下

### package.json

```
入口文件
```

```json
{  "name": "node.package",  "version": "1.0.0", //语义化版本  "description": "",  "main": "index.js",// 入口文件  "scripts": {    "test": "node index.js"  },  "author": "",  "license": "ISC"}
```

```js
markdown => htmlnpm install markdown-it --savenpm markdowk-it包https://www.npmjs.com/package/markdown-it// node.js, "classic" way:var MarkdownIt = require('markdown-it'),    md = new MarkdownIt();var result = md.render('# markdown-it rulezz!');// node.js, the same, but with sugar:var md = require('markdown-it')();var result = md.render('# markdown-it rulezz!');// browser without AMD, added to "window" on script load// Note, there is no dash in "markdownit".var md = window.markdownit();var result = md.render('# markdown-it rulezz!');
```

### package.json字段分析

- name：包的名称，必须是唯一的，由小写英文字母、数字和下划线组成，不能包含空格
- description：包的简要说明 描述
- version：符合语义化版本识别规范的版本字符串
- keywords：关键字数组，通常用于搜索
- maintainers：维护者数组，每个元素要包含name、email（可选）、web（可选）字段
- contributors：贡献者数组，格式与maintainers相同。包的作者应该是贡献者数组的第一- 个元素
- bugs：提交bug的地址，可以是网站或者电子邮件地址
- licenses：许可证数组，每个元素要包含type（许可证名称）和url（链接到许可证文本的- 地址）字段
- repositories：仓库托管地址数组，每个元素要包含type（仓库类型，如git）、url（仓- 库的地址）和path（相对于仓库的路径，可选）字段
- dependencies：``生产环境包的依赖``，一个关联数组，由包的名称和版本号组成 生产依赖
- devDependencies：``开发环境包的依赖``，一个关联数组，由包的名称和版本号组成 开发依赖
- homepage
- os
- cpu engine
- builtin
- main 
- author
- script
- json 文件不能有注释

### 自定义包案例

动态网站开发

```js
const http = require('http');const fs = require('fs')const path = require('path')const querystring = require('querystring')const scoreData = require(./scores.json)http.createServer((req,res)=>{	// 路由（请求路径 + 请求方式）	// 查询成绩的入口地址 query	if(req.url.statsWith('/query') && req.method == 'GET'){		fs.readFile(path.join(__dirname,'view','index.tpl'),'utf-8',(err,content)=>{			if(err){			res.writeHead(500,{				'Content-Type':'text/plain;charset=utf-8'			});			res.end('服务器错误，请与管理员联系');			}		}            res.end(content);            }); 	}else if(req.url.startsWith('/score') && req.method == 'POST'){	// 获取成绩的结果 score		let pdata = '';		req.on('data',(chunk)=>{			pdata += chunk;		});		req.on('end',()=>{			let obj = querystring.parse(pdata);			let result = scoreData[obj.code];            fs.readFile(path.join(__dirname,"view","result.tpl"),"utf-8",(err,content)=>{               	if(err){			res.writeHead(500,{				'Content-Type':'text/plain;charset=utf-8'			});			res.end('服务器错误，请与管理员联系');			}		}             // 返回内容之前要进行数据渲染             content = content.replace('$$chinese$$',result.chinese);                content = content.replace('$$math$$',result.math);                 content = content.replace('$$english$$',result.english);                 content = content.replace('$$summary$$',result.summary);           		res.end(content);            });		});	}	}).listen(3000,()=>{	console.log('running.....');});
```

```
scores.json{	"no123":{		"chinese":"100",		"math":"140",		"english":"149",		"summary":"289"	},	"no124":{		"chinese":"100",		"math":"140",		"english":"149",		"summary":"289"	},	"no125":{		"chinese":"100",		"math":"140",		"english":"149",		"summary":"289"	}}
```

```html
view/index.tpl // 模板查询页面<!DOCTYPE html><html lang="en"><head>    <meta charset="UTF-8">    <meta name="viewport" content="width=device-width, initial-scale=1.0">    <title>Document</title></head><body>    <form action="http://localhost:3000/score/" method="post">        请输入考号:<input type="text" name="code">        <input type="submit" value="查询">    </form></body></html>// 结果页面 result.tpl<!DOCTYPE html><html lang="en"><head>    <meta charset="UTF-8">    <meta name="viewport" content="width=device-width, initial-scale=1.0">    <title>Document</title></head><body>    <ul>        <li>语文:$$chinese$$</li>        <li>数学:$$math$$</li>        <li>外语:$$english$$</li>        <li>综合:$$summary$$</li>    </ul></body></html>
```

Web开发-初步实现服务

请求路径分发

```js
//初步实现服务器功能const http = require('http');//创建服务器实例对象let server = http.createServer();//绑定请求事件server.on('request',(req,res)=>{    res.end('hello');});//监听端口server.listen(3000);// 127.0.0.1:3000 // localhost:3000//简单的方法http.createServer((req.res)=>{    res.end('hello');}).listen(3000)// 指定IP地址http.createServer((req.res)=>{    res.end('hello');}).listen(3000,'本地IP地址192.168.3.4',()=>{    console.log('running...')})
```

初步实现静态资源

```js
处理请求路径的分发1.req 对象是Class: http.IncomingMessage的实例对象2.res对象是Class : http.ServerResponse的实例对象response.end([data[, encoding]][, callback])// end方法用来完成响应，只能执行一次response.write(chunk[, encoding][, callback]) // write向客户端响应内容，可以写多次const http = require('http');http.createServer((req, res) => {     // res.end(req.url); url的地址 req.url可以获取URL中的路径(端口之后部分)    // res.end(req.url);    if (req.url.startsWith('/index')) {        res.end('index');    } else if (req.url.startsWith('/about')) {        res.write('hello')        res.write('new')        res.write('world')        res.end();    } else {        res.end('404');    }}).listen(3300, '127.0.0.1', () => {    console.log('running');})
```

文件的读取操作

```js
根据路径读取文件的内容，并且响应到浏览器端// 响应完整的页面信息const http = require('http');const path = require('path');const fs = require('fs');let readFile = (url, res) => {    fs.readFile(path.join(__dirname, 'www', url), 'utf8', (err, fileContent) => {        if (err) {            res.end('server error');        } else {            res.end(fileContent);        }    })}http.createServer((req, res) => {    //处理路径的分发    if (req.url.startsWith('/index')) {        readFile('index.html', res);    } else if (req.url.startsWith('/about')) {        readFile('about.html', res);    } else {        // writeHead 数组相应类型和编码        res.writeHead(200, {            'Content-Type': 'text/plain;charset= utf8'        });        res.end('404网页');    }}).listen(3000, '127.0.0.1', () => {    console.log('running...');})
```

```js
封装06.jsconst path = require("path");const fs = require("fs");const mime = require('./mine.json')// 模块exports.staticServer = (req, res, root) => {    fs.readFile(path.join(__dirname, "www", req.url), (err, fileContent) => {        if (err) {            res.writeHead(404, {                "Content-Type": "text/plain;charset=utf8",            });            res.end("404页面");        } else {            // 获取请求文件的后缀            let dtype = 'text/html';            // 如果请求的文件后缀合理，就获取标准的响应格式            let ext = path.extname(req.url);            if (mime[ext]) {                dtype = mime[ext];            }            // 如果响应的内容是文本，就设置成utf8            if (dtype.startsWith('text')) {                dtype += ';charset=utf8'            }            // 设置响应头信息            res.writeHead(200, {                'Content-Type': dtype            });            res.end(fileContent);        }    });}const http = require("http");const path = require("path");const fs = require("fs");const ss = require('./06.js')http.createServer((req, res) => {    ss.staticServer(req,res,path.join(_dirname,'www'));})  .listen(3000, "127.0.0.1", () => {    console.log("running...");});
```



## 标准

模块规范 CommonJS AMD CMD

CommonJS定义的模块分为:{模块引用(require)} {模块定义(exports)} {模块标识(module)}

- require()用来引入外部模块；
- exports对象用于导出当前模块的方法或变量，唯一的导出口；
- module对象就代表模块本身

浏览器不兼容CommonJS的根本原因，在于缺少四个Node.js环境的变量。

- module
- exports
- require
- global

[Browserify](http://browserify.org/) 是目前最常用的 CommonJS 格式转换的工具

```
npm install browser-unpack -gbrowserify main.js > compiled.js
```

[js模块化编程之彻底弄懂CommonJS和AMD/CMD！ - 每天都要学进去一些 - 博客园](https://www.cnblogs.com/chenguangliang/p/5856701.html)

### commonJS

- 什么是 CommonJS？

CommonJS 就是为 JS 的表现来制定规范，因为 JS 没有模块系统、标准库较少、缺乏包管理工具，所以 CommonJS 应运而生，它希望 JS 可以在任何地方运行，而不只是在浏览器中，从而达到 Java、C#、PHP 这些后端语言具备开发大型应用的能力。

- CommonJS 的应用？

1. 服务器端 JavaScript 应用程序。（Node.js）
2. 命令行工具
3. 桌面图形界面应用程序。

node 寻找模块

-  当前目录
-  上级node_modlue
-  再上级目录
-  磁盘根目录

缺点：

```
var math = require('math.js') //要等待加载完成，会导致浏览器假死math.add(2,3)
```

- Node.js 中的模块化？

1. 在 Node 中，模块分为两类：一是 Node 提供的模块，称为核心模块；二是用户编写的模块，成为文件模块。核心模块在 Node 源代码的编译过程中，编译进了二进制执行文件，所以它的加载速度是最快的，例如：HTTP 模块、URL 模块、FS 模块；文件模块是在运行时动态加载的，需要完整的路劲分析、文件定位、编译执行过程等……所以它的速度相对核心模块来说会更慢一些。
2. 我们可以将公共的功能抽离出一个单独的 JS 文件存放，然后在需要的情况下，通过 exports 或者 module.exports 将模块导出，并通过 require 引入这些模块。

```
// 导入var http = require("http");  // 导出module.exports 是真正的接口exports 是一个辅助工具// exports 使用方法// var str = "jsliang is very good!";// exports.str = str; // { str: 'jsliang is very good!' }// module.exports 使用方法module.exports = tools;
```



CMD





AMD

浏览器端的模块，不能采用"同步加载"（synchronous），只能采用"异步加载"（asynchronous）。这就是AMD规范诞生的背景。

[AMD](https://github.com/amdjs/amdjs-api/wiki/AMD)是"Asynchronous Module Definition"的缩写，意思就是"异步模块定义"。它采用异步方式加载模块，模块的加载不影响它后面语句的运行。所有依赖这个模块的语句，都定义在一个回调函数中，等到加载完成之后，这个回调函数才会运行。

```
require([module], callback);第一个参数[module]，是一个数组，里面的成员就是要加载的模块；第二个参数callback，则是加载成功之后的回调函数。如果将前面的代码改写成AMD形式，就是下面这样：
```

AMD比较适合浏览器环境。目前，主要有两个Javascript库实现了AMD规范：[require.js](http://requirejs.org/)和[curl.js](https://github.com/cujojs/curl)。**RequireJS就是实现了AMD规范的呢。**

require.js的诞生，就是为了解决这两个问题：

 

> 　　　　![img](http://image.beekka.com/blog/201211/bg2012110701.png)
>
> 　　　　（1）实现js文件的异步加载，避免网页失去响应；
>
> 　　　　（2）管理模块之间的依赖性，便于代码的编写和维护。



```
// 加载这个文件，也可能造成网页失去响应。解决办法有两个，一个是把它放在网页底部加载，另一个是写成下面这样：<script src="js/require.js" defer async="true" ></script> // require.js 文件// async属性表明这个文件需要异步加载，避免网页失去响应。IE不支持这个属性，只支持defer，所以把defer也写上。<script src="js/require.js" data-main="js/main"></script> // 代码文件是main.jsdata-main属性的作用是，指定网页程序的主模块。在上例中，就是js目录下面的main.js，这个文件会第一个被require.js加载。由于require.js默认的文件后缀名是js，所以可以把main.js简写成main。
```

```
main.js

require(['moduleA', 'moduleB', 'moduleC'], function (moduleA, moduleB, moduleC){

// some code here

});
require()函数接受两个参数。第一个参数是一个数组，表示所依赖的模块，上例就是['moduleA', 'moduleB', 'moduleC']，即主模块依赖这三个模块；第二个参数是一个回调函数，当前面指定的模块都加载成功后，它将被调用。加载的模块会以参数形式传入该函数，从而在回调函数内部就可以使用这些模块。

　　require(['jquery', 'underscore', 'backbone'], function ($, _, Backbone){

　　　　// some code here

　　});
```

## 命令

cnpm 、 npm、 nvm、 yarn 、nrm

> nvm:	Node.js版本控制 nvm version
>
> npm:	 Node.js 官方提供的包管理工具 npm -v
>
> nrm :	npm镜像管理工具  (cnpm:	 淘宝的npm 镜像的加速)  nrm -V
>
> yarn : facebook 的一款与npm 功能相似的包管理工具
>
> [Yarn](https://classic.yarnpkg.com/zh-Hans/)  yarn --version

NPM 包管理工具

[npm 中文文档 | npm 中文网](https://www.npmjs.cn/)

[npm | build amazing things](https://www.npmjs.com/)

[npm命令详解 ](https://juejin.im/post/5de4856051882516e524b566)

[npm 常用命令详解 ](https://www.cnblogs.com/PeunZhang/p/5553574.html)

NPM(Node Package Manager)是Node.js 官方提供的包管理工具，是随同NodeJS一起安装的包管理和分发工具，它很方便让JavaScript开发者下载、安装、上传以及管理已经安装的包。

> - [npm install 安装模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-install)
> - [npm uninstall 卸载模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-uninstall)
> - [npm update 更新模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-update)
> - [npm outdated 检查模块是否已经过时](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-outdated)
> - [npm ls 查看安装的模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-ls)
> - [npm init 在项目中引导创建一个package.json文件](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-init) -y
> - [npm help 查看某条命令的详细帮助](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-help)
> - [npm root 查看包的安装路径](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-root)
> - [npm config 管理npm的配置路径](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-config)
> - [npm cache 管理模块的缓存](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-cache)
> - [npm start 启动模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-start)
> - [npm stop 停止模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-stop)
> - [npm restart 重新启动模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-restart)
> - [npm test 测试模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-test)
> - [npm version 查看模块版本](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-version)
> - [npm view 查看模块的注册信息](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-view)
> - [npm adduser 用户登录](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-adduser)
> - [npm publish 发布模块](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-publish)
> - [npm access 在发布的包上设置访问级别](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-access)
> - [npm package.json文件的语法](https://www.cnblogs.com/PeunZhang/p/5553574.html#npm-package.json)

> 与npm 命令相关的两个 node_module 和 package.json

```bash
npm init    //生成package.json文件npm init -y //生成默认的package.json文件
```

安装：全局安装与本地安装

```bash
npm install express -g // 全局安装 工具npm install express  // 本地安装 安装模块到项目目录下  没有添加到依赖中npm install --save moduleName // dependencies(生产环境) 部署环境// -save 的意思是将模块安装到项目目录下，并在package文件的dependencies节点写入依赖。npm install --save-dev moduleName  // devDependencies(开发环境) // -save-dev 的意思是将模块安装到项目目录下，并在package文件的devDependencies节点写入依赖。npm install gulp --save-optional 或 npm install gulp -O //-O, --save-optional 安装包信息将加入到optionalDependencies（可选阶段的依赖）
```

> Express 是一种保持最低程度规模的灵活 Node.js Web 应用程序框架，为 Web 和移动应用程序提供一组强大的功能。

安装不同的版本

```bash
npm install moduleName@lastest 最新版本npm install moduleName@版本号
```

查看npm 的版本

```bash
npm v
```

查看所有模块的版本

```bash
npm version
```

npm install 命令默认会安装 package.json 中 dependencies 字段和 devDependencies 字段中的所有模块，

如果使用 --production 参数，可以只安装 dependencies （生产环境的依赖）字段的模块。

```bash
npm install --production# 或者NODE_ENV=production npm install
```

添加--only=dev安装项目所需依赖时，只有devDependencies字段中的依赖包会被安装，dependencies字段中的依赖包不会被安装。与添加--production的效果刚好相反。

```bash
npm install --only=dev
```

npm install 也支持直接输入Github代码地址

```bash
npm install  git://github.com/package/path.git// git的地址
```

| 模式     | 可通过 require 使用 | 注册 PATH | 安装目录                       |
| -------- | ------------------- | --------- | ------------------------------ |
| 本地模式 | 是                  | 否        | 当前项目的 node_modules 子目录 |
| 全局模式 | 否（命令行里使用）  | 是        | 安装在node软件的安装目录下     |

| npm命令                                                      | 安装模块位置         | package.json                                           | npm install 初始化项目时不会下载模块 |                                                              |
| ------------------------------------------------------------ | -------------------- | ------------------------------------------------------ | ------------------------------------ | ------------------------------------------------------------ |
| npm install moduleName                                       | 项目node_modules目录 | `不会将模块依赖写入devDependencies或dependencies 节点` | 不会                                 | 主要作用是安装配置好package.json文件中的相关依赖             |
| npm install -g moduleName                                    | 全局                 | `不会将模块依赖写入devDependencies或dependencies 节点` | 不会                                 |                                                              |
| npm install moduleName  -save//简写：npm install moduleName -S | 项目node_modules目录 | 会将模块依赖写入dependencies 节点                      | 下载到项目目录下                     | 运行npm install --production或者注明NODE_ENV变量值为production时，**会**自动下载模块到node_modules目录中。 |
| npm install  moduleName -save-dev// 简写: npm install moduleName -D | 项目node_modules目录 | . 会将模块依赖写入devDependencies 节点                 | 下载到项目目录下                     | 运行npm install --production或者注明NODE_ENV变量值为production时，**不会**自动下载模块到node_modules目录中 |

卸载模块

```bash
npm uninstall express //本地模块 当前目录npm uninstall -g <package> //全局模块 （一般都是一些工具）npm uninstall 模块：删除模块，但不删除模块留在package.json中的对应信息npm uninstall 模块 --save 删除模块，同时删除模块留在package.json中dependencies下的对应信息npm uninstall 模块 --save-dev 删除模块，同时删除模块留在package.json中devDependencies下的对应信息npm remove 模块 npm r  模块
```

卸载完以后查看一下该模块是否存在

```bash
npm lsnpm list -g // 查看安装信息npm list 命令也可以列出单个模块npm list underscorenpm list <packagename> PS C:\Users\by\Desktop\jsPang\awesomePos> npm list element-uiawesome_pos@1.0.0 C:\Users\by\Desktop\jsPang\awesomePos`-- element-ui@2.2.2npm list <packagename> -g
```

更新模块

```bash
npm update moduleName(express)
```

搜索模块

```html
npm search express
```

模块的具体信息

```
npm info underscore //查看underscore 模块的信息
```

`npm run`

npm 不仅可以用于模块管理，还可以用于执行脚本。package.json 文件有一个 scripts 字段，可以用于指定脚本命令，供 npm 直接调用。

```
"scripts": {    "lint": "jshint **.js",    "test": "mocha test/" }
```

版本号 `NPM使用语义版本号来管理代码`

语义版本号分为X.Y.Z三位，分别代表主版本号、次版本号和补丁版本号。

- 如果只是修复bug，需要更新Z位。
- 如果是新增了功能，但是向下兼容，需要更新Y位。
- 如果有大变动，向下不兼容，需要更新X位。

版本号有了这个保证后，在申明第三方包依赖时，除了可依赖于一个固定版本号外，还可依赖于某个范围的版本号。例如"argv": "0.0.x"表示依赖于0.0.x系列的最新版argv。

nrm镜像切换地址

**作用：提供一些最常用的NPM包镜像地址，能够让我们快速的切换安装包的服务器地址：**

什么是镜像：原本包刚一开始只是存在于国外的NPM服务器，但是由于网络原因，经常访问不到，这时候，我们可以在国内创建一个和官网完全一样的NPM服务器，只不过，数据都是从人家那里拿过来的，除此之外，使用方式完全一样：

- 全局安装nrm包npm 


```bash
npm i 软件包 -g
npm i nrm -g 
npm i cnpm -g 
```

- 查看当前所有可用镜像地址以及当前所使用的镜像源地址


```bash
nrm ls
```

- 切换不同的镜像源地址


```bash
nrm use 镜像源地址
nrm use npm 
nrm use taobo
```

> nrm只是单纯提供几个常用的下载包的URL地址，并能够让我们在这几个地址之间，很方便的进行切换，但是，我们每次装包的时候，使用的装包工具，都是npm

## 框架

> [2021年 Nodejs Web框架排行榜 ](https://www.ponote.com/news/76085)
>
> [如何选择正确的Node框架：Express，Koa还是Hapi？ - SegmentFault 思否](https://segmentfault.com/a/1190000018973856)

# express

Express解决的功能

- jwt-token认证
- md5加密
- 中间件路由模块
- 异常错误处理
- 跨域配置
- 自动重启

## Express VsCode



## Express作用

- 单页应用 多页应用 混合应用
- 静态服务器
- 路由
- 中间件
- 模板引擎整合
- 常用API基本使用

特性

- 更快的服务端开发
- 赋能开发者更快地构建 RESTful API
- Express 支持 MVC 架构，但需要开发者做一些额外工作
- 开箱支持 NoSQL 数据库

## 基本知识

[Express](https://www.expressjs.com.cn/)[4.17.1](https://www.expressjs.com.cn/changelog/4x.html#4.17.1)基于 [Node.js](https://nodejs.org/en/) 平台，快速、开放、极简的 Web 开发框架

> Express 
>
> - 是一个简单灵活的node.js Web应用框架
> - 提供了各种特性和丰富的Http工具
> - 可以快速搭建一个完整功能的网站
> - 不限制应用设计模式（MVC、MVP）
> - 不限制代码规范
> - 不限制功能的选择（是否含View层）

### Express 安装

```bash
npm init -y
// 修改 entry point: (index.js)
npm install express -save
node app.js
express --version
```

> 报错“express不是内部或外部命令：原来express默认安装是最新的版本，已经是4.x.x的版本。而最新express4.0+版本中将命令工具分出来了，所以必须要安装express-generator。解决方法是执行命令行：

```bash
npm install -g express-generator
```

### Express-generator 安装

Express -generator
Express generator 为一个完整的应用程序创建了脚手架，其中包含大量的 JavaScript 文件、 Jade 模板和各种用途的子目录，Express的应用生成器，可以快速创建一个Express的应用骨架

```bash
npm install -g express-generatorexpress myapp(项目名)cd myappnpm installnpm start 运行项目express -h// 出现  node ./bin/www// 默认访问 http://127.0.0.1:3000/
```

目录结构

```bash
├── app.js├── bin│   └── www├── package.json├── public│   ├── images│   ├── javascripts│   └── stylesheets│       └── style.css├── routes│   ├── index.js│   └── users.js└── views    ├── error.pug    ├── index.pug    └── layout.pug
```

|    文件名    |                     作用                      |
| :----------: | :-------------------------------------------: |
|     bin      | 启动文件，以何种方式启动文件，默认为npm start |
|    public    |    存放项目的静态文件，imagea/js/css等文件    |
|    routes    |          项目路由信息，控制地址路由           |
|    views     |     视图文件，模板文件jade等，相当于html      |
|    app.js    |              入口文件（主文件）               |
| package.json |                依赖的模板列表                 |

### hello world案例

```js
app.js方法一const express = require('express')const app = express()// 相当于 const app = require('express')();const port = 3000app.user(express.json());//绑定路由app.get('/', (req, res) => res.send('Hello World!'))//监听端口 ${port}app.listen(port, () => console.log(`Example app listening on port ${port}!`))方法二app.get('/', (req, res) => {     res.send('ok');}).listen(port, () => {     console.log(`Example app listening on port ${port}!`)})let server = app.get('/',(req,res)=>{     res.send('ok');});server.listen(3000,()=>{      console.log(`Example app listening on port ${port}!`)})app.post("/",(req,res) =>{    console.log('收到请求体',res.body)    res.status(201).send()})app.put("/:id",(req,res) => {    console.log("收到的请求参数",req.params.id)    res.status(204).send()})app.delete("/:id",(req,res) => {    console.log("收到的请求参数",req.params.id)    console.log("收到的请求体",req.body)    res.send()})
```

安装

```bash
模板引擎整合: art-templatenpm install art-template --sace
```

使用

```bash
const express = require('express');const template = require('art0template');const app = express();
```

## 路由处理

*路由*用于确定应用程序如何响应对特定端点的客户机请求，包含一个 URI（或路径）和一个特定的 HTTP 请求方法（GET、POST 等）。 
Express 支持对应于 HTTP 方法的以下路由方法：`get`、`post`、`put`、`head`、`delete`、`options`、`trace`、`copy`、`lock`、`mkcol`、`move`、`purge`、`propfind`、`proppatch`、`unlock`、`report`、`mkactivity`、`checkout`、`merge`、`m-search`、`notify`、`subscribe`、`unsubscribe`、`patch`、`search` 和 `connect`。

```bash
app.METHOD(PATH, HANDLER) 
```

- `app` 是 `express` 的实例。
- `METHOD` 是 [HTTP 请求方法](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)。
- `PATH` 是服务器上的路径。
- `HANDLER` 是在路由匹配时执行的函数。、

### 路由匹配

| 匹配规则                                                     |             |
| ------------------------------------------------------------ | ----------- |
| 匹配 `acd` 和 `abcd`                                         | `/ab?cd`    |
| 匹配 `abcd`、`abbcd`、`abbbcd`                               | `/ab+cd`    |
| 匹配 `abcd`、`abxcd`、`abRABDOMcd`、`ab123cd`                | `/ab*cd`    |
| 匹配 `/abe` 和 `/abcde`                                      | `/ab(cd)?e` |
| 匹配名称中具有`a`的所有路由                                  | `/a/`       |
| 匹配 `butterfly` 和 `dragonfly`，但是不匹配 `butterflyman`、`dragonfly man` | `/.*fly$/`  |

### 路由处理程序

可以提供多个回调函数，以类似于[中间件](https://expressjs.com/zh-cn/guide/using-middleware.html)的行为方式来处理请求。唯一例外是这些回调函数可能调用 `next('route')` 来绕过剩余的路由回调。您可以使用此机制对路由施加先决条件，在没有理由继续执行当前路由的情况下，可将控制权传递给后续路由。
路由处理程序的形式可以是一个函数、一组函数或者两者的结合，如以下示例中所示。
多个回调函数可以处理一个路由（确保您指定 `next` 对象）。

```js
app.get('/example/b', function (req, res, next) {  console.log('the response will be sent by the next function ...');  next();}, function (req, res) {  res.send('Hello from B!');});
```

一组回调函数可以处理一个路由

```js
var cb0 = function (req, res, next) {  console.log('CB0');  next();}var cb1 = function (req, res, next) {  console.log('CB1');  next();}var cb2 = function (req, res) {  res.send('Hello from C!');}app.get('/example/c', [cb0, cb1, cb2]);
```

独立函数与一组函数的组合可以处理一个路由

```js
var cb0 = function (req, res, next) {  console.log('CB0');  next();}var cb1 = function (req, res, next) {  console.log('CB1');  next();}app.get('/example/d', [cb0, cb1], function (req, res, next) {  console.log('the response will be sent by the next function ...');  next();}, function (req, res) {  res.send('Hello from D!');});
```

### app.router()

使用 `app.route()` 为路由路径创建可链接的路由处理程序。 因为在单一位置指定路径，所以可以减少冗余和输入错误。

```
app.route('/book')  .get(function(req, res) {    res.send('Get a random book');  })  .post(function(req, res) {    res.send('Add a book');  })  .put(function(req, res) {    res.send('Update the book');  });
```

### express.Router()

使用 `express.Router` 类来创建可安装的模块化路由处理程序。`Router` 实例是完整的中间件和路由系统；因此，常常将其称为“微型应用程序”。
以下示例将路由器创建为模块，在其中装入中间件，定义一些路由，然后安装在主应用程序的路径中。
在应用程序目录中创建名为 `birds.js` 的路由器文件，其中包含以下内容：

```js
var express = require('express')
var router = express.Router();
router.use(function timeLog(req, res, next) {
  console.log('Time: ', Date.now());
  next();
});
// define the home page route
router.get('/', function(req, res) {
  res.send('Birds home page');
});
// define the about route
router.get('/about', function(req, res) {
  res.send('About birds');
});
router.get('/user',function(){
    res.render('user',{ title:'Express' }) // user.html 
})
module.exports = router;

app.js
var indexRouter = require('./routes/index')
var usersRouter = require('./routes/users')
app.use()
```

接着，在应用程序中装入路由器模块：
app.js

```
const routes = require('./routes')routes(app);
```

routes/index.js

```js
const post = require('./birds')module.exports = (app) = {	app.use("post",post)}
```

routes/birds.js

```javascript
var birds = require('./birds');var route = express.Router();route.post("/",(req,res) =>{    console.log('收到请求体',res.body)    res.status(201).send()})route.put("/:id",(req,res) => {    console.log("收到的请求参数",req.params.id)    res.status(204).send()})route.delete("/:id",(req,res) => {    console.log("收到的请求参数",req.params.id)    console.log("收到的请求体",req.body)    res.send()})http://localhost:3333/birds/http://localhost:3333/birds/about
```

### 响应方法

响应对象 (`res`) 的方法可以向客户机发送响应，并终止请求/响应循环。如果没有从路由处理程序调用其中任何方法，客户机请求将保持挂起状态。

| 方法                                                         | 描述                                             |
| ------------------------------------------------------------ | ------------------------------------------------ |
| [res.download()](https://expressjs.com/zh-cn/4x/api.html#res.download) | 提示将要下载文件。                               |
| [res.end()](https://expressjs.com/zh-cn/4x/api.html#res.end) | 结束响应进程。                                   |
| [res.json()](https://expressjs.com/zh-cn/4x/api.html#res.json) | 发送 JSON 响应。                                 |
| [res.jsonp()](https://expressjs.com/zh-cn/4x/api.html#res.jsonp) | 在 JSONP 的支持下发送 JSON 响应。                |
| [res.redirect()](https://expressjs.com/zh-cn/4x/api.html#res.redirect) | 重定向请求。                                     |
| [res.render()](https://expressjs.com/zh-cn/4x/api.html#res.render) | 呈现视图模板。                                   |
| [res.send()](https://expressjs.com/zh-cn/4x/api.html#res.send) | 发送各种类型的响应。                             |
| [res.sendFile()](https://expressjs.com/zh-cn/4x/api.html#res.sendFile) | 以八位元流形式发送文件。                         |
| [res.sendStatus()](https://expressjs.com/zh-cn/4x/api.html#res.sendStatus) | 设置响应状态码并以响应主体形式发送其字符串表示。 |
| res.cookie()                                                 |                                                  |
| res.clearCookie()                                            |                                                  |
| res.location()                                               |                                                  |
| res.redirect()                                               |                                                  |
| res.status()                                                 |                                                  |
| res.links()                                                  |                                                  |

## 静态文件

为了提供诸如图像、CSS 文件和 JavaScript 文件之类的静态文件，请使用 Express 中的 `express.static` 内置中间件函数。

```js
app.use(express.static('public'))
http://localhost:3000/images/kitten.jpg
http://localhost:3000/css/style.css
http://localhost:3000/js/app.js
http://localhost:3000/images/bg.png
http://localhost:3000/hello.html
```

```js
app.use('/static',express.static('public'))
http://localhost:3000/static/images/kitten.jpg
http://localhost:3000/static/css/style.css
http://localhost:3000/static/js/app.js
http://localhost:3000/static/images/bg.png
http://localhost:3000/static/hello.html
```

而，向 `express.static` 函数提供的路径相对于您在其中启动 `node` 进程的目录。如果从另一个目录运行 Express 应用程序，那么对于提供资源的目录使用绝对路径会更安全：

```js
app.use('/static', express.static(__dirname + '/public'));
```

## 中间件

什么是中间件？
Express 是``一个路由和中间件Web框架``，其自身只具有最低程度的功能：Express 应用程序基本上是一系列中间件函数调用
中间件函数能够访问请求对象（req）、响应对象（res）以及应用程序的请求/响应循环中的下一个中间件函数。下一个中间件函数通常由名为 `next` 的变量来表示。

- 执行任何代码
- 对请求和响应对象进行更改
- 结束请求/响应循环
- 调用堆栈中的下一个中间件函数
	如果当前中间件函数没有结束请求、响应循环，那么它必须调用 `next()`，以将控制权传递给下一个中间件函数。否则，请求将保持挂起状态。

### 中间件的分类

- 应用层中间件
- 路由中间件
- 错误处理中间件
- 内置中间件
- 第三方中间件

### 应用层中间件`app.use()`

没有安装路径的中间件函数。应用程序每次收到请求时执行该函数
参数`(req,res,next) 和 next()`

- originalUrl
- method

```js
var app = express();
app.use(function(req,res,next){
	console.log('Time',Data.now())
    next()
})
// 使用安装路径装入一系列中间件函数
app.use('/user/:id',function(req,res,next){
    console.log('',req.originalUrl)
    next()
},function(req,res,next){
    console.log('',req.method)
    next()
})
```

指定路径的中间件函数

```js
app.use('/user/:id',function(req,res,next{
	console.log('',req.method)
	next()
});
```

指定http请求方式

```js
app.get('/user/:id',function(req,res,next){   res.send('') })
```

跳过路由器中间件堆栈中剩余的中间件函数，请调用 `next('route')` 将控制权传递给下一个路由。 **注**：`next('route')` 仅在使用 `app.METHOD()` 或 `router.METHOD()` 函数装入的中间件函数中有效。
此示例显示一个中间件子堆栈，用于处理针对 `/user/:id` 路径的 GET 请求。

```js
app.get('/user/:id',function(req,res,next){
	if(req.params.id == 0) next('route');
	else next();	
},function(req,res,next){
    res.render('regular');
});
app.get('/user/:id',function(req,res,next){
    res.render('special');
})
```

### 路由中间件

路由器层中间件的工作方式与应用层中间件基本相同，差异之处在于它绑定到 `express.Router()` 的实例。

```js
var app = express()
var router = express.Router()
app.use(router)
router.use(function(req,res,next){
    console.log('Time:',Date.now());
    next();
});
router.use('/user/:id',function(req,res,next){
     console.log('Request URL:', req.originalUrl);
  	 next();
},function(req,res,next){
     console.log('Request Type:', req.method);
     next();
})
router.get('/user/:id',function(req,res,next){
    if(req,params.id == 0) next('route');
    else next();
},function(req,res,next){
    res.render('regular');
})
router.get('/user/:id',function(req,res,next){
    console.log(req.params.id);
    res.render('special');
})
app.use('/',router)
```

### 错误处理中间件

- 错误处理中间件的定义方式与其他中间件函数基本相同
- 差别在于错误处理函数有四个自变量而不是三个`(err,req,res,next)`
	路由遇到错误时可以通过

```js
app.use(function(err,req,res,next){
	console.error(err.stack);
	res.status(500).send(‘错误’);
});
```

### 内置中间件(静态文件)

#### express.static

```js
var options = {
}
```

### 第三方中间件

- 使用第三方中间件向Express应用程序添加功能
- 安装具有所需功能的 Node.js 模块，然后在应用层或路由器层的应用程序中将其加入

```bash
npm install cookie-parser
```

```js
var express = require('express')
var app = express()
var cookieParser = require('cookie-parser')
app.use(cookieParser())
```

## 错误处理

```js
app.use(function(err,req,res,next){
	console.log(err,stack);
	res.status(500).send('error message')
})
```

### 错误处理中间件

```js
var bodyParser = require('body-parser');
var methodOverride = require('method-override')
```

### 缺省错误处理程序

## 模板引擎

安装pug

```bash
npm install pug --save
```

- views ： 模板文件所在目录 `app.set('view','./views')`
- view engine ：要`app.set('view engins','pug')`

```js
app.js
app.set('views', './views')   // 模板文件所在目录
// view/index.pug 文件
app.set('view engine', 'pug'); // 使用的模板引擎
app.get('/', function (req, res) {
  res.render('index', { title: 'Hey', message: 'Hello there!'});
});
```

```pug
// index.pug 的pug 模板文件
html
  head
    title= title
  body
    h1= message
```

## 数据库集成

[Express 数据库](https://expressjs.com/zh-cn/guide/database-integration.html)

- [Cassandra](https://expressjs.com/zh-cn/guide/database-integration.html#cassandra)
- [CouchDB](https://expressjs.com/zh-cn/guide/database-integration.html#couchdb)
- [LevelDB](https://expressjs.com/zh-cn/guide/database-integration.html#leveldb)
- [MySQL](https://expressjs.com/zh-cn/guide/database-integration.html#mysql)
- [MongoDB](https://expressjs.com/zh-cn/guide/database-integration.html#mongo)
- [Neo4j](https://expressjs.com/zh-cn/guide/database-integration.html#neo4j)
- [PostgreSQL](https://expressjs.com/zh-cn/guide/database-integration.html#postgres)
- [Redis](https://expressjs.com/zh-cn/guide/database-integration.html#redis)
- [SQLite](https://expressjs.com/zh-cn/guide/database-integration.html#sqlite)
- [ElasticSearch](https://expressjs.com/zh-cn/guide/database-integration.html#elasticsearch)

## Express API

### 表现

### 应用

### 请求

### 响应

### 路由器

# koa

Koa.js 最适合用于创建服务器、路由、处理响应和处理错误。

作用

- 前台系统
- 后台系统
- 混合系统

# nestjs

[Nestjs中文文档](https://www.itying.com/nestjs/)

Nest.js 是一个渐进的Node.js 框架，可以在Typescript 和 JavaScript (ES6、ES7、ES8) 之上构建高效、可伸缩的企业级服务器端应用程序。它的核心思想是提供了一个层与层直接的耦合度较小、抽象化较高的一个架构体系。

Nest.js是一个服务器端应用框架

安装

```bash
npm i -g @nestjs/cli  // yarn global add @nestjs/cli
nest new project-name
npm run start
```

# hapi.js

Hapi.js 是开发安全、实时、可扩展和社交媒体应用的理想选择。大多数移动应用开发者都喜欢用 Hapi.js 来创建代理和 API 服务器。

作用

- 网站
- HTTP 代理应用
- 应用程序接口服务

安装

```
npm install @hapi/hapi
```

```js
const Hapi = require('@hapi/hapi')
const init = async() => {
    const server = Hapi.server({
        port:3000,
        host:'localhost'
    })
    await server.start()
    console.log('Server running on %s',server.info.url)
}

process.on('unhandledRejection',(err) => {
    console.log(err)
    process.exit(i)
})

init()
```

