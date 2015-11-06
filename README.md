#前端编码规范
##说明
此手册由六月网络研发中心基于[编码规范 by @mdo](http://codeguide.bootcss.com/) 基础而编制
##黄金定律
不管有多少人共同参与同一项目，一定要确保每一行代码都像是同一个人编写的。
##HTML
###语法
* 用两个空格来代替制表符（tab） -- 这是唯一能保证在所有环境下获得一致展现的方法。
* 嵌套元素应当缩进一次（即两个空格）。
* 对于属性的定义，确保全部使用双引号，绝不要使用单引号。
* 不要在自闭合（self-closing）元素的尾部添加斜线 -- HTML5 规范中明确说明这是可选的。
* 不要省略可选的结束标签（closing tag）（例如，</li> 或 </body>）。
```Html
<!DOCTYPE html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company">
    <h1 class="hello-world">Hello, world!</h1>
  </body>
</html>
```

