# TypeScript

* TypeScript 是一种开源的编程语言,它是 JavaScript 的一个超集,扩展了 JavaScript,并为其添加了静态类型和其他功能,以提供更强大的工具和开发支持.  
* TypeScript 可以进行更严格的类型检查,并提供更好的代码提示和静态分析.同时,它还兼容 JavaScript 语法和库,可以无缝地与现有的 JavaScript 项目集成.  
* TypeScript 的主要目的是提高大型项目的可维护性和可扩展性,它的面向对象编程能力和模块化系统也有助于组织和管理复杂的代码结构.  
* TypeScript 可处理已有的 JavaScript 代码,并只对其中的 TypeScript 代码进行编译.  

## 变量声明 

在变量名后加上类型
```ts
var foo : String = "Hello world";
```
或者
```ts
var foo = "abc";
```

## 函数

```ts
function foo(args...): return_type {
    ...
}
function bar(args...) {
    ...
}
```
其中args的格式为`argname : argtype`或不加`: argtype`, 多个参数用逗号隔开.  
设置为可选参数`argname?[ : argtype] `  
设置为带默认值的参数`argname[ : argtype] = value`  

匿名函数  
```ts
var fn = function(args...) {
    ...
}
```

## Map

`let myMap = new Map();`
```ts
let myMap = new Map([
        ["key1", "value1"],
        ["key2", "value2"]
    ]); 
```

map.clear()
* 移除 Map 对象中的所有键值对,即清空整个 Map.  
map.set(key, value)  
* 用于设置 Map 对象中的键值对.  
* 接受两个参数，key 表示要设置的键,value 表示要设置的值.  
* 返回被修改后的 Map 对象本身,因此可以使用链式调用.  
map.get(key)  
* 用于获取 Map 对象中指定键对应的值.  
* 接受一个参数 key,表示要获取值的键.  
* 如果键存在于 Map 中,则返回对应的值;如果键不存在,则返回 undefined.  
map.has(key)  
* 用于判断 Map 对象中是否包含指定的键.  
* 接受一个参数 key,表示要检查是否存在的键.  
* 如果键存在于 Map 中,则返回 true;如果键不存在,则返回 false.  
map.delete(key)  
* 从 Map 对象中删除指定的键值对.  
* 接受一个参数 key,表示要删除的键.  
* 如果成功删除了键值对,则返回 true;如果键不存在,则返回 false.  
map.size  
* 返回 Map 对象中键值对的数量.  
map.keys()
* 返回一个迭代器对象,其中包含了 Map 对象中每个元素的键.  
* 迭代器对象可以用于遍历 Map 中的键.  
map.values()
* 返回一个新的迭代器对象,其中包含了 Map 对象中每个元素的值.  
* 迭代器对象可以用于遍历 Map 中的值.  

## Tuple 

数组中元素的数据类型都一般是相同的,如果存储的元素数据类型不同,则需要使用元组.  
元组中允许存储不同类型的元素,可以作为参数传递给函数.  
创建元组的语法格式如下:  

`var tuple_name = [value1,value2,value3,…value n]`
```ts
var mytuple = []; 
mytuple[0] = 120
mytuple[1] = 240
```

元组中元素使用索引来访问,第一个元素的索引值为 0,与数组相同  

push() 向元组添加元素,添加在最后面.  
pop() 从元组中移除元素,并返回移除的元素.  

## 联合类型 
创建联合类型的语法格式如下：  
```ts
function printId(id: number | string) {
  console.log('ID:', id);
}

printId(123); // 输出：ID: 123
printId('abc'); // 输出：ID: abc
```

## 接口 

TypeScript 接口定义如下:  
`interface interface_name { }`

```ts
interface MyInterface {
  property1: Type1;
  property2: Type2;
  method1(): ReturnType;
}
interface IPerson { 
    firstName:string, 
    lastName:string, 
    sayHi: ()=>string 
}
var customer:IPerson = {
    firstName:"Tom",
    lastName:"Hanks",
    sayHi: ():string =>{return "Hi there"}
}
```

## 命名空间 

在 TypeScript 中,命名空间是一种组织和管理代码的方式.它将相关的类、接口、函数等内容封装在一个独立的作用域中,避免命名冲突,并提供了一种逻辑上分组和组织代码的方法.使用命名空间可以避免全局命名冲突,并且能够将相关的代码模块化,提高代码的可维护性和可读性.  

TypeScript 中命名空间使用 namespace 来定义，语法格式如下：  
```ts
namespace SomeNameSpaceName { 
   export interface ISomeInterfaceName {      }  
   export class SomeClassName {      }  
}
```