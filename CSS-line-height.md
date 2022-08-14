# CSS-position位置-绝对定位和相对定位

## position: relative 相对定位

当元素的定位设置为relative时，它允许你通过CSS指定该元素在当前文档流页面下的相对偏移量。

CSS中，控制各个方向偏移量的属性是left,right,top和bottom

它们代表从原来位置向远离该方向偏移指定的像素，百分比或者em。

```html
<style>
  h2 {
position: relative;
bottom: 10px;

  }
</style>
<body>
  <h1>On Being Well-Positioned</h1>
  <h2>Move me!</h2>
  <p>I still think the h2 is where it normally sits.</p>
</body>
```

<img src="https://static.meowrain.cn/i/2022/08/10/zj16du-3.png" alt="image-20220810214828721" style="zoom:67%;" />

> 把元素的位置设置成相对，不会改变该元素在布局中所占的位置，也不会对其它元素的位置产生影响



### 使用CSS偏移移动相对定位的元素

`top:10px`就是让元素向下移动10像素，同理，`bottom:10px`相当于让元素向上移动10像素。

`left:10px`就是让元素向右移动10px，`right:10px`让元素向左移动10px



## positon: absolute 绝对定位

当position的值设置为absolute时，绝对定位会将元素从当前的文档流里面移除，周围的元素会忽略它，这样我们可以使用CSS的top,bottom,left,right的属性来调整元素的位置

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 400px;
            height: 400px;
            background-color: burlywood;
            position: absolute;
            top: 20px;
        }
        p { 
            text-transform: capitalize;
        }
    </style>
</head>
<body>
    <p>let us see the position</p>
    <div>
    </div>
</body>
</html>
```

![image-20220810220418382](https://static.meowrain.cn/i/2022/08/10/10gban5-3.png)



上面是绝对定位，我们看看相对定位

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 400px;
            height: 400px;
            background-color: burlywood;
            position: relative;
            top: 20px;
        }
        p { 
            text-transform: capitalize;
        }
    </style>
</head>
<body>
    <p>let us see the position</p>
    <div>
    </div>
</body>
</html>
```



![image-20220810220505484](https://static.meowrain.cn/i/2022/08/10/10gu8dc-3.png)



> **从上面我们能看出来，这个positon设置为absolute的话，再设置top:20px，就是忽略周围所有元素，然后把它自己的位置设置为距离浏览器窗口顶部的10px的距离**





## position:fixed 特殊的绝对定位

其类似于绝对位置，也会将元素从当前的文档流中移除

> **但fixed和absolute的最明显的区别就在于，前者定位的元素不会随着皮姆滚动而移动**

### 案例：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: bisque;
            color: blueviolet;
        }
        nav ul {
            text-decoration: none;
        }
        nav ul li {
            display: inline;
            padding-left: 20px;
        }
        div {
            box-sizing: border-box;
            margin: 150px auto;
            width: 400px;
            height: 400px;
            background-color: burlywood;
            text-transform: capitalize;
            text-align: center;
            line-height: 400px;
        }
    </style>
</head>
<body>
    <header>
    <nav id="navbar">
<ul>
    <li>Home</li>
    <li>Archive</li>
    <li>Image</li>
    <li>Experiment</li>
    <li>Contact</li>
</ul>
    </nav>
</header>
    
    <div>
        <p>let us see the position</p>
    </div>
    <div>
        <p>let us see the position</p>
    </div>
    <div>
        <p>let us see the position</p>
    </div>
</body>
</html>
```



![动画](https://static.meowrain.cn/i/2022/08/10/10zvwe9-3.gif)