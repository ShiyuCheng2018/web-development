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
> offsetWidth = (内容宽度width+内边距padding+边框border)， 注意： 无外边距
> 因此答案为122px
### 补充： 如何让offsetWith等于100px, 该如何做？
> 只需要加上 box-sizing: border-box, width不仅仅变为内容宽度而是整个box宽度

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
> 相邻元素的margin-top和margin-bottom会发生重叠
> 空白内容的<p></p>也会重叠，类似于忽略
> 答案是15px

## margin负值问题
> margin-top和margin-left负值，元素向上， 向左移动
> margin-right负值， 右侧元素左移， 自身不受影响
> margin-bottom负值, 下方元素下移， 自身不受影响

## BFC理解与应用
* Block format context, 块级格式化上下文
* 一块独立渲染区域， 内部元素的渲染不会影响边界以外的元素
* 形成BFC条件
    * float不是none
    * position是absolute或fixed
    * overflow不是visible
    * display是flex，inline-block等
* 常见的应用
    * 清除浮动 以免脱离文档流
    
## float布局

* 如何实现圣杯布局和双飞翼布局
* 手写clearfix

### 圣杯布局和双飞翼布局的目的
* 三栏布局， 中间一栏最先加载和渲染（内容最重要）
* 俩测内容固定， 中间内容随着宽度自适应
* 一般用于PC网页

> 总结：
> * 使用float布局
> * 俩测使用margin负值， 以便和中间内容横向重叠
> * 防止中间内容被俩测覆盖， 可以用padding或margin
    