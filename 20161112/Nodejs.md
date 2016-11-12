### 进入 Nodejs 的世界


在 [Nodejs 官网](https://nodejs.org/en/) 上可以看到 ， Nodejs 是

> 一个可以安装到本地机器上的 Javascript 运行环境

其实 ，传统上 Javascript 只能运行在浏览器里 ， 也就是说 Javascript 唯一的运行环境就是浏览器 。但是 Nodejs 出现以后 ，就可以在本地机器上执行 Javascript 了 。这个特点带来了 Web 开发的革命 。

比如 ， 我们有一个 main.js 文件 ，里面写一个

```
hello world
```

在几年前 ，想要执行这个 main.js 唯一的方法就是把它放在浏览器里执行 。

即 ：html中在 script 标签下添加 main.js 的路径

```
<script src='./main.js'></script>
```

但是本地安装 Nodejs 之后 ，就可以这样执行 main.js 了 ：

```
node main.js
```
其实 Nodejs 就是一个剥了皮的 Chrome 浏览器 。

---

### Nodejs 诞生的巨大意义

 一个 Web 项目 都有前台代码和后台代码组成 ，前台代码都是用 html + css + javascript 来写的 ，但是传统上由于本地机器上不能运 JS ，所以后台运行代码是不能用 JS 来写的 ，so我们还要学习另外一种语言才能写 Web 程序 ，通常用来 Web 后台程序的语言有 ：PHP 、Java 、C# 、Python 、Ruby 、Go ...

 所以 Nodejs 的意义就在于 ，现在开发者终于只要学习一种语言 ，就可以同时进行前台和后台的开发了 。

 ### Linux系统上 Nodejs 的安装

 具体步骤可以参考[Nodejs乐高安装第二小节](http://haoqicat.com/nodejs-lego)

---

### ES6 介绍

我们之前学习的 JS ，底层技术规范是 ES5 ，ES5 语法的特点就是 **可以直接在浏览器里执行** 。但是 ，当前成熟的工程师更多的是采用 **ES6 规范的 JS** ( 简称 ES6 ) 。

ES6 的特点 ，简单来说 ：

- 语法更完善 ，例如 ，不推荐使用 var ，而是使用 let const 来声明变量
- 功能更强大 ，引入了 class 关键字 ，从此 JS 有了面向对象的特性
- 语法更简单 ，这一点从 class 与 prototype 的使用去别上可以看到

所以 ，我们后续的课程会采用 ES6 来写程序 。

但是 ，ES6 目前的一个问题就是 ：很多 ES6 语法 ，浏览器不支持 。这个需要通过 **预处理** 来解决 。所谓所谓预处理 ，就是把 ES6 编译成 ES5 。那么 ，这个编译器就是Babel 。

---

### Babel 简介

Babel 的官网 ：http://babeljs.io/ 。官网上对它的描述是

>一个JS的编译器

它可以将 ES6 的语句转换为 ES5 。

到 Babel 官网 ，点击try it out 可以进入 Babel 在线的试用环境 ，左侧如果我们输入 ES6 语句 ，例如 ：

```
let i = 1；
```
那么右侧会将 ES6 语句翻译成 ES5语句 ：

```
var i = 1；
```

---

### Webpack + Babel 来编译 ES6

使用 Babel 的在线翻译环境 ，实际项目中没有办法使用 ，因此比较麻烦 。实际中 ，我们是使用命令行工具来自动化的完成编译工作的 。具体涉及道德工具就是 Webpack 和 Babel 。

---

### node 项目

新建一个项目( node 项目的名称用小写)

- 初始化 node 项目 'npm init' ，生成 package.json 文件
- 安装 Webpack ，Babel 模块

安装 Webpack

```
npm install webpack --save-dev
或者
npm install webpack -D
```

- 安装 Babel

在 Babel 官网下载 ，官网下找 setup 下 webpack

```
npm install --save-dev babel-loader babel-core
```

Webpack 使用时 ，需要增加它的配置文件 ，载配置文件里 ，记录 webpack 各项配置 ，它的配置文件默认 'webpack.config.js'

在 webpack.config.js 下粘贴以下代码 ( webpack 的配置信息 )
```
var path = require('path');

module.exports = {
    entry: path.resolve(__dirname, 'src/index.js'),
    output: {
        path: path.resolve(__dirname, 'build'),
        filename: 'bundle.js'
    },
};
```

执行 webpack 任务

```
./node_modules/.bin/webpack
```
