# JavaScript

## 为什么学习

> JavaScript是世界上最流行的脚本语言
> 在Web世界里，只有JavaScript能跨平台、跨浏览器驱动网页，与用户交互

## ECMAScript & JavaScript

> ECMAScript是一种语言标准，而JavaScript是网景公司对ECMAScript标准的一种实现

## 开始基础学习 2017/3/21 8:12:06 

- 基本语法
- 数据类型和变量
- 字符串
- 数组
- 对象
- 条件判断
- 循环
- Map和Set
- iterable

### 基本语法

> JavaScript引擎自动加分号在某些情况下会改变程序的语义，导致运行结果与期望不一致
> JavaScript严格区分大小写，如果弄错了大小写，程序将报错或者运行不正常

### 数据类型和变量

> 第一种是==比较，它会自动转换数据类型再比较，很多时候，会得到非常诡异的结果；
第二种是===比较，它不会自动转换数据类型，如果数据类型不一致，返回false，如果一致，再比较;
> 由于JavaScript这个设计缺陷，不要使用==比较，始终坚持使用===比较。
> 不用var申明的变量会被视为全局变量，为了避免这一缺陷，所有的JavaScript代码都应该使用strict模式。

### 字符串

> ES6新增了一种模板字符串，表示方法和上面的多行字符串一样，但是它会自动替换字符串中的变量：

    var name = '小明';
    var age = 20;
    var message = `你好, ${name}, 你今年${age}岁了!`;
    alert(message);
    
### 数组

> 大多数其他编程语言不允许直接改变数组的大小，越界访问索引会报错。然而，JavaScript的Array却不会有任何错误。在编写代码时，不建议直接修改Array的大小，访问索引时要确保索引不会越界。
> 如果不给slice()传递任何参数，它就会从头到尾截取所有元素。利用这一点，我们可以很容易地复制一个Array

    var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
    var aCopy = arr.slice();
    aCopy; // ['A', 'B', 'C', 'D', 'E', 'F', 'G']
    aCopy === arr; // false
    
> concat()方法把当前的Array和另一个Array连接起来，并返回一个新的Array
> **所以一定要注意返回的对象才是最新的数组，而不是原来的数组**
> 实际上，concat()方法可以接收任意个元素和Array，并且自动把Array拆开，然后全部添加到新的Array里：

    var arr = ['A', 'B', 'C'];
    arr.concat(1, 2, [3, 4]); // ['A', 'B', 'C', 1, 2, 3, 4]
    
    
    