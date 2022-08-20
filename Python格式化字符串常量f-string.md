# Python格式化字符串常量f-string

直接举例子吧：

我们想打印出

`meowrain is 18 years old`

可以这么写

```python
name = 'meowrain '
age = 18
print(name + 'is ' + str(age) + ' years old')

```

> 在`meowrain`后添加一个空格，在`years old`前加一个空格
>
> ![image-20220816191315700](https://static.meowrain.cn/i/2022/08/17/55c4m0-3.png)

---



可是这样太麻烦了吧

接下来就要用到  **格式化字符串常量了**

```Python
name = 'meowrain'
age = 18
print(f'{name} is {age} years old')
# f可以是小写的，也可以是大写的
# print('{} is {} years old'.format(name, age))
# 上面的f相当于format
```

![image-20220816191448895](https://static.meowrain.cn/i/2022/08/17/56dcbh-3.png)

结果是相同的

>  参考：[[编程基础\] Python格式化字符串常量f-string总结_落痕的寒假的博客-CSDN博客_格式化字符串常量](https://blog.csdn.net/LuohenYJ/article/details/106817999)