# ES6 Set数据结构

[Set - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Set)

## 基本语法

ES6提供了新的数据结构set，它类似于数组，但是成员的值都是唯一的，没有重复的值。

Set本身是一个个构造函数，用来生成Set数据结构



## 创建Set 对象

```js
const set1 = new Set();
```

## 初始化set对象

```js
let s = new Set([1,2,3,4,5,6]);
```

## 输出set对象内容&获取Set对象的条目数

```js
let s = new Set([1,2,3,4,5,6]);
console.log([...s]); //输出s内容
console.log(s.size); //size的值是一个整数，表示Set对象有多少条目
```

> 注意：使用`Set.prototype.size()`重复的不会算在条目里
>
> ```js
> var items = new Set([1, 2, 3, 4, 5, 5, 5, 5]);
> console.log(items.size); //重复的不会算在条目里，5
> console.log(...items);
> ```
>
> 



## 向Set对象中输入内容`.add()`

[Set.prototype.add() - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Set/add)

`Set.prototype.add()`

**`add()`** 方法用来向一个 `Set` 对象的末尾添加一个指定的值。

```js
mySet.add(value);
```

```js
const set1 = new Set();

set1.add(42);
set1.add(42);
set1.add(13);

for (const item of set1) {
  console.log(item);
  // expected output: 42
  // expected output: 13
}

```

## 从一个Set对象中删除指定的元素

`Set.prototype.delete()`

**`delete()`** 方法可以从一个 `Set` 对象中删除指定的元素。

语法：

```js
mySet.delete(value); //value为将要删除的元素
```



案例：

```js
let gg = new Set([1,2,3,4,5,"meowrain"]);
console.log(...gg); //1,2,3,4,5,"meowrain"
console.log(gg.delete("meowrain")); //删除成功返回true
console.log(gg.has("meowrain")); //查看是否还存在meowrain这个字符串，因为前面已经删除，所以返回false
console.log(...gg); //1,2,3,4,5
console.log(gg.delete(6)); //不存在，删除失败，返回FALSE
```



## 从Set对象中删除所有的成员clear()

```js
let gg = new Set([1,2,3,4,5,"meowrain"]);
gg.clear();
console.log(gg.has(1));  //false
```

如上