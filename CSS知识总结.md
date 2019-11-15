# CSS知识总结

## 浏览器渲染原理

* 根据HTML构建HTML树（DOM）
* 根据CSS构建CSS树（CSSOM）
* 将两颗树合并成一颗渲染树（reader.tree）
* Layout布局（文档流、盒模型、计算大小和位置）
* Paint绘制（把边框颜色、文字颜色、阴影等样式画出来）
* Compose合成（根据层叠关系展示画面）
* 可利用chrome等浏览器开发者工具中Timelie-Paint-Layer查看优化（绘制分析器）

## CSS 动画的两种做法

### transition（过渡）
* 补充中间帧，实现动画效果
* transition:属性名|时长|过渡方式|延迟
* 截取部分代码
```（css）
#heart{
  display: inline-block;
  margin: 100px;
  position: relative;
  transition: all 1s;
  
}
#heart:hover{
  transform: scale(1.2);
  
}
```
* 过渡需要有起始（如hover和非hover状态）
* 让动画停留在最后一帧，在其声明上加上forward

### animation（动画）

* 声明关键帧，添加动画
* 配合@keyframe实现动画
```(CSS)
#heart{
  display: inline-block;
  margin: 100px;
  position: relative;
  animation: .5s heart infinite alternate-reverse;
  
}
@keyframes heart {
  0%{
    transform: scale(1);
  }
  100%{
    transform: scale(1.2);
  }
}    /*利用百分比控制范围*/

/*利用from to控制*/
{from{ transform:translateX(0%); }
to{    transform:translateX(100%);   }
}
```
* 










