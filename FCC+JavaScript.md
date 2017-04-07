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
```js
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
```js
变量名的第一个单词的首写字母小写，后面的单词的第一个字母大写。
var someVariable;
var anotherVariableName;
var thisVariableNameIsTooLong;
```
## 运算
```js
var sum = 10 + 10;
var difference = 45 - 33;
var product = 8 * 10;
var quotient = 66 / 33;
myVar++;
myVar--;
var ourDecimal = 5.7;
var product = 2.0 * 2.5;
var quotient = 4.4 / 2.0;
var remainder = 11 % 3;
var myVar += 5; 
var myVar -= 5;
myVar *= 5;
myVar /= 5;
```
[不是所有的实数都可以用 浮点数 来表示。因为可能存在四舍五入的错误](https://en.wikipedia.org/wiki/Floating_point#Accuracy_problems)
### 温度转换小例子
```js
function convert(celsius) {
  // Only change code below this line
  var fahrenheit=celsius*9/5+32;
  // Only change code above this line
    return fahrenheit;
}
// Change the inputs below to test your code
convert(30);
```
## Declare String Variables
字符串是用单或双引号包裹起来的一连串的零个或多个字符。  
### 在引号前面使用 反斜杠 (\) 来转义引号
```js
var sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```
### 单双引号
在 JavaScript 中的 字符串 要用单引号或双引号来包裹它，只要你在开始和结束都使用相同类型的引号，单引号和双引号的功能在JavaScript中是相同的。
当我们需要在字符串中使用与开头结尾相同的引号时，我们需要对引号进行 转义 。
若字符串中有很多双引号时，使用转义字符可能导致难以阅读，这时开头结尾可以使用单引号，而内部可以直接用双引号不用转义。
```js
ar myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
```
### 转义字符
|Code|Output|
| --   | -----:  |
| \\'  | 单引号 |
|\\"|双引号|
| \\\ |反斜杠符|
|\\n|	换行符|
|\\r|	回车符|
|\\t|	制表符|
|\\b|	退格符|
|\\f|	换页符|
### 连接字符串
连接操作不会添加两个字符串之外的空格，所以想加上空格的话，你需要自己在字符串里面添加。
#### 1. 用+放在两个字符串之间
#### 2. 用+=连接字符串到现有字符串的结尾
```js
var ourStr = "I come first. ";
ourStr += "I come second.";
```
#### 3. 填字风格的字符串
```js
var ourName = "Free Code Camp";
var ourStr = "Hello, our name is " + ourName + ", how are you?";
```
### 获取字符串长度
你可以通过在字符串变量或字符串后面写上 .length 来获得字符串变量 字符串 值的长度。
```js
var firstNameLength = 0;
var firstName = "Ada";
firstNameLength = firstName.length;
NameLength="Ada Lovelace".length;
```
### 索引
[ ]叫中括号，{ }叫大括号，( )叫小括号。  

JavaScript中只有字符串类型，没有字符类型。那么如何获取到字符串中的某个字符呢？  
我们通过[索引] 来获得对应的字符。

大多数现代编程语言，如JavaScript，不同于人类从1开始计数。它们是从0开始计数，这被称为 基于零 的索引。
```js
var firstLetterOfFirstName = "";
var firstName = "Ada";
firstLetterOfFirstName = firstName[0];
```
### 字符串的不可变性
理解字符串的不可变性！当你搞懂不可变性后immutable.js对于你就是小菜一碟了。

在 JavaScript 中，字符串的值是不可变的，这意味着一旦字符串被创建就不能被改变。
```js
var myStr = "Bob";
myStr[0] = "J";
```
是不会把变量 myStr 的值改变成 "Job" 的，因为变量 myStr 是不可变的。注意，这并不 意味着 myStr 永远不能被改变，只是字符串字面量 string literal 的各个字符不能被改变。改变 myStr 中的唯一方法是重新给它赋一个值，就像这样：
```js
var myStr = "Bob";
myStr = "Job";
```
### 倒数第N个字符
为了得到一个字符串的最后一个字符，你可以用[字符串的长度减去1]。
```js
var firstName = "Ada";
var lastLetterOfFirstName = firstName[firstName.length - 1];
```
## 数组
### 1. 创建一个包含 字符串 和 数字 的数组
```js
var array = ["John", 23];
```
### 2. 创建一个名为 myArray的多维数组
```js
var ourArray = [["the universe", 42], ["everything", 101010]];
```
### 3. 数组索引的使用与字符串索引一样，不同的是，通过字符串的索引得到的是一个字符，通过数组索引得到的是一个条目。  
与字符串类似，数组也是 基于零 的索引，因此数组的第一个元素的索引是 0。
```js
var ourArray = [1,2,3];
var ourData = ourArray[0]; // equals 1
```
REVIEW字符串的索引
```js
var firstLetterOfFirstName = "";
var firstName = "Ada";
firstLetterOfFirstName = firstName[0];
```
### 4. 与字符串的数据不可变不同，数组的数据是可变的，并且可以自由地改变。
```js
var ourArray = [1,2,3];
ourArray[1] = 3; // ourArray now equals [1,3,3].
```
### 5. 多维数组
可以把多维数组看作成是一个数组中的数组。当使用[ ]去访问数组的时候，第一个[index]访问的是第N个子数组，第二个[index]访问的是第N个子数组的第N个元素。
```js
var arr = [ [1,2,3],
            [4,5,6],
            [7,8,9],
            [[10,11,12], 13, 14]
          ];
