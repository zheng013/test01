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

