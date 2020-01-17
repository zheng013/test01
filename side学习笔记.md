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
