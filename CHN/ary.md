### ary

创建一个可以接收n个参数的函数, 忽略其他额外的参数。

调用提供的函数`fn`,参数最多为n个, 使用 `Array.prototype.slice(0,n)` 和展开操作符 (`...`)。

```js
const ary = (fn, n) => (...args) => fn(...args.slice(0, n));
```

<details>
<summary>示例</summary>

```js
const firstTwoMax = ary(Math.max, 2);
[[2, 6, 'a'], [8, 4, 6], [10]].map(x => firstTwoMax(...x)); // [6, 8, 10]
```