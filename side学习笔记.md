directives指令主要是对原生的DOM的操作，
如果某个DOM操作你经常使用的话，可以封装成指令。
如果某个DOM操作比较复杂，也可以封装成指令。

mixins 的作用其实就是减少对data，methods，钩子的重复的引用  进行了一个
相对意义上的封装操作。

虽然extends的需求肯mixins的需求差不多一致，但是我们一般用于继承全局对象都必须需要的一些属性，才会用到这个构造选项。


函数调用后会去获取它的最新的值然后去进行一个渲染。

React.reate返回的元素是一个虚拟的dom元素。
习惯在return 后面加上()

2020-01-15 17:00
利用函数对象去调用，我们就可以拿到最新的值。然后去定义对象。{}
注意react框架下的元素，和函数元素的功用的区别。


一个返回react元素的函数就是一个组件。
element vs component
在vue里，构造选项就是一个组件。
小写 元素 const div = React.createElement('div',...）
大写 组件 const Div= () =>React.createElement('div',...)

函数组件 和 类组件

类:class Welcome extends React.component{
constructor(){
实例对象上会出现的属性
}

render(){
}
}

在类组件上传参，其上面的参数会自动的变成this下面的对应的值。


function Welcome（props）{
return （<div>
........
</div>）

}


this在普通函数中代表一个参数，取决于你如何去调用，所以值会有所不同。
而箭头函数不支持this，this代表它的原始值。

2020  -1-17-   10：28


由于赋值语句只在运行时执行，而function生成的匿名函数会在代码被执行之前就
被解析（hoisted），故可写在当前上下文的任意一个地方，因为其也可以被正常的调用。


存在一个解析的顺序问题。
call（this指向的对象，后面的参数只能够一个一个地去写）
apply(this指向的对象，后面的参数用一个数组去表示)

因为函数是 JavaScript 中唯一拥有自身作用域的结构，因此闭包的创建依赖于函数。
for(var i = 0; i < 10; i++) {
    (function(e) {
        setTimeout(function() {
            console.log(e);  
        }, 1000);
    })(i);
}
自执行匿名函数。
arguments是一个管理所有传递到函数参数的一个参数列表的伪数组
这个参数列表的数组并不会从Array.prototype上继承数组的属性
有for循环遍历的方法，利用Array.prototype.slice.call(arguments)
这个转换较慢，不推荐。

v-pre不会对内容进行一个替换，只是会显示相对应有东西
不管是vue还是react在模板下都需要有一个包围的div对齐
<ul>
<li v-for="(u,index) in users" :key="index"> 这里的key是为了便于区分才加上的
一般我们会用id来进行绑定识别。
{{index}} {{u.name}}
</li>
</ul>

廖雪峰的教程

-------------------------------arguments往下函数之前的传参


项目的建立
1.yarn global add vue@cli 
2.vue create 目录名
3.cd 
4.yarn serve 
5.Vue.use(Vuerounter)


类型---------------------     2020-01-20
对象比较
虽然 == 和 === 操作符都是等于操作符，但是当其中有一个操作数为对象时，行为就不同了。
这里等于操作符比较的不是值是否相等，而是是否属于同一个身份；也就是说，只有对象的同一个实例才被认为是相等的。 这有点像 Python 中的 is 和 C 中的指针比较。

例子：
{} === {};                   // false
new String('foo') === 'foo'; // false
new Number(10) === 10;       // false
var foo = {};
foo === foo;                 // true

typeof 操作符
typeof 操作符（和 instanceof 一起）或许是 JavaScript 中最大的设计缺陷， 因为几乎不可能从它们那里得到想要的结果。

尽管 instanceof 还有一些极少数的应用场景，typeof 只有一个实际的应用
（译者注：这个实际应用是用来检测一个对象是否已经定义或者是否已经赋值）， 而这个应用却不是用来检查对象的类型。
JavaScript 标准文档只给出了一种获取 [[Class]] 值的方法，那就是使用 Object.prototype.toString。

Object.prototype.toString 返回一种标准格式字符串，所以上例可以通过 slice 截取指定位置的字符串，如下所示：

Object.prototype.toString.call([])    // "[object Array]"
Object.prototype.toString.call({})    // "[object Object]"
Object.prototype.toString.call(2)    // "[object Number]"


*** 为了检测一个对象的类型，强烈推荐使用 Object.prototype.toString 方法； 

因为这是唯一一个可依赖的方式。正如上面表格所示，typeof 的一些返回值在标准文档中并未定义， 因此不同的引擎实现可能不同。

除非为了检测一个变量是否已经定义，我们应尽量避免使用 typeof 操作符。------

instanceof 操作符
instanceof 操作符用来比较两个操作数的构造函数。只有在比较自定义的对象时才有意义。
 如果用来比较内置类型，将会和 typeof 操作符 一样用处不大。

内置类型（比如 Number 和 String）的构造函数在被调用时，使用或者不使用 new 的结果完全不同。

new Number(10) === 10;     // False, 对象与数字的比较
Number(10) === 10;         // True, 数字与数字的比较
new Number(10) + 0 === 10; // True, 由于隐式的类型转换
使用内置类型 Number 作为构造函数将会创建一个新的 Number 对象， 而在不使用 new 关键字的 Number 函数更像是一个数字转换器。

字符串转换为数字的常用方法：

+'010' === 10
Number('010') === 10
parseInt('010', 10) === 10  // 用来转换为整数

+'010.2' === 10.2
Number('010.2') === 10.2
parseInt('010.2', 10) === 10
转换为布尔型
通过使用 否 操作符两次，可以把一个值转换为布尔型。

!!'foo';   // true
!!'';      // false
!!'0';     // true
!!'1';     // true
!!'-1'     // true
!!{};      // true
!!true;    // true



---------------核心（JS）
这个语言也定义了一个全局变量，它的值是 undefined，这个变量也被称为 undefined。
 但是这个变量不是一个常量，也不是一个关键字。这意味着它的值可以轻易被覆盖。

JavaScript 中的 undefined 的使用场景类似于其它语言中的 null，实际上 JavaScript 中的 null 是另外一种数据类型。

JavaScript 不是一个没有分号的语言，恰恰相反上它需要分号来就解析源代码。
因此 JavaScript 解析器在遇到由于缺少分号导致的解析错误时，会自动在源代码中插入分号。

自动的分号插入被认为是 JavaScript 语言最大的设计缺陷之一，因为它能改变代码的行为。

代码里面存在括号的话，javascript都会相应的往上去靠一个函数的，除非没有内容。可以加上一个！或者使用加分号;的代码风格


其他

定时处理不是 ECMAScript 的标准，它们在 DOM (文档对象模型) 被实现。

基于 JavaScript 引擎的计时策略，以及本质上的单线程运行方式，所以其它代码的运行可能会阻塞此线程。 
因此没法确保函数会在 setTimeout 指定的时刻被调用。

作为第一个参数的函数将会在全局作用域中执行，因此函数内的 this 将会指向这个全局对象。

手工清空定时器
可以通过将定时时产生的 ID 标识传递给 clearTimeout 或者 clearInterval 函数来清除定时， 至于使用哪个函数取决于调用的时候使用的是 setTimeout 还是 setInterval。

var id = setTimeout(foo, 1000ms);
clearTimeout(id);

注意点：
@@##**setTimeout 的第一个参数是函数对象，一个常犯的错误是这样的 setTimeout(foo(), 1000)， 
这里回调函数是 foo 的返回值，而不是foo本身。 大部分情况下，这是一个潜在的错误，
因为如果函数返回 undefined，setTimeout 也不会报错。



处理可能的阻塞调用
最简单也是最容易控制的方案，是在回调函数内部使用 setTimeout 函数。

function foo(){
    // 阻塞执行 1 秒
    setTimeout(foo, 100);
}
foo();
这样不仅封装了 setTimeout 回调函数，而且阻止了调用指令的堆积，可以有更多的控制。
 foo 函数现在可以控制是否继续执行还是终止执行。


setTimeout 和 setInterval 也接受第一个参数为字符串的情况。 这个特性绝对不要使用，因为它在内部使用了 eval。






















vue router ---HTML5的History模式下的后端支持。

原生 Node.js
const http = require('http')
const fs = require('fs')
const httpPort = 80

http.createServer((req, res) => {
  fs.readFile('index.htm', 'utf-8', (err, content) => {
    if (err) {
      console.log('We cannot open "index.htm" file.')
    }

    res.writeHead(200, {
      'Content-Type': 'text/html; charset=utf-8'
    })

    res.end(content)
  })
}).listen(httpPort, () => {
  console.log('Server listening on: http://localhost:%s', httpPort)
})




项目的建立
1.yarn global add vue@cli 
2.vue create 目录名
3.cd 
4.yarn serve 
5.Vue.use(Vuerounter)

