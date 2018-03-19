# Zepto-study
### zepto@1.1.6


### 最外层结构 ###
  最外层是一个自执行的匿名函数,内部定义了$变量，最后`return $`
  在匿名函数的外部， `Zepto`和`$`变量挂载到全局window上
```
  var Zepto = (function(){
    var $
    ..

    return $;
    })()

    window.Zepto = Zepto
    window.$ === undefined && (window.$ = Zepto)
   ...
```




 - zepto.init
 -  zepto.Z = function(dom, selector) {
     dom = dom || []
     dom.__proto__ = $.fn            // fn 替换掉 dom 的原型
     dom.selector = selector || ''
     return dom
   }

[zepto@1.1.6版本 源码解析加中文注释](./zepto@1.1.6.js)
