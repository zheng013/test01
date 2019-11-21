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
