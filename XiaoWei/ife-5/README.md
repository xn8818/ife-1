# 任务五：零基础HTML及CSS编码（二） 

任务描述  
基于第一个任务“零基础HTML编码”的代码，参考 示例图，在步骤一的代码基础上增加CSS样式代码的编写   
头部和底部的黑色区域始终是100%宽  
页面右侧部分为固定宽度，左侧保持与浏览器窗口变化同步自适应变化  
左侧的各个模块里面的内容宽度跟随左侧整体宽度同步自适应变化  
10张图片需要永远都完整展现，所以会随着宽度变窄，从两行变成三行甚至更多，也有可能随着宽度变宽，变成一行  

任务注意事项  
只需要完成HTML，CSS代码编写，不需要写JavaScript  
示例图仅为参考，不需要完全实现一致，其中的图片、文案均可自行设定  
尽可能多地尝试不同的、更多的样式设定来实践各种CSS属性   
HTML 及 CSS 代码结构清晰、规范  

我的思路:  
1.总体布局是横向两列,左列自适应,右列固定宽度:    
  解决方法:  
  第一种:右列向右浮动,左列让他自动向上,设置margin-right值为右列盒子宽度.(注意这需要html里右列内容先于左列内容出现).  
  第二种:左侧设置margin-right值为右列盒子宽度,右侧绝对定位position:absolute;top:0; right:0;(之所以可以这样做是因为左列自适应高度绝对比右列要高,父元素就不会凹陷).  
2.对于图片自适应:  
  图片外层加一层div或者在其他元素容器内,例如:   
  < div class="img_wrap">  
  < img src ="" />  
  < /div>  
  则相应css样式设置为如下:  
.img_wrap{  
  max-width:xxpx;  
}  
.img{  
  width:100%;  
  height:auto;(这一句可以让图片保持比例放大缩小)  
  }  

      
