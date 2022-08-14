## for-in语句

```javascript
let lessons = [
    {title: '媒体查询响应式布局',category: 'css'},
    {title: 'FLEX 弹性盒模型',category: 'css'},
    {title: 'MYSQL多表查询随意操作',category: 'mysql'}
];

for (const num in lessons) {
    console.log(`标题: ${lessons[num].title}`);
}
```



![image-20220803222159703](https://static.meowrain.cn/i/2022/08/03/10qofym-3.png)





---

## for-of语句

与 `for/in` 不同的是 `for/of` 每次循环取其中的值而不是索引。

