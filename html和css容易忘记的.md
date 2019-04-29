### 块状垂直居中.
+ 不知道父盒子高度的情况下,可以用transform.
+ html代码如下.
 ```
	<div class="box">
		<div class="son">
		</div>
	</div>
```
+ css代码如下.
```
.son{
			top:50%;
			transform: translateY(-50%);
		}
```
+ 同理水平方向用translateX().
***
### 分液器
+ 按钮有种水波扩散的效果.
+ 对box里的a标签设置分液器如下.
+ background-clip:content-box:使背景填充只对内容区域有效.
```其中background-clip:content是取消原背景色蔓延到border区域.
.box{
			height: 50px;
			width: 50px;
			background-color:pink;
		}
		a{
			display: block;
			width: 8px;
			height: 8px;
			background-color:yellow;
			border: 3px solid transparent;
			border-radius: 50%; 
			background-clip: content-box;
		}
		a:hover{
			border-color: yellow;
			background-color: white;
		}
```
***
### 对transform的匀速运动.
+ 对一个盒子hover,如长宽或位置发生变化,都可以匀速处理.
+ html代码如下.
```
<div class="box">
		<div class="son"></div>
	</div>
```
+ css代码如下.
```
.box{
			width: 800px;
			height: 200px;
			background-color:pink;
		}
		.son{
			width: 200px;
			height: 200px;
			background-color: yellow;
		}
		.box:hover .son{
			transform: translateX(600px);
			transition: all 4s ease;
		}
```
***
### 嵌套崩塌
+ 两个盒子发生嵌套的时候，给子类设置maring会给父类造成一种崩塌现象，子类的margin-top没有效果，而直接作用到父类.
+ 解决方案： 1. 父类 overflow: hidden ; 2. 父类 设置极小的padding.
***
+ z-index可以指定一个整数作为参数，值越大元素显示的优先级越高，也就是z-index值较大的元素会显示在网页的最上层.
***
### 规避脱标流
+ 能用标准流（没有脱标）解决就不用浮动
+ 解决不了就考虑有浮动（页面布局类型，“不完全脱标”）
+ 浮动解决不了用定位（小图标，完全脱标，不影响内容）
***
### margin-bottom无效的问题
+ 这不是定位...margin-bottom是下方的外边距，并不能让元素向下方移动，margin-top作为上边距，把元素“推”了下去。
***

