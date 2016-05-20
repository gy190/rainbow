- 单页应用跳转新模板时，模板路径写相对路径，后退按钮失效。 所以要写绝对路径

- 路由路径写绝对路径，url参数要放在锚点路径后面，否则浏览器会让认为是新的连接。页面将会被重新初始化。全局变量失效，如$rootScope
 > window.location.href = "xxx.html#main" 与 window.location.href = "xxx.html?a=12#main"是两个页面
 > window.location.href = "xxx.html#main" 与 window.location.href = "xxx.html#main?a=12"是一个页面
 > $rootParam 可以获取到锚点后面的url参数

- 不支持多个ng-view，貌似可以用ui-router组件解决
 > 基页状态如何保证？


-结合实际业务场景使用angularjs ： 用都不会，谈不上原理的理解。 太简单，不符合实际的业务需求。
 - 场景1： 路由， 路由的坑：相对路径，锚点不能回退。绝对路径可以。 router时的controller懒加载问题。  path后面带url参数，全局变量丢失的问题
 - 场景2： 事件绑定
 - 场景3： 动态添加dom   ng-repeat
 - 场景4： 动画
 - 场景5： $http扩展
 - 场景6： controller  service（共享数据）  factory provider（可以注入config，初始化数据） config是什么鬼
 - 场景7： 数据驱动本质上是：数据驱动dom变化。  在事件驱动之后加入了数据驱动（封装了dom操作）。
 - 场景8： 过滤器、自定义过滤器
 - 场景9： 只使用行内事件，通过监听数据变化进行相应的操作