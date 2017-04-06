## 开始进入Bootstrap的世界
将下列代码加到你的HTML开头来将Bootstrap添加到任意应用中：
```html
<link rel="stylesheet" href="//cdn.bootcss.com/bootstrap/3.3.1/css/bootstrap.min.css"/>
```
然后将所有的HTML内容放在class为container-fluid的div下
## 使图片宽度适应界面
```html
<img class="img-responsive" src="/images/running-cat.jpg">
```
## 居中
你可以用空格分开多个class来为同一个元素添加多个 class 属性
```html
<h2 class="red-text text-center">your text</h2>
```
## 按钮
```html
<button class="btn">在这儿输入想要在按钮上显示的文字</button>
```
### 行内元素与块级元素的区别
通常情况下，你的 button 元素仅与它所包含的文本一样宽。
通过使其成为块级元素，你的按钮将会伸展并填满页面整个水平空间，任何在它之下的元素都会跟着浮动至该区块的下一行。

![行内元素与块级元素的区别](https://i.imgur.com/O32cDWE.png)

注意按钮仍然需要有btn属性！
```html
<button class="btn btn-block">Like</button>
```
### 按钮颜色-深蓝色
深蓝色btn-primary是你的应用的主要颜色
注意按钮仍然需要 btn 和 btn-block 属性！
```html
<button class="btn btn-block btn-primary">Like</button>
```
### 按钮颜色-浅蓝色
浅蓝色 btn-info
注意按钮仍然需要 btn 和 btn-block 属性！
```html
<button class="btn btn-block btn-info">Info</button>
```
### 按钮颜色-红色
红色btn-danger被用来提醒用户该操作具有“破坏性”
注意按钮仍然需要 btn 和 btn-block 属性！ 
```html
 <button class="btn btn-block btn-danger">Delete</button>
 ```
 ## 响应式网格布局
可轻松实现将多个元素放入一行并指定各个元素的相对宽度的需求。Bootstrap 中大多数的class属性都可以设置于 div 元素中。
 ![Bootstraps 的12列网格布局](https://i.imgur.com/FaYuui8.png)
在这张图表中，class属性 col-md-* 正被使用。
在这里，md 表示 medium (中等的)，* 代表一个数字，它指定了这个元素所占的列宽。
通过此图表的属性设置可知，在中等大小的屏幕上(例如笔记本电脑)，元素的列宽被指定了。
若使用 col-xs-* ，
其中 xs 是 extra small 缩写（应用于较小的屏幕，比如手机屏幕），* 是你需要填写的数字，代表在一行中,各个元素应该占的列宽。
```html
  <div class="row">
    <div class="col-xs-4"> <button class="btn btn-block btn-primary">Like</button></div>
    <div class="col-xs-4"> <button class="btn btn-block btn-info">Info</button></div>
    <div class="col-xs-4"> <button class="btn btn-block btn-danger">Delete</button> </div>
  </div>
  ```
把三个按钮一并放入一个 <div class="row"> 元素中；
然后，其中的每一个按钮都需要各自被一个 <div class="col-xs-4"> 元素包裹。
当div 元素设置了 class 属性 row 之后，那几个按钮便可嵌入其中。
## 文字
text-primary为蓝色
 "smaller -image" class ，替换为 Bootstrap的 img-responsive
 ## span 标签来创建行内元素
![inline 元素与 block-level 块级元素的区别](https://i.imgur.com/O32cDWE.png)
把 "Things cats hate" 中的 "hate" 放到 span 标签下。然后为其添加 text-danger class 来使文字变成红色。
```html
<p>Top 3 things cats <span class = "text-danger">hate:</span></p>
```
### 综合示例
```html
<div class="container-fluid">
  <div class="row">
    <div class="col-xs-8">
      <h2 class="text-primary text-center">CatPhotoApp</h2>
    </div>
    <div class="col-xs-4">
      <a href="#"><img class="img-responsive thick-green-border" src="/images/relaxing-cat.jpg"></a>
    </div>
  </div>
</div>
  ```
  ## Font Awesome图标库
  这些图标都是矢量图形，被保存在 .svg 的文件格式中。这些图标就和字体一样，你可以通过像素单位指定它们的大小，它们将会继承其父HTML元素的字体大小。
  你可以将 Font Awesome 图标库增添至任何一个应用中，方法很简单，只需要在你的 HTML 头部增加下列代码即可：
```html
<link rel="stylesheet" href="//cdn.bootcss.com/font-awesome/4.2.0/css/font-awesome.min.css"/>
```
i 元素起初一般是让其它元素有斜体(italic)的功能，不过现在一般用来指代图标。你可以将 Font Awesome 中的 class 属性添加到 i 元素中，把它变成一个图标，比如：
```html
<i class="fa fa-info-circle"></i>
<!--fa-thumbs-up或者fa-trash或者fa-paper-plane-->
``` 

## 综合
### 1. 居中，蓝色字
```html
<!--注意text-primary就是蓝色字，不要误认为是自己建的类名
<style>
  .text-primary{
    text-align: center;
  }
</style>
-->
<h3 class="text-primary text-center">
  jQuery playground
</h3>
```
### 2. 添加响应式
```html
<div class="container-fluid" >
<h3 class="text-primary text-center">jQuery Playground</h3>
</div>
```
### 3. 为我们的内联元素创建一个 Bootstrap 行
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
  </div>
</div>
```
### 4. 把 Bootstrap 行分成两栏来放置我们的元素
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
    </div>
    <div class="col-xs-6">
    </div>
  </div>
</div>
```
### 5. Bootstrap 有一个 class 属性叫做 well，它的作用是为设定的列创造出一种视觉上的深度感
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <div class="well">
                  
      </div>
    </div>
    <div class="col-xs-6">
      <div class="well">
                  
      </div>
    </div>
  </div>
</div>
<!--注意与<div class="col-xs-6 well">效果的区别-->
```
### 6. 在 div 中添加 button 元素
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <div class="well">
        <button class="btn"></button>
        <button class="btn"></button>
        <button class="btn"></button>
      </div>
    </div>
    <div class="col-xs-6">
      <div class="well">
        <button class="btn"></button>
        <button class="btn"></button>
        <button class="btn"></button>
      </div>
    </div>
  </div>
</div>
```
### 7. Bootstrap 还有一种属于按钮的 class 属性叫做 btn-default 为每一个 button 元素增加两个 class 属性: btn 和 btn-default
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <div class="well">
        <button class="btn btn-default"></button>
        <button class="btn btn-default"></button>
        <button class="btn btn-default"></button>
      </div>
    </div>
    <div class="col-xs-6">
      <div class="well">
        <button class="btn btn-default"></button>
        <button class="btn btn-default"></button>
        <button class="btn btn-default"></button>
      </div>
    </div>
  </div>
</div>
```
### 8. 并不是每一个 class 属性都是用于 CSS 的。 有些时候我们创建一些 class 只是为了更方便地在jQuery中选中这些元素。
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <div class="well">
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>             <button class="btn btn-default target"></button>
      </div>
    </div>
    <div class="col-xs-6">
      <div class="well">
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>             <button class="btn btn-default target"></button>
      </div>
    </div>
  </div>
</div>
```
### 9. 除了可以给元素增加 class 属性，还可以给你的每个元素增添一个 id 属性。每一个指定元素的 id 都是唯一的，并且在每个页面中只能使用一次。
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <div class="well" id="left-well">
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
      </div>
    </div>
    <div class="col-xs-6">
      <div class="well" id="right-well">
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
      </div>
    </div>
  </div>
</div>
```
### 10. 为我们的 wells 都标上它们的 id 吧。
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4> #left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4> #right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
        <button class="btn btn-default target"></button>
      </div>
    </div>
  </div>
</div>
```
### 11. 使用jQuery并通过每个按钮各自唯一的 id 来标识出它们。
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" 
                  id="target1"></button>
        <button class="btn btn-default target"
                   id="target2"></button>
        <button class="btn btn-default target"
                   id="target3"></button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target"
                   id="target4"></button>
        <button class="btn btn-default target"
                   id="target5"></button>
        <button class="btn btn-default target"
                   id="target6"></button>
      </div>
    </div>
  </div>
</div>
```
### 12. 正如我们标注了每个 wells， 我们同样想要标注每一个按钮。
```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```
### END
当我们开始使用jQuery，我们将修改HTML元素，但是实际上我们并不是直接在 HTML 文本中修改。  
我们必须确保让每个人都知道，他们不应该直接修改此页面上这些代码，你可以进行评论注释告诉它们在上面修改。