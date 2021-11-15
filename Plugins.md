# Plugins

插件⽤于 bundle ⽂件的优化，资源管理和环境变量注⼊

作⽤于整个构建过程


### 常见的 Plugins
* CommonsChunkPlugin : 将 chunks 相同的模块代码提取成公共 js
* CleanWebpackPlugin : 清理构建目录
* ExtractTextWebpackPlugin : 将 CSS 从 bundle 文件里提取成一个独立的 CSS 文件
* CopyWebpackPlugin : 将文件或者文件夹拷贝到构建的输出目录
* HtmlWebpackPlugin : 创建 html 文件去承载输出的bundle
* UglifyjsWebpackPlugin : 压缩 js
* ZipWebpackPlugin : 将打包出的资源生成一个 zip 包


### 代码示例
```js
module.exports = {
    plugins: [
        new HtmlWebpackPlugin({template: './src/index.html'})
    ]
};
```






