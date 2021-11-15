# Entry

指定 webpack 的打包入口


### 单入口
```js
// 值是一个字符串
module.exports = {
    entry: './src/app.js'
};
```

### 多入口
```js
// 值是一个对象
module.exports = {
    entry: {
        app: './src/app.js',
        adminApp: './src/adminApp.js'
    }
};
```