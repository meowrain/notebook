# Python的写操作

案例：

```Python
# 打开文件
f = open('./python.txt', 'w', encoding="UTF-8")
# 文件写入
f.write('hello world')
# 本质上并没有把内容写到python.txt中，而是存储在内存中，知道我们执行.flush()函数
# 内容刷新
f.flush()
```

![image-20220820215622105](https://static.meowrain.cn/i/2022/08/21/961f39-3.png)



