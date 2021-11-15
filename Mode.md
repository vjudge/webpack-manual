# Mode

⽤来指定当前的构建环境是：production、development 还是 none

设置 mode 可以使⽤ webpack 内置的函数，默认值为 production


### 函数功能
* production : 设置 process.ENV.NODE_ENV 的值为 production。开启 FlagDependencyUsagePlugin，FlagIncludedChunksPlugin，ModuleConcatenationPlug，NoEmitOnErrorsPlugin，OccurrenceOrderPlugin， SideEffectsFlagPlugin 和 TerserPlugin
* development : 设置 process.ENV.NODE_ENV 的值为 development。开启 NamedChunksPlugin 和 NamedModulesPlugin
* none : 不开启任何优化选项





