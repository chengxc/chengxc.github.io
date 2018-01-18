## 其他
### 介绍对vue的理解？
### 说说vue/react/angular等框架的优缺点？
### vue-router实现原理？
+ 1、有3种模式，默认是hash模式，还可以配置为history模式，以及服务端的abstract模式
+ 2、hash模式通过监听hashchange事件，监听hash值的变化，从而进行页面的跳转
+ 3、history模式通过监听popstate事件，监听历史记录的变化

### http和https有什么区别？

### 如何检测http的请求？如何检测https的请求？

### 如何检测手机访问的网站请求？

### vue中slot？
+ 在使用组件的时候，组件中间有一些代码，那么，在组件页面中，就可以使用slot标签来占位，表示那一段内容

### vue-router中params、query的区别？
+ params只能获取路由参数
+ query往路由对象中传递参数

### 请问vuex中保存的数据刷新页面是否依然存在？
+ 不存在

### 数组去重的2种方法？

### http状态码有哪些？301/302/304/401/403/204/206表示什么意思？
+ 301：永久重定向
+ 302：暂时重定向
+ 304：资源没有更新
+ 401：授权失败
+ 403：禁止访问

### 如何实现响应式布局？
+ 媒体查询
+ 百分比布局

### css中flex有哪些属性？
### 如何实现前端的单页应用程序？
+ 通过监听hashchange事件判断hash值的变化
+ 通过监听popstate事件监听history的变化

### 已知a页面跳转到b页面，想要实现在b页面回到a页面并刷新怎么做？

### vuex的使用过程？
+ state数据状态
+ mutations用来改变数据状态     
    - 规则：必须同步执行（不能执行异步的代码）
    ```js
    mutations:{
        changeState(state){
            state.count++;
        }
    }
    ```
+ actions用来提交mutations      
    - 每一个action函数都携带一个参数对象，这个参数中有一个commit方法用来提交mutation
        ```js
        actions:{
            increment(context){
                context.commit("changeState");
            }
        }
        ```
    - action通过dispatch触发：`store.dispatch("increment")`
    - action可以执行同步、异步的代码

### 如何实现vue中的组件之间通信？

### node使用过哪些框架？
+ express

### react、vue、angular有哪些不同？

### 如何看待前端路由和后端路由？

### vue组件之间如何通信？
+ 父传子通过属性
+ 子传父通过事件
+ 路由传参(query/params)
+ eventBus
+ 通过vuex状态管理

### vuex的实现过程？
+ action-->mutaion-->state
+ action.js：处理请求
+ mutaion.js：改变state里面的值

### 为什么要使用vuex进行状态管理？
+ 组件之间通信的成本增高。React 采用了单项数据流，但是现实中组件的通信往往不是单向的。子组件想要改变父组件的状态的话（逆向），就只能通过父组件传递 callback 作为 props 这种方式来进行。但是随着组件嵌套层数的增加，就不得不把 callback 一级级地传递下去，这样做的成本显然是非常高的。

+ 数据流变得模糊。也正是因为上文提出的组件间通信的问题，传递 callback 使得子组件能够”改变“父组件的 state。但是这样一来，React 的单项数据流也就在一定程度上被破坏了，数据流也因而变得非常模糊复杂。

+ 组件变得臃肿。有的时候几个组件共用一个 state，这时候就不得不把这个 state 提升到这几个组件的共同父级组件。在这种情况下，组件所持有的一些特定状态往往很不 make sense，而只是为了组件间通信而强行加上去，导致某些组件变得十分臃肿。

### DNS 查询过程？
+ 浏览器检查域名是否在缓存当中（要查看 Chrome 当中的缓存， 打开 `chrome://net-internals/#dns`）。
+ 查看操作系统DNS缓存：可以在命令行下使用 ipconfig /displaydns 来进行查看 
+ 检查域名是否在`本地 Hosts`里，Hosts 的位置 不同的操作系统有所不同
+ 查询本地 首选DNS 服务器,一般是运营商提供的
+ 运营商DNS会向根域发送DNS请求