##遍历祖先


向上遍历 DOM 树


这些 jQuery 方法很有用，它们用于向上遍历 DOM 树：

    parent() 方法返回被选元素的直接父元素。
    parents()方法返回被选元素的所有祖先元素,直到文档的根元素 (<html>)。
    parentsUntil()方法返回介于两个给定元素之间的所有祖先元素

实例
$(document).ready(function(){

返回介于 <span\> 与 <div\> 元素之间的所有祖先元素：
  $("span").parentsUntil("div");

}); 
##向下遍历 DOM 树
  
  下面是两个用于向下遍历 DOM 树的 jQuery 方法：
  
      children()方法返回被选元素的所有直接子元素。也可以使用可选参数来过滤对子元素的搜索
      find()方法返回被选元素的后代元素，一路向下直到最后一个后代。
##有许多有用的方法让我们在 DOM 树进行水平遍历：
  
      siblings()方法返回被选元素的所有兄弟元素。可选参数过滤
      next()返回被选元素的下一个弟弟元素。
      nextAll()返回被选元素的下面所有的弟弟元素。
      nextUntil()返回介于两个给定参数之间的所有弟弟元素。
      prev()
      prevAll()
      prevUntil()
##过滤
      first()方法返回被选元素的首个元素。
      last() 方法返回被选元素的最后一个元素。
      eq() 方法返回被选元素中带有指定索引号的元素。
      filter() 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。
      not() 方法返回不匹配标准的所有元素。  not方法与 filter() 相反。
      
      
      