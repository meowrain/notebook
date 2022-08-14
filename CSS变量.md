# CSS变量

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="root.css">
</head>
<body>
    <p>asdfasdfadsfa</p>
</body>
</html>


```



```css
:root {
    --bg-color: blue;
    --ft-color: white;
    --size: 32px;
}
body {
    background-color: var(--bg-color);
    color: var(--ft-color);
    font-size: var(--size);
}
```

> 如上，:root下放的是变量，--变量名 来创建变量。在使用变量的时候，我们通过var(变量名)来使用变量

![image-20220810144925661](https://static.meowrain.cn/i/2022/08/10/nyujve-3.png)