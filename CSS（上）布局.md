## Float布局
* 子元素加float
* 父元素(class="clearfix)
```(css)
.clearfix::after{
 content='';
 display:block;
 clear:both;
 img{max-width:100%;/*处理图片类型的文档加上最大宽度百分百，并且只给出宽高中任意一值*/
     vertical-align:middle;/*消除图片在div下的多余背景内容*/}
 /*起手式*/  *{ padding:0;margin:0;box-sizing:border-box;}
 /*清除列表样式*/ ol,ul{list-style:none;}
 
 /*让整个块居中*/{margin-left:auto;margin-right:auto;}
 
}
```
* reverse-将起点放至默认终点开始
* order-的默认开始处是0
* 负margin用于调试元素的对齐空间的给出
* inline-block尽量将元素缩窄且依次排列，block将元素固定在一行上由其中的文本流元素决定的尺寸
* flex会消除margin合并在使用需要注意margin边距要减半

