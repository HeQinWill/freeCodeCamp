## 给h2元素添加inline style(内联样式)
```html
<h2 style="color: red">CatPhotoApp</h2>
```
## 为所有的h2元素创建一个元素选择器
```css
<style>
  选择器 {属性名称: 属性值;}
  /*注意属性值后面的;*/
  h2 {color: red;}
</style>
```
### 实例
```html
<style>
  h2 {color: blue;}
</style>

<h2 >我家的猫咪</h2>
<!--这才是html的注释-->
```
## 类选择器
```css
<style>
  .blue-text {
    color: blue;
  }
  /*css中，类选择器应该添加.为前缀；
  而在HTML中，class属性不能添加.为前缀*/
</style>

<h2 class="blue-text">CatPhotoApp</h2>
```
### 实例
```html
<style>
  .red-text {
    color: red;
  }
</style>

<h2 class="red-text">我家的猫咪</h2>
```
## 字号
```css
h1 {
  font-size: 30px;
}
```
### 比较css和直接使用style的区别
```html
<style>
  .red-text {
    color: red;
    font-size:16px;
  }
</style>

<h2 class="red-text">我家的猫咪</h2>
<p class="red-text">在大家心目中，猫。</p>
<p style="font-size:16px">养动发脾气中重创。</p>
```
## 字体
```css
h2 {
  font-family: Sans-serif;
}
```
## 导入谷歌字体
```html
<link href="https://fonts.gdgdocs.org/css?family=Lobster" rel="stylesheet" type="text/css">
```
### 实例
```html
<link href="https://fonts.gdgdocs.org/css?family=Lobster" rel="stylesheet" type="text/css">

<style>
  .red-text {
    color: red;
  }
</style>

<h2 class="red-text" style="font-family:Lobster">CatPhotoApp</h2>
```
## 添加图片
```html
<img src="https://www.your-image-source.com/your-image.jpg">
<!--img元素是自关闭元素，不需要结束标记。-->
```
## 图片尺寸
``` css
<style>
  .larger-image {
    width: 500px;
  }
</style>
```
## 边框
```css
<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
    border-radius:10px;/*"边框半径"属性来让边框变成圆的*/
    /*改为50%变成圆形边框*/
  }
</style>
```
### 你可以应用多个class到一个元素，只需要在多个class之间用空格分开即可。
```html
<img class="class1 class2">
```
## anchor（锚点）元素
![a元素](http://i.imgur.com/hviuZwe.png)
```html
<p>Here's a 
 <a href="http://freecodecamp.cn">
 link to FreeCodeCamp中文社区 
 </a> for you to follow.
 </p>
 <!--link to FreeCodeCamp中文社区 被加上了链接,放在p中嵌套（nesting）-->
 <p><a href="http://freecatphotoapp.com"> cat photos </a></p>
 <!--把你的a元素的href属性的值替换为一个#，别名hash(哈希)符号，将其变为一个固定链接。-->
 <p>Click here for <a href=# >cat photos</a>.</p>
 <!--把你的图片嵌套进a元素-->
 <a href="#"><img src="/images/relaxing-cat.jpg"></a>
```
## alt属性
```html
<img src="www.your-image-source.com/your-image.jpg" alt="your alt text">
```
## unordered lists（无序列表）
```html
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```
## ordered lists（有序列表）
```html
<ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
```
## form(表单)
```html
<input type="text">
<!-- 占位符(placeholder text)是用户在input(输入)框输入任何东西之前放置在input(输入)框中的预定义文本。-->
<input type="text" placeholder="this is placeholder text">
```
### 给表单增加action和button和必需字段required
```html
<form  action="/submit-cat-photo"> 
<input type="text" required>
<button type="submit">Submit</button>
</form>
```
## 单选按钮radio
```html
<label><input type="radio" name="indoor-outdoor">Indoor</label>
```
## 复选按钮checkboxes
```html
<label><input type="checkbox" name="personality">A</label>
```

## 设置按钮默认被选中
```html
<!--只需在input元素中添加属性checked-->
<label><input type="radio" name="indoor-outdoor" checked>Indoor</label>
<label><input type="checkbox" name="personality" checked>A</label>
```
## div元素
也被称作division(层)元素，是一个盛装其他元素的通用容器。
所以可以利用CSS的继承关系把div上的CSS传递给它所有子元素。

## id属性
除了 class属性之外，每一个 HTML 元素还可以使用 id 属性。
使用 id 属性有若干好处，一旦当你开始使用 jQuery 的时候你会有更深的体会。
id 属性应该是唯一的，虽然浏览器并不强制唯一，但基于最佳实践，这一点是被广泛认可的，所以请不要给一个以上的元素设置相同的 id 属性。
```html
<h2 id="cat-photo-app">
```
和类选择器一样，你也可以使用ID选择器来声明样式。
声明一个叫cat-photo-element的ID选择器 ，并设置背景色为绿色。
```css
#cat-photo-element {
  background-color: green;
}
```
### 区分：
class是在前面加.
id实在前面加#

## 布局
有三个影响HTML元素布局的重要属性：
### padding(内边距)
padding-top、padding-right、padding-bottom 和 padding-left
padding: 10px 20px 10px 20px这四个值以顺时针方式排列：顶部、右侧、底部、左侧，简称：上右下左。
### margin(外边距)
margin-top、margin-right、margin-bottom 和 margin-left 
margin: 10px 20px 10px 20px这四个值以顺时针方式排列：顶部、右侧、底部、左侧，简称：上右下左。
### border(边框)
 margin-top、margin-right、margin-bottom 和 margin-left 

##  CSS 继承
每一个 HTML 页面都有一个 body 元素。
通过将其 background-color 设置为黑色，我们可以证明 body 元素的存在。
```css
<style>
  body {
  background-color: black;}
</style>
```
现在我们证明了每一个 HTML 页面都有一个 body 元素，并且其 body 元素同样能够应用样式。
```css
<style>
  body {
    background-color: black;
    color:green;
    font-family:Monospace;
  }
</style>

<h1>Hello World</h1>
```
除了 pink-text class 之外，再把 blue-text class 应用到你的 h1 元素，让我们来看看谁会赢
如下例，通过用空格分隔多个 class 属性，可对 HTML 元素应用多个 class 属性：
class="class1 class2"
注意：在 HTML 中这些 class 如何排序是无所谓的。
然而，在 style部分中 class 声明的顺序却非常重要，第二个声明总是比第一个具有优先权。因为 .blue-text 是第二个声明，它覆盖了 .pink-text 属性。
```html
<style>
  body {
    background-color: black;
    font-family: Monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
  .blue-text{
    color:blue;
  }
</style>
<h1 class="pink-text blue-text">Hello World!</h1>
```
浏览器读取 CSS 的顺序是从上到下，这意味着，在发生冲突时，浏览器会使用最后的 CSS 声明。
在类选择器的上面还是下面是无所谓的,id 属性总是具有更高的优先级。
in-line style（行内样式）的优先级更高
```html
<h1 style="color: white" id="oange-text" class="pink-text blue-text">Hello World!</h1>
```
还有最后一种覆盖 CSS 的方法，这是所有方法中最强大的，但是在讲它之前，我们先讲讲为什么你要覆盖 CSS。
很多情况下，你会使用 CSS 库，这些库可能会意外覆盖掉你自己的 CSS。所以当你需要确保某元素具有指定的 CSS 时，你可以使用 !important。

##  [十六进制表示颜色](https://en.wikipedia.org/wiki/RGB_color_model)
hexadecimal code（十六进制编码），简写为 hex code。
在 CSS 中，我们可以使用 6 位十六进制数字来表示颜色，
每 2 位分别表示红色 (R)、绿色 (G) 和蓝色 (B) 成分。
例如，#000000 是黑色，同时也是可能的数值中最小的。
0 是 hex code（十六进制编码）中最小的一个，它代表颜色的完全缺失。
F 是 hex code（十六进制编码）中最大的一个，它代表最大可能的亮度。
让我们通过把 background-color 的 hex code 修改为 #FFFFFF，以把 body 元素的背景改为白色。
橙色#FFA500，注意#和数字或字母是贴着的
我们也可以通过平均混合所有三种颜色得到不同灰度等级的灰色。
灰色hex code值#808080 深灰色#111111 
红色#F00 
CSS 中表示颜色的另一个方法是使用 rgb 值
rgb(0, 0, 0)

代表白色的 RGB 值看起来是下面的样子：

rgb(255, 255, 255) 