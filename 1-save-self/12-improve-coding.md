如果这篇文章你读完只记住一句话，请记住这句：

**说出自己的每行代码是什么意思**。

## Before All

几乎所有的计算机专业笔试都会带上算法题。

关于算法题的声音历来呈对立态势。有人说数据结构很实用，说算法能锻炼思维，锻炼在压力环境下解决问题的能力，但也有人说算法题都是花招之类，说一块奖牌没多大用。

虽然声音不统一，但是可见的是，只要有笔试，不管是申请实验室还是找工作，算法题是常客。所以，即使不从纯粹的学术角度出发，在刚进入大学的时候，多刷算法题还是对自己的发展还是很有帮助的。

如果是刚刚入坑计软网的小白，首先推荐去[洛谷](https://luogu.com.cn/)的题单，把官方题单刷一遍。刚开始刷题时，即使自己完成了，也要看题解中是否有更优秀的方案（一般是没有，leetcode 这种时间卡得松的会有）；如果独立完成不了，思考最多 10 分钟，去把题解看懂，不要觉得气馁，因为很多题目都需要特定的数据结构和算法，你只是不知道而已。

一般~~只~~需要掌握以下内容：

* 基础：程序控制语句、数组、指针、函数
* 基础算法：排序、穷举、贪心，等
* 数据结构：链表、二叉树、图，等
* 图论：搜索、最短路、连通性、连通分量
* 询问：区间最值、单点修改区间维护、区间修改区间维护，以及各种变种
* 动态规划与记忆化搜索
* 数论（密码学）
* 数值计算（较少）
* 计算几何（CAD 之类）
* 等等

熟练掌握了这些（大概 500 道题的训练），你应该能通过该通过的笔试了。

如果做不到，也没关系，按照自己的安排有选择地完成一些也可以。

## 工程导向

### 工欲善其事

首先，**不要相信 `vim` 是地表最强编辑器**之类的鬼话。`vim` 在控制台应用里有一定应用，但其产生的 `swp` 文件**可能造成信息泄露**，所以不管是在开发环境还是在生产环境大量使用 `vim` 都是**强烈不建议**的，投入大量时间研究其插件体系也是极大的浪费。

其次，我们要选择合适的工具。（非广告）

* `IntelliJ IDEA`：强大且全面的`Java IDE`，JetBrains 公司开发。分为 Community 和 Ultimate 版本。Community 为纯 Java IDE，Ultimate 提供了 Python、JavaScript、Go、数据库等支持。其它主流语言也有配套的 IDE 支持。
* `Visual Studio`：`Windows` 下最强调试器，微软开发。提供很棒的 `C#` 和 `C++` 开发体验。同时可以提供 Python、Node.js 等的支持。
* `Visual Studio Code`：轻量级编辑器，微软开发。其以强大的插件体系，基于 `Language Server Provider` 的语法提示，以及优雅的界面和快捷键操作而广受好评。

### 技术栈的选择

技术栈的概念是经常在一起使用的，能够构成一整个系统的许多技术的有机结合。

#### `Web` 方向技术栈举例讲解

##### `Java` Web

首先学习 `Java` 的基础语法，一开始就用 `Maven` 或者 `Gradle` 构建项目，保证工程开发的规范性；学习基础语法、`Collection`、标准库等，对反射、`Java Native Interface`、多线程等也要有所涉及。此阶段“巧”不如“拙”，最好是踏踏实实地把每一个看起来很“笨”的知识点学明白、试明白。

数据库方面，学习 `MySQL` 的设计范式和性能优化，做一些面试或笔试的题目，或者设计一个较大的数据库系统。

Web 前端方面，学习 HTML + CSS + JavaScript，达到能做可以展示的界面的效果。

之后考虑 SSH（Spring+Struts2+Hibernate）或 SSM（Spring+SpringMVC+MyBatis）框架，利用这些知识开发一些 Web 项目、服务器项目等。

然后可以进行一些拓展。把 Spring 的大部分学完，可以学习 Spring Boot 的相关内容；也可以学习 `Kotlin`、`Groovy` 或 `Scala` 等基于 `Java`的语言，或者学习 Android 开发等。Docker 部署方式也要学习一下。

##### `JavaScript` 技术栈

`JS` 栈的优点多端通吃：`Web` 是最擅长的，可以使用 `React`、`Angular`、`Vue.js` 等成熟的框架和 `Webpack`、`Vite` 等打包工具；桌面端可以使用 `Electron` 框架；移动端有基于 `Vue` 的 `uni-app` 和基于 `React` 的 `React Native`等框架（虽然二者都不主流）；后端可以使用 `Node.js` 软件，`Express`、`Koa` 等框架快速构建服务器程序。

但其缺点也明显：官方、民间标准繁杂，各标准下构建的模块交互困难；另外 `Node.js` 的性能相比 `Go`、`Java` 等也相差一段距离。类型上，`JS` 是 `duck typed` 语言，属于弱类型，并且在很多 `corner case` 中表现奇葩，被戏称为“黑洞”。

`TypeScript` 是微软推出的基于 `JS` 的**强类型**语言，最终可以编译到 `JS`，运行在浏览器或 `Node.js`，在静态类型安全检查上做了很大贡献。还有一些历史久远的项目只支持 `JS`，类型检查上需要使用专用的类型定义文件才能使用。不过 `TS` 的应用也越来越广泛，使用 `TS` 开发逐渐成为行业共识。

首先学习 `JavaScript` 语法，或者直接学习 `TypeScript`。

推荐红宝书《JavaScript 高级程序设计》，或者犀牛书《JavaScript 权威指南》。~~相信你会被这门语言折磨到。~~

### 做实际项目

做几个项目，精益求精的那种。

可以是自己想做的东西，可以是仿造市面上一个流行软件，也可以是接一些外包项目。

认真对待每一个项目，不要随写随丢，一个大型项目比一百个小型项目能锻炼人。

### 培养读源码/原文档的能力

在接触一段时间之后，就会发现：百度一下能找到的东西太有限了。很多知识都存在于官方文档中，甚至为了明白到底发生着什么需要直接进入所引用模块的源码，将来就慢慢地熟悉了。