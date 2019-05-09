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
## date实例对象有很多方法.
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
### 找出水仙花数
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
## switch
```
有限的类别可以使用,代码逻辑更清晰
var fruit = prompt('请输入水果名称');
switch (fruit){
    case '苹果':
      alert('苹果很好吃');
      break;
    case '梨子':
      alert('梨子很甜');
      break;
    case '香蕉':
      alert('很好吃');
      break;
    dafault:
      alert('我没吃过');
      break;
}
```
***
## while
```
做while循环,一定要注意跳出循环的条件;
var num = 0;
while(num<10){
    console.log(num);
    num++;
}
console.log(num);   10
```
***
## do while
```
var num = 0;
do{
    console.log(num);
    num++;
}while(num<10);
console.log(num);  10
```
***
## continue
```
需求:找到0-100中所有能被3整除或者能被7整除的数
for(var i = 0; i<=100; i++){
    if(i%3==0){
        console.log(i);
        continue;
    }
    if(i%7==0){
        console.log(i);
    }
}
相当于条件为if(i%3==0 || i%7==0);
```
***
## 九九乘法表
```
for(var i = 1; i <= 9; i++){
    var str = '';
    for(var j = 1; j <= 9; j++){
        if(j > i){
            break;
        }
        str = str + i+ '*' + j + '=' i*j + ' ';
    }
    console.log(str);
}
```
***
## 数组的方法
```
var arr1 = [1,3,5];
var arr2 = [2,4,6];
1  concat  合并  不影响原来的数组;
   console.log(arr1.concat(arr2));
2  join  把数组转换为字符串;
   如果没有连接符,默认为逗号;
3  split 把字符串打断为数组;
   var str = 'Hello everyone today is a fine day!'
   console.log(str.split('o',2));
4  push  从后面添加一个值,并返回新的长度;
   arr.push(3);
5  unshift  从前面添加,并返回新长度;
6  pop  删除最后一个元素,并且返回被删除的值;
   写法:arr.pop();
7  shift  删除第一个元素,并且返回第一个删除的值;
```
***
## 冒泡排序
```
var arr = [10,8,1,7,5,2];
for(var j = 0; j < arr.length - 1; j++){
    for(var i = 0; i < arr.length - 1 - j; i++){
        if(arr[i] > arr[i+1]){
            var temp = arr[i+1];
            arr[i+1] = arr[i];
            arr[i] = temp;
        }
    }
}
console.log(arr);  最终从小到大的排序结果;
```
***
## 数组当中最大值和最小值
```
var arr = [2,35,67,45,78,3];
function getMax(arr){
    var max = 0;
    for(var i = 1; i < arr.length; i++){
        if(arr[max]>arr[i]){
            max = i;
        }
    }
    return arr[max];
}
console.log(max);
```
***
## 阶乘递归写法
```
求num的阶乘,如5! = 5*4*3*2*1
递归必须有跳出条件
function jc(num){
    if(num==1){
        return 1
    }
    return jc(num-1)*num
}
```
***
## JSON对象
```
var obj = {
    a:'hello',
    b:'world'
};  这是一个对象
var json = '{"a":"hello", "b":"world"}';
这是一个JSON字符串,可以进行网络传输
var json ={
    "title":"西虹市首富",
    "directors":"闫菲",
    "year":"2018"
};
把json字符串转换为JSON对象;
var jsonobj =JSON.parse(json)
把对象转换为字符串(任何对象)
var str = JSON.stringify(obj);
```
## 数组高级API,高级方法
```
arr.toString();  把数组转换为字符串
arr.reverse();  反转数组,会改变原数组
给数组排序，返回排序后的数组。如何排序看参数
无参：按照数组元素的首字符对应的Unicode编码值从小到大排列数组元素。

带参：必须为函数（回调函数--callback）。函数中带有两个参数，
代表数组中的前后元素。如果计算后（a-b），返回值为负数，a排b前面。等于0不动。
返回值为正数，a排b后面。
var arr = [1,2,4,3,13];
arr.sort();从小到大排序,会改变原数组,按照Unicode排序
arr.sort(function(a,b){
    return a-b;
})
console.log(arr);
indexOf(),lastIndexOf()  返回对应数值的下标,如果没找到,返回-1
arr.slice(start,end)  从当前数组中截取一个新的数组，不影响原来的数组，取的到start,取不到end
arr.slice(0);   复制数组
arr.splice(start,count,op);  分别对应要替换的下标位置,从这里替换几个,用什么代替,不写就是删除.
```
***
