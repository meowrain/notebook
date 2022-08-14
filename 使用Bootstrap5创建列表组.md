# 使用Bootstrap5创建列表组

## 创建列表组

> 列表组用于以漂亮的方式显示元素列表，在最基本的形式中，列表组只是一个带有`.list-group`类的无序列表，且列表中的元素都带有`.list-group-item`类
>
> 

![image-20220813173833342](https://static.meowrain.cn/i/2022/08/13/sqy5a8-3.png)

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
<style>

</style>
</head>
<body>
<div class="container mt-3">
    <ul class="list-group w-25">
    <li class="list-group-item">二次元美图</li>
    <li class="list-group-item">手办</li>
    <li class="list-group-item">二次元网站</li>
    <li class="list-group-item">番剧</li>
</ul>
</div>
</body>
</html>
```

## 设置禁用和活动项

我们可以简单地将类 `.active` 添加到 `.list-group-item` 类的后面用来指示当前项目元素是活动的。 同样，可以将 `.disabled` 添加到 `.list-group-item` 后面，从而使其看起来是禁用状态。

![image-20220813173922879](https://static.meowrain.cn/i/2022/08/13/srhbvt-3.png)

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
<style>

</style>
</head>
<body>
<div class="container mt-3">
    <ul class="list-group w-25">
    <li class="list-group-item active">二次元美图</li>
    <li class="list-group-item">手办</li>
    <li class="list-group-item">二次元网站</li>
    <li class="list-group-item disabled">番剧</li>
</ul>
</div>
</body>
</html>
```

> 对于带有链接的列表组，链接仍然是可点击的。 要真正禁用链接，您需要使用 JavaScript 或手动删除 a 标签的 href 属性。

## Edge-to-Edge 列表组

我们可以选择将 `.list-group-flush` 类添加到 list-group 元素上，用以移除外边框和圆角，从而创建与其父容器边对边的列表组。

![image-20220813174117543](https://static.meowrain.cn/i/2022/08/13/ssn7u7-3.png)

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
<style>

</style>
</head>
<body>
<div class="container mt-3">
    <ul class="list-group w-25 list-group-flush">
    <li class="list-group-item active">二次元美图</li>
    <li class="list-group-item">手办</li>
    <li class="list-group-item">二次元网站</li>
    <li class="list-group-item disabled">番剧</li>
</ul>
</div>
</body>
</html>
```



## 创建编号列表组

![image-20220813174229062](https://static.meowrain.cn/i/2022/08/13/stayf2-3.png)





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
<style>

</style>
</head>
<body>
<div class="container mt-3">
    <ol class="list-group w-25 list-group-numbered">
    <li class="list-group-item active">二次元美图</li>
    <li class="list-group-item">手办</li>
    <li class="list-group-item">二次元网站</li>
    <li class="list-group-item disabled">番剧</li>
</ol>
</div>
</body>
</html>
```



## 带有复选框和单选框的列表组

![image-20220813180419566](https://static.meowrain.cn/i/2022/08/13/tu5y56-3.png)

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
<style>

</style>
</head>
<body>
    <div class="list-group w-50">
        <label class="list-group-item">
            <input type="checkbox" class="form-check-input me-1" name="hobbies"> 音乐
        </label>
        <label class="list-group-item">
            <input type="checkbox" class="form-check-input me-1" name="hobbies"> 旅行
        </label>
        <label class="list-group-item">
            <input type="checkbox" class="form-check-input me-1" name="hobbies"> 阅读
        </label>
    </div>
</body>
</html>
```

![image-20220813180529398](https://static.meowrain.cn/i/2022/08/13/tuthx0-3.png)

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
<style>

</style>
</head>
<body>
    <div class="m-4">
        <div class="list-group w-50">
            <label class="list-group-item">
                <input type="radio" class="form-check-input me-1" name="gender"> Male
            </label>
            <label class="list-group-item">
                <input type="radio" class="form-check-input me-1" name="gender"> Female
            </label>
        </div>
    </div>
</body>
</html>
```

## 创建带有链接项目的列表组

![image-20220813180804591](https://static.meowrain.cn/i/2022/08/13/twgikg-3.png)

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
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.5.0/font/bootstrap-icons.css">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>
<style>

</style>
</head>
<body>
    <div class="m-4">
        <div class="list-group w-50">
            <a href="#" class="list-group-item list-group-item-action active">
                <i class="bi-house-fill"></i> 主页
            </a>
            <a href="#" class="list-group-item list-group-item-action">
                <i class="bi-camera-fill"></i> 图片
                <span class="badge rounded-pill bg-primary float-end">145</span>
            </a>
            <a href="#" class="list-group-item list-group-item-action">
                <i class="bi-music-note-beamed"></i> 音乐
                <span class="badge rounded-pill bg-primary float-end">50</span>
            </a>
            <a href="#" class="list-group-item list-group-item-action">
                <i class="bi-film"></i> 视频
                <span class="badge rounded-pill bg-primary float-end">8</span>
            </a>
        </div>
    </div>
</body>
</html>
```

