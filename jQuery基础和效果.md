#JQuery

    $(this).hide() - 隐藏当前元素
    $("p").hide() - 隐藏所有 <p> 元素
    $("p.test").hide() - 隐藏所有 class="test" 的 <p> 元素
    $("#test").hide() - 隐藏所有 id="test" 的元素

##语法
- 在完全加载（就绪）之后运行 jQuery 代码。
   $(document).ready(function(){
   // 开始写 jQuery 代码...
  });
##选择器
#####元素选择器
   $("p")    在页面中选取所有p元素
##### #id选择器 
   $("#test")  通过 id 选取元素
##### .class选择器
   $(".test")  通过类查找元素

##事件  
        鼠标事件               键盘事件             表单事件 	         文档/窗口事件
        click 	            keypress            submit 	               load
        dblclick双击 	    keydown键按下      	change                 resize
        mouseenter  	    keyup键抬起 	        focus 获取焦点          scroll
        mouseleave 	  	                        blur 失去焦点	       unload
        mousedown鼠标按下
        mouseup鼠标抬起
        hover 光标悬停
 -  $("p").click(function(){
      鼠标点击p元素后执行的代码!!
   });
   
 -  $("#p1").mouseenter(function(){
     alert("p1");  鼠标移入p1时，桌面弹出p1
   });
   
#jquery效果

> $(selector).show(speed,callback);
  可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。 
  可选的 callback 参数是隐藏或显示完成后所执行的函数名称。
  
##显示和隐藏       (可以指定时间)
  $("#hide").click(function(){
        $("p").hide(); 隐藏
  });
  
  $("#show").click(function(){
          $("p").show();  显示
  });
  $("button").click(function(){
    $("p").toggle();  切换
  });
  > toggle() 方法来切换 hide() 和 show() 方法。

    
##淡入淡出        (可以指定时间)

  jQuery fadeIn(speed,callback)淡入
  jQuery fadeOut(speed,callback)淡出
  jQuery fadeToggle(speed,callback)切换淡入和淡出
  jQuery fadeTo(speed,opacity,callback)渐变为给定的不透明度（值介于 0 与 1 之间）。
  
- 实例 $("button").click(function(){
          $("#div1").fadeIn();
          $("#div2").fadeIn("slow");
          $("#div3").fadeIn(3000);
       });

##滑动       (可以指定时间)

    slideDown(speed,callback)向下滑
    slideUp(speed,callback)向上
    slideToggle(speed,callback)切换上下
##动画
$(selector).animate({params},speed,callback);
必需的 params 参数定义形成动画的 CSS 属性。
可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。
可选的 callback 参数是动画完成后所执行的函数名称。

#####jQuery animate() - 操作多个属性

实例
$("button").click(function(){
  $("div").animate({
    left:'250px',
    opacity:'0.5',
    height:'150px',
    width:'150px'
  });
});
##停止动画
 $(selector).stop(stopAll,goToEnd);
可选的 stopAll 参数规定是否应该清除动画队列。默认是 false，即仅停止活动的动画，允许任何排入队列的动画向后执行。
可选的 goToEnd 参数规定是否立即完成当前动画。默认是 false。
##callback
- Callback 函数在当前动画 100% 完成之后执行。
   
$("button").click(function(){
  $("p").hide("slow",function(){
    alert("The paragraph is now hidden");
  });
});
##Chaining 链式写法
$("#p1").css("color","red").slideUp(2000).slideDown(2000);

