---
title: axios的异步数据请求
categories:
- 前端
tags:
- axios
abbrlink: 58361
---
# vue-resource

Vue 2.0 后 作者停止更新，作者建议使用Axios替换 vue-resource

# axios

> [Gitee API 文档](https://gitee.com/api/v5/swagger#/getV5ReposOwnerRepoStargazers?ex=no)
>
> [Vue.js Ajax(axios) ](https://www.runoob.com/vue2/vuejs-ajax-axios.html)
>
> [axios中文文档|axios中文网 | axios](http://www.axios-js.com/zh-cn/docs/index.html)
>
> [axios/axios: Promise based HTTP client for the browser and node.js](https://github.com/axios/axios)
>
> [免费在线接口文档](https://www.cnblogs.com/10ve/p/10742571.html)

## 快速上手

axios 依赖原生的 ES6 Promise 实现
Vue.js 2.0 版本推荐使用 axios 来完成 ajax 请求

- Axios 是一个基于 Promise 的易用、简洁且高效的HTTP 库，可以用在浏览器和 Node.js。
	特点

- 从浏览器中创建XMLHttpRequests
- 从node.js 创建 http 请求
- 支持Promise API

重点概念

- axios API  axios({})
- 请求方法的别名 axios.get 
- 并发 all([fuc(),fuc()])  axios.spread(callback)
- 创建实例 axios.create()
	- 实例方法
		-  axios#request(config)
		- axios#get(url[, config])
		-  axios#delete(url[, config])
		-  axios#head(url[, config])
		- axios#options(url[, config])
		-  axios#post(url[, data[, config]])
		-  axios#put(url[, data[, config]])
		- axios#patch(url[, data[, config]])
- 请求配置
- 拦截器
- 错误处理

API

| axios                              |          |
| ---------------------------------- | -------- |
| axios(config)                      |          |
| axios(url,config)                  |          |
|                                    |          |
| axios.requires(config)             |          |
| axios.get(url.config)              |          |
| axios.delete(url,[,config])        |          |
| axios.post(url[, data[, config]])  |          |
| axios.head(url[,config])           |          |
| axios.option(url[,config])         |          |
| axios.put(url[, data[, config]])   |          |
| axios.patch(url[, data[, config]]) |          |
|                                    |          |
| axios.create([config])             |          |
|                                    |          |
| axios.all(iterable)                | 并发请求 |
| axios.spread(callback)             |          |

配置文件

axios方法有两类

- axios.get / post   // 请求方法的别名
	- axios.all(iterable) 并发 
- axios(config)

```js
// get
// get /user?ID=123  = get /user  params: {ID: 12345}
axios.get('/user?ID=123').then(res => {}).catch(err=>{})
axios.get('/user',{ params:{ ID :123}}).then().catch()

const axios = require('axios')
axios.get('http://192.168.1.15:3000/search?keywords=%E6%B5%B7%E9%98%94%E5%A4%A9%E7%A9%BA')
    .then(res => {
        console.log(res.data.result.songs[1])
    })
    .catch(err => {
        console.error(err);
    })
axios.get('http://192.168.1.15:3000/search', { params: { keywords: '林俊杰' } })
    .then(res => {
        console.log(res.data.result.songs[1])
    })
    .catch(err => {
        console.error(err);
    })


// post
axios.post('/user',{
	firstName: 'Fred',
    lastName: 'Flintstone'
}).then((res)=>{}).catch((err)=>{})

// axios.all([fuc(),fuc()]).then().catch()
function getUserAccount() {
  return axios.get('/user/12345');
}

function getUserPermissions() {
  return axios.get('/user',{ params :{ ID:1231 }});
}

axios.all([getUserAccount(), getUserPermissions()])
  .then(axios.spread(function (acct, perms) {
    // 两个请求现在都执行完成
  }));
```

```js
axios API
// post
axios([
	method:'post',
    url:'',
    data:{
      firstName: 'Fred',
      lastName: 'Flintstone'
    }
]);

// 发送 GET 请求（默认的方法） axios.()
axios('/user/12345');

 axios('http://120.78.149.188:3000/simi/song', { params: { id: 347230 } }).then((res) => {
            console.log(res)
        }).catch((err) => {
            console.log(err)
        })
```

创建实例  设置代理名

```js
// 可以把实例封装到axios.js 文件中
// 方法一
const instance = axios.create({
  baseURL: 'https://some-domain.com/api/',
  timeout: 1000,
  headers: {'X-Custom-Header': 'foobar'}
});

var instance = axios.create({
baseURL: 'http://120.78.149.188:3000',
timeout: 1000,
headers: { 'X-Requested-With': 'XMLHttpRequest' }
})

// console.log(instance)

instance.get('/top/mv?limit=10').then((res) => {
    console.log(response.data);
    console.log(response.status);
    console.log(response.statusText);
    console.log(response.headers);
    console.log(response.config);
}).catch((err) => {
console.log(err)
})
// 配置全局 方法二

var instance = axios.create();
instance.default.timeout = 2500

instance.get('/longRequest', {
  timeout: 5000
});

// 添加请求拦截器
axios.interceptors.request.use(function (config) {
    // 在发送请求之前做些什么
    return config;
  }, function (error) {
    // 对请求错误做些什么
    return Promise.reject(error);
  });

// 添加响应拦截器
axios.interceptors.response.use(function (response) {
    // 对响应数据做点什么
    return response;
  }, function (error) {
    // 对响应错误做点什么
    return Promise.reject(error);
  });

```

- 拦截器
- 错误处理
- 取消

## 安装

cdn
> axios 依赖于vue
```js
 <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
或
 <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<script src="https://cdn.staticfile.org/axios/0.18.0/axios.min.js"></script>
```
npm、yarn、bower
```bash
npm install axios
yarn add axios
bower install axios
```
```
https://heweiliang88.github.io/data.json
```
JSON 文件的构成
- 键值对
- 数组 （数组元素）可以是任何的数据类型
- 对象（键值对） 字符串类型要用双引号 
- 数组对象 // 对象数组
- 大括号
```js
axios 组成部分
// 方法部分(请求方法的别名)
get()
post()
create()
...
.then()	 // 数据处理部分
.catch() // 错误处理部分
```
### Get 方法

Get 方法解析JSON 文件
```html
<div id="app">
	{{msg}}
</app>
<div id="app">
	<h1 v-for="msgs in msg">
    	{{msgs}}
    </h1> 
</app>
var vm = new Vue({
	el:'#app',
	data():{
		msg:null
	}
	mounted():{	axios.get('https://heweiliang88.github.io/data.json')
			.then(response => (this.msg = response.data)) // response 读取 json 文件 response.data 读取json数据
// res => { this.msg = response.data }
			.catch(
				function(error){
					console.log(error);
				}
			)
	}
})
```
GET方法传递参数 URL （/user?ID=12345） 和  params :{ } 传递参数 (传递参数的两种方式)
```js
// 直接在 URL 上添加参数 ID=12345
axios.get('/user?ID=12345')
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  });
// 也可以通过 params 设置参数：
axios.get('/user', {
    params: {
      ID: 12345
    }
  })
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  });
```
### POST方法

```js
new Vue({
	el:'#app',
	data(){
		return{
			info:null
		}
	},
	mounted(){
		axios
			.post('https://heweiliang88.github.io/data.json')
			.then(response => (this.info = response))
			.catch(
				function(error){
					console.log(error);
				}
			)
	}
})
```
```js
axios.post('/user', {
    firstName: 'Fred',        // 参数 firstName
    lastName: 'Flintstone'    // 参数 lastName
  })
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  });
```
> GET  和 POST 的传递参数的方法
>
> GET  url 传递参数 和 params 传递参数
>
> POST 
```
axios.get('/user?firstname=he&&lastname=weiliang')
axios.get('/user',{
	params:{
        firstname:'he',
        lastname:'weiliang'
	}
})
axios.post('/user',{
	firstname:'he',
	lastname:'weiliang'
})
```
## axios API
| 方法                | 作用                  |
| ------------------- | --------------------- |
| axios(config)       | 发送POST请求          |
| axios(url[,config]) | 发送GET请求默认的方法 |
可以通过向 axios 传递 相关配置创建请求
```js
axios(config)
// 发送POST请求 axios({json}) 和上面的axios.get() / axios.post() 方法相同
axios({
	methods:'post',
	url:'/user/12345',
	data:{
		firstName:'HE'
        lastName:'WeiLiang'
	}
})
//  GET 请求远程图片
axios({
  method:'get',
  url:'http://bit.ly/2mTM3nY',
  responseType:'stream'
})
.then(function(response) {
  response.data.pipe(fs.createWriteStream('ada_lovelace.jpg'))
});
axios(url[, config])
// 发送 GET 请求（默认的方法）
axios('/user/12345');
```
>axios({methods、url、data})
## 请求方法的别名
> 请求方法提供了别名、可以直接使用别名来发起请求
```js
axios.request(config)
axios.get(url[, config])
axios.delete(url[, config])
axios.head(url[, config])
axios.post(url[, data[, config]])
axios.put(url[, data[, config]])
axios.patch(url[, data[, config]])
request、get、post、put、head、patch、delete
```
## 并发

同步和异步
处理并发请求的助手函数`all() 和 spread()`

```
axios.all(iterable); iterable 中的是一个数组
axios.spread(callback);
```
执行多个并发请求(就是同时执行多个请求) axios.all() 方法 
axios.all([函数1，函数2，函数3])
```js
function getUseAccount(){
	return axios.get('/user/12345');
}
function getUserPrermissions(){
	return axios.get('/user/12345/permission');
}
axios.all() // 方法 
axios.all([getUseAccount(),getUserPermissions()])
	.then(axios.spread(function(acct.perms){
		// 两个请求现在都在执行完成
}));
```
## 创建实例
使用方法 axios.create([config])
```js
axios.create([config])
const instance = axios.create({
	baseURL = '',
	timeout:1000,  // 超时时间
	headers: {'X-Custom-Header': 'foobar'} //头信息
}
```
### 实例方法

指定的配置将与实例的配置合并
```js
axios#request(config)
axios#get(url[, config])
axios#delete(url[, config])
axios#head(url[, config])
axios#post(url[, data[, config]])
axios#put(url[, data[, config]])
axios#patch(url[, data[, config]])
```
## 请求配置

### 响应结构(响应数据)

axios请求的响应包含以下信息（就是请求后返回的信息）
```json
{
	// data 由服务器提供的响应 数据
    data:{},
    // status HTTP 状态码
    status:200,
    //  statusTest 来自服务器响应的HTTP状态信息
    statusText:"OK",
    // headers 服务器响应的头信息
    headers:{}
    // config 是为请求提供的配置信息
    config:{}
}
```
```json
{ 
// data 由服务器提供的响应数据
"data": { "roles": { "name": "名字", "num": "数量", "companies": "公司种类" }, "name": "公司表", "num": 5, "companies": [ "腾讯", "Google", "github", "阿里巴巴", "百度" ], "effect": { "social": [ "腾讯", "Google", "github" ], "shopping": [ "阿里巴巴" ], "search": [ "Google", "百度" ] }, "sites": [ { "name": "Google", "info": [ "Android", "Google 搜索", "Google 翻译" ] }, { "name": "阿里巴巴", "info": [ "淘宝", "支付宝", "滴滴打车" ] }, { "name": "腾讯", "info": [ "王者荣耀", "微信", "QQ" ] }, { "name": "github", "info": [ "git" ] }, { "name": "百度", "info": [ "百度云", "百度搜索", "百度打车" ] } ] }, 
// 状态码
"status": 200,
//  statusTest 来自服务器响应的HTTP状态信息
"statusText": "", 
// headers 服务器响应的头信息
"headers": { "cache-control": "max-age=600", "content-length": "397", "content-type": "application/json; charset=utf-8", "expires": "Tue, 07 Jul 2020 01:38:21 GMT", "last-modified": "Mon, 06 Jul 2020 10:55:58 GMT" },
// config 是为请求提供的配置信息
"config": { "transformRequest": {}, "transformResponse": {}, "timeout": 0, "xsrfCookieName": "XSRF-TOKEN", "xsrfHeaderName": "X-XSRF-TOKEN", "maxContentLength": -1, "headers": { "Accept": "application/json, text/plain, */*" }, "method": "get", "url": "https://heweiliang88.github.io/data.json" }, "request": {} 
}
```
使用then 
```js
axios.get("/user/12345")
.then(function(response){
	console.log(response.data);
	console.log(response.status);
    console.log(response.statusText);
    console.log(response.headers);
    console.log(response.config);
});
then(response => (this.info = response))
```
使用catch
```
.catch(function(error){
	console.log(error);
})
```
### 配置默认值(default)

全局的 axios 默认值：
> 全局的axios(作用域作用在全局) 配置默认值，防止多次重复操作，减少代码的重复 URL headers.common/post
```js
axios.defaults.baseURL = 'https://api.example.com';  //默认URL
axios.defaults.headers.common['Authorization'] = AUTH_TOKEN;  // headers
axios.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded'; //post
```
自定义实例默认值
```js
// 创建实例设置默认配置的默认值
var instance = axios.create({
	baseURL:'https://api.example.com'
})
// 在实例已创建后修改默认值
instance.defaults.headers.common['Authorization'] = AUTH_TOKEN;
```
### 配置的优先级

> 配置会以一个优先顺序进行合并。这个顺序是：在 lib/defaults.js 找到的库的默认值，然后是实例的 defaults 属性，最后是请求的 config 参数。后者将优先于前者。
>
> lib/defaults.js库   => 实例的defaults  => config 参数  后者将优先于前者。
>
> 自定义创建实例默认值 > 实例的defaults > lib/defaults.js 库
```js
// 使用由库提供的配置的默认值来创建实例
// 此时超时配置的默认值是 `0`
var instance = axios.create();
// 覆写库的超时默认值
// 现在，在超时前，所有请求都会等待 2.5 秒
instance.defaults.timeout = 2500;
// 为已知需要花费很长时间的请求覆写超时设置 get 请求
instance.get('/longRequest', {
  timeout: 5000
});
```
## 拦截器

在请求或响应被then或catch 处理前拦截它们
> interceptors 拦截器  请求拦截器 和 响应拦截器
>
> interceptors.request.use()
```js
// 添加请求拦截器
axios.interceptors.request.use(
	function (config){
		return config;
	},function(error){
		return Promise.reject(error);
	}
});
// 添加响应拦截器
axios.interceptors.response.use(
	function (config){
		return config;
	},function(error){
		return Promise.reject(error);
	}
})
```
移除拦截器 `axios.interceptors.requeset.eject`
```js
var myInterceptor = axios.interceptors.request.use(function(){});
axios.interceptors.requeset.eject(myInterceptor);
// interceptors.use/eject 
```
可以为``自定义axios 实例``添加拦截器
```
var instance = axios.create();
instance.interceptors.request.use(function(){
})
```
> 自定义 axios 实例
>
> 创建axios 添加 拦截器
>
> 请求拦截器
>
> 直接使用拦截器
## 取消
使用 cancel token 取消请求
Axios 的 cancel token 
可以使用CancelToken.source 工厂方法创建 cancel token 

```js
var CancelToken = axios.CancelToken;
var source = CancelToken.source();
axios.get('/user.12345',{
	cacelToken:source.token
}).catch(function(thrown){
	if(axios.isCancel(thrown)){
		console.log('Requst canceled',thrown.message)
	}else{
	}
}})
source.cancel
```
## 错误处理
```js
axios.get('/user/123445')
.catch(function(error){
	if(error.response){
		console.log(error.response.data);
		console.log(error.response.status);
		console.log(error.response.headers);
	}else{
		console.log(’Error‘,error.message);
	}
	console.log(error.config);
});
```
`可以使用 validate Status 配置选项定义一个自定义 HTTP 状态码的错误范围。`
> validateStatus
```js
axios.get('/user/12345',funciton(){
	validateStatus:funciton(status){
		return status < 500  // 状态码在大于或等于500时才会 reject
	}
})
```
# axios二次封装

```js
axios.js
import axios from 'axios'
// @ == src  默认找config/index.js
import config from '@/config'
// 开发环境处理跨域问题
const baseUrl = process.env.NODE_ENV === 'development' ? config.baseUrl.dev : config.baseUrl.pro
class HttpRequest{
    constructor(baseUrl){
        this.baseUrl = baseUrl
    }
    request(option){
        {
            url:''
            methods:'get'
        }
        options =     
    }
}
export default new HttpRequest(baseUrl)    
```
```js
config/index.js
export default{
	title:'ele',
	baseUrl:{
		dev:'/api/'
        pro:''
	}
}
```

utils

```

```

