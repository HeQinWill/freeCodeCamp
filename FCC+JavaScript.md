## Declare JavaScript Variables
### JavaScript提供七种不同的data types(数据类型)，
1. undefined（未定义）
1. null（空）
1. boolean（布尔型）
1. string（字符串）
1. symbol（符号） 
1. number（数字）
1. object（对象）
### Variables（变量）
允许计算机以一种动态的形式来存储和操作数据，通过操作指向数据的指针而不是数据本身来避免了内存泄露，以上的七种数据类型都可以存储到一个变量（variable）中。  

Variables 非常类似于你在数学中使用的x,y变量, 这意味着它们都是以一个简单命名的名字来代替我们赋值给它的数据。计算机中的variables（变量）与数学中的变量不同的是，计算机可以在不同的时间存储不同类型的变量。

Variable （变量）的名字可以由数字、字母、$ 或者 _组成，但是不能包含空格或者以数字为首。
## 简单赋值
```javascript
var a = 7;
var b = a;
var c;

a=5;
b=10;
c="I am a";

a = a + 1;
b = b + 5;
c = c + " String!";
```
## 驼峰命名法
```javascript
变量名的第一个单词的首写字母小写，后面的单词的第一个字母大写。
var someVariable;
var anotherVariableName;
var thisVariableNameIsTooLong;
```
## 运算
```javascript
var sum = 10 + 10;
var difference = 45 - 33;
var product = 8 * 10;
var quotient = 66 / 33;
myVar++;
myVar--;
var ourDecimal = 5.7;
```
[不是所有的实数都可以用 浮点数 来表示。因为可能存在四舍五入的错误](https://en.wikipedia.org/wiki/Floating_point#Accuracy_problems)