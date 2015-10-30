- 单页应用跳转新模板时，模板路径写相对路径，后退按钮失效。 所以要写绝对路径

- 路由路径写绝对路径，url参数要放在锚点路径后面，否则浏览器会让认为是新的连接。页面将会被重新初始化。全局变量失效，如$rootScope
 > window.location.href = "xxx.html#main" 与 window.location.href = "xxx.html?a=12#main"是两个页面
 > window.location.href = "xxx.html#main" 与 window.location.href = "xxx.html#main?a=12"是一个页面
 > $rootParam 可以获取到锚点后面的url参数