### allEqual

检查是否数组中所有的元素都是相等的。

使用 `Array.prototype.every()` 来检测是否数组中的所有元素都和第一个元素相等。

```js
const allEqual = arr => arr.every(val => val === arr[0]);
```

<details>
<summary>示例</summary>

```js
allEqual([1, 2, 3, 4, 5, 6]); // false
allEqual([1, 1, 1, 1]); // true
```
