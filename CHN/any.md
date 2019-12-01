### any

如果被提供的断言函数接收数组中任意一个元素作为参数都返回`true`，则返回`true`，否则返回`false`。

使用 `Array.prototype.every()`来测试是否第二个参数`fn`以集合中任意一个元素作为参数都返回`true`，使用`Boolean`作为默认值。

```js
const any = (arr, fn = Boolean) => arr.some(fn);
```
