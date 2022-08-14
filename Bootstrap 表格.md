# Bootstrap 表格

## 使用Bootstrap创建一个简单的表格

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
    <div class="container-xl bg-light text-dark border">
<table class="table">
    <thead>
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

![image-20220812212029013](https://static.meowrain.cn/i/2022/08/12/z2ddi2-3.png)



## 创建带背景颜色的表格

Bootstrap5 可以提供类如 `.table-primary`，`.table-secondary`，`.table-success`，`.table-danger`，`.table-warning`，`.table-info`，`.table-light`和`.table-dark`等对表格的背景添加颜色，也可以对表中的行或单单元格进行颜色的添加。

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
    <div class="container-xl bg-light text-dark border">
<table class="table table-dark">
    <thead>
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

### table-dark

![image-20220812212206734](https://static.meowrain.cn/i/2022/08/12/z3fb4j-3.png)

### table-danger

![image-20220812212253801](https://static.meowrain.cn/i/2022/08/12/z3pclv-3.png)

### table-info

![image-20220812212313533](https://static.meowrain.cn/i/2022/08/12/z423zg-3.png)

### table-primary

![image-20220812212342916](https://static.meowrain.cn/i/2022/08/12/z48vpj-3.png)

### table-secondary

### ![image-20220812212408705](https://static.meowrain.cn/i/2022/08/12/z4mgun-3.png)

### table-warning

![image-20220812212436013](https://static.meowrain.cn/i/2022/08/12/z4skbk-3.png)

### table-success

![image-20220812212509942](https://static.meowrain.cn/i/2022/08/12/z587qf-3.png)

### table-light

![image-20220812212612005](https://static.meowrain.cn/i/2022/08/12/z5ub74-3.png)



---

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
    <div class="container-xl bg-light text-dark border">
<table class="table table-light">
    <thead class="table-success">
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr class="table-info">
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr class="table-danger">
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr class="table-dark">
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr class="table-warning">
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

![image-20220812212813229](https://static.meowrain.cn/i/2022/08/12/z71d2l-3.png)



## 创建带条纹行的表

我们还可以通过简单地向 `.table` 基类添加一个额外的类 `.table-striped` 来向 `<tbody>` 中的行添加斑马条纹，如下所示：

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
    <div class="container-xl bg-light text-dark border">
<table class="table table-striped">
    <thead>
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

![image-20220812213115712](https://static.meowrain.cn/i/2022/08/12/z8u37l-3.png)





## 带有边框的表格

通过将类 `.table-bordered` 添加到 `.table` 基类创建的表格上，就可以在表格和单元格的所有边上添加边框，如以下示例所示：



![image-20220812213422788](https://static.meowrain.cn/i/2022/08/12/zanrrb-3.png)

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
    <div class="container-xl bg-light text-dark border">
<table class="table table-striped table-bordered">
    <thead>
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

## 无边框表格

`.table-borderless` 类可以设置一个无边框的表格：

![image-20220812213542172](https://static.meowrain.cn/i/2022/08/12/zbdhl3-3.png)

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
    <div class="container-xl bg-light text-dark border">
<table class="table table-striped table-borderless">
    <thead>
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```









## 在表格行上启用悬停状态

联合使用 `.table-dark` 和 `.table-hover` 类可以设置黑色背景表格的鼠标悬停效果：

![动画](https://static.meowrain.cn/i/2022/08/12/zd7ide-3.gif)

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
    <div class="container-xl">
<table class="table table-striped table-borderless table-hover">
    <thead>
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

## 设置表头颜色

我们也可以设置表头的颜色，例如` .table-dark` 类用于给表头添加黑色背景， `.table-light`类用于给表头添加灰色背景:

把这个属性加在`<thead>`标签中

![image-20220812214201989](https://static.meowrain.cn/i/2022/08/12/zfaz7r-3.png)

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
    <div class="container-xl">
<table class="table table-striped table-borderless table-hover table-warning">
    <thead class="table-dark">
        <th>#</th>
        <th>Name</th>
        <th>Price</th>
        <th>Categories</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Bananas</td>
            <td>$10</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Apple</td>
            <td>$5</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Orange</td>
            <td>$6</td>
            <td>Fruits</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Pork</td>
            <td>$20</td>
            <td>Meat</td>
        </tr>
    </tbody>
</table>
    </div>
</body>
</html>
```

## 使用 Bootstrap 创建响应式表

`.table-responsive` 类用于创建响应式表格：在屏幕宽度小于 992px 时会创建水平滚动条，如果可视区域宽度大于 992px 则显示不同效果（没有滚动条）:

<img src="https://static.meowrain.cn/i/2022/08/12/zifwg7-3.gif" alt="动画1" style="zoom:80%;" />



```html
<!DOCTYPE html>
<html lang="zh">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Bootstrap5 响应式表格 - 迹忆客(jiyik.com)</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>
<style>
    /* Custom style to make this example easy to understand */
    table * {
        white-space: nowrap;
    }
</style>
</head>
<body>
<div class="m-4">
    <div class="table-responsive"> 
        <table class="table">
            <thead>
                <tr>
                    <th>#</th>
                    <th>First Name</th>
                    <th>Last Name</th>
                    <th>Email</th>
                    <th>Biography</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>Clark</td>
                    <td>Kent</td>
                    <td>clarkkent@mail.com</td>
                    <td>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>John</td>
                    <td>Carter</td>
                    <td>johncarter@mail.com</td>
                    <td>Vestibulum consectetur scelerisque bibendum scelerisque purus.</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>Peter</td>
                    <td>Parker</td>
                    <td>peterparker@mail.com</td>
                    <td>Integer pulvinar leo id risus interdum vel metus dignissim.</td>
                </tr>
            </tbody>
        </table>
    </div> 
    <p class="mt-4"><strong>Note:</strong> Change the editor layout/orientation to see how responsive table works.</p>
</div>
</body>
</html>
```

