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

### Nodejs 诞生的巨大意义

 一个 Web 项目 都有前台代码和后台代码组成 ，前台代码都是用 html + css + javascript 来写的 ，但是传统上由于本地机器上不能运 JS ，所以后台运行代码是不能用 JS 来写的 ，so我们还要学习另外一种语言才能写 Web 程序 ，通常用来 Web 后台程序的语言有 ：PHP 、Java 、C# 、Python 、Ruby 、Go ...

 所以 Nodejs 的意义就在于 ，现在开发者终于只要学习一种语言 ，就可以同时进行前台和后台的开发了 。

 ### Linux系统上 Nodejs 的安装

 具体步骤可以参考[Nodejs乐高安装第二小节](http://haoqicat.com/nodejs-lego)
