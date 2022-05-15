---
title: 前端常用开发命令
categories:
- 前端
tags:
- 常用命令
abbrlink: 61107
---
# 常用命令

## backage

- vue、vue-cli、vue-router、vuex、axios
- webpack
- jquery
- json5

```bash
// vue 2.0
npm i @vue/cli-g  //vue-cli

//vue 3.0
npm install vue@next  //
npm install -g @vue/cli@next  // yarn global add @vue/cli@next
// Vue 3 你应该使用 npm 上可用的 Vue CLI v4.5 作为 @vue/cli@next

//vite
npm init vite-app <project-name>
yarn create vite-app <project-name>

vue -V
npm install -g @vue/cli @vue/cli-service-global
```

```bash
npm install elementui
```

```
npm install webpack -g
```

vue 必备插件

```
// sass、less、stylus
npm install -D sass-loader node-sass
npm install -D less-loader
npm install -D stylus-loader stylus

npm install vue-router 

npm install vuex

npm install axios -S

g：全局安装。表明这个包将安装到你的计算机中，你可以在计算机任何一个位置使用它。
--save/-S：通过该种方式安装的包的名称及版本号会出现在 package.json 中的 dependencies 中。dependencies 是需要发布在生成环境的。例如：ElementUI 是部署后还需要的，所以通过 -S 形式来安装。
--save-dev/-D：通过该种方式安装的包的名称及版本号会出现在 package.json 中的 devDependencies 中。


// 懒加载
npm install vue-lazyload -S

npm list：查看当前目录下都安装了哪些 npm 包。
npm info 模块：查看该模块的版本及内容。
npm i 模块@版本号：安装该模块的指定版本。
```

```bash
vue create <project-name>

vue add element
```

## git

```bash
git clone
git pull
git push

```

## nvm

[nvm-sh/nvm: Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions](https://github.com/nvm-sh/nvm)

[安装nvm]([nvm-sh/nvm: Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions](https://github.com/nvm-sh/nvm))

[(...) win10安装nvm踩坑实录_个人文章 - SegmentFault 思否](https://segmentfault.com/a/1190000020112650)

设置环境变量

安装、切换不同Node.js版本的管理器

```bash
nvm ls
nvm install <version> [arch]
nvm install latest 64(默认64位)
nvm uninstall <vesion> [arch]
nvm use <version>
nvm v
nvm list 查看当前安装的Node.js所有版本
nvm install 版本号 安装指定版本的Node.js nvm install latest 最新版本
nvm uninstall 版本号 卸载指定版本的Node.js
nvm use 版本号 选择指定版本的Node.js
```

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

切换node版本，安装的其他版本安装的全局工具无效

两个重要的目录

> nvm 目录 nvm 管理工具 + v12.16.3 + v13.5.0 （不同的版本）
>
> node.js 目录 （正在使用的node版本）

## node

node的命令行工具

```bash
node  进入REPL环境  REPL : Read、Eval 、print 、Loop
node -v
node -e 'console.log("Hello World")'
node index.js
node path/index.js  // path/index
node --help
.exit 退出 // process.exit()
```

## npm

Node Package Manager

> NPM 出现了两层概念：
>
> - 一层含义是 Node 的开放式模块登记和管理系统，亦可以说是一个生态圈，一个社区。
> - 另一层含义是 Node 默认的模块管理器，是一个命令行下的软件，用来安装和管理 Node 模块。

```bash
npm config get registry
npm install npm -g  // npm install -g npm 

npm update -g nvm
```

## nrm

nrm 是一个 NPM 源管理器，允许你快速地在如下 NPM 源间切换

作用：提供了一些最常用的 NPM 包镜像地址，能够让我们快速的切换安装包时候的服务器地址；
什么是镜像：原来包刚一开始是只存在于国外的 NPM 服务器，但是由于网络原因，经常访问不到，这时候，我们可以在国内，创建一个和官网完全一样的 NPM 服务器，只不过，数据都是从人家那里拿过来的，除此之外，使用方式完全一样；

```bash
npm install -g nrm  //全局安装`nrm`包
nrm ls // 显示全部镜像 查看当前所有可用的镜像源地址以及当前所使用的镜像源地址
nrm use taobao
nrm test  // 测试镜像速度
```

## cnpm

```bash
npm install cnpm -g
```

## yarn

```bash
npm install yarn -g
yarn config get registry
```

## yrm

yrm 是一个 yarn源管理器，允许你快速地在yarn源间切换

```
npm install -g yrm
yrm ls
yrm use taobao
yrm test  // 测试源的响应时间
```

## cgr

```bash
npm install -g cgr
```

## .vuerc

- loader
- plugins

全局 CLI 配置

- 有些针对 `@vue/cli` 的全局配置，例如你惯用的包管理器和你本地保存的 preset，都保存在 home 目录下一个名叫 `.vuerc` 的 JSON 文件。你可以用编辑器直接编辑这个文件来更改已保存的选项。

- `vue config` 命令来审查或修改全局的 CLI 配置。

```json
{
  "useTaobaoRegistry": true,
  "packageManager": "yarn",
  "presets": {
    "electricity-admin": {
      "useConfigFiles": true,
      "plugins": {
        "@vue/cli-plugin-babel": {},
        "@vue/cli-plugin-router": {
          "historyMode": false
        },
        "@vue/cli-plugin-eslint": {
          "config": "standard",
          "lintOn": [
            "save"
          ]
        }
      }
    }
  }
```

## webpack

```
vue init webpack <project-name>
```

