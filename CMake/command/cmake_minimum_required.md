[TOC]

# cmake_minimum_required

指定cmake的最小版本。

```cmake
cmake_minimum_required(VERSION <major>[.<minor>[.<patch>[.<tweak>]]] [FATAL_ERROR])
```

如果执行的cmake的版本小于此处指定的最小版本，那么cmake将停止执行，并报告错误。

> 此命令需在顶层CMakeLists.txt文件里调用，最好在CMakeLists.txt文件的最开头调用。
>
> 在2.6以前版本的cmake中，需要指定参数**FATAL_ERROR**来让cmake直接报错误，而不是报警告。但是在2.6版本及以后的cmake中，不需要特意指定该选项。

## 示例

```cmake
# 指定cmake的最小版本为3.8
cmake_minimum_required(VERSION 3.8)
```

