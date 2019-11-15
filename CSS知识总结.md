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
* animation: 时长|过渡方式|延迟|次数|方向|填充模式|是否暂停|动画名

## 其他相关的知识点
* 需要动画的优化时可查看Google团队写的文章，可以写成blog以备面试时所需
* 性能指的是避免执行工作的艺术，并尽可能使您执行的任何操作都高效
* 三种更新样式：①JS/CSS→样式→布局→绘制→合成  ②JS/CSS→样式→绘制→合成 ③JS/CSS→样式→合成
* 不同的属性名会触发不同的更新流程（可通过csstriggers.com网站查看）
* 要使用translate的Z属性，需要先确定一个perspective的三维中心点
* 要学会去看懂MDN中关于属性的语法示例
* inline元素不支持transform，需先变成block
* display：none  不会添加到渲染树里面 
* visiblity：hidden属于隐藏效果，该元素虽然消失，但还是会占住原来的位置
* opacity（透明度）background 可以实现过渡  rgba（255，0，0，1/0.5/.....）
* border-radius: | |  |  |

### CSS动画这一块的知识感觉用到比较少，最重要的熟悉语法和css的操作，可以看看动画优化那一块的技术文章。

-----css布局和定位的知识blog后续会更新补上------
加油呀，每天都有比昨天更好
#### 谢谢观看！














