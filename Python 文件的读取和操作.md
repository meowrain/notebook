# Python 文件的读取和操作

## 打开文件：

在python种，使用open函数，可以打开一个已经存在的文件，或者创建一个新文件，语法如下

``VariableName = open(name,mode,encoding)``

> **name:是要打开的目标文件名的字符串**
>
> **mode:设置打开文件的模式（访问模式）：只读，写入，追加**
>
> **encoding:编码格式（推荐UTF-8）**

示例代码：

```python
f = open('python.txt', 'r', encoding="UTF-8")
```

![image-20220820192310523](https://static.meowrain.cn/i/2022/08/21/5b8vwe-3.png)





## 读操作相关方法：

### read()方法

`文件对象.read(num)`

> num表示要从文件种读取的数据的长度，如果没有传入num，那么就表示读取文件中的所有数据

代码：

```python
thing = open('./python.txt', 'r', encoding="UTF-8")
print(thing.read()) #读取文件内容
```

python.txt内容：

```txt
My name is Meowrain
Hello World!
```

代码在控制台的输出内容为：

![image-20220820193006380](https://static.meowrain.cn/i/2022/08/21/5fe6ox-3.png)





### readlines()方法

读取文件的全部行，封装到列表中

```python
thing = open('./python.txt', 'r', encoding="UTF-8")
lines = thing.readlines()  # 读取文件的全部行，封装到列表中
print(type(lines))
print(lines)
```

![image-20220820193634482](https://static.meowrain.cn/i/2022/08/21/5j4uiu-3.png)



### readline()方法

一次读取一行内容

执行一次读一行

```python
thing = open('./python.txt', 'r', encoding="UTF-8")
lines = thing.readline()
print(type(lines))
print(lines)
```

![image-20220820193800018](https://static.meowrain.cn/i/2022/08/21/5k4chs-3.png)





```python
thing = open('./python.txt', 'r', encoding="UTF-8")
lines = thing.readline()
lines_2 = thing.readline()
print(lines, lines_2)
```

![image-20220820193913578](https://static.meowrain.cn/i/2022/08/21/5ksi85-3.png)



通过for循环方法来读取文件的所有行

```python
thing = open('./python.txt', 'r', encoding="UTF-8")
for line in thing:
    print(f'每一行的数据是：{line}')

```

![image-20220820194259765](https://static.meowrain.cn/i/2022/08/21/5n39ce-3.png)





## 关闭文件：

### close()关闭文件对象

```python
thing = open('./python.txt', 'r', encoding="UTF-8")
for line in thing:
    print(f'每一行的数据是：{line}')
thing.close()
```

通过调用close，关闭文件对象，也就是关闭对文件的占用

如果不调用close，同时程冠希没有停止运行，那么这个文件将一直被python程序占用





## with open语法

> 通过with open方法。可以在操作完成后自动关机close文件，解除python对文件的占用

语法：`with open(name,mode,encoding) as VariableName`

```python
with open('./python.txt', 'r', encoding="UTF-8") as thing:
    for line in thing:
        print(f'每一行的数据是：{line}')
```

![image-20220820195326619](https://static.meowrain.cn/i/2022/08/21/5t7e7c-3.png)





----

# 操作汇总

![image-20220820195657373](https://static.meowrain.cn/i/2022/08/21/5vewk1-3.png)





# 练习：单词计数

查看apple这个单词在python.txt中的出现次数

python.txt

```txt
name apple banana
watermelon green red apple
```



代码：

```Python
with open('./python.txt', 'r', encoding='UTF-8') as thing:  # 打开文件，在执行完成后关闭文件
    num = thing.read()  # 读取文件内全部文字
    count = num.count("apple")  # 打印apple在python.txt中重复次数
    print(f'\'apple\'这个单词在 python.txt中的出现次数为{count}')
```

![image-20220820212906860](https://static.meowrain.cn/i/2022/08/21/8pvdgi-3.png)







第二种方法：

python.txt 

```
name apple banana red
good nice cat dog
map jog run wise wisedom green red
red red google microsoft micraft apple
```



代码：

```python
with open('./python.txt', 'r', encoding='UTF-8') as thing:  # 打开文件，在执行完成后关闭文件
    count = 0  # 使用count 变量来累计red的出现次数
    for line in thing:
        line = line.strip()  # 去除开头和结尾的空格和换行符,不去除的话结果会因为\n这个换行符而不正确
        words = line.split(" ")  # 以空格为分隔符，并转换为列表形式，方便我们接下来的遍历列表
        for word in words:
            if word == "red":
                count += 1
    print(f'\'red\'这个单词在python.txt文本文档中出现的次数为：{count}')

```

![image-20220820215130697](https://static.meowrain.cn/i/2022/08/21/93422d-3.png)



