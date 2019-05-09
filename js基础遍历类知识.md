+ js当中内置对象
+ 创建构造函数(Date)的实例对象
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