arr[0]; // 等于 [1,2,3]
arr[1][2]; // 等于 6
arr[3][0][1]; // 等于 11
```
### 6. 追加数据到数组末尾
.push() 接受把一个或多个参数，并把它“推”入到数组的末尾。
```js
var ourArray = ["Stimpson", "J", "cat"];
ourArray.push(["happy", "joy"]); 
// ourArray now equals ["Stimpson", "J", "cat", ["happy", "joy"]]
ourArray.push("happy", "joy"); 
// ourArray now equals ["Stimpson", "J", "cat", "happy", "joy"]
```
### 7. 移出数组中最后一个元素
.pop() 函数用来“抛出”一个数组末尾的值。我们可以把这个“抛出”的值赋给一个变量存储起来。  
数组中任何类型的条目（数值，字符串，甚至是数组）可以被“抛出来” 。
```js
var ourArray = [1,2,3];
var removedFromOurArray = ourArray.pop(); 
// removedFromOurArray now equals 3, and ourArray now equals [1,2]
```
### 8. 移出第一个元素
.shift()的工作原理就像 .pop()，但它移除的是第一个元素，而不是最后一个。
### 9. 移入一个元素到数组的头部
.unshift() 函数用起来就像 .push() 函数一样, 但不是在数组的末尾添加元素，而是在数组的头部添加元素。

## Write Reusable JavaScript with Functions
### 1. 函数
```js
function myFunction(){
  console.log("Hi World");
}
myFunction();
```
### 2. 参数
函数的参数parameters在函数中充当占位符(也叫形参)的作用，参数可以为一个或多个。  
调用一个函数时所传入的参数为实参，实参决定着形参真正的值。简单理解：形参即形式、实参即内容。
```js
function ourFunction(a, b) {
  console.log(a - b);
}
ourFunction(10, 5); // Outputs 5
```
### 3. 作用域
在函数外定义的变量具有全局作用域。这意味着，具有全局作用域的变量可以在代码的任何地方被调用。

这些没有使用var关键字定义的变量，会被自动创建在全局作用域中，形成全局变量。当在代码其他地方无意间定义了一个变量，刚好变量名与全局变量相同，这时会产生意想不到的后果。因此你应该总是使用var关键字来声明你的变量。

```js
var myGlobal=10;//不加var也是全局变量
function fun1() {
  oopsGlobal=5;//函数内不加var同样是全局变量
}
```
在一个函数内声明的变量，以及该函数的参数都是局部变量，意味着它们只在该函数内可见。
```js
function myTest() {
  var loc = "foo";
  console.log(loc);
}
myTest(); // "foo"
console.log(loc); // "undefined",在函数外，loc 是未定义的。
```
一个程序中有可能具有相同名称的 局部 变量 和 全局 变量。在这种情况下，局部 变量将会优先于 全局 变量。

### 4. return传出数据
我们可以把数据通过函数的 参数 来传入函数，也可以使用 return 语句把数据从一个函数中传出来。
```js
function plusThree(num) {
  return num += 3;//错误示例  
  return num + 3;
}
plusThree(5); // 错误示例 
var answer = plusThree(5); // 8
```
## 队列
新的条目会被加到 队列 的末尾，旧的条目会从 队列 的头部被移出。
```js
function queue(arr, item) {
  // Your code here
  arr.push(item);
  item=arr[0];
  arr.shift();
  return item;  // Change this line
}

// Test Setup
var testArr = [1,2,3,4,5];

// Display Code
console.log("Before: " + JSON.stringify(testArr));
console.log(queue(testArr, 6)); // Modify this line to test
console.log("After: " + JSON.stringify(testArr));
```
## 一些简单的语法
### 1. 布尔
Boolean 值绝不会写作被引号包裹起来的形式。字符串 的 "true" 和 "false" 不是 布尔值，在 JavaScript 中也没有特殊含义。
### 2. if 语句
### 3. 比较
  1   ==  1    // true  
   1   ==  2    // false  
   1   == '1'   // true  
  "3"  ==  3    // true 

3 === 3   // true  
3 === '3' // false

1 != 2      // true  
1 != "1"    // false  
1 != '1'    // false  
1 != true   // false  
0 != false  // false

3 !== 3   // false  
3 !== '3' // true  
4 !== 3   // true

 5 > 3   // true  
 7 > '3' // true  
 2 > 3   // false  
'1' > 9  // false

 6  >=  6  // true  
 7  >= '3' // true  
 2  >=  3  // false  
'7' >=  9  // false

  2 < 5  // true  
'3' < 7  // true  
  5 < 5  // false  
  3 < 2  // false  
'8' < 4  // false

  4 <= 5  // true  
'7' <= 7  // true  
  5 <= 5  // true  
  3 <= 2  // false  
'8' <= 4  // false
### 4. 逻辑与&&
### 5. 逻辑或||
### 6. if···else···
### 7. if···else if···
```js
if (num > 15) {
  return "Bigger than 15";
} 
else if (num < 5) {
  return "Smaller than 5";
}
else {
  return "Between 5 and 15";
}
```
### 8. switch case
如果你有非常多的选项需要选择，可以使用switch语句。根据不同的参数值会匹配上不同的case分支，语句会从第一个匹配的case分支开始执行，直到碰到break就结束。
测试case 值使用严格等于，break关键字告诉javascript停止执行语句。如果没有break关键字，下一个语句会继续执行。
```js
switch (num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  default:
    defaultStatement;
}

switch(val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
```
P.S.应该'b'==="b"是true
因为=== 总是返回 true 或 false，所以我们可以直接返回比较的结果：
```js
function isEqual(a,b) {
  return a === b;
}
```