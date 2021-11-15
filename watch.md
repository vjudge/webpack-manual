# watch

⽂件监听是在发现源码发⽣变化时，⾃动重新构建出新的输出⽂件


### 监听原理
轮询判断⽂件的最后编辑时间是否变化

某个⽂件发⽣了变化，并不会⽴刻告诉监听者，⽽是先缓存起来，等 aggregateTimeout


### 开启监听模式
* 启动 webpack 命令时，带上 --watch 参数
* 在配置 webpack.config.js 中设置 watch: true


### 代码示例
```js
module.export = {
    //默认 false，也就是不开启
    watch: true,
    //只有开启监听模式时，watchOptions才有意义
    wathcOptions: {
        //默认为空，不监听的文件或者文件夹，支持正则匹配
        ignored: /node_modules/,
        //监听到变化发生后会等300ms再去执行，默认300ms
        aggregateTimeout: 300,
        //判断文件是否发生变化是通过不停询问系统指定文件有没有变化实现的，默认每秒问1000次
        poll: 1000
    } 
}
```