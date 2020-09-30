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




<!-- pack   -->
<!-- query -->
