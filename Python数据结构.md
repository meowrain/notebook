# Python数据结构

# list(列表)

### 创建两个列表List

```python

name = ["meowrain","mike","John"]
matrix = [[0,1],[2,3]]
```



### 访问列表中的值

```python
name = ["a","b","c"]
matrix = [[0,1],[2,3]]
print(name[0])
print(matrix[0])
print(matrix[0][0])
```

> ![image-20220818110508625](https://static.meowrain.cn/i/2022/08/18/vh7lmb-3.png)



### 将列表中的值反过来显示

第一种方法：

```python
num = [1,2,3,4,5,6,7,8,9]
print(num[::-1])
```

![image-20220818113130075](https://static.meowrain.cn/i/2022/08/18/vwqkeb-3.png)

第二种方法：

```python
num = [1, 2, 3, 4, 5, 6, 7, 8, 9]
num.sort(reverse=True)
print(num)

```

![image-20220818123225185](https://static.meowrain.cn/i/2022/08/18/xku8rh-3.png)

### 把列表中乱七八糟的数字，按照从小到大或者从大到小的顺序排序

`sorted(listname)`

案例：把num列表中的数字，按照从小到大的顺序排序

```python
num = [9,54,129,44,66,33,78,999]
print(sorted(num))

```

![image-20220818123722176](https://static.meowrain.cn/i/2022/08/18/xnst7q-3.png)



案例： 把num列表中的数字，按照从大到小的顺序排序

```python
num = [9,54,129,44,66,33,78,999]
print(sorted(num,reverse=True))

```

![image-20220818123907812](https://static.meowrain.cn/i/2022/08/18/xowjc3-3.png)

### 合并两个列表

```python
name = ["a","b","c"]
name_2 = ["d","e","f","g"]
combined = name + name_2
print(combined)
```



### 使用list函数，创建list（包括0到20的数字）

```python
num = list(range(0,21)) #创建列表 包括数字 0 到 20
print(num)
```

![image-20220818111104704](https://static.meowrain.cn/i/2022/08/18/vkojav-3.png)



### 使用list函数，把字符串的每一个字母添加到list中

```python
characters = list("meowrain")
print(characters)

```

![image-20220818111235468](https://static.meowrain.cn/i/2022/08/18/vlgmdk-3.png)



### 使用for循环，遍历list下的元素

```python
num = [1,2,3,4,5,6,7,8,9]
for i in num:
    print(i)
```

![image-20220818114020961](https://static.meowrain.cn/i/2022/08/18/w21fxu-3.png)



### python enumerate()函数

>  enumerate() 函数用于将一个可遍历的数据对象(如列表、元组或字符串)组合为一个索引序列，同时列出数据和数据下标，一般用在 for 循环当中。

以上来自菜鸟教程

```python
name = ["java","javascript","mysql","python"]
for uname in enumerate(name):
    print(uname)

```

![image-20220818114258950](https://static.meowrain.cn/i/2022/08/18/w3p3yh-3.png)



### 在列表中添加项和删除项

#### 添加项：

1. 在列表末尾添加`list.append(object)`

2. 在列表开头添加`list.insert(index, object)`

   > 当然，用这个也可以改变index为1或者其它数字对应的元素

案例1，在name列表末尾添加`c#

```python
name = ["java","javascript","mysql","python"]
name.append("c#")
print(name)
```

![image-20220818115349635](https://static.meowrain.cn/i/2022/08/18/wa6ytk-3.png)

案例2：在name列表头添加`c#`

```python
name = ["java","javascript","mysql","python"]
name.insert(0, "c#")
print(name)
```

![image-20220818115601799](https://static.meowrain.cn/i/2022/08/18/wbga1j-3.png)





#### 删除列表中的元素 `list.pop(index)`，`list.remove(value)`,`del list[number:number]`,`list.clear()`

案例1： 删除列表中的第一个元素

```python
name = ["java","javascript","mysql","python"]
name.pop(0)
print(name)
```

```python
name = ["java","javascript","mysql","python"]
name.remove("java")
print(name)
```

![image-20220818121826019](https://static.meowrain.cn/i/2022/08/18/xci9e0-3.png)





删除列表中的多个元素 `del list[number:number]`

案例2：删除列表中的第一个到第三个元素

```python
name = ["java", "javascript", "mysql", "python"]
del name[0:3]
print(name)

```

![image-20220818121808857](https://static.meowrain.cn/i/2022/08/18/xcepl7-3.png)



删除列表中的所有元素

```python
name = ["java", "javascript", "mysql", "python"]

name.clear()

print(name)
```

![image-20220818121927188](https://static.meowrain.cn/i/2022/08/18/xd42qg-3.png)





### 查看列表元素对应的索引 `list.index(value)`

案例1：查看python在name列表中的索引值为：

```python
name = ["java", "javascript", "mysql", "python"]
print(name.index("python"))

```

![image-20220818122738417](https://static.meowrain.cn/i/2022/08/18/xhxrex-3.png)

### `list.count(value)`查看元素在列表中的出现次数

案例：查看python在name列表中的出现次数

```python
name = ["java", "javascript", "mysql", "python","python"]
print(name.count("python"))

```

![image-20220818122725242](https://static.meowrain.cn/i/2022/08/18/xhuz4s-3.png)











## turple（元组）

如果想要传递的信息不被篡改，列表就不合适了

元组和列表一样，都可以封装多个，不同类型的元素在内

> 元组一旦定义完成，就不可修改

### 定义元组

```python
# 元组定义：定义使用圆括号，用逗号隔开数据
# 方式1
variable = ("element1","element2"...)
```

> ![image-20220819155021637](https://static.meowrain.cn/i/2022/08/19/12u54a3-3.png)
>
> 注意： 定义元组的时候，如果只有一个元素，要在后面添加一个逗号，否则它就不是元组类型了
>
> 比如：
>
> ```python
> example = ("good")
> print(type(example))
> 
> ```
>
> ![image-20220819155105546](https://static.meowrain.cn/i/2022/08/19/12un97r-3.png)
>
> 可以看到，如果不加逗号，就变成字符串类型了
>
> 那加上逗号呢？
>
> ```python
> example = ("good",)
> print(type(example))
> 
> ```
>
> ![image-20220819155151098](https://static.meowrain.cn/i/2022/08/19/12v5ljm-3.png)

### 定义空元组

第一种方法：

```python
n = ()
print(n)
```

第二种方法：

```python
n = tuple()
print(n)
```



### 元组下标取内容

直接参考下面的元组嵌套就行了，我觉得已经足够说明怎么取内容了

### 元组的嵌套

```Python
# 定义一个嵌套元组
thing = ((1, 2, 3), (2, 3, 4))
print(f'thing的类型是{type(thing)}，内容是{thing},\n 第一个元素的内容是{thing[0]}, 第一个元素也是元组，第一个元素中的第一个元素为：{thing[0][0]}')
```

![image-20220819160056797](https://static.meowrain.cn/i/2022/08/19/130jm7c-3.png)



### 元组的相关操作

![image-20220819160357470](https://static.meowrain.cn/i/2022/08/20/194ir-3.png)

```python
tu = ("nice", "good", "yyds", "nb", "good")
print(
    f'我们来看下nb这个字符串对应的下标吧：\n {tu.index("nb")} \n接下来我们来看一下count,来查一下good出现了多少次吧：\n {tu.count("good")}\n最后呢，我们来看一下这个元组的长度吧：\n {len(tu)}')

```

![image-20220819160753019](https://static.meowrain.cn/i/2022/08/20/3m32f-3.png)



###  元组的遍历

while遍历

```Python
tu = ("nice", "good", "yyds", "nb", "good")
i = 0
while i < len(tu):
    print(f'tu元组中的元素有： {tu[i]}')
    i += 1
```

for遍历

```Python
tu = ("nice", "good", "yyds", "nb", "good")
i = 0
for j in tu:
    print(f'tu元组中的元素有： {j}')
```

打印结果：

![image-20220819161413596](https://static.meowrain.cn/i/2022/08/20/7axoe-3.png)



> 元组的内容虽然不能修改，但是如果嵌套了一个list,那就是可以修改List里的内容的





## 集合set

### 定义集合

```python
n = {"done", "uu"}
print(type(n))
```

### 定义空集合

```python
n = set()
```

> 因为集合是无序的，所以集合不支持下标索引访问，但是集合是允许修改的

### 集合修改方法

添加新元素： add

```python
n = set()
n.add("python")
n.add("javascript")
print(f"添加元素后，n集合内容： {n}")
```

![image-20220819180309821](https://static.meowrain.cn/i/2022/08/20/3bt18w-3.png)



删除元素: 

```python
n = set()
n.add("python")
n.add("javascript")
print(f"添加元素后，n集合内容： {n}")
n.remove("python")
print(f"删除元素后，n集合内容： {n}")
```

![image-20220819180500487](https://static.meowrain.cn/i/2022/08/20/3cxz4u-3.png)



随机取一个元素：pop

```Python
n = {"python", "javascript", "java"}
print(f'随机取的元素为 {n.pop()}')
```

![image-20220819180749015](https://static.meowrain.cn/i/2022/08/20/3enwz8-3.png)

![image-20220819180810631](https://static.meowrain.cn/i/2022/08/20/3esbsp-3.png)



清空集合：clear

```Python
n = {"python", "javascript", "java"}
print(f'随机取的元素为 {n.pop()}')
n.clear()
print(f'清除所有元素以后，n集合内的元素为: {n}')
```

![image-20220819181052364](https://static.meowrain.cn/i/2022/08/20/3ggp8w-3.png)



### 取出2个集合的差集: difference

语法： 集合1.difference(集合2) 功能：取出集合1和集合2的差集，**集合1有而集合2没有的**

```Python
set1 = {1, 2, 3}
set2 = {1, 3, 4, 5, 6}
set3 = set1.difference(set2)  #  输出set1和set2的差集，为2
print(f"set1和set2的差集为： {set3}")
```

![image-20220819181600126](https://static.meowrain.cn/i/2022/08/20/3jhqck-3.png)



### 消除2个集合的差集：

语法： 集合1.difference_update(集合2) 

功能： 消除集合1中，集合1和集合2共同有的元素

```Python
set1 = {1, 2, 3}
set2 = {1, 5, 6}
set1.difference_update(set2)
print(f"消除差集后，set1的结果： {set1}")
print(f"消除差集后，set2的结果： {set2}")
```

![image-20220819182336643](https://static.meowrain.cn/i/2022/08/20/3nvc8r-3.png)



### 两个集合合并为一个

```python
set1 = {1, 2, 3}
set2 = {1, 5, 6}
set3 = set1.union(set2)
print(set3)
```

![image-20220819182817254](https://static.meowrain.cn/i/2022/08/20/3qql0u-3.png)



### 查看集合中的元素个数

```python
set1 = {1, 2, 3, 4, 5, 6, 7}
print(f"set1集合中的元素个数为{len(set1)}个")
```

![image-20220819183048012](https://static.meowrain.cn/i/2022/08/20/3sclhu-3.png)



### 集合的遍历

```python
set1 = {1, 2, 3, 4, 5, 6, 7}
for i in set1:
    print(f"集合的元素有： {i}")
```

![image-20220819185204037](https://static.meowrain.cn/i/2022/08/20/44y633-3.png)









## 字典

### 基础定义

> value可以为任何数据结构 

和集合一样，都用花括号，不过存储的元素是一个个的键值对

```python
my_dict = {"name": "meowrain", "age": 18, "earn": 7000}
print(my_dict)
```

### 定义空字典

```python
my_dict = {}
my_dict = dict()
```



### 字典数据的获取

字典和集合一样，不可以使用下标索引

但是字典可以通过key值获取对应的value值

语法：` dictname[key]  ---> 获取value值`

```python
my_dict = {"name": "meowrain", "age": 18, "earn": 7000}
print(f"获取键值name的值: {my_dict['name']}")
```



### 字典的嵌套

案例：**查学生成绩信息**

```python
stu_score_dict = {
    "李明": {
        "语文": 88,
        "数学": 150,
        "英语": 120
    },
    "张三": {
        "语文": 90,
        "数学": 100,
        "英语": 56,
    },
    "赵六": {
        "语文": 90,
        "数学": 139,
        "英语": 123,
    }
}
print(f'学生的考试信息：{stu_score_dict}')
# 看一下赵六的成绩信息
print(f'赵六的考试信息：{stu_score_dict["赵六"]}')
# 看一下张三的英语信息
print(f'张三的英语成绩：{stu_score_dict["张三"]["英语"]}')
```

![image-20220819193158042](https://static.meowrain.cn/i/2022/08/20/5gjkxz-3.png)

### 字典的常用操作

#### 新增元素：

语法：字典[key]  = value

```python
n = {}
n["name"] = "meowrain"
print(n)
```

![image-20220819193211537](https://static.meowrain.cn/i/2022/08/20/5gm8rb-3.png)



#### 更新元素

语法：

字典[key] = value

> 字典的key不可以重复，对已经存在的key执行上述操作，就是更新value值

```Python
n = {"name": "meowrain","age":19}
n["age"] = 18
print(n)
```

![image-20220819193401175](https://static.meowrain.cn/i/2022/08/20/5hr2js-3.png)



### 删除元素

语法：`.pop("key")`

```Python
dic = {"name":"meowrain","age":18}
age = dic.pop("age")
print(f'经过移除，现在dic字典的内容为{dic}，被移除元素age的值为：{age}')
```



### 清空字典

`dicname.clear()`

```Python
dic = {"name":"meowrain","age":18}
dic.clear()
print(f'字典被清空了，内容是： {dic}')
```



### 获取字典中全部的key

`dicname.keys()`

```Python
stu_score_dict = {
    "李明": {
        "语文": 88,
        "数学": 150,
        "英语": 120
    },
    "张三": {
        "语文": 90,
        "数学": 100,
        "英语": 56,
    },
    "赵六": {
        "语文": 90,
        "数学": 139,
        "英语": 123,
    }
}
print(stu_score_dict.keys())
```

![image-20220819194820261](https://static.meowrain.cn/i/2022/08/20/5q761n-3.png)



### 遍历字典

 通过获取到全部的key来完成遍历

```Python
# 通过获取到全部的key来完成遍历
keys = stu_score_dict.keys()
for key in keys:
    print(f'字典的key是：{key}')
    print(f'{key}的value是：{stu_score_dict[key]}')
```

![image-20220819195543772](https://static.meowrain.cn/i/2022/08/20/5ui52m-3.png)

直接对字典进行for循环

```Python
# 直接对字典进行for循环
for key in stu_score_dict:
    print(f'字典的key是：{key}')
    print(f'{key}的value是：{stu_score_dict[key]}')
```



### 统计字典内的元素数量

```python
stu_score_dict = {
    "李明": {
        "语文": 88,
        "数学": 150,
        "英语": 120
    },
    "张三": {
        "语文": 90,
        "数学": 100,
        "英语": 56,
    },
    "赵六": {
        "语文": 90,
        "数学": 139,
        "英语": 123,
    }
}
print(len(stu_score_dict))
```





---

