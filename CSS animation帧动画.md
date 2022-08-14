# CSS animation帧动画

## from-to方法

```css
@keyframes meow {
    from {
    background-color: white;
    }
    to {
    background-color: red;
    }
}
```

如上，我们创建了一个名为meow的帧动画，它将会从白色变为红色

接下来，我们在想要使用帧动画的元素中添加css属性

```css
main {
    width: 100px;
    height: 100px;
    background-color: white;
    animation-name: meow; //添加动画,这里可以写一个逗号，添加更多的动画
    animation-duration: 2s; //设置动画时长，这里也可以写一个逗号，添加第二个动画的时长
}
```



---

## %方法

```css
@keyframes meow {
    0% {
        background-color: white;
    }
    25% {
        background-color: #ff8500;
    }
    50% {
        background-color: #0a51cc;
    }
    100% {
        background-color: #1b1e21;
    }
}
```

如果帧动画改成上面这种，那么main盒子就会先白后橙色再蓝色，最后变黑色，动画时长2s





##  案例：移动的小方块

html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" href="animate.css">
</head>
<body>
<main>
    <div></div>
</main>
</body>
</html>
```

css

```css
* {
    padding: 0;
    margin: 0;
}

body {
    width: 100vw;
    height: 100vh;
    background-color: #34495e;
    display: flex;
    justify-content: center;
    align-items: center;
}

main {
    width: 400px;
    height: 400px;
    background-color: white;
}

div {
    width: 100px;
    height: 100px;
    background-color: #ff8500;
    animation-name: meow;
    animation-duration: 5s;
}

@keyframes meow {
    25% {
        transform: translateX(300px); //向右移动300像素
    }
    50% {
        transform: translate(300px,300px);//向右向下移动300px
    }
    75% {
        transform: translate(0px,300px);//向下移动300px
    }
    100% {
        transform: translate(0px,0px); //恢复原始位置
    }
}
```

效果

![动画](https://static.meowrain.cn/i/2022/08/04/fss8u1-3.gif)







##  动画执行的次数

```css
animation-iteration-count: 执行次数;
```

### 无限循环

```css
animation-iteration-count: infinite;
```





## 动画延迟执行

```css
animation-delay: 秒数;
```



## 动画流畅执行

```css
animation-direction: alternate; // 0 - 100 100-0缓慢变化
animation-direction: alternate-reverse;//100-0 0-100缓慢变化
```





案例：小球下落动画

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" href="animate.css">
</head>
<body>
<div class="container">
    <div class="ball"></div>
    <hr>
</div>
</body>
</html>
```

```css
* {
    padding: 0;
    margin: 0;
}

body {
    width: 100vw;
    height: 100vh;
    background-color: #34495e;
    display: flex;
    justify-content: center;
    align-items: center;
}

.ball {
    border-radius: 50%;
    width: 100px;
    height: 100px;
    background-color: #fff;
    animation-name: ball;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
}

@keyframes ball {
    from {
        border-radius: 50% 50% 40% 40%;
    }
    to {
        transform: translateY(-50px);
    }
}
```

效果

![动画](https://static.meowrain.cn/i/2022/08/04/nu7foi-3.gif)
