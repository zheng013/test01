# JS对象的基本用法

## 声明对象的两种语法

```(JavaScript)
let obj = { 'name' : 'paul' , 'age' : '22' }  //简单通用流行的写法
let obj = new Object({ 'name':'George' , 'age': '32' }) //标准官方的写法
```

## 如何删除对象的属性
```(JavaScript)
delete obj['name']  //推荐新手常用的删除的方法
delete obj.name //熟悉了解之后可用
```
## 如何查看对象的属性
```(JavaScript)
Object.keys(obj) // 查看对象的所有属性（包括隐藏属性）
console.dir（obj）//查看打印出对象的所有属性（包括隐藏属性）
obj.hasOwnProperty('name') //判断该属性是否为自身的属性
obj.name  obj['name']  //查看某个对象的具体的属性
Object.values(obj)  //查看对象的所有属性值
Object.entries（obj）  //查看对象所有属性和属性值
```
## 如何修改或增加对象的属性（写属性）
* 直接赋值
```(JavaScript)
let obj = { name: 'frank'} //name是字符串
obj.name='jack' //name是字符串
obj['name']='paul'
obj[name] = 'frank' // 错误，因为name变量值不确定
obj['na'+'me']='frank'
let key ='name',obj[key]='frank'
let key ='name',obj.key='frank' // 错误 因为 obj.key 等价于 obj['key']
```
* 批量赋值
```(JavaScript)
Object.assign(obj,{name:'frank',age:18})
```

## 'name' in obj 和 obj.hasOwnProperty('name')的区别

* 'name' in obj 是判断一个属性是否在对象中，不管是不是在对象地原型中。
*  obj.hasOwnProperty('name')只能判断属性是否在自身的对象中，而不是原型中。










