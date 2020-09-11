# HTML 面试题

## 1. 如何理解语义话？
> 非语义话


~~~html
<div>Title</div>
<div>
    <div>Lorem ipsum dolor sit amet</div>
    <div>
            <div>list_1</div>
            <div>list_2</div>
    </div>
</div>
~~~

> 语义话

~~~html
<h1>Title</h1>
<div>
    <p>Lorem ipsum dolor sit amet</p>
    <ul>
            <li>list_1</li>
            <li>list_2</li>
    </ul>
</div>
~~~

> 总结
> * 语义话增加路代码的可读性
> * 让搜索引擎更容易爬取（SEO）
 

## 2. 默认情况下， 哪些HTML标签是快级元素， 哪些是内联元素？

> 块状元素： display: block/table; div, h1, h2, table, ui, ol, ol, etc.
> 内联元素： display: inline/inline-block; span, img, input, button, etc. 
> 区别： 最大区别为块状元素独占一行， 内联元素不独占一行。