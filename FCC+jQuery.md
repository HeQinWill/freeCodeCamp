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