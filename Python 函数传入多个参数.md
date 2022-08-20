# Python 函数传入多个参数

## *形参，以元组形式传参（元组）

直接在传参处填写 `*形参`就行了

```python
def save_information(*info):
    print(info)
save_information("good", 1, 2, True)
```

> 运行结果：![image-20220817231811697](https://static.meowrain.cn/i/2022/08/18/buftwi-3.png)

---



如下，我们写一个计算乘法的函数

```Python
def multiply(*numbers):
    total = 1
    for i in numbers:
        total *= i
    return total


print(multiply(1, 2, 3, 4))
```



## **形参，以集合方式传参（字典）

如果填写`**形参`呢

```Python
def save_user(**user):
    print(user)


save_user(id=1, name="meowrain", age=18, money=100)
```

> 运行结果![image-20220817231610494](https://static.meowrain.cn/i/2022/08/18/bt8q00-3.png)

从运行结果来看，是个`字典`

> 关于字典https://www.w3school.com.cn/python/python_dictionaries.asp









# 补充：Python数据类型

Python 编程语言中有四种集合数据类型：

- *列表（List）*是一种有序和可更改的集合。允许重复的成员。
- *元组（Tuple）*是一种有序且不可更改的集合。允许重复的成员。
- *集合（Set）*是一个无序和无索引的集合。没有重复的成员。
- *词典（Dictionary）*是一个无序，可变和有索引的集合。没有重复的成员。