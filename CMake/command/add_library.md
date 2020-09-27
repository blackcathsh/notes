[TOC]

# add_library

使用指定的源文件生成一个库。

## Normal Libraries

```cmake
add_library(<name> [STATIC | SHARED | MODULE]
    [EXCLUDE_FROM_ALL]
    [source ...]
)
```

使用指定的源文件生成一个库文件。库的名字在一个工程中必须是唯一的。库文件的名根据平台决定（例如静态库lib\<name\>.a或\<name\>.lib）。

库的类型：

- STATIC：静态库将会链接成为目标文件的一部分
- SHARED：动态库在运行时动态加载
- MODULE：插件，不进行链接，但可以在运行时使用像dlopen一样的功能进行动态加载

如果未指定库类型，默认库类型取决于变量BUILD_SHARED_LIBS当前的值。

## Imported Libraries

## Object Libraries

## Alias Libraries

## Interface Libraries

## 示例

```cmake
# 指定源文件a.c和b.c生成静态库test（libtest.a或test.lib）
add_library(test STATIC "a.c" "b.c")
```

