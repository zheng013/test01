# HTML常用标签
## a标签的用法
1. 属性：href、target、download（少用）、rel=noopener（js）
2. 作用：跳转外部页面、跳转内部锚点、跳转到邮箱或电话

3. a的href的取值
* 网址（https://google.com、http://google.com、//google.com）
* 路径（a/b/c及a/b/c、index.html及./index.html）
* 伪协议（javascript:代码、mailto：邮箱、tel:手机号）
* id（href=#xxx 锚链接）
* 在http协议下的根目录和文件地址的目录不同
   
4. a的target取值
* 内置名字（-blank、-top、-parent、-self）
* 程序员命名（windows的name、iframe的name）

5. a的download
* 不是打开页面，而是下载页面
* 不是所有浏览器都支持，尤其是手机浏览器可能不支持

## img 标签的用法
* 作用（发出get请求，展示一张图片）
* 属性（alt、height、width、src）
* 事件（onload、onerror  js监听是否调用成功）
* 响应式（max-width:100% 满足手机的观看）
* 可替换元素（面试的时候可能会问到）
* 永远不要让图片变形作为前端开发，要么只写宽或高
* alt：当图片没有正常加载出来时，给出的提示

## table标签的用法
1. 相关的标签
* thead（表头）
* tbody（在里面放置tr、th、td）
* tfoot
* tr（一行）
* th （内容标题）
* td （内容）

2. 相关样式
* table-layout（行列的适应）
* border-collapse（合并）
* border-spacing（单元格之间的间距）

## 其他相关知识点
* 我们不用使用双击打开index.html的文件查看（因为在文件中打开，浏览器会默认使用文件路径去查找，可能会出现bug）
* 使用http-server查找网址，在网址后面加上你的路径即可
```(cmder)
yarn global add http-server
http . -c-1
```
* 使用parcel加上文件路径查看
```（cmder）
yarn global add parcel
parcel 文件名
```
* form里面的input要有name
* form里面要放一个type=submit，才能触发submit事件
* 其实常用的标签也就是那么几个，我们可以简单的记住这些标签的用法和属性。但是最重要的是我们要运用到实际的项目去，多做，多想，多写，这样才是最有效率的方法。
* 学习如逆水行舟，不进则退。希望自己能够坚持下来，每天进步一点点。相信自己一定可以达到自己的目标。

### 这些标签还是要多练习使用，才能记牢。相信我们都可以的！
 
谢谢观看！！！ 
