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

