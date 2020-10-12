#### JavaScript 的组成

- ECMAScript：JavaScript 的语法标准。
- DOM：JavaScript 操作网页上的元素的 API。
- BOM：JavaScript 操作浏览器的部分功能的 API。

#### JavaScript 的特点

- 可以使用任何文本编辑工具编写，然后使用浏览器就可以执行程序。
- 是一种解释型脚本语言：代码不进行预编译，从上往下逐行执行，不需要进行严格的变量声明。
- 主要用来向 HTML 页面添加交互行为。

---

JavaScript 代码是放在 `<script>……</script>` 标签里，而包含 JavaScript 代码的 script 标签，我们可以放在` <body>……</body>`  标签里，也可以放在`<head>……</head>` 标签里。

## 变量

变量的命名规则如下：

- 变量名必须以字母、下划线 “_”、美元符号 “$” 开头，不能以数字开头。
- 变量可以包含字母、数字、下划线和美元符号。
- 不能使用 JavaScript 中的关键字做为变量名。
- 变量名不能有空格。
- 变量名对大小写敏感，比如：name 和 Name 就是两个完全不同的变量。

在 JavaScript 中，变量也可以不作声明，而在使用时再根据数据的类型来确其变量的类型，如：

```javascript
x = 50; // 变量 x 为整数
```

#### 变量类型

- Number：存储数字

- String：存储字符

字符串可以是引号中的任意文本，你可以使用单引号或双引号，也可以在字符串中使用引号，只要不匹配包围字符串的引号即可

- Boolean：布尔类型的值有两种：true 和 false。通常被用于在适当的代码之后，测试条件是否成立

- Array：数组是一个单个对象，其中包含很多值，方括号括起来，并用逗号分隔。

  >```var myNameArray = ['Tom', 'Bob', 'Jim']; var myNumberArray = [10, 15, 20];```

- Object：对象类型。
### 动态类型  
javasprict是一种动态类型语言，不与要指定变量将包含什么数据类型，可以
全部用var关键字进行声明。
> 比如声明一个变量并给它一个带引号的值，浏览器就会知道它是一个字符串
> `var myyString = 'hello'`  
我们可以在控制台中通过typeof函数来查看声明的变量是什么类型的  
！！！需要注意，如果引号中是一个数字，那它仍然是string类型的  
### 注释  
单行注释：快捷键： ctrl + /  
`// 这是注释`  
多行注释：快捷键： ctrl + shift + /   
```javascript
/*
hello
this
is
注释
*/
```
### 数字类型  
- 整数  
- 浮点数  
- 双精数：是一种特定类型的浮点数，具有比标准浮点数更高的精度。  
不过JavaScript中，数字类型全部用var声明就可以了，并且JavaScript中
只有一个数据类型：Number   
### 算数运算符  
- ++ 累加  
- ++ 累减
- % 取余数  
#### 区别x++ / ++x  
```  javascript
var num1 = 3;
var result1 = num1++;
console.log(result1);
console.log(num1);
var num2 = 4;
var result2 = ++num2;
console.log(result2);
console.log(num2);
```
**最后控制台打印的数字为：3 4 5 5**  
可以看出 num++ 和 ++num 的区别，前者是先赋值再自增，
后者是先自增再赋值。同样的 num-- 和 --num 也是一样的效果  
###  操作运算符

###    ![操作运算符](https://github.com/Lixk100/js/blob/master/%E6%93%8D%E4%BD%9C%E8%BF%90%E7%AE%97%E7%AC%A6.png)


