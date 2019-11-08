# HTML入门知识点总结（第九到十课）
## HTML概览

1. 知识一(概念介绍）
* HyperText Markup Language (超文本标记语言）
* WWW(万维网)是基于互联网的基础上建立的
* HTML之父—Tim Berners-Lee (发表了一遍文章HTML-Tags）
* WWW=URL(网址)+HTTP(服务器)+HTML(网页)
* 互联网的本质—就是内容的共享

2. 知识二(如何制作出网页)
* 域名知识
* HTTP服务器知识
* HTML知识
* 其他(js css 等等）

3. 知识三
* 原始的18个标签（ title h1~h6 nextid address base hp1/hp2 a dl/dt/dd isindex ul/li listing menu p dir )
* H5指的就是在手机上呈现的页面
* 利用较为权威的[MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)学习HTML知识
* 狭义的HTML5(标签 css 等等）
* 广义的HTML5（HTML5的技术合集，详情可查看MDN文档）

4. 知识四(正确的学习HTML的方法)
* 把所有标签读一遍，并理解用法。
* 最重要的记住div/span标签
* 找页面仿写,记忆遗忘曲线—要多写，多改。

5. 知识五(体系化学习-学习一门语言)
* 语法(大小写有区别吗 要加引号吗 如何注释(CTRL+/） 如何组合）
* 如何调试(看vscode、webstorm的颜色提示，使用HTML5验证器 ）
```(cmder)
yarn global add node-w3c-validator
node-w3c-validator -i index.html
```
* 在哪里查资料（MDN文档）
* 标准制定者(w3c委员会，区别于w3cschool）

## HTML标签
1. 英语小课堂(重要的英文解释)

  英文|翻译| |英文|翻译
  ---|---|---|---|---
  heading|标题|  |order|顺序|
  body|正文|  |ordered|有顺序的|
  paragraph|段落|  |unordered|无顺序的|
  section|章节|  |description|描述|
  article|文章|  |term|术语|
  main|主体|  |data|数据|
  aside|旁边的|  |quote|引用|
  anchor|锚、定点|  |block|块|
  strong|内容重要|  |inline|行内[计]|
  emphasis|强调(语气)|  |break|打断|
 
 2. 学习工具
 * 三上：马上、枕上、厕上（欧阳修）
 * 《网道HTML教程》免费书籍，可用于平时阅读
 * vscode插件：prettier（更好的代码格式化美化工具）
 * jsBin.com在线编辑器（可将自己写的代码，复制路径给同学或老师纠错）
 * 代码沙盒（codesand.com 在线编辑器）
 
 3. HTML起手式
 * Emmet！
 ```(html)
 <!DOCTYPE html> <!--文档类型-->
 <html lang="en"> <!--html标签，可把lang变成lang="zh-cn"-->
 <head>
 <meta charset="UTF-8"> <!--文件的字符编码-->
 <meta name="viewport" content="width=device-width,initial-scale=1.0"> <!--禁用缩放，兼容手机-->
 <meta http-equiv="X-U-Compatible" content="ie=edge"> <!--告诉ie浏览器使用最新内核-->
 <title>Document</title><!--标题-->
 </head>
 <body>
 
 </body>
 </html>
 ```
4. 章节标签(表示文章/书的层级 常用的表章节的标签有哪些)

  标签|用途(翻译)
  ---|---
  h1~h6|一级标题到六级标题
  section|章节
  article|文章
  p|段落
  header|头部
  footer|脚部
  main|主要内容
  aside|旁支内容
  div|划分（区域 块）
  &copy|版权声明标致

5. 全局属性(所有标签都拥有的属性)

  标签|用途(翻译)
  ---|---
  class|类、标记
  contenteditable|可直接在编辑器页面中编辑文档内容
  hidden|隐藏元素
  title|属性标签（显示完整内容）
  style|元素的样式（优先级更高比css）
  tabindex|可利用tab切换（顺序访问）
  
 6. 知识点
  * tabindex=0(利用tab键切换最后才访问)  tabindex=-1(不访问该模块)
  * 文字过长但只想让其显示一行并出现省略号
  ```(html)
  style{
  white-space:nowrap;
  text-overflow:ellipsis;
  overflow:hidden;}
  ```











