## 函数

语法为：

```javascript
function functionName(parameters){
    //代码
}
```

例子：

```javascript
function f(a, b) {
  console.log(a + b);
} // 创建一个名为 f 的函数，它有两个形参 a，b

f(2, 3); // 调用函数 f，传入实参 2 和 3，最终运行结果为在控制台上打印出 5
```

### 函数表达式创建函数  

JavaScript函数可以通过一个表达式定义。函数表达式可以储存在变量中。

语法为：

```JavaScript
var functionName = function (parameters){
    //代码
}
```

把函数声明创建函数的例子改写为用函数表达式创建函数：

```javascript
var f = function (a, b) {
  console.log(a + b);
};
f(2, 3);
```

> #### 函数声明和函数表达式的区别
>
> - 函数声明
>
> ```javascript
> // 此处的代码执行没有问题，JavaScript 解析器首先会把当前作用域的函数声明提前到整个作用域的最前面。
> f(2, 3);
> 
> function f(a, b) {
>   console.log(a + b);
> }
> ```
>
> - 函数表达式
>
> ```javascript
> // 报错：f is not a function
> // 这是因为函数表达式，如同定义其它基本类型的变量一样，只在执行到某一句时也会对其进行解析
> 
> f(2, 3);
> 
> var f = function (a, b) {
>   console.log(a + b);
> };
> ```
>
> #### 函数的参数
>
> - 形参：`function f(a, b){return a + b;} // a, b 是形参`，占位用，函数定义时形参无值。
> - 实参：当我们调用上面的函数时比如 `f(2, 3);`其中 2 和 3 就是实参，会传递给 a 和 b，最后函数中执行的语句就变成了：`return 2 + 3;`。
>
> 注：在 JavaScript 中，实参个数和形参个数可以不相等。

#### 在 JavaScript 中没有重载

```javascript
function f(a, b) {
  return a + b;
}
function f(a, b, c) {
  return a + b + c;
}
var result = f(5, 6);
result; // returns NaN
```

上述代码中三个参数的 f 把两个参数的 f 覆盖，调用的是三个参数的 f，最后执行结果为 NaN，而不是 5。

#### 在 JavaScript 中函数的返回值

- 如果函数中没有 `return` 语句，那么函数默认的返回值是：undefined。
- 如果函数中有 `return` 语句，那么跟着 `return` 后面的值就是函数的返回值。
- 如果函数中有 `return` 语句，但是 `return` 后面没有任何值，那么函数的返回值也是：undefined。
- 函数在执行 `return` 语句后会停止并立即退出，也就是说 `return` 语句执行之后，剩下的代码都不会再执行了。
- 当函数外部需要使用函数内部的值的时候，我们不能直接给予，需要通过 `return` 返回。比如：

```javascript
var f = function (a, b) {
  a + b;
};
console.log(f(2, 3)); // 结果为 undefined
var f = function (a, b) {
  return a + b;
};
console.log(f(2, 3)); // 结果为 5
```
#### 匿名函数

匿名函数就是没有命名的函数，一般用在绑定事件的时候。语法为：

```javascript
function(){
    // 执行的代码
}
```

例子：

```javascript
var myButton = document.querySelector('button');

myButton.onclick = function () {
  alert('hello');
};
```

注：将匿名函数分配为变量的值，也就是我们前面所讲的函数表达式创建函数。一般来说，创建功能，我们使用函数声明来创建函数。使用匿名函数来运行负载的代码以响应事件触发（如点击按钮），使用事件处理程序。

#### 自调用函数

匿名函数不能通过直接调用来执行，因此可以通过匿名函数的自调用的方式来执行。比如：

```javascript
(function () {
  alert('hello');
})();
```





----



#### if...else 语句

1. 最基本的 `if...else` 语句。它的语法为：

```javascript
if (条件) {
  // 当条件为 true 时执行的语句
} else {
  // 当条件为 false 时执行的语句
}
```

例子：

```javascript
if (3 > 2) {
  console.log('我真帅');
} else {
  console.log('不可能');
}
```

1. `if...else` 嵌套。它的语法是：

```javascript
if(条件 1){
    // 当条件 1 为 true 时执行的代码
    }
else if(条件 2){
    // 当条件 2 为 true 时执行的代码
    }
else{
    // 当条件 1 和 条件 2 都不为 true 时执行的代码
    }
```

注：根据实际情况，还可以嵌套更多的 `else if`。

例子：

```javascript
var d = new Date().getDay();
if (d == 0) {
  console.log('今天星期天');
} else if (d == 1) {
  console.log('今天星期一');
} else if (d == 2) {
  console.log('今天星期二');
} else {
  console.log('好多啊，我不想写了');
}
```

#### switch case 语句

从前面的例子中我们可以看出来，当条件很多的时候，一直嵌套 `else if` 语句，显然是有点不科学的，由此我们引出了 `switch case` 语句，先来看看它的语法：

```javascript
switch(k){
    case 1:
        执行代码块 1 ;
        break;
    case 2:
        执行代码块 2 ;
        break;
    default:
        默认执行（k 值没有在 case 中找到匹配时）;
}
```

通过 `switch case` 语句来改写上面的例子：

```javascript
var d = new Date().getDay();
switch (d) {
  case 0:
    console.log('今天星期天');
    break;
  case 1:
    console.log('今天星期一');
    break;
  case 2:
    console.log('今天星期二');
    break;
  case 3:
    console.log('今天星期三');
    break;
  case 4:
    console.log('今天星期四');
    break;
  case 5:
    console.log('今天星期五');
    break;
  default:
    console.log('今天星期六');
    break;
}
```