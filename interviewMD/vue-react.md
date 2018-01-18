## vue和react的比较
### 入门
+ vue入门更容易
    - vue是国人开发的，有非常易读的中文开发文档
+ react入门相对麻烦
    - react由facebook开发，中文文档有所劣势

### 组件渲染
+ react有个shouldComponentUpdate生命周期事件，需要自己去做处理从而防止组件重复渲染；
+ vue内部充分考虑了什么时候需要重新渲染组件

### vue模板和react中的jsx？
+ 简单来说，vue模板适合html操作比较习惯的开发(arttemplate)；jsx适合对js比较熟悉的开发
+ 抽象一点来看，我们可以把组件区分为两类：
    - 一类是偏视图表现的 ，我们推荐使用模板
    - 一类则是偏逻辑的 ，我们推荐使用 JSX 或渲染函数