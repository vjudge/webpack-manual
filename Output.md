# Output

告诉 webpack 如何将编译后的文件输出到磁盘


### 单入口
```js
module.exports = {
    output: {
        filename: 'bundle.js',
        path: __dirname + '/dist'
    }
};
```

### 多入口
```js
module.exports = {
    output: {
        filename: '[name].js', // 通过占位符确保文件名唯一
        path: __dirname + '/dist'
    }
};
```