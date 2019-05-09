+ js当中内置对象
+ 创建构造函数(Date)的实例对象
## Date对象
```
var date = new Date();
console.log(date);
Sun May 05 2019 09:37:20 GMT+0800 (中国标准时间)
```
***
```
var xiaoming = {
    height:172,
    weight:60,
    say:function(){
        alert('你好)
    }
}
console.log(xiaoming.height);
调用对象的say方法:xiaoming.say();
对象.xx:获取对象的属性
对象.xx():调用对象的方法.
```
***
+ date实例对象有很多方法.
```
var day = date.getDay();
var month = date.getMonth()+1;   0----11;
var year = date.getFullyear();
var hour = date.getHours();
var min = date.getMinutes();
var seconds = date.getSeconds();
程序语言,时间最小单位为毫秒  1s = 1000 ms
var milliseconds = date.GetMilliseconds();
var weekDay = date.getDay();   周几
var stamp date.getTime();  时间戳
```
***
## Math对象
```
console.log(Math);   js当中的内置对象
console.log(Math.ceil(2.3));  3 向上取整
console.log(Math.floor(2.3));  2 向下取整
console.log(Math.max(2,3,5,7)); 取最大
console.log(Math.min(2,3,5,8)); 取最小
console.log(Math.random());  [0,1),如果取0到99,*100
console.log(Math.pow(3,4));  3的4次方
console.log(Math.round(2.4)); 四舍五入
```
***
## 逻辑运算符
```
console.log(true && false);  false
console.log(true || false);  true
console.log(false || false);  false
console.log(!true);  false
console.log(3<2<5>);  连比,错误写法;
console.log(2>3 && 2<5>);  false
```
***
## if语句
+ 找出水仙花数
```
for(var i = 100; i<=999; i++){
    var x = Math.floor(i/100);
    var y = Math.floor(Math.floor(i%100)/10);
    var z =Math.floor(i%10);
    if(Math.pow(x,3) + Math.pow(y,3) + Math.pow(z,3) = i){
        console.log(i);
    }
}
if语句中,如果else什么都不干,可以省略.
```
***
