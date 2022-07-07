### 1.简介

- canvas是一个轻量级的画布，我们使用canvas进行javascript的变成，不需要增加额外的插件，创建的是位图，不可以支持事件

### 2.canvas 的基本使用
```js
 	//!需要先填充颜色然后才能执行绘制 不然颜色是不会生效的。
    //1.获取canvas元素

	var canvas = document.getElementById('canvas')
	
	//2.得到画布的上下文，上下文有两个2d上下文和3d上下文
	// 所有的图像绘制都是由ctx属性和方法设置的与canvas标签没有关系
	
	var ctx =canvas.getContext("2d")
	
	//4.设置颜色
	ctx.fillStyle = 'green'
	
	//3.绘制矩形

	//ctx.fillRect('x轴,y轴,宽,高')
	ctx.fillRect(100,100,200,50)

	

```

###  3.清除画布
- canvas一旦绘制不能再去修改，如果想要canvas 的图形改变 只能根据:清屏 -更新-渲染的逻辑执行
```js
	//clearRect(开始的x轴，开始的y轴，到x轴范围，到y轴的范围)
	ctx.clearRect(0,0,100,100)
```

```js
	var left = 100;
	var canvas = document.getElementById("canvas");
	var ctx = cavas.getContext('2d');
	ctx.fillStyle='blue';
	ctx.fillRect(100,100,200,200)
	setInterval(function(){
		ctx.clearRect(0,0,500,500)
		left++;
		ctx.fillRect(left,100,200,200)
	},10)
```

### 4. canvas绘制矩形
```js
		//4.设置颜色
	ctx.fillStyle = 'green'
	
	//3.绘制矩形

	//ctx.fillRect('x轴,y轴,宽,高')
	ctx.fillRect(100,100,200,50)

```

### 5.canvas 填充矩形
```js
	ctx.strokeStyle='red'
	ctx.strokeRect(100,100,200,200)
```

### 6.绘制路径

- 绘制路经是为了绘制不规则的多边形
- 路径都是闭合的 使用路经进行绘制的时候需要既定步骤
	- 需要设置起点
	- 使用绘制命令画出路径
	- 封闭路径
	- 填充或者绘制已经封闭路径的形状

```js
	//创建一个路径
	ctx.beginPath();
	//移动绘制点
	ctx.moveTo(100,100);
	//描述进行路径
	ctx.lineTO(200,100);
	ctx.lineTo(200,200);
	ctx.lineTo(100.200);
	// 闭合路径
	ctx.closePath();
	// 绘制这个不规则的图形
	ctx.strokeStyle='red';
	//绘制
	ctx.stroke()
```