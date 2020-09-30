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
```
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
```  
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

###    ![操作运算符](C:\Users\MI\Documents\GitHub\js\操作运算符.png)

  
### 比较运算符  
  ![比较运算符](C:\Users\MI\Documents\GitHub\js\比较运算符.png)
在控制台中输入这些示例，如果成立的话会返回 true 如果不成立的话则返回 false  

### 逻辑运算符  
  ![逻辑运算符](C:\Users\MI\Documents\GitHub\js\逻辑运算符.png)
### 运算符的优先级  

![运算符的优先级](C:\Users\MI\Documents\GitHub\js\运算符的优先级.png)

<!-- pack   -->
<!-- query -->