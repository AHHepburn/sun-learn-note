## jQuery
+ 引用  
```
<script src="lib/jquery-3.4.1.min.js"></script>
```
***
### 基本选择器
```
    $('h2').css('color','red');  通过标签选择器

    $('.p1').css('color','blue');  通过class选择器

    $('#d1').css('background-color','green');  通过id

    $('.d3 .box').css('color','orange');  后代选择器

    $('.d2,.d3').css('backgroundColor','black')  并集选择器

    $('.d3.active').css('background-color','pink')  交集选择器
```
***
### 层级选择器
```
css当中也可以使用

.li3+li  选择紧挨着的下一个元素

.li3~li  后面的所有兄弟元素

.d1>.box  子代选择器,直接孩子,不管孙子

$('.li3+li').css('color','red');
$('.li3~li').css('background-color','red');
$('.d1>.box').css('width','400px')
```
***
## 过滤选择器
```
$('li:eq(1)').css('background','red');  对下标为1的li标签设置属性

$('li:gt(5)').css('background','red');  选择序号大于5的li标签

$('li:lt(5)').css('background','blue');  选择序号小于5的li标签

$('li:first').css('background','red');  第一个

$('li:last').css('background','red');  最后一个
```
***
## 关系查找
```
$('.box').find('div').css('color','red');  查找指定元素的所有后代元素

$('.box').children().css('color','orange');  查找指定元素的直接子元素（亲儿子元素）

$('.li3').siblings().css('color','red');  查找所有兄弟元素（不包括自己）

$('.d2').parent().css('width','200px');  查找父元素
```
***
## 变色
```
var colorBefore = '';
$('li').mouseenter(function(){
    colorBefore = $(this).css('background-color');  获取之前的颜色
    $(this).css('background-color','red');
})
$('li').mouseleave(function(){
    $('this).css('background-color',colorBefore);
})
```
***
## dom对象和jQuery对象转化
```
jQuery对象后加上[0]或get(1)即可转换为dom对象
$(boxEl)
```
***
## attr属性
```
$('.box').attr('class');  获取boxclass属性

$('.box').attr('class','danger');  往class里设值danger类名

$('div').removeAttr('class');  删除div里的class
```
***
## 取值设值
```
$('.box').text();  获取文本内容

$('.box').text('天气很好');  设值文本内容

$('ul').html('<p>今天天气很好</p>');  在ul里添加p标签

$('input').val();  获取表单内容

$('input').val('呵呵呵');  设值表单内容;
```
***
## 操作类名
```
$('p').addClass('danger strong');  向被选元素添加一个或多个类,有则不加

$('p').removeClass('strong');  从被选元素删除一个或多个类

$('p').toggleClass('em');  对被选元素进行添加/删除类的切换操作  (有则删除,无则添加)

$('p').hasClass('strong');  判断是否存在相应类名
```
***
## 节点操作
```
var $spanNode = $('<span>我是一个span元素</span>');  创建节点

$('.box').html($spanNode);

$('.box'),append($spanNode);  从后追加元素

$(selector).appendTo(node);  把selector追加到node里

prepend()  在元素的第一个子元素前追加

$(selector).after(node);  在node之后追加selector  

before()

$('.box').empty();  清空选中节点的所有子节点(包括内容和节点)

$('.box').remove();  清空,包括自己

$('.box').clone();  复制
```
***
## 表单prop
```
    <input type="checkbox" class="like">
    <input type="radio" class="sex">
    <button class="btn1">获取选中状态</button>
    获取表单当中 单选框 和 多选框的状态
        $('.btn1').click(function(){
            console.log($('.like').prop('checked'));
            console.log('单选框状态',$('.sex').prop('checked'));

        })
    $("input[type='checkbox']").prop("checked");  返回true或false

    用于遍历 form表单中的多选框和单选框的选中状态
    $('.btn1').click(function()  {
    alert($('.like').prop('checked'));
    alert($('.sex').prop('checked'));
    })
```
***
## 动画
```
$('.box').show(2000);  2000毫秒后显示
show有三个值  slow  normal  fast

$('.box').show(1000,function(){
    $('.box').css({
        width:'200px',
        height:'200px',
        backgroundColor:'green'
    })
});  动画结束后,执行function

$('.box').hide(2000);  隐藏

$('.box').slideDown(2000);  滑下

$('.box').slideUp(2000);  滑上

$('.box').slideToggle(1000);  滑下滑上

$('.box').fadeIn(2000);  淡入

$('.box').fadeOut(1000);  淡出

$('.box').fadeToggle(1000); 淡入淡出

$('.box').fadeTo(2000,.7);  改变透明度到某个值
```
***
## 自定义动画
```
$('.box').click(function(){
        $('.box').animate({
            width:'200px',
            height:'200px',
            fontSize:'50px',
            left:'1000px',
            top:'100px'
        },2000,'swing',function(){
            $('.box').animate({
                 left:'100px',
                 top:0,
                 fontSize:'20px'
             },1000)
        })
          box的 第一个动画 执行完,才会执行第二个
        $('.box').animate({
            left:'100px',
            top:0,
            fontSize:'20px'
        },1000)
    })

stop(stopAll,goToEnd);
stopAll  是否全部停止，默认false 停止队列中所有的动画
goToEnd  是否将停止的动画  默认 false 停止在当前动画的最后一个状态  

    $('.btn').click(function(){
        $('.box').stop(true);
    })
```
***
## on方式绑定解绑事件
```
$('.box').on('mouseenter',function(){
            alert('不凡学院')
        })

$('button').click(function(){
            $('.box').off('mouseenter');
        })  off解绑事件
```
***
