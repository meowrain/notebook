# Bootstrap5 按钮组组件

要创建按钮组，只需将一系列带有 `.btn` 类的按钮放在 <div> 元素中，并在其上面添加额外的 `.btn-group` 类

![image-20220813194219419](https://static.meowrain.cn/i/2022/08/13/w4bikb-3.png)

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
    <div class="container">
        <div class="btn-group">
            <button type="button" class="btn btn-primary">主页</button>
            <button type="button" class="btn btn-primary">服务</button>
            <button type="button" class="btn btn-primary">关于我们</button>
        </div>
    </div>
</body>
</html>
```



还可以做成下面这种效果

![动画2](https://static.meowrain.cn/i/2022/08/13/w5kbjg-3.gif)

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
    <div class="container mt-3">
        <div class="btn-group">
            <button type="button" class="btn btn-outline-primary">主页</button>
            <button type="button" class="btn btn-outline-primary">服务</button>
            <button type="button" class="btn btn-outline-primary">关于我们</button>
        </div>
    </div>
</body>
</html>
```

## 混合样式按钮组

![image-20220813194732038](https://static.meowrain.cn/i/2022/08/13/w7dkgu-3.png)

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
    <div class="container mt-3">
        <div class="row">
            <div class="btn-group">
                <button type="button" class="btn btn-outline-primary">主页</button>
                <button type="button" class="btn btn-outline-primary">服务</button>
                <button type="button" class="btn btn-outline-primary">关于我们</button>
            </div>
        </div>
        <div class="btn-group mt-3">
            <button type="button" class="btn btn-success">
                <i class="bi-eye"></i> View
            </button>
            <button type="button" class="btn btn-warning">
                <i class="bi-pencil"></i> Edit
            </button>
            <button type="button" class="btn btn-danger">
                <i class="bi-trash"></i> Delete
            </button>
        </div>
    </div>
</body>

</html>
```

## 按钮组高度调整

通过在`.btn-group`后添加`.btn-group-lg` `.btn-group-md` `.btn-group-sm`来调整工按钮组高度

![image-20220813195623021](https://static.meowrain.cn/i/2022/08/13/wcoftb-3.png)

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
<div class="container mt-3">
    <div class="btn-group btn-group-lg mb-2">
        <button type="button" class="btn btn-primary">主页</button>
        <button type="button" class="btn btn-primary">服务</button>
        <button type="button" class="btn btn-primary">关于</button>
    </div>
    <br>
    <!-- Medum button group-->

    <div class="btn-group btn-group-md mb-2">
        <button type="button" class="btn btn-primary">主页</button>
        <button type="button" class="btn btn-primary">服务</button>
        <button type="button" class="btn btn-primary">关于</button>
    </div>
    <br>
    <!-- Small button group -->
    <div class="btn-group btn-group-sm">
        <button type="button" class="btn btn-primary">主页</button>
        <button type="button" class="btn btn-primary">服务</button>
        <button type="button" class="btn btn-primary">关于</button>
    </div>
</div>
</body>

</html>
```



## 嵌套按钮组

![动画3](https://static.meowrain.cn/i/2022/08/13/x8fetn-3.gif)

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
<div class="container mt-3">
  <div class="btn-group">
      <a href="" class="btn btn-warning">主页</a>
      <a href="" class="btn btn-warning">归档</a>
      <div class="btn-group">
          <a href="#" class="btn btn-warning dropdown-toggle" data-bs-toggle="dropdown">友链</a>
          <div class="dropdown-menu">
              <a class="dropdown-item" href="#">baidu</a>
              <a class="dropdown-item" href="#">google</a>
          </div>
      </div>
  </div>
</div>
</body>

</html>
```

## 垂直堆叠的按钮组

把`.btn-group`改成`.btn-group-vertical`

![image-20220813201316060](https://static.meowrain.cn/i/2022/08/13/xaknzz-3.png)

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
<div class="container mt-3">
  <div class="btn-group-vertical">
      <a href="" class="btn btn-warning">主页</a>
      <a href="" class="btn btn-warning">归档</a>
      <div class="btn-group">
          <a href="#" class="btn btn-warning dropdown-toggle" data-bs-toggle="dropdown">友链</a>
          <div class="dropdown-menu">
              <a class="dropdown-item" href="#">baidu</a>
              <a class="dropdown-item" href="#">google</a>
          </div>
      </div>
  </div>
</div>
</body>

</html>
```

## 创建两端对齐的按钮组

![image-20220813201503246](https://static.meowrain.cn/i/2022/08/13/xbos2h-3.png)

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
<div class="container mt-3">
  <div class="btn-group-vertical d-flex">
      <a href="" class="btn btn-warning">主页</a>
      <a href="" class="btn btn-warning">归档</a>
      <div class="btn-group">
          <a href="#" class="btn btn-warning dropdown-toggle" data-bs-toggle="dropdown">友链</a>
          <div class="dropdown-menu">
              <a class="dropdown-item" href="#">baidu</a>
              <a class="dropdown-item" href="#">google</a>
          </div>
      </div>
  </div>
</div>
</body>

</html>
```

