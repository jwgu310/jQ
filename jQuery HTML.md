##jq的捕获
###获得内容 - text()、html() 以及 val()
    text() - 设置或返回所选元素的文本内容
    html() - 设置或返回所选元素的内容（包括 HTML 标记）
    val() - 设置或返回表单字段的值
###获取属性 - attr()
##设置内容和属性
$("#btn1").click(function(){

    $("#test1").text("Hello world!");
});

$("#btn2").click(function(){

    $("#test2").html("\<b\>Hello world!\</b\>");
});

$("#btn3").click(function(){

    $("#test3").val("RUNOOB");    
});
##jQuery attr() 方法也用于设置/改变属性值。
$("button").click(function(){

    $("#runoob").attr({
        "href" : "http://www.runoob.com/jquery",
        "title" : "jQuery 教程"
    });
})
##添加新的 HTML 内容  
      append() - 在被选元素的结尾插入内容
      prepend() - 在被选元素的开头插入内容
      after() - 在被选元素之后插入内容
      before() - 在被选元素之前插入内容
- 在下面的例子中，我们创建若干个新元素。这些元素可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建。然后我们通过 append() 方法把这些新元素追加到文本中（对 prepend() 同样有效）：
实例
function appendText()
{
    var txt1="\<p\>文本。\</p\>";              // 使用 HTML 标签创建文本   
    var txt2=$("\<p\>\</p\>").text("文本。");  // 使用 jQuery 创建文本
    var txt3=document.createElement("p");
    txt3.innerHTML="文本。";               // 使用 DOM 创建文本 text with DOM
    $("body").append(txt1,txt2,txt3);        // 追加新元素
}

##删除元素/内容
  
  如需删除元素和内容，一般可使用以下两个 jQuery 方法：
  
      remove() - 删除被选元素（及其子元素） 自己也被移除
      empty() - 从被选元素中删除子元素  不删除自己
      $("p").remove(".abc");    过滤删除  只删除类名为abc的p元素
##jQuery 操作 CSS
  
  jQuery 拥有若干进行 CSS 操作的方法。我们将学习下面这些：
  
      addClass() - 向被选元素添加一个或多个类
      removeClass() - 从被选元素删除一个或多个类
      toggleClass() - 对被选元素进行添加/删除类的切换操作
      css() - 设置或返回样式属性
##jQuery css() 方法
  
  css() 方法设置或返回被选元素的一个或多个样式属性。
  
  $("p").css({"background-color":"yellow","font-size":"200%"}); 
  
##尺寸
 http://www.runoob.com/jquery/jquery-dimensions.html
  