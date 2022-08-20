# Python 匿名函数

## Python作为参数传递

案例：

> 函数**compute**，作为参数，传入了**test_func函数**中使用

```python
def test_func(compute):
    result = compute(1, 2)
    print(result)


def compute(x, y):
    return x + y


test_func(compute)
```

![image-20220819233541319](https://static.meowrain.cn/i/2022/08/20/c4qfbg-3.png)



## 匿名函数lambda

函数的定义中，

def关键字，可以定义带有名称的函数

lambda关键字，可以定义匿名函数

有名称的函数，可以基于名称重复使用

无名称的匿名函数，只可临时使用一次



匿名函数定义语法：

`lambda 传入参数: 函数体()`

- lambda是关键字，表示定义匿名函数
- 传入参数表示匿名函数的形式参数，如x,y表示接收2个形式的参数
- 函数体，就是函数的执行逻辑，要注意：只能写一行，无法写多行



```Python
def test_func2(a):
    result = a(1, 2)
    print(result)


test_func2(lambda x, y: x + y)
```

![image-20220819233541319](https://static.meowrain.cn/i/2022/08/20/c4qfbg-3.png)

> lambda关键字定义的函数是匿名的，无法二次使用