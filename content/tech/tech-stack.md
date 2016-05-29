<!--
title: Kiteam的技术栈
-->

## 总揽

Kiteam前后端都是基于`Javascript`的方言`CoffeeScript`开发，前后端彻底分离，还包括命令行工具，通知服务器，逆向代理服务器，iOS客户端，Chrome插件等。

## Coffeescript

`Kiteam`是我用CoffeeScript开发的第三个大项目，也可能是最后一个，目前es6的开发体验已经挺不错了，不再需要这种语法糖，还是拥抱原生吧，要不以后麻烦。

## 后端

* `Node.js` - 不解释了吧
* `Knex` - 数据持久化，可以兼容Sqlite/MySql/PostalSql，不过目前Kiteam仅支持MySql
* `RestFul` - Kiteam的API遵从RestFul规范
* `MySql` - 数据库不用解析了，最初考虑用`sqlite`，不过`sqlite`编译安装太麻烦，后来干脆用`MySql`算了
* `Redis' - 用来做cookie保存，以及缓存，比如说像权限、用户列表这些都是读到redis缓存中的
* `express.io` - express.io就是`express + socket.io`，用起来还是蛮方便的。目前`WebSocket`主要是用来推送消息，另外在逆向代理中也是有用到`WebSocket`的。

## 前端

* `Angular` - Angular 1，其实还是蛮好用的，对于开发者来说，学习曲线略高
* `WebPack` - 最初Kiteam是用Silky打开构建前端代码的，开源后我改成了WebPack。主要是WebPack现在变得足够流行，有足够多的插件支持，使用起来也很简单，我不能因为我是Silky的作者就强行使用对吧。
* `Silky` - WebPack更好用，放弃治疗了，虽然我觉得还可以抢救一下
* `Less`
* `Charm.js` - 我写的另一个小工具，更优雅的方式调用RestFul API
* `Simditor` - Tower的编辑工具，简单好用
* `Socket.io` - 目前主要用来推送，未来可能会同时支持WebSocket和RestFul API两种接口

### 其它用到的模块(未列出所有)

* moment
* marked
* loadsh
* store2
* FileAPI

## 其它端

* iOS - 原生`Objective-C`代码
* 浏览器插件
* 命令行工具