### 比较运算符  
  ![比较运算符](https://github.com/Lixk100/js/blob/master/%E6%AF%94%E8%BE%83%E8%BF%90%E7%AE%97%E7%AC%A6.png)  

在控制台中输入这些示例，如果成立的话会返回 true 如果不成立的话则返回 false  

### 逻辑运算符  
  ![逻辑运算符](https://github.com/Lixk100/js/blob/master/%E9%80%BB%E8%BE%91%E8%BF%90%E7%AE%97%E7%AC%A6.png)
### 运算符的优先级  

![运算符的优先级](https://github.com/Lixk100/js/blob/master/%E8%BF%90%E7%AE%97%E7%AC%A6%E7%9A%84%E4%BC%98%E5%85%88%E7%BA%A7.png)



## 数组概述  

###  数组语法

```javascript
var myarray = new Array(1, 2, 3, 4, 5); // 创建数组同时赋值 
// or
var myarray = [1, 2, 3, 4, 5]; // 直接输入一个数组（称“字面量数组”）
```

### 多维数组

多维数组就是数组中还包含数组。

```javascript
var student = [
  ['张三', '男', '18'],
  ['李四', '女', '20'],
];
student[0][2]; // returns "18"
```

### 修改数组 

```javascript
var color = ['red', 'green', 'blue', 'yellow'];
color[0] = 'black';
color; // returns ["black", "green", "blue", "yellow"]
```
### 获取数组长度 **length** 
```javascript
var color = ['red', 'green', 'blue', 'yellow'];
color.length; // returns 4
```
### 数组和字符串之间的转换  
通过**split()**方法，将字符串转换为数组  
```javascript
'1:2:3:4'.split(':'); // returns ["1", "2", "3", "4"]
'|a|b|c'.split('|'); // returns ["", "a", "b", "c"]
```
通过**join()**方法将数组转换为字符串  
```javascript
['1', '2', '3', '4'].join(':'); 
// returns "1:2:3:4"
['', 'a', 'b', 'c'].join('|'); 
// returns "|a|b|c"
```
>  我们同样可以使用 `toString()` 方法将数组转换为字符串，但是 `join()` 方法可以指定不同的分隔符，而 `toString()` 方法只能是逗号。

### 添加和删除数组项   
使用**push()**方法在数组尾部添加一个或多个元素。

```javascript
var arr = ['1', '2', '3', '4'];
arr.push('5', '6');
arr; // returns ["1", "2", "3", "4", "5", "6"]
```
使用`pop()`方法可以删除数组的最后一个元素，把数组长度减1，并返回它删除的元素的值。如果数组已空，则`pop()`不改变数组，返回`undefined`值。
> ```javascript
> var arr = ['1', '2', '3', '4'];
> arr.pop(); // returns 4
> arr; // returns ["1", "2", "3"]
> var arr1 = [];
> arr1.pop(); // returns undefined
> arr1; // returns []
> ```

`unshift()` 和 `shift()` 从功能上与 `push()` 和 `pop()` 完全相同，只是它们分别作用于数组的开始，而不是结尾。

## NUll和Undefined  

通过控制台测试可以知道

![1](https://doc.shiyanlou.com/document-uid897174labid9222timestamp1547019784085.png)

null 和 undefined 的值不等于 0，它们的值相等，但是类型不相等。undefined 表示所有没有赋值变量的默认值，而 null 则表示一个变量不再指向任何对象地址。

### 字符串  

单引号和双引号都可以包扩字符串，字符串中有单引号就用双引号包扩，有双引号就用单引号包扩，除此之外，还有一种方法可以实现在字符串中使用引号，即使用转义符号。在JavaScript中，通过在符号前放一个反斜杠来实现。

```javascript
var x1 = 'I\'ve got no right to take my place...';
```

#### 常用的转义符  

<img src="https://doc.shiyanlou.com/document-uid897174labid9222timestamp1547519780285.png" alt="1"  />

#### 字符串的连接  

通过`+`可以连接字符串。

```javascript
var one = 'hello';
var two = 'Lxk';
result = one + two;
```

> 输出结果:"hello,Lxk"。

扩展：在控制台输入'LXk'+18,输出结果：Lxk18。输入"20"+20,输出2020

#### 字符串的转换 

通过`toString()`函数可以把数字转换成字符串。

```javascript
var myNum = 111;
var myString = myNum.toString();
typeof myString;
```

通过`Number()`可以把对象传递给它的**字符串类型的数字转换成数字**。

```javascript
var myString ='111';
var myNum = Number(myString);
typeof = myNum;
```

扩展：如果传递给它的字符串不是纯数字，则返回的不是数字，而是NaN(not a number)。

#### 获取字符串的长度  

通过`length`属性来获取字符串的长度，结果返回一个数字。

```javascript
var myString = 'hello world ';
myString.length;
```

> 运行结果:12(10个字母加2个空格)。

扩展：如何查找字符串中的第N个字符：

```javascript
myString[N-1]
```

#### 在字符串中查找子字符串并提取它  

通过`indexof()`可以查找一段话中是否包含一个词或一个字。

```javascript
str.indexOf(searchValue,fromIndex);
```

> str 指的是我们需要查的较长的字符串，`searchValue` 表示我们指定的较小的字符串，`fromIndex` 表示调用该方法的字符串中开始查找的位置，是一个可选的任意整数值，也可以不写，默认是 0 表示从头开始查，`fromIndex < 0` 和 `fromIndex = 0` 是一样的效果，表示从头开始查找整个字符串。如果 `fromIndex >= str.length`，则该方法的返回值为 -1。这里有个特殊的情况：就是如果被查找的字符串（searchValue）是一个空字符串，那么当 `fromIndex <= 0` 时返回 0，`0 < fromIndex <= str.length` 时返回 `fromIndex`，`fromIndex > str.length` 时返回 `str.length`。

> ```javascript
> 'Blue Sky'.indexOf('Blue'); // returns  0
> 'Blue Sky'.indexOf('Ble'); // returns -1
> 'Blue Sky'.indexOf('Sky', 0); // returns  5
> 'Blue Sky'.indexOf('Sky', -1); // returns  5
> 'Blue Sky'.indexOf('Sky', 5); // returns  5
> 'Blue Sky'.indexOf('Sky', 9); // returns -1
> 'Blue Sky'.indexOf('', 0); // returns  0
> 'Blue Sky'.indexOf('', 5); // returns 5
> 'Blue Sky'.indexOf('', 9); // returns 8
> ```

扩展：返回值指的是指定值第一次出现的索引，如果没有找到返回 -1。`indexOf()` 方法区分大小写，比如：

```javascript
'Blue Sky'.indexOf('blue'); // returns -1
'Blue Sky'.indexOf('Blue'); // returns 0
```

通过`slice()`来提取子字符串

```javascript
'Blue Sky'.slice(0, 3); // returns "Blu"
```

注：`slice(strat，end)`，第一个参数 start 是开始提取的字符位置，第二个参数 end 是提取的最后一个字符的后一个位置。所以提取从第一个位置开始，直到但不包括最后一个位置。另外第二个参数也可以不写，不写代表某个字符之后提取字符串中的所有剩余字符。比如：

```javascript
'Blue Sky'.slice(2); // returns "ue Sky"
```

#### 转换大小写  

字符串方法 `toLowerCase()` 和 `toUpperCase()` 字符串并将所有字符分别转换为小写或大写。

#### 替换字符串的某部分

可以使用 `replace()` 方法将字符串中的一个子字符串替换为另一个子字符串。

```javascript
var string = 'I like study';
string.replace('study', 'sleep'); // returns "I like sleep"
```

注意这样只能替换第一个出现的字符串，如果字符串是类似 `I like study study`，那么第二个 `study` 不会被替换。

此时可以使用全局替换方法。

```js
var string = 'I like study study';
string.replace(/study/g, 'sleep');
```

<!-- pack   -->
<!-- query -->

