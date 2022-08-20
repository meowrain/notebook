# Python转义字符

如果像下面这样写的话，会直接被IDE红线报错

```python
course = "python "programming""
print(course)
```

![image-20220816185941061](https://static.meowrain.cn/i/2022/08/17/49c8k4-3.png)

那么我想打印出`python "programming"`这样的字符串怎么办呢？

这就要用到转义字符了

```python
course = "python \"programming\""
print(course)

```

![image-20220816190116076](https://static.meowrain.cn/i/2022/08/17/4adrji-3.png)

可以看到红线消失了，我们运行一下看看

![image-20220816190143267](https://static.meowrain.cn/i/2022/08/17/4ajnt7-3.png)