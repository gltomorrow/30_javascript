### arrayToCSV

将2D数组转换为逗号分隔值(CSV)字符串。

使用 `Array.prototype.map()` 和 `Array.prototype.join(delimiter)` 将一个一维数组转换为字符串。

使用 `Array.prototype.join('\n')` 将所有行合并成CSV字符串, 用换行符分割每一行。

如果没有第二哥参数, `delimiter`会使用一个默认分隔符 `,`.

```js
const arrayToCSV = (arr, delimiter = ',') =>
  arr.map(v => v.map(x => `"${x}"`).join(delimiter)).join('\n');
```
