# Grid布局

## 基本概念

![image-20220804175942462](https://static.meowrain.cn/i/2022/08/04/t3ir08-3.png)

![image-20220804180448711](https://static.meowrain.cn/i/2022/08/04/tucn9n-3.png)



1. 容器---有容器属性![image-20220804181037456](https://static.meowrain.cn/i/2022/08/04/txumnt-3.png)

2. 项目---有项目属性![image-20220804181111233](https://static.meowrain.cn/i/2022/08/04/tyagde-3.png)

3. 

   

## 容器属性

  grid-template-columns: ;

  grid-template-rows: ;

  grid-row-gap: ;

  grid-column-gap: ;

  grid-gap: ; //上面两种的简写

  grid-template-areas: ;

  justify-items: ;

  align-items: ;

  place-items: ; //justify-items和align-items的简写

  justify-content: ;

  align-content: ;

  place-content: ;//上面两种的简写

  grid-auto-columns: ;

  grid-auto-rows: ;

  grid-auto-flow: ;



---



## 容器属性-grid-template-*

- `grid-template-rows`

- `grid-template-columns`
- `grid-auto-rows `

想要多少行或者列，就填写相应的属性值的个数，不填写，则自动分配



### rows&columns

> 这里要说明一下，`grid-template-rows`没有设定的时候，item会占满container的高，如果`grid-template-columns`没有设定的时候，item会占满container的宽

> **auto-fill**，有时，单元格的大小是固定的，但是容器的大小不确定，这个属性就会自动填充
>
> ![image-20220804184020625](https://static.meowrain.cn/i/2022/08/04/ufm95l-3.png)

> 为了方便表示比例关系，网格布局提供了fr关键字(frction的缩写，意为片段)
>
> grid-template-columns: repeat(4,1fr);// 宽度平均分成4份

> minxmax()，函数产生一个长度范围，表示长度就在这个范围中，它接受两个参数，分别为最小值和最大值
>
> `grid-template-columns: 1fr minmax(150px,1fr)`最小不会小于150px

**HTML&CSS**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="grid.css">
</head>
<body>
    <div class="container">
        <div class="item item-1">1</div>
        <div class="item item-2">2</div>
        <div class="item item-3">3</div>
        <div class="item item-4">4</div>
        <div class="item item-5">5</div>
        <div class="item item-6">6</div>
        <div class="item item-7">7</div>
        <div class="item item-8">8</div>
        <div class="item item-9">9</div>
    </div>
</body>
</html>
```

```css
* {
    padding: 0;
    margin: 0;
}
.container {
    display: grid;
    width: 600px;
    height: 600px;
    border: 10px solid skyblue;
    grid-template-columns: 200px 200px 200px;
  /* 可以用这个代替 grid-template-columns: repeat(3,200px); */
     /* grid-template-columns: repeat(3,1fr); */
    grid-template-rows: 200px 200px 200px;
 /* 可以用这个代替 grid-template-rows: repeat(3,200px); */
}
.item {
    color:brown;
}
.item-1 {
    background-color: black;
}
.item-2 {
    background-color: lightblue;
}
.item-3 {
    background-color: lightgreen;
}
.item-4 {
    background-color: lightyellow;
}
.item-5 {
    background-color: antiquewhite;
}
.item-6 {
background-color: red;
}
.item-7 {
background-color: aquamarine;
}
.item-8 {
background-color: beige;
}
.item-9 {
background-color: blue;
}

```

图:\

![image-20220804182912031](https://static.meowrain.cn/i/2022/08/04/u90glp-3.png)

### gap

  row-gap: 20px;

  column-gap: 20px;

上面这串css代码相当于`gap: 20px 20px `



```css
* {
    padding: 0;
    margin: 0;
}
.container {
    display: grid;
    width: 600px;
    height: 600px;
    border: 10px solid skyblue;
    grid-template-columns: [c1] 200px [c2] 200px [c3] 200px [c4];
    grid-template-rows: repeat(3,200px);
    row-gap: 20px;
    column-gap: 20px;
}
.item {
    color:brown;
}
.item-1 {
    background-color: black;
}
.item-2 {
    background-color: lightblue;
}
.item-3 {
    background-color: lightgreen;
}
.item-4 {
    background-color: lightyellow;
}
.item-5 {
    background-color: antiquewhite;
}
.item-6 {
background-color: red;
}
.item-7 {
background-color: aquamarine;
}
.item-8 {
background-color: beige;
}
.item-9 {
background-color: blue;
}

```

![image-20220804213440373](https://static.meowrain.cn/i/2022/08/04/zarshm-3.png)





### grid-template-areas

一个区域由单个或多个单元格组成，由你决定

> ![image-20220804214030515](https://static.meowrain.cn/i/2022/08/04/zea31q-3.png)

**css**

```css
* {
    padding: 0;
    margin: 0;
}
.container {
    display: grid;
    width: 600px;
    height: 600px;
    border: 10px solid skyblue;
    grid-template-areas: 'a b c'
                         'd e f'
                         'g h j';
}
.item {
    color:brown;
}
.item-1 {
    background-color: black;
}
.item-2 {
    background-color: lightblue;
}
.item-3 {
    background-color: lightgreen;
}
.item-4 {
    background-color: lightyellow;
}
.item-5 {
    background-color: antiquewhite;
}
.item-6 {
background-color: red;
}
.item-7 {
background-color: aquamarine;
}
.item-8 {
background-color: beige;
}
.item-9 {
background-color: blue;
}

```

**html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="grid.css">
</head>
<body>
    <div class="container">
        <div class="item item-1">1</div>
        <div class="item item-2">2</div>
        <div class="item item-3">3</div>
        <div class="item item-4">4</div>
        <div class="item item-5">5</div>
        <div class="item item-6">6</div>
        <div class="item item-7">7</div>
        <div class="item item-8">8</div>
        <div class="item item-9">9</div>
    </div>
</body>
</html>
```

**效果**

![image-20220804213723930](https://static.meowrain.cn/i/2022/08/04/zcgbyp-3.png)



### justify-items(水平方向)&align-items(垂直方向)

![image-20220804214522567](https://static.meowrain.cn/i/2022/08/04/zh7kwm-3.png)





案例：让盒子水平垂直居中

> 注：
>
>  `place-items: center center;`相当于`    justify-items: center;align-items: center;`
>
> 效果是一样的，可以让盒子水平垂直居中

**HTML**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="grid.css">
</head>
<body>
    <div class="container">
        <div class="yyds">yyds</div>
        <div class="yyds">yyds</div>
        <div class="yyds">yyds</div>
        <div class="yyds">yyds</div>
    </div>
</body>
</html>
```

**CSS**

```css
* {
    padding: 0;
    margin: 0;
}

.container {
    width: 800px;
    height: 800px;
    display: grid;
    grid-template-columns: 400px 400px;
   grid-template-rows: 400px 400px;
    place-items: center center;
}

.yyds {
    width: 200px;
    height: 200px;
    background-color: aqua;
    border: 1px solid red;
}
```

效果：![image-20220804220647445](https://static.meowrain.cn/i/2022/08/04/10hocu0-3.png)





### justify-content/align-content

设置整个内容区域的水平和垂直的对齐方式

![image-20220804220910784](https://static.meowrain.cn/i/2022/08/04/10j8qj5-3.png)



```css
* {
    padding: 0;
    margin: 0;
}

.container {
    width: 800px;
    height: 800px;
    display: grid;
    justify-content: center;
    align-content: center;
}

.yyds {
    width: 200px;
    height: 200px;
    background-color: aqua;
    border: 1px solid red;
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="grid.css">
</head>
<body>
    <div class="container">
        <div class="yyds">yyds</div>
    </div>
</body>
</html>
```

### grid-auto-columns/grid-auto-rows

> 用来设置多出来的项目宽和高

![image-20220804232440727](https://static.meowrain.cn/i/2022/08/04/12fw083-3.png)



### grid-column-start/grid-column-end&grid-row-start/grid-row-end

![image-20220804235204265](https://static.meowrain.cn/i/2022/08/04/12wcl6x-3.png)



比如这个，我用grid布局把列分成了五份

![image-20220804235438469](https://static.meowrain.cn/i/2022/08/04/12xqmd0-3.png)

```css
.item-1 {
    background-color: black;
    grid-column-start: 1;
    grid-column-end: 3;
 /* grid-column: 1/3; */
}
```

从左边第一根数到第三根，就是第一个黑色盒子的宽





### grid-area

![image-20220805000650214](https://static.meowrain.cn/i/2022/08/05/3vhlc-3.png)