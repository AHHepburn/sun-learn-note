+ js引入
  + js格式`<script></script>`
  + 外部引入方式:`<script src="test.js"></script>`
  + 可在head区书写,也可以在body所有标签之后书写.
  + 代码严格区分大小写.
  ***
  ```
  if(confirm('你是中国人吗?')){
			alert('你好')
		}else{
			alert('不会外语')
		}
  ```  
  + if:如果'是',输出'你好'
  + else:否则输出'不会外语'.
  + prompt(''):输入框.
  + 基本数据类型
    + 1 Number类型:整数和浮点数(小数)
    + 2 String类型:字符串.
    + 3 boolean类型:true和false.
    + 4 undefined类型:只有一个值undefined.
    + 5 null:指向一个空对象.
  ***
``` 
  var str = 'hello "wo" rld';
  cosole.log(str)
```
+ 引号不能嵌套：双引号里不能再放双引号，单引号里不能再放单引号。但是单引号里可以嵌套双引号.
***
+ 无穷大(正无穷):Infinity,无穷小:-infinity
+ NaN:是一个特殊数字,表示Not a Number,非数值.
+ `console.log('abc/18');NaN`
+ `console.log('abc'*'abcd');NaN`
+ isNaN();任何不能被转换为数值的值,都会让这个函数返回true.
+ `console.log(isNaN(123));false`
+ `console.log(isNaN('blue'));true`
```
var c;
console.log(c);
undefined,声明但没有被赋值.
```
`console.log(typeof null);object`
+ typeof:查看数据类型.
+ 函数:function
  + `function fucname (){}`
#### 判断数据类型
```
var age = 22;
var sex = true;
var like = ['篮球','足球'];
var child = {
  name:'zhang',
  age:2
} 
function fucname(){

}
```
`console.log(typeof age);Number`
`console.log(typeof sex);boolean`
`console.log(typeof like);object`
`console.log(typeof child);object`
`console.log(typeof fucname);function`
***
#### 数据类型转换
+ 1 转换为string类型
`console.log(数据类型 + '');将该数据类型转换为字符串类型.`
+ 2 转换为number类型.
```
console.log(Number(null));0
console.log(Number(undefined));NaN
console.log(Number(true));1
console.log(Number(false));0
console.log(Number('123a'));NaN
console.log(Number('123'));123
console.log(Number('-123'));-123
console.log(Number('12.99'));12.99
console.log(Number(' 12 3'));123
console.log(Number(''));0
```
+ 3 parseInt():转换为整数
  + 规则:从第一个非空白字符（空格、换行、tab）开始转换，直到遇到一个非数字字符为止.向下取整.
  ```
  console,log(parseInt(''));NaN
  console,log(parseInt('12.9'));12
  console,log(parseInt('12adc9'));12
  console,log(parseInt('a123'));NaN
  ```
+ 4 parseFloat():转换为浮点数(小数)
  + 规则:第一个小数点有效,之后的无效.
  + 从第一个非空白字符(空格,换行,tab)开始转换,直到遇到一个非数字字符.
```
console.log(parseFloat('12.3'));12,3
console.log(parseFloat('12..3'));12
console.log(parseFloat('a12.3'));NaN
```
+ 5 转换为boolean类型
  + 数字-->boolean:除了0和NaN,其余都是true.
  + 字符串-->boolean:除了空串,其余都是true(包括空格).
  + null和undefined都会被转换为false.
  + 对象会被转换为true.
***
#### 比较运算符
+ >  <  >=  <=:只比较数值,不比较类型.
+ ==:之比较数值,不比较类型.
+ ===:先比较数据类型,不一致:false,类型一致,再比较数值.
***
+ 算术运算符
  + 加:+,除了加法运算,还可以拼接字符串.
  + 减:-
  + 乘:*
  + 除:/
  + 取余:%
***  
+ 带操作的赋值运算
  + 只记一个易忘的
  ```
  var c = 20;
  c = c + 1,可写成c +=1,还可以写成c++;
  c = c - 1,同理.
  var d = 10;
    不管是 d++ 还是 ++d 都实显现了+1
    ++d 返回值是 +1之后的 11
    d++ 返回值是 +1之前的 10
    var fd = ++d;
    var bd = d++;
  ```


