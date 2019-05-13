## DOM节点的获得
```
有三种方法;
document.getElementById('id名')
document.getElementsByTagName("div");
document.getElementsByClassName("a");
```
***
## 获取节点
```
1  父节点:
调用方式:调用者(节点).parentNode;

2  兄弟节点:
nextSibling：调用者是节点。（存在浏览器兼容问题);
nextElementSibling：在火狐谷歌IE9都指的是下一个元素节点;
兼容写法：nextEle =节点.nextElementSibling || 节点.nextSibling;

previousSibling：调用者是节点。IE678中指前一个元素节点（标签）。在火狐谷歌IE9+以后都指的是前一个节点（包括空文档和换行节点）
previousElementSibling：在火狐谷歌IE9都指的是前一个元素节点;

3  单个子节点
firstChild：调用者是父节点。IE678中指第一个子元素节点（标签）。在火狐谷歌IE9+以后都指的是第一个节点（包括空文档和换行节点）。
firstElementChild:在火狐谷歌IE9都指的第一个元素节点。

lastChild:调用者是父节点。IE678中指最后一个子元素节点（标签）。在火狐谷歌IE9+以后都指的是最后一个节点（包括空文档和换行节点）。
lastElementChild：在火狐谷歌IE9都指的最后一个元素节点;

4 所有子节点
childNodes  它返回指定元素的子元素集合，包括HTML节点，所有属性，文本节点,火狐 谷歌等高本版会把换行也看做是子节点

nodeType  ==  1  表示的是元素节点,记住,元素就是标签.
children  它返回指定元素的子元素集合;
children在IE6/7/8中包含注释节点.在IE678中，注释节点不要写在里面.
```
***

## DOM节点操作
```
1  创建节点  document.createElement();

2  插入节点  父节点.appendChild();
            父节点.insertBefore(要插入的节点,参考节点);
            父节点.insertBefore(要插入的节点,null); 在节点最后插入一个节点.

3  删除节点  父节点.removeChild(子节点);
            node.parentNode.removeChild(node);

4  复制节点  oldNode.cloneNode(true);  深层复制,如果是false,只复制节点本身.

5  节点属性(节点,属性)
            获取  getAttribute(名称);
            设置  setAttribute(名称,值);
            删除  removeAttribute(名称);
```
***
## DOM各种属性
```
onabort       图像加载被中断
onblur        元素失去焦点
onchange      用户改变域的内容
onclick       鼠标点击某个对象
ondblclick    鼠标双击某个对象
onerror       当加载文档或图像时发生某个错误
onfocus       元素获得焦点
onkeydown     某个键盘的键被按下
onkeypress    某个键盘的键被按下或按住
onkeyup       某个键盘的键被松开
onload        某个页面或图像被完成加载
onmousedown   某个鼠标按键被按下
onmousemove   鼠标被移动
onmouseout    鼠标从某元素移开
onmouseover   鼠标被移到某元素之上
onmouseup     某个鼠标按键被松开
onreset       重置按钮被点击
onresize      窗口或框架被调整尺寸
onselect      文本被选定
onsubmit      提交按钮被点击
onunload      用户退出页面
