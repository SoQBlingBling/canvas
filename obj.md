### 1. canvas的像素化
-  我们使用canvas绘制了一个图形， 一旦绘制成功了 canvas就会像素化了他们 。我们没有办法再去获取这个图形 

### 2. canvas的动画思想
-  如果我们想让canvas图形移动，必须按照 清屏-更新-渲染的逻辑进行变成 ，总之就是重新再画一次
 
 ### 3.canvas的绘制功能
 
 1. 绘制前需要先获取canvas元素

 ```js
var canvas = document.getElementById('myCanvas')

```
 2. 得到画布的上下文 ，2d的上下文和3d的上下文，所有图像绘制都是通过上下文进行的和canvas元素就没有关系了
 ```js
 var ctx = canvas.getContext('2d')
 ```
