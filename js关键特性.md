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

