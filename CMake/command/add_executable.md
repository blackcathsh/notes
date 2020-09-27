[TOC]

# add_executable

使用指定的源文件生成一个可执行文件。

## Normal Executables

```cmake
add_executable(<name> [WIN32] [MACOSX_BUNDLE]
    [EXCLUDE_FROM_ALL]
    [source ...]
)
```

使用指定的源文件构建一个可执行文件，可执行文件的名字根据平台的不同，可能为\<name\>.exe或\<name\>。可执行文件名在一个工程中必须是唯一的。

## Imported Executables

## Alias Executables

## 示例

```cmake
# 使用源文件a.c和b.c生成可执行文件a.exe或a
add_executable(a "a.c" "b.c")
```

