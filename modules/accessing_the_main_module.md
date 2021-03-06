
<!-- type=misc -->

当 Node.js 直接运行一个文件时，`require.main` 会被设为它的 `module`。
这意味着你可以通过如下检测直接确定一个文件是否已运行：

```js
require.main === module
```

对于 `foo.js` 文件，如果通过 `node foo.js` 运行则为 `true`，但如果通过 `require('./foo')` 运行则为 `false`。

因为 `module` 提供了一个 `filename` 属性（通常等同于 `__filename`），所以可以通过检查 `require.main.filename` 来获取当前应用程序的入口点。

