## 美团
### ES6知道哪些新语法
+ let/const
+ 模板字符串
+ 箭头函数
+ 解构赋值
+ class
+ 模块化
+ promise

### 介绍promise的使用方式？有哪些实例方法？then的第二个回调和catch有什么区别？如果连续调用then有什么结果？

### async的使用方式？如何捕获错误？

### webpack、gulp各自的优缺点

### 继承的实现方式
+ 给原型添加方法
    ```js
    F.prototype.say=function(){}
    ```
+ 修改构造函数的原型对象
    ```js
    F.prototype={ 
        constructor:F,
        say:function(){} 
    }
    ```
+ 拷贝继承：将一个对象中的属性拷贝到另一个对象中

+ 借用构造函数
    ```js
    function Parent(a,b,c){
        this.a=a;
        this.b=b;
        this.c=c;
    }
    function Child(a,b,c,d,e){
        Parant.call(this,a,b,c);
        this.d=d;
        thid.e=e;
    }
    ```
+ 经典继承：Object.create

### 如何实现让一个元素垂直+水平居中

### node里面用过哪些express中间件
+ router
+ cookie
+ bodyparser

### vue和react有哪些区别

### vue生命周期？react生命周期
+ vue生命周期：beforeCreate/created/beforeMount/mounted/beforeUpdate/updated/beforeDestory/destroyed

### 为什么要使用vuex
+ vuex实现状态管理，也就是追踪、管理数据状态

### vue如何实现双向绑定

### 如何实现一个bind方法

### 封装一个函数，传入数组：[1,[2,3],[4,[5,6]]]，返回[1,2,3,4,5,6]

### es6的类和普通构造函数+原型的实现有什么不同

### 分析以下代码的执行结果：let {a:m}={a:3};
+ 创建一个块级作用域的变量：m，值为3

### 原型链

### JS有哪些数据类型
+ 数字、字符串、布尔值、null、undefined、对象

### 如何判断某个数据是一个数组
+ Array.isArray
+ Object.prototype.toString.call(arr)==="[object Array]"

### 如何实现事件委托？
+ 把事件绑定在父元素中，在事件回调函数汇中，通过判断事件对象的e.target属性判断事件源，根据事件源执行不同的事件

### 原生js有哪些兼容性问题？
+ innerText/textContent
+ innerHTML
+ getComputedStyle/currentStyle
+ addEventListener/attachEvent

### 你觉得typescript有哪些特点
+ 强类型
+ 装饰器

### 原生ajax如何实现？

### 跨域解决方案？
+ jsonp
+ window.name
+ iframe

### http状态码有哪些？301、302、304、401、403、404、500分别表示什么？
+ 301：永久重定向
+ 302：暂时重定向
+ 304：资源没有更新
+ 401：权限不足
+ 403：访问被拒绝
+ 500：服务器错误