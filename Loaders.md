# Loaders

Webpack 开箱即用只支持 JS 和 JSON 两种文件类型。
通过 Loaders 支持其他文件类型并且把它们转化成有效的模块，并且可以添加到依赖图中

本身是一个函数，接受源文件作为参数，返回转换的结果

### 常见的 Loaders
* babel-loader : 转换 ES6、ES7 等 JS 新特性语法
* css-loader : 支持 .css 文件的加载和解析
* less-loader : 将 less 文件转换成 css
* ts-loader : 将 TS 转换成 JS
* file-loader : 进行图片、字体等的打包
* raw-loader : 将文件以字符串形式导入
* thread-loader : 多进程打包 JS 和 CSS


### 代码示例
```js
module.exports = {
    module: {
        rules: [
            // test: 制定匹配规则
            // use: 指定使用的 loader 名称
            { test: /\.txt$/, use: 'raw-loader' },
            // 解析 ES6，babel的配置⽂件是：.babelrc
            { test: /\.js$/, use: 'babel-loader' }

        ]
    }
};
```




















