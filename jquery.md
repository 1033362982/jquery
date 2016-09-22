#jquery
##1.jquery基本格式：要实现功能的代码写在script标签中
###<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <script>
        // alert("hellow world")
        console.log("hello world")
    </script>
</body>
</html>
##2.jquery选择器
###先引入jquery，用<script src="script/jquery.js"></script>语句，选择器形式为$("选择器名")，示例如下：
####<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style type="text/css">
        .box{
            height: 100px;
            width: 100px;
            background-color: red;
                }
    </style>
</head>
<body>
    <div class="box"></div>
    <script src="script/jquery.js"></script>
    <script>
        $(".box").css("background-color","blue");
    </script>
</body>
</html>  实现一个背景色为红色的盒子背景色变成蓝色
##3.点击事件：改变样式用.css,改变属性用.attr
###$(".box").click(function(){
             $(".box").css("background-color","blue");
            // $(this).css("background-color","blue");
        });
##4.节点种类：元素节点，文本节点，属性节点
##5.JS分为：DOM:文档对象模型；BOM:浏览器对象模型；ECMAscript:语言标准
##6.jquery常用事件：click,mouse,hover;blur,focus
##7.jquery常用方法：.attr .css addClass removeClass siblings find parent eq index
##8.函数名+()/方法名+()即为调用函数
##9.改变元素属性节点：
###<img id="pic" src="images/0.jpg" alt="">
    <script src="script/jquery.js"></script>
    <script>
        $("#pic").click(function(){
            $(this).attr("src","images/1.jpg")
        })
    </script>
##10.siblings找到同级其他元素
##11.通过元素找索引：
###<form id="myForm"action="">
        <input type="button" value="1">
        <input type="button" value="2">
        <input type="button" value="3">
    </form>
    <div class="box">
        <div></div>
        <div></div>
        <div></div>
    </div>
    <script src="script/jquery.js"></script>
    <script>
        $("#myForm input").click(function(){
            var index = $(this).index();
            $(".box div").eq(index).css("background-color","blue").siblings().css("background-color","#fff")
        })
    </script>
##12.index与eq区别：
###index为索引，var num=$(this).index(),把index返回值给num,得到数字；eq得到元素，根据数字找到元素
##13.jquery动画
###显示 "show"
###隐藏 "hide"
###渐入 "fadeIn"
###渐出 "fadeOut"
###下拉 "slideDown"
###上卷 "islideUp"
###切换渐入渐出  "fadeToggle"
###切换上卷下拉  "slideToddle"
###切换显示隐藏  "toggle"
###自定义动画   "animate"
##14.添加节点：
###append：添加子节点，追尾添加
###prepend：在前面添加，给子集添加
###before：中间添加，同级添加
##15.JS六中数据类型：数字，字符串，布尔，null，未定义，对象
##16.日期对象：
###var today=new Date();
    var year=today.getFullYear();
    var month=today.getMonth();
    var Day=today.getDay();
    var hours=today.getHours();
    var minutes=today.getMinutes();
    var seconds=today.getSeconds();
    var time=today.getTime();
    $("#year").text(year);
    $("#month").text(month);
    $("#date").text(Day);
    $("#hours").text(hours);
    $("#minutes").text(minutes);
    $("#seconds").text(seconds);

