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