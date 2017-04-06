## 基本结构
```html
<script>
    //开始写第一个jQuery语句，所有jQuery方法都是由$开始的，通常称作为 美元符号，或者简称为bling。
$(document).ready
(
    function() {
        //添加动作效果
    }
);
</script>
```
## 用 $("WILL")来选中,用.addClass("WILL")来添加效果
```javascript
//jQuery通过选择器来选择一个元素的，然后操作元素做些改变。
function() 
{
    $("button").addClass("animated bounce");//要让所有的按钮做弹回效果
    $(".well").addClass("animated shake"); //class为well的div元素晃动，class用.
    $("#target3").addClass("animated fadeOut");//id为target3的button元素消失,css用#
}
```
### 选择器类型
1. 元素type选择器：$("button")
1. class选择器：$(".btn")
1. id选择器：$("#target1")
### 添加的类可以有
1. animated
1. shake
1. btn-primary
1. hinge


## 通过.removeClass()方法去掉元素上的class
```javascript
    $("button").removeClass("btn-default");
```
## 通过.css()来改变HTML元素的CSS样式
```javascript
    $("#target1").css("color", "red");
    //这跟通常的CSS语法有点不同，这里CSS的属性和值是在引号内的，并且用逗号分开。
```
## 通过.prop()的方法让你来调整元素的属性
```javascript
    $("#target1").prop("disabled", true);
    //当你把按钮设置成不可选以后，这会让按钮变灰并且不能点击。
```
## 通过.html()方法可以添加HTML标签和文字到元素，而元素之前的内容都会被方法的内容所替换掉
```javascript
    $("h3").html("<em>jQuery Playground</em>");
```
### 通过em[emphasize]标签来重写和强调标题文本的
### 通过.text()只能改变文本但不能修改标记。只会把传进来的任何东西(包括标记)当成文本来显示。 
## 通过.remove() 的方法可以移除HTML元素
```javascript
        $("#target4").remove();
```
## 通过.appendTo()方法可以把选中的元素加到其他元素中
```javascript
    $("#target2").appendTo("#right-well");//把target2元素从left-well移到right-well中
```
## 通过.clone()方法可以拷贝元素
两个jQuery方法合在一起使用了？这就叫方法链function chaining，使用起来很方便。
```javascript
    $("#target5").clone().appendTo("#left-well");
```
## 访问父/子元素
### 通过.parent()允许你访问指定元素的父元素
让#target1元素的父元素的背景色变成红色
```javascript
    $("#target1").parent().css("background-color", "red")
```
### 通过.children()允许你访问指定元素的子元素
让#right-well元素的所有子元素的文本颜色都变成橙色（orange）
```javascript
    $("#right-well").children().css("color", "orange")
```
## 用CSS选择器来选取元素
你已经看到了当用jQuery选择器通过id属性来选取元素的时候是多么方便，但是你不能总是写这么整齐的id。
### CSS选择器 target:nth-child(n) 允许你按照索引顺序(从1开始)选择目标元素的所有子元素。
给目标元素的第二个子元素添加animated和bounce class
```javascript
    $(".target:nth-child(2)").addClass("animated bounce");
```
### 选择奇数
jQuery里的索引是从0开始的，也就是说：:odd 选择第2、4、6个元素，因为target#2(索引为1)，target#4(索引为3)
### 选择偶数
获取class为target且索引为偶数的所有元素
```javascript
    $(".target:even").addClass("animated shake");
```        
## 整个body来个效果结束
```javascript
    $("body").addClass("animated hinge");//铰链效果
```