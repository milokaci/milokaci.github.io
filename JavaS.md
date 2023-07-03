# JavaScript 

JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备.  
* JavaScript 是一种轻量级的编程语言.  
* JavaScript 是可插入 HTML 页面的编程代码.  
* JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行.  

## 注释 

1. `//` 单行注释
2. `/**/` 多行注释

## 变量 

```js
var age = 30;
console.log(age); // 输出: 30
var name = "Alice";
console.log(name); // 输出: Alice
var isStudent = true;
console.log(isStudent); // 输出: true
```

### 基本类型 

Boolean：表示逻辑上的两个值,即 true和 false,用于条件判断和逻辑运算.  
Null：表示一个空或不存在的值,它是一个特殊的关键字,用于表示变量没有值.  
Undefined：表示一个未初始化或未赋值的变量,当变量声明但未赋予相应的值时,它的默认值为 undefined.  
Number：用于表示数字,包括整数和浮点数,可以进行数学运算和比较操作.  
String：用于表示文本数据,字符串是由字符序列组成的,可以使用单引号或双引号包裹起来.  
Symbol：是 ECMAScript 6 引入的一种新的数据类型,每个通过符号创建的值都是唯一的,用于创建对象的属性名,防止属性名冲突.  

## 函数 

```js
function foo(args...) {
    ...
}
function myAdd(x, y) {
    return x + y;
}
function average(arr) {
  var sum = 0;
  for (var i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum / arr.length;
}
```

## 常用语句

```js
if (expr) {
    ...
}
else if (expr2) {
    ...
}
else {
    ...
}
var num = 1;
switch(num) {
    case 1:
        ...
        break;
    ...
    default:
        ...
        break;
}

for (var i = 0; i < 8; ++i) {
    ...
}
while (expr) {
    ...
}
do {
    ...
}
while (expr);
```

## break & continue

在循环语句中, break; 结束循环, continue; 结束本次迭代.
```js
for (var i = 0; i < 5; i++) {
  if (i === 3) {
    break;
  }
  console.log(i);
}
```
在循环语句外 break lebal; 跳到lebal标识的代码处.
```js
for (var i = 0; i < 5; i++) {
  if (i === 2) {
    continue;
  }
  console.log(i);
}
```

## 比较和逻辑运算 

== ：检查两个值是否相等.  
* 它会进行类型转换,如果类型不同,则尝试将它们转换为相同类型再进行比较.  
=== ：严格相等比较,检查两个值是否相等并且类型相同.  
!= ：检查两个值是否不相等,与 == 相反.  
!== ：严格不相等比较,检查两个值是否不相等或者类型不同.  
> ：检查左侧的值是否大于右侧的值.  
< ：检查左侧的值是否小于右侧的值.  
>= ：检查左侧的值是否大于等于右侧的值.  
<= ：检查左侧的值是否小于等于右侧的值.  

&& ：当两个操作数都为真时,返回真;否则返回假.  
* 它是一个短路运算符,如果第一个操作数为假,则不会对第二个操作数进行求值.  
|| ：当至少有一个操作数为真时，返回真；否则返回假。和 && 一样，|| 也是一个短路运算符。  
! ：用于取反操作，将真变为假，将假变为真。  

## typeof 

typeof 是JavaScript中的一个运算符,用于获取操作数的数据类型.  
```js
String str = "Hello";
if (str instanceof String) {
    System.out.println("str 是 String 类型");
}
```