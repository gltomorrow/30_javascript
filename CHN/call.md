### call

给定一个key和一组参数，给定一个上下文时调用它们。主要用于合并。

使用闭包调用上下文中key对应的值，即带有存储参数的函数。

```js
const call = (key, ...args) => context => context[key](...args);
```

<details>
<summary>示例</summary>

```js
Promise.resolve([1, 2, 3])
  .then(call('map', x => 2 * x))
  .then(console.log); // [ 2, 4, 6 ]
const map = call.bind(null, 'map');
Promise.resolve([1, 2, 3])
  .then(map(x => 2 * x))
  .then(console.log); // [ 2, 4, 6 ]
```
