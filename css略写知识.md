### css知识略写
1.在使用div+css布局时，尽量避免指定元素的宽度和高度，这种砌砖头的写法这会带来许多不确定的影响，增加调试麻烦，

2.div高度是由其内部文档流元素高度综合决定的（核心）；文档流：文档内元素的流动的方向；

3.注意理解定位相关方面的知识，尤其是`position:relative,position:absolute,position:fixed`,在日常布局中经常使用，

4.对于内联元素需要设置width,height,padding，margin时，可以使用display：inline-block;block,（基础）

5.理解<font color=red>伪元素和伪类</font>的区别，伪元素：直意为伪造的元素，为了达到某种效果，增加一个元素， 然后再添加样式，例:

    p:first-letter {color: red}
    I love Web.</p>
<font color=red>I</font> love Web

//伪元素：frist-letter添加样式到第一个字母

如果不是用伪元素的话，就得按照下面的方法做：

    .first-letter {color: red}
    <p><span class='first-letter'>I</span> love Web.</p>
//给首字母添加一个`span`元素，然后给 `span` 增加样式。
伪类：本质上是一个类选择器，为了达到在特定状态下呈现样式，可以使用伪类诸如：`a:hover`;`a:visited`……
例:

    p>i:first-child {color: red}
    <p>
    <i>first</i>
    <i>second</i>
    </p>
  <font color=red>first</font><br/>
                        second

//伪类 :first-child 添加样式到第一个子元素
如果我们不使用伪类，而希望达到上述效果，可以这样做：

    .first-child {color: red}
    <p>
    <i class="first-child">first</i>
    <i>second</i>
    </p>
即我们给第一个子元素添加一个类，然后定义这个类的样式。

所以两者的区别就是：

    伪类的效果可以通过添加一个实际的类来达到，而伪元素的效果则需要通过添加一个实际的元素才能达到，这也是为什么他们一个称为伪类，一个称为伪元素的原因。
    
6.了解css `float`相关知识，布局时经常使用，

7.`line-height`可以控制元素的高度，一些情况下可以不用写`height`

8.`vertical-align`在内联元素居中对齐方面发挥重要作用，详细了解相关知识

9.字体不同，字体的高度也不同，内联元素的默认行高受到浏览器的影响也不尽相同，

10.两种盒模型，`content-box`和`border-box`，border-box目前在布局上越来越成为趋势了。

    

