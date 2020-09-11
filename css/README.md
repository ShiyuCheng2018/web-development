# CSS

## 盒模型计算

~~~html
<!-- 如下代码，请问div1 的 offsetWidth 是多大 -->
<style>
    #div1{
        width: 100px;
        padding: 10px;
        border: 1px solid #ccc;
        margin: 10px
    }   
</style>
<div id="div1"></div>
~~~

## margin纵向重叠问题
~~~html
<!-- AAA 和 BBB 之间的距离是多少？ -->
<style>
    p{
        font-size: 16px;
        line-height: 1;
        margin-top: 10px;
        margin-bottom: 15px;
    }   
</style>
<p>AAA</p>
<p></p>
<p></p>
<p></p>
<p>BBB</p>
~~~