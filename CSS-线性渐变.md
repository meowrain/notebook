# CSS-线性渐变

HTML 元素的背景色并不局限于单色。 CSS 还为我们提供了颜色渐变。 可通过 `background` 里的 `linear-gradient()` 实现线性渐变， 以下是它的语法：

```css
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);
```

第一个参数指定了颜色过渡的方向——它的值是角度，`90deg` 表示垂直渐变（从左到右），`45deg` 表示沿对角线渐变（从左下方到右上方）。 其他参数指定了渐变颜色的顺序：

例如



```css
background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
```







案例：使用 `linear-gradient()` 给 `div` 元素添加 `background` 渐变色，渐变角度为 35 度，从 `#CCFFFF` 过渡到 `#FFCCCC`。

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;
    background: linear-gradient(35deg,#CCFFFF,#FFCCCC);
  }

</style>

<div></div>
```

![image-20220811101201626](https://static.meowrain.cn/i/2022/08/11/gqizuh-3.png)