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
* 不要省略可选的结束标签（closing tag）（例如，\</li\> 或 \</body\>）。
```HTML
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
###HTML5 doctype声明
为每个 HTML 页面的第一行添加标准模式（standard mode）的声明，这样能够确保在每个浏览器中拥有一致的展现。
```HTML
<!DOCTYPE html>
<html>
  <head>
  </head>
</html>
```
###语言属性
根据 HTML5 规范：

  强烈建议为 html 根元素指定 lang 属性，从而为文档设置正确的语言。这将有助于语音合成工具确定其所应该采用的发音，有助于翻译工具确定其翻译时所应遵守的规则等等。

更多关于 lang 属性的知识可以从 [此规范](http://www.w3.org/html/wg/drafts/html/master/semantics.html#the-html-element) 中了解。

这里列出了[语言代码表](http://reference.sitepoint.com/html/lang-codes)。
```HTML
<html lang="zh-CN">
  <!-- ... -->
</html>
```
###IE 兼容模式
IE 支持通过特定的 <meta> 标签来确定绘制当前页面所应该采用的 IE 版本。除非有强烈的特殊需求，否则最好是设置为 edge mode，从而通知 IE 采用其所支持的最新的模式。

阅读这篇 stack overflow 上的文章可以获得更多有用的信息。
```HTML
<meta http-equiv="X-UA-Compatible" content="IE=edge,Chrome=1" />
```
###字符编码
通过明确声明字符编码，能够确保浏览器快速并容易的判断页面内容的渲染方式。这样做的好处是，可以避免在 HTML 中使用字符实体标记（character entity），从而全部与文档编码一致（一般采用 UTF-8 编码）。
```HTML
<head>
  <meta charset="UTF-8">
</head>
```

