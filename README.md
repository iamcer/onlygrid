# onlygrid
单纯为了网格布局而生的CSS框架，没有对HTML元素的样式做任何改变，大小只有1KB

##容器
- 100%容器 .container-fluid
.container-fluid提供创建100%容器的功能，定义如下：
~~~
.container-fluid {
    display: block;
    width: 100%;
}
~~~
- 固定大小的容器 .container
.container 是固定大小的容器，宽度为1190px，自动水平居中，定义如下：
~~~
.container {
    width: 1190px;
    display: block;
    margin-left: auto;
    margin-right: auto;
}
~~~
##行
.r提供行的功能，宽度100%，并且自带清楚float浮动功能，定义如下：
~~~
.r {
    display: block;
    width: 100%;
    position: relative;
    zoom: 1;
}
.r:after {
    content: "";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}
~~~
##列
这是一个12列的网格布局系统，使用`float:left`和百分比实现列， 列定义如下:
~~~
.c-12, .c-11, .c-10, .c-9, .c-8, .c-7, .c-6, .c-5, .c-4, .c-3, .c-2, .c-1 {
    /*解决float: left列内容为空的时候，列被忽略的问题*/
    min-height: 1px;
    float: left;
}

.c-12 {
    width: 100%;
}

.c-11 {
    width: 91.66666667%;
}

.c-10 {
    width: 83.33333333%;
}

.c-9 {
    width: 75%;
}

.c-8 {
    width: 66.66666667%;
}

.c-7 {
    width: 58.33333333%;
}

.c-6 {
    width: 50%;
}

.c-5 {
    width: 41.66666667%;
}

.c-4 {
    width: 33.33333333%;
}

.c-3 {
    width: 25%;
}

.c-2 {
    width: 16.66666667%;
}

.c-1 {
    width: 8.33333333%;
}
~~~

##列的右偏移
onlygrid.css提供列的右偏移，偏移距离为当前列宽度的整倍数，列偏移定义如下：
~~~
/*采用相对定位进行偏移，偏移的时候其他列布局不受到影响*/
.c-move-right-12, .c-move-right-11, .c-move-right-10, .c-move-right-9, .c-move-right-8, .c-move-right-7, .c-move-right-6, .c-move-right-5, .c-move-right-4, .c-move-right-3, .c-move-right-2, .c-move-right-1 {
    position: relative;
}

.c-move-right-12 {
    left: 100%;
}

.c-move-right-11 {
    left: 91.66666667%;
}

.c-move-right-10 {
    left: 83.33333333%;
}

.c-move-right-9 {
    left: 75%;
}

.c-move-right-8 {
    left: 66.66666667%;
}

.c-move-right-7 {
    left: 58.33333333%;
}

.c-move-right-6 {
    left: 50%;
}

.c-move-right-5 {
    left: 41.66666667%;
}

.c-move-right-4 {
    left: 33.33333333%;
}

.c-move-right-3 {
    left: 25%;
}

.c-move-right-2 {
    left: 16.66666667%;
}

.c-move-right-1 {
    left: 8.33333333%;
}
~~~
