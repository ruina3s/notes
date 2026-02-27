---
title: Javascript再学习
time: 2023-1-24 15:32:00
tab: 
---

Javascript再学习笔记
==

JS作为一种编程语言，可用来与游览器中的网页元素进行交互（比如点击按钮后的事件），看起来像java但并不是（名字像也叫像的话），可实时编译。Node.js是运行在服务器中的js。网页中使用的js要在html文件中引用才能使用——使用script标签引用。而服务器中使用js则需要安装Node.js。

学习参考：[微软官方 JavaScript 入门教程_bilibili](https://www.bilibili.com/video/BV18a4y1L7kD/)



[toc]



# 第一个程序

安装Node.js，建立一个工程文件夹新建一文件**<u>helloworld.js</u>**

![image-20230124161050738](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20230124161050738.png)

在命令行中，进入对应的文件夹位置，输入命令<kbd>node helloworld.js</kbd>

![image-20230124161313527](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20230124161313527.png)



# 语法

## 1.注释

```javascript
//单行注释
console.log('hello world');

/*
多行注释
多行注释
*/
```



## 2.变量声明

```js
//变量声明3种方式
var one = 1;
/*
var是最原始的声明方式，在函数中使用，那么即使声明在最后一行，该变量也可在最初使用
变量在作用域内可改动，可重新赋值也可改变数据类型
*/

let two = 2;
/*
let与var相似，但作用域只能在块中，即一对{}中，且只能在声明后才能使用
let在作用域内也可如var改动值与类型
*/

const three = 3;
/*
const的作用域与let相同，也只能在块中，声明后使用
但const只能设置，不能重置（即常量）
*/

//一般常量用const，循环用let
```



## 3.字符串拼接

```js
let str1 = "str1";
let str2 = "str2";
console.log(str1+str2);
console.log(str1+" and "+str2);

let num1 = "1";
let num2 = 1;
console.log(num1+num2);
console.log(num2+1);
```



## 4.模板字符串

```js
//通常字符串用单引号和双引号表示，而模板字符串用``来表示，且用${}来连接想用的值
let str1 = "javascript";
let str2 = "fun";
console.log(`I feel ${str1} is ${str2}`);

let bool = true;
console.log(`1 + 1 is ${1+1}`);
console.log(`the numbers is ${bool} or ${!bool}`);
```



## 5.数据类型

```js
/*基本类型
number(float)、string、boolean、date、function、array、object
*/
/*特殊类型
NaN(非数)、null、undefined
*/
//typeof返回变量的类型
//instanceof返回一个Boolean确定是否为某一类型的变量
```



## 6.数学运算

与其它编程语言类似，不多做复述

```js
let num1 = 100;
console.log(num1 + 1500);
console.log(num1 - 100);
console.log(num1 * 10);
console.log(num1 / 1500);

console.log(num1 % 1500);
console.log(++num1);
console.log(--num1);

console.log(Math.PI);//圆周率
console.log(Math.sqrt(num1));//开平方
```



## 7.数据类型转换

```js
parseInt(); //字符串转整数
ParseFloat(); //字符串转小数
toString(); //数字转字符串
```



## 8.错误抛出

```js
try{
    //可能发生错误的代码
}catch(ex){
    //对上述代码发生的错误处理
}
finally{
    //无论是否发生错误都要执行的代码
}

throw "myerror"; //手动抛出错误
//抛出的错误如果未处理程序会中断
```



## 9.Date对象

处理时间相关的都使用Date对象，包含日期和时间。js内部时间存储自1970.1.1的毫秒数

```js
const now = new Date(); //得到当前时间

const randomDate = new Date(2015, 3, 12, 6, 25, 58); //设置时间为2015.04.12 6:25:58
//月份从0开始，0表示1月

const now2 = new Date();

now2.setFullYear(2014);
now2.setMonth(3);
now2.setDate(4);

now2.setHours(4);
//小时显示格林尼治时间
now2.setMinutes(24);
now2.setSeconds(46);
```



## 10.比较

与其它语言相近，不做特别说明

```js
== //判断两端的值是否相同
=== //判断两端的值和数据类型是否相同
!= //判断两端的值是否不同
!== //判断两端的值和数据类型是否不同

const a = 2;
if (a == 2){
    
}else if(a === 1){
    
}else{
    
}

const message = (a === 2) ? 'yes' : 'no';

switch(a){
    case 2:
    	break;
    case 3:
        break;
    case 3:
        break;
    default:
        break;
}
```



## 11.数组

```js
//创建数组
let length = 5;

let arr1 = [];
let arr2 = Array(length);

//访问数组元素
let arr3 = ["A", true, 2];
console.log(arr3[0]);
console.log(arr3[1]);

//添加数组元素
let arr4 = Array(2);
arr4[0] = "test";
console.log(arr4[0]);
console.log(arr4[1]);

//数组长度与索引值
console.log(arr3.length);
console.log(arr3[3]); 
console.log(arr3[2]); 
console.log(arr3[arr3.length-1]);
            
let arr5 = Array(2); 
arr5[1] = "Adding a value! ";
console.log(arr5[1]); //Last index 0f array
console.log(arr5[arr5.length - 1]); //lndex: 1
console.log(arr5[0]); //NO value yet

//添加删除数组元素
let arr = ["A", true, 2];
arr.push("new value"); //在数组最后位置增加元素并返回数组长度
arr.pop(); //删除数组最后一个元素，并返回删除的值
arr.unshift("new value"); //在数组最开始增加元素并返回数组长度
arr.shift(); //删除数组第一个元素，并返回删除的值

//数组合并
arr.concat([1,2,3]);
```



## 12.循环

```js
while (bool){//为真则一直运行
    
}

for (let i = 0; i < 4; i++){
    //循环判断变量; 循环时的条件; 变量步长
}

const arr = Array(5);
for (let j of arr){
    //遍历数组元素
}
```



## 13.函数

函数是一组代码块，可能会在程序中反复使用

```js
function functionName(parameters){
    //...
    return ;
}
//调用
functionName("");

//函数本身是一种对象，可以通过用.来调用其它方法
functionName.name

//js不会在你调用函数时检查你的参数数量和类型

//还有一种特殊的匿名函数,用 => 作为关键字
//隐式返回，但返回值有多个时，必须用return
const add = (a,b) => a+b;
console.log(add(1,2));

const subtract = (a,b) => {
    return a - b;
}
console.log(subtract(2,1));
```



## 14.JSON

用于数据的传输

```js
{
    "key1":"value1",
    "key2":"value2",
    "key3":"value3",
    //...
}

//js对象转为JSON
JSON.stringify(Object); //其它用法需要查询资料

//JSON转为js对象
JSON.parse(jsonObj);
```



## 15.对象

对象既有属性又有函数（方法）

```js
//创建对象的方法
const obj = {
    key1: "value1",
    key2: "value2",
    //...
    methodName1: function(){ },
    methodName2: function(){ },
	//...
};//多组键值对的集合，函数也是一组键值对

const obj2 = new Object();
obj2.key1 = "value1";
obj2.key2 = "value2";
obj2.methodName1 = function(){ };
obj2.methodName2 = function(){ };

//对象调用值
obj.key1; //<object>.<name>
obj[key1] //<object>["name"]

//对象调用方法
obj.methodName1;
obj["methodName1"];
obj.methodName1();
obj["methodName1"]();
```



## 16.异步与promise

当程序工作时，未达到执行条件时进行暂停，等其它线程使条件满足时再重新开始

promise即是在该线程运行时，允许其它程序调用或访问运行的结果

e.g.

```js
function promiseTimeout(ms) {
    return new promise((resolve, reject) =>{
        setTimeout(res01ve, ms);
    });
}
promiseTimeout(2000)
.then( () =>{    
    console.log('done');
    return Promise.res01ve(42);
})
.then( (response) => {
    console.log( response);
})
.catch( () =>{
    console.log('cool error handling');
})
```



## 17.Async与Await

使异步代码看起来更像同步

```js
function promiseTimeout(ms){
    return new Promise(
        (resolve, reject) => {
            setTimeout(resolve, ms);
        }
    );
}

//有async作为前缀则说明函数中有await
async function run(){
    console.log('start!!');
    await promiseTimeout(2000); //await使函数暂停去执行await后跟着的函数，直到该函数结束才继续执行
    console.log('stop!!');
}

run();
```



## 18.包(package)

指一系列可复用的代码、图片等其它资源，当你需要使用**包**时，可以在NPM上找

包一般以package.json开始

包含Metadata（项目名字、版本、许可等信息）、Dependencies（依赖项）、Script（脚本部分）

具体使用可查看资料



# 参考资料

https://jgthms.com/javascript-in-14-minutes/
