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
### 分液器
+ 按钮有种水波扩散的效果.
+ 对box里的a标签设置分液器如下.
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
### 对transform的匀速运动.
+ 对一个盒子hover,如长宽或位置发生变化,都可以匀速处理.
+ 代码:transition:all 2s ease.
###嵌套崩塌
+ 两个盒子发生嵌套的时候，给子类设置maring会给父类造成一种崩塌现象，子类的margin-top没有效果，而直接作用到父类.
+ 解决方案： 1. 父类 overflow: hidden ; 2. 父类 设置极小的padding.
***
+ z-index可以指定一个整数作为参数，值越大元素显示的优先级越高，也就是z-index值较大的元素会显示在网页的最上层.