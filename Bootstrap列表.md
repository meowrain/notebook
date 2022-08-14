# Bootstrap列表

## 无样式的有序和无序列表

`list-unstyled`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <div class="container">
        <ul class="list-unstyled">
            <li>主页</li>

        <li>产品
            <ul>
<li>教程</li>
<li>工具</li>
            </ul>
        </li>
        <li>关于</li>
        <li>联系</li>
    </ul>
    </div>
</body>
</html>
```



## 内联放置有序和无序列表项

要使用有序或者无序列表创建水平菜单，需要将所有列表项放在一行中。

我们可以简单的通过将类`.list-inline` 添加到`<ul>`或者`<ol>`上，把类`.list-inline-item`添加到子`<li>`元素上

![image-20220812234318469](https://static.meowrain.cn/i/2022/08/12/12r2l8o-3.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <div class="container">
        <ul class="list-inline">
            <li class="list-inline-item">主页</li>
            <li class="list-inline-item">工具</li>
            <li class="list-inline-item">关于我们</li>
            <li class="list-inline-item">联系我们</li>
        </ul>
    </div>
</body>
</html>
```

## 创建水平定义列表

```html
<dl class="row">
    <dt class="col-sm-3">User Agent</dt>
    <dd class="col-sm-9">An HTML user agent is any device that interprets HTML documents.</dd>
    <dt class="col-sm-3 text-truncate">Client-side Scripting</dt>
    <dd class="col-sm-9">Client-side scripting generally refers to the category of computer programs on the web that are executed by the user's web browser.</dd>
    <dt class="col-sm-3">Document Tree</dt>
    <dd class="col-sm-9">The tree of elements encoded in the source document.</dd>
</dl>
```

![image-20220812235104897](https://static.meowrain.cn/i/2022/08/12/12vqzd6-3.